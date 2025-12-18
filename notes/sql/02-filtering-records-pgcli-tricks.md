# SQL Basics

## What is it?
Pratice with WHERE clause to filter records based on conditions, UPDATE, DELETE and other basic operations.

### WHERE to Filter Records

```sql
SELECT name, population / area AS population_density FROM cities WHERE population / area > 6000;

RESULT:
   name    | population_density
-----------+--------------------
 Delhi     |              12555
 Sao Paulo |               6879
(2 rows)
```

### UPDATE Records

```sql
UPDATE cities SET population = 39505000 WHERE name = 'Tokyo';

RESULT:
UPDATE 1
playground=# SELECT * FROM cities;
   name    | country | population | area
-----------+---------+------------+------
 Delhi     | India   |   28125000 | 2240
 Shanghai  | China   |   22125000 | 4015
 Sao Paulo | Brazil  |   20935000 | 3043
 Tokyo     | Japan   |   39505000 | 8223
(4 rows)
```

### DELETE Records

```sql
DELETE FROM cities WHERE name = 'Tokyo';

RESULT:
DELETE 1
playground=# SELECT * FROM cities;
   name    | country | population | area
-----------+---------+------------+------
 Delhi     | India   |   28125000 | 2240
 Shanghai  | China   |   22125000 | 4015
 Sao Paulo | Brazil  |   20935000 | 3043
(3 rows)
```

## pgCLI Tricks

### List of Tables

```sql
\dt
```

### Table Schema

```sql
\d table_name
```

### Database List

```sql
\l
```

### Clear Screen

```sql
\clear
```