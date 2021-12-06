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
