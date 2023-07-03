__DELETE FROM имя таблицы WHERE выборка;__
![[Pasted image 20230703151303.png]]


##  DELETE и TRUNCATE
Команда `DELETE` — это DML-операция, которая удаляет записи из таблицы, соответствующие заданному условию:
```clike
DELETE FROM table_name WHERE condition;
```
При этом создаются логи удаления, то есть операцию можно отменить.

`TRUNCATE` — это DDL-операция, которая полностью пересоздаёт таблицу, и отменить такое удаление невозможно:
```clike
TRUNCATE TABLE table_name;
```