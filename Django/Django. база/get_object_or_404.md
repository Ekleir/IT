_from_ django.shortcuts _import_ get_object_or_404


_def_ show_one_movie(request, slug_movie: str):  
    movie = _get_object_or_404_(Movie, slug=slug_movie)  
    return render(request, 'movie_app/one_movie.html', {  
        'movie': movie  
    })

Что бы не возникала ошибка при вызове функции, если для передаваемого аргумента нет данных, можно использовать _get_object_or_404_
В этот метод передаётся _модель_ и название колонки с соответствующим значением, где будет происходить поиск.
В случае исключения вернётся ошибка 404