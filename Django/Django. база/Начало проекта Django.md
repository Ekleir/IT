1)Создание проекта.  Django-admin startproject *имя проекта*

2)Запуск сервера. Python manage.py runserver

3) Остановка сервера. Ctrl + C

4) Создание приложения Python manage.py startapp *имя приложения*

5) settings.py -> INSTALLED_APPS -> прописываем в список *имя приложения*

6) Во views создаём пул реквестов.

 *имя проекта*  -> views.py ->

  from django.http import HttpResponse

7) *имя приложения* -> urls->

from django.urls import path**, *!**include!*

добавляем ссылку на конфиг(*имя проекта*.urls)

path('horoscope/'**,** include(horoscope.urls))

8) *имя проекта* -> создаём новый файл urls.py

from django.urls import path
from . import views

 копируем сюда из urls и создаём ссылки на реквесты во views

urlpatterns = [  
    path('leo/'**,** views.leo)]

ЛИБО

urlpatterns = [path('<sign_zodiac>/'**,** views.get_info_about_sign_zodiac)]

во views создаем

def get_info_about_sign_zodiac(request**,** sign_zodiac):

и перечисляем ссылки

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Дебаг:

Run\Debug configuration ->

                 Даём имя

 workingDirectory-*имя приложения*

 Parameters –runserver

Script path – *имя проекта* - manage.py

![[Pasted image 20230717162122.png]]

