прописываются в шаблоне после вызова переменной через знак - _|_

![[Pasted image 20230515165543.png]]

{{ value|add:"2" }}

{{ first|add:second }}

"{{ value|center:"15" }}"

{{ value|cut:" " }}

{{ value|default:"_nothing_" }} (If value is "" (the empty string), the output will be _nothing_.)

{{ value|default_if_none:"nothing" }}

{{ value|divisibleby:"3" }} (проверяет делится ли без остатка на 3, для 21-True)

{{ value|first }} (If value is the list ['a', 'b', 'c'], the output will be 'a'.)

{{ value|join:" // " }}
If value is the list ['a', 'b', 'c'], the output will be the string "a // b // c".

{{ value|length }}

{{ value|length_is:"4" }}
If value is ['a', 'b', 'c', 'd'] or "abcd", the output will be True.

"{{ value|ljust:"10" }}"
If value is Django, the output will be "Django " (прижимает к левой стороне экрана)

{{ value|make_list }}
If value is the string "Joel", the output would be the list ['J', 'o', 'e', 'l']. If value is 123, the output
will be the list ['1', '2', '3']

{{ value|random }}
If value is the list ['a', 'b', 'c', 'd'], the output could be "b".

{{ some_list|slice:":2" }}
If some_list is ['a', 'b', 'c'], the output will be ['a', 'b']

{{ value|title }}
If value is "my FIRST post", the output will be "My First Post"

