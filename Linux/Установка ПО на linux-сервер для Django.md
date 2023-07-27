https://www.digitalocean.com/community/tutorials/how-to-set-up-django-with-postgres-nginx-and-gunicorn-on-ubuntu-20-04-ru

_Установка проекта только из под пользователя с правами sudo, никакого root! Создавать проект в новой директории, на которую сразу открыты права на исполнение файлов для этого пользователя._

__django-admin.py startproject myproject ~/myprojectdir__
Если не создаёт проект, то можно убрать __.py__

__source _myprojectenv_/bin/activate__ войти в venv
__deactivate__ выйти

не забыть сделать _импорт os_ , перед миграцией

В процессе настройки Nginx, при задании __location__, важен их порядок, т.к. выполняются они по очереди сверху в низ






