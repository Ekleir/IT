_from_ django.views.generic _import_  DetailView

В _URL_ файле необходимо указать только(!) либо _slug_ либо _pk_ (primary key) 
![[Pasted image 20230601194726.png]]
это значение будет обрабатываться классом DetailView
В самом классе прописывается только шаблон и модель
![[Pasted image 20230601194827.png]]
> В html шаблоне обращение к переменной осуществляется по названию класса в нижнем регистре либо по переменной __object__
![[Pasted image 20230601195233.png]]
имя __object__ можно переопределить через __context_object_name__