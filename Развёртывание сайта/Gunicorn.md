WSGI сервер

Что делает:
- Запуск пула рабочих процессов / потоков (выполнение написанного кода)
- Переводит запросы, поступающие от Nginx, для совместимости с WSGI 
- Переведит ответы WSGI  приложения в правильные ответы HTTP 
- Вызывает код Python, когда приходит запрос 
- Gunicorn может общаться с различными веб-серверами

Что  не делает:
- Не может работать с фронтендом
- Не может поддерживать работу по SSL (без обработки https)
- Не может обеспечить работу полноценного веб-сервера, как например Nginx  

