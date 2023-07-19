 reverse перестраивает маршрут, берёт 'horoscope-name', он прописан в *имя приложения*, это horoscope/  и добавляет к нему args=(name_zodiac, ), туда могут попасть несколько аргументов
 
 redirect_url = reverse('horoscope-name', args=(name_zodiac,))

  urlpatterns = **[
		path('<str:sign_zodiac>/', views.get_info_about_sign_zodiac, name='horoscope-name')]
		]**