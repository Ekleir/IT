Это специальные символы, которые нужны для замены каких-либо знаков в запросе. Они используются вместе с оператором `LIKE`, с помощью которого можно отфильтровать запрашиваемые данные.

-   `%` — заменить ноль или более символов;
-   `_` — заменить один символ.
```clike
SELECT * FROM user WHERE name LIKE '%test%';
```

Данный запрос позволяет найти данные всех пользователей, имена которых содержат в себе «test».

```clike
SELECT * FROM user WHERE name LIKE 't_est';
```

А в этом случае имена искомых пользователей начинаются на «t», после содержат какой-либо символ и «est» в конце.