SQL Basics: Simple JOIN with COUNT:

```
select p.* ,COUNT(toys.name) as toy_count from people
p join toys on
p.id = toys.people_id Group by p.id;
```

Easy SQL: Moving Values:

```
SELECT LENGTH(name) AS id, LENGTH(CAST(legs AS VARCHAR)) AS name,
LENGTH(CAST(arms AS VARCHAR)) AS legs,LENGTH(characteristics) AS arms,
LENGTH(CAST(id as VARCHAR)) AS characteristics from monsters;
```

SQL Basics: Simple EXISTS

```
SELECT id, name from departments WHERE EXISTS
(SELECT * from sales WHERE departments.id =
sales.department_id AND price > 98.00);
```

SQL Basics: Simple JOIN and RANK

```

SELECT people.id, people.name, COUNT(*)AS sale_count,
RANK()OVER(ORDER BY COUNT(*) DESC) AS sale_rank
FROM people JOIN sales ON
people.id = sales.people_id GROUP BY people.id
```
