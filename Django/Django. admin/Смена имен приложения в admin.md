- В файле __apps.py__ добавить имя в __verbose_name__
![[Pasted image 20230811212943.png]]
- в **__init__** прописать 
 __default_app_config = 'application_movie.apps.ApplicationMovieConfig'__ (имя приложения->apps->имя класса конфига)

__admin.site.site_title = 'Dj Movies1'__  - меняет название вкладки
__admin.site.site_header = 'Dj Movies2'__ - меняет основное название Админ панели.

![[Pasted image 20230811220942.png]]