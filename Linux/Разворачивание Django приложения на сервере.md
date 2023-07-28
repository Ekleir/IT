Это делается после [[Установка ПО на linux-сервер для Django]]
- __cd /var/www__ (обычно есть везде, директория для сайтов)
- __apt-get install git__
- __git clone репозиторий__
-   __cp /etc/nginx/sites-available/myproject etc/nginx/sites-available/books__
 (копируем из пробного проекта для изменения под нужный)
- __vim /etc/nginx/sites-enabled/books__
Меняем файл под проект
![[Pasted image 20230728162219.png]]
- __ln -s /etc/nginx/sites-available/books /etc/nginx/sites-enabled/books__
создаётся символическая ссылка из sites-available на sites-enabled
__ls -l /etc/nginx/sites-enabled/__ проверка, что всё подключилось.
__rm  /etc/nginx/sites-enabled/myproject__ удаляется тестовая ссылка, если делалось через неё(не будет если первоначальная настройка была сразу на нужный проект, а не тестовый)
- __nginx -t__ проверка на правильность конфига:
![[Pasted image 20230728163217.png]]
- __nginx -s reload__ перезагрузка для применения настроек
- __mkdir /var/venvs__ создание директории под venv
- __virtualenv booksenv__ создание виртуального окружения проекта
- __source /var/venvs/booksenv/bin/activate__ активация
- установка зависимостей из requirements.txt (я надеюсь он есть, не так ли? иначе всё придётся писать ручками)
-  __vim /etc/systemd/system/gunicorn.service__ меняется файл gunicorn под проект
![[Pasted image 20230728165206.png]]
- __systemctl stop gunicorn__, останавливаем службу, если не получилось, то:
 __systemctl daemon-reload__
 __systemctl stop gunicorn__
- __systemctl start gunicorn__ запускаем заново
>Пути и названия скачанных папок с Git обязательно проверить!!!
  После изменений файлов питона делать останов и старт gunicorn

## PostgreSQL
Находясь в виртуальном окружении:
- зайти в папку проекта, где находится manage.py
- __sudo -u postgres psql__ Выполнить команду от имени postgres
- __CREATE USER books_user WITH PASSWORD 'PASSWORD';__
 создать пользователя
- __CREATE DATABASE books_db;__ создать БД
- __GRANT ALL PRIVILEGES ON DATABASE books_db TO books_user;__
наделение пользователя правами
- __Ctrl + D__ выход из консоли postgresql
- settings.py поставить пароль, который был создан на пользователя БД.
- __python manage.py migrate__
- перезагрузить gunicorn

## Статика
- создать путь к статике в settings.py
STATIC_ROOT = 'static/'
-  __python manage.py collectstatic__
- __nginx -s reload__ перезагружаем nginx




