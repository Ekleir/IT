![[Pasted image 20230522170201.png]]
![[Pasted image 20230522171150.png]]
поле ForeignKey прописывается в _зависимой_ модели, первым параметром указывается _главная_ модель , далее тип поведения зависимой модели при удалении _on_delete_ данных из главной модели.
_ForeignKey_- внешний ключ, это поле по умолчанию именуется в БД как _director_id_, можно переименовать через _related_name= 


