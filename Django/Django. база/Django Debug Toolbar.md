https://django-debug-toolbar.readthedocs.io/en/latest/index.html

$ python -m pip install django-debug-toolbar

Проверить, что есть запись в settings
INSTALLED_APPS = 
    # ...
    "django.contrib.staticfiles",
    # ...
STATIC_URL = "static/"
и
TEMPLATES = 
    {
        "BACKEND": "django.template.backends.django.DjangoTemplates",
        "APP_DIRS": True,
        # ...
    }

Прописать приложение 
INSTALLED_APPS = 
    # ...
    "debug_toolbar",
    # ...

Добавить в главный URL конфиг
urlpatterns = 
    # ...
    path('__debug__/', include('debug_toolbar.urls')),

Добавить в settings
MIDDLEWARE = 
    # ...
    "debug_toolbar.middleware.DebugToolbarMiddleware",
    # ...

Прописать в settings(этой настройки нет по умолчанию)
INTERNAL_IPS = 
    # ...
    "127.0.0.1",
    # ...

Перезапустить сервер

