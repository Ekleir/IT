позволяет осуществлять фильтрацию по  значению в указанной колонке адресной строки.
![[Pasted image 20230720203641.png]]

пакет для установки - django-filter
![[Pasted image 20230720172735.png]]
импорт __DjangoFilterBackend__ из _django_filters.rest_framework_ во __view__
![[Pasted image 20230720175055.png]]
указываем нужный фильтр - __filter_backends = DjangoFilterBackend__ и поля для фильтрации - __filterset_fields__
