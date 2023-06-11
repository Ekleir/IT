    # response = render_to_string('horoscope/info_zodiac.html')
    # return HttpResponse(response)

render объединяет конвертацию шаблона в строку _render_to_string_ и  _HttpResponse_.
Этот метод принимает _request_, берёт запрошенные данные и подставляет их в html-шаблон

![[Pasted image 20230515151806.png]]

С помощью ключа в словаре _context_ можно потом работать в html-шаблоне:
![[Pasted image 20230515164025.png]]

