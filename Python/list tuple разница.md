list - __изменяемый__, упорядоченный, обычно хранит элементы __одного__ типа, О(1) доступ к элементу.
tuple - __неизменяемый__, упорядоченный,  обычно хранит элементы __разных__ типов, О(1)  доступ к элементу.
Доступ к элементу не зависит от размера коллекции в обоих случаях.

Сама коллекция не расположена в памяти. в памяти находятся ссылки на объекты коллекции. Соответственно не важно какого размера объект в коллекции, он не будет влиять на скорость доступа к нему. Поиск будет осуществляться по индексам этой коллекции, они представляют собой числа. Их значение можно узнать с помощью метода __id()__

Так же кортеж работает быстрее. Python по умолчанию при загрузке резервирует память под работу с кортежами. При работе со спискам память выделяется по запросу к ОС.

Пустой список занимает места в памяти больше чем пустой кортеж.

В итоге, если  использовать кортежи вместо списков, где есть возможность, то прирост в большой системе по скорости и ресурсам может быть существенный.
Однако такой подход не предусматривает слияние кортежей, т.к. происходит выделение новой памяти и перенос объединённого кортежа туда.

