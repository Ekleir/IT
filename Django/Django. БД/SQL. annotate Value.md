_from_ django.db.models _import_ Value

Создание дополнительных полей вне БД при помощи класса _Value_ и метода _annotate_, оно будет вычисляться на лету. 
_annotate_ можно создать в любом queryset, просто дописав в конце.
![[Pasted image 20230723172846.png]]

movies = Movie.objects.annotate(  
    true_bool=Value(True),  
    false_bool=Value(False),  
    str_field=Value('hi'),  
    int_field=Value(123),  
    new_budget=F('budget')+100,  
    new_field=F('budget')+F('rating'),  
)

>Первый параметр-это название поля
>к нему через _ добавляется какой тип значения оно будет хранить(не обязательно)
>и что мы туда сохраняет соответственно
 
Можно добавлять сколько угодно полей, они будут отображаться на странице в виде SQL таблицы (в тулбаре->SQL->select в нужном запросе)
![[Pasted image 20230518203321.png]]
