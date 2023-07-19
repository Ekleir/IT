Замена БД в проекте Django:
- зайти в консоль PostgreSQL
- создать юзера 
	__CREATE USER books_user WITH PASSWORD 'password';__
- создать БД с этим юзером
	__CREATE DATABASE books_db WITH OWNER books_user;__
![[Pasted image 20230719172924.png]]
- поменять поля в __settings__ django проекта:
> DATABASES = {  
    'default': {  
            'ENGINE': 'django.db.backends.postgresql_psycopg2',  
            'NAME': 'books_db',  
            'USER': 'books_user',  
            'PASSWORD': '123',  
            'HOST': 'localhost',  
            'PORT': '',  
    }  
}
![[Pasted image 20230719172950.png]]

- установить пакет psycopg2
![[Pasted image 20230719173538.png]]

>Если не даёт создать миграции из-за слишком старой версии Postqresql ( ниже 12 ), то можно даунгреднуть Django до версии 4.0.(удалить и поставить заново)

Так же могут понадобиться права на создание БД, например при тестах.
__ALTER ROLE books_user CREATEDB;__
![[Pasted image 20230719212417.png]]
