# SQL Basics

## What is it?
Practice with CREATE, INSERT, SELECT, Math/String Operators and other basic operations.

### Create Table in Postgres

```sql
CREATE TABLE cities (
  name VARCHAR(50),
  country VARCHAR (50),
  population INTEGER,
  area INTEGER
);
```

#### When to Use
Create a new table

### INSERT into Table

```sql
INSERT INTO cities (name, country, population, area)
VALUES 
  ('Tokyo', 'Japan', 38505000, 8223)
  ('Delhi', 'India', 28125000, 2240)
  ('Shanghai', 'China', 22125000, 4015),
  ('Sao Paulo', 'Brazil', 20935000, 3043);

RESULT: INSERT 0 2
```

#### When to Use
Insert records into a table

### SELECT records

```sql
SELECT * FROM cities;

RESULT:
   name    | country | population | area
-----------+---------+------------+------
 Tokyo     | Japan   |   38505000 | 8223
 Delhi     | India   |   28125000 | 2240
 Shanghai  | China   |   22125000 | 4015
 Sao Paulo | Brazil  |   20935000 | 3043
(4 rows)
```

```sql
SELECT name, population, population / area as population_density FROM cities;

RESULT:
   name    | population | population_density
-----------+------------+--------------------
 Tokyo     |   38505000 |               4682
 Delhi     |   28125000 |              12555
 Shanghai  |   22125000 |               5510
 Sao Paulo |   20935000 |               6879
(4 rows)
```

```sql
SELECT CONCAT(name, ', ', UPPER(country)) AS location, population / area as population_density FROM cities;

RESULT:
     location      | population_density
-------------------+--------------------
 Tokyo, JAPAN      |               4682
 Delhi, INDIA      |              12555
 Shanghai, CHINA   |               5510
 Sao Paulo, BRAZIL |               6879
(4 rows)
```

#### When to Use
Retrieve records from a table