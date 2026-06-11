# SQL. Практика 8. Задача 1 — Решение с объяснением

## Решение

```sql
select complexity,
       count(*) as count_of_problems
from problem
group by complexity
order by complexity;
```

## Объяснение

| Часть запроса | Что делает |
|---------------|------------|
| `select complexity` | Выводим уровень сложности |
| `count(*) as count_of_problems` | Считаем количество строк (задач) в каждой группе |
| `from problem` | Берём данные из таблицы `problem` |
| `group by complexity` | Группируем строки по уровню сложности — для каждого уникального `complexity` считаем свой `count(*)` |
| `order by complexity` | Сортируем результат по возрастанию complexity |

### Как работает `GROUP BY`

Без `GROUP BY` запрос `select complexity, count(*) from problem` вернул бы ошибку — нельзя одновременно вывести конкретное значение поля и агрегатную функцию по всей таблице.

`GROUP BY complexity` разбивает таблицу на группы с одинаковым `complexity`. Затем `count(*)` применяется к каждой группе отдельно.

Пример:
```
Таблица problem
complexity
──────────
Лёгкий
Лёгкий
Средний
Сложный
Сложный
Сложный

Результат запроса:
complexity | count_of_problems
───────────┼─────────────────
Лёгкий     │ 2
Средний    │ 1
Сложный    │ 3
```

### Можно ли использовать `count(*)` вместо `count(complexity)`?

Да, `count(*)` считает количество строк в группе. `count(complexity)` посчитал бы то же самое, если в поле `complexity` нет `NULL`. Разницы в данной задаче нет.
