https://django-debug-toolbar.readthedocs.io/en/latest/index.html

$ python -m pip install django-debug-toolbar

- Проверить, что есть запись в settings
__INSTALLED_APPS = 
    # ...
    "django.contrib.staticfiles",
    # ...
STATIC_URL = "static/"__
и
__TEMPLATES = 
    {
        "BACKEND": "django.template.backends.django.DjangoTemplates",
        "APP_DIRS": True,
        # ...
    }__

- Прописать приложение 
__INSTALLED_APPS = 
    # ...
    "debug_toolbar",
    # ...__

- Добавить в главный URL конфиг
urlpatterns = 
    # ...
    path('__debug__/', include('debug_toolbar.urls')),

- Добавить в settings
__MIDDLEWARE = 
    # ...
    "debug_toolbar.middleware.DebugToolbarMiddleware",
    # ...__

- Прописать в settings(этой настройки нет по умолчанию)
__INTERNAL_IPS = 
    # ...
    "127.0.0.1",
    # ...__

- Перезапустить сервер


DDT force позволяет показывать это расширение на странице с api.
- Установить пакет __django-debug-toolbar-force__
- Добавить в MIDDLEWARE
__MIDDLEWARE += (
    'debug_toolbar.middleware.DebugToolbarMiddleware',
    'debug_toolbar_force.middleware.ForceDebugToolbarMiddleware',
)__
![[Pasted image 20230724150212.png]]
- что бы панель была видна, надо в конце запроса прописывать 
__?debug-toolbar__
![[Pasted image 20230724150448.png]]