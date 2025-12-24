# Subqueries, Correlated Subqueries, SELECT without FROM, GREATEST, LEAST functions, CASE statements, DISTINCT, PgAdmin setup in SQL

## What is it?
This note covers advanced SQL concepts including subqueries, correlated subqueries, the use of SELECT without a FROM clause, GREATEST and LEAST functions, CASE statements, and the DISTINCT keyword. These concepts are essential for writing more complex and efficient SQL queries.

## Subqueries
A subquery is a query nested inside another query. It can be used in various places such as the SELECT, FROM, and WHERE clauses.

### Example of a Subquery in WHERE clause
```sql
SELECT price, name
FROM products
WHERE price > (SELECT AVG(price) FROM products)
ORDER BY price DESC
LIMIT 10;

-- RESULT:
 price |           name
-------+---------------------------
   991 | Small Fresh Gloves
   989 | Incredible Granite Mouse
   982 | Awesome Fresh Keyboard
   982 | Incredible Granite Bacon
   966 | Fantastic Fresh Chips
   959 | Handmade Rubber Chicken
   948 | Practical Rubber Mouse
   947 | Practical Steel Shoes
   945 | Handcrafted Rubber Towels
   939 | Licensed Steel Towels
(10 rows)
```

### Example of a Subquery in SELECT clause
```sql
SELECT name, price, (
	price::numeric / (SELECT MAX(price) FROM products)
) AS price_ratio
FROM products
ORDER BY price_ratio DESC
LIMIT 5;

-- RESULT:
           name           | price |      price_ratio
--------------------------+-------+------------------------
 Small Fresh Gloves       |   991 | 1.00000000000000000000
 Incredible Granite Mouse |   989 | 0.99798183652875882947
 Incredible Granite Bacon |   982 | 0.99091826437941473259
 Awesome Fresh Keyboard   |   982 | 0.99091826437941473259
 Fantastic Fresh Chips    |   966 | 0.97477295660948536831
(5 rows)
```

### Example of a Subquery in FROM clause
```sql
-- Problem Statement: Find the average number of orders for all users.
SELECT AVG(order_count) AS avg_orders
FROM (
	SELECT user_id, COUNT(*) AS order_count
	FROM orders
	GROUP BY user_id
) AS user_orders;

-- RESULT:
     avg_orders
---------------------
 11.0000000000000000
(1 row)
```

#### Key Points:
- Aliasing the subquery result is mandatory when using it in the FROM clause.

## Correlated Subqueries
A correlated subquery is a subquery that references columns from the outer query. It is executed once for each row processed by the outer query.

### Example of a Correlated Subquery
```sql
-- Find most expensive product in each category
SELECT name, department, price
FROM products p1
WHERE p1.price = (
	SELECT MAX(price)
	FROM products p2
	WHERE p1.department = p2.department
);

-- RESULT:
           name            | department  | price
---------------------------+-------------+-------
 Gorgeous Steel Towels     | Outdoors    |   412
 Gorgeous Concrete Towels  | Grocery     |   328
 Incredible Granite Mouse  | Home        |   989
 Gorgeous Rubber Ball      | Books       |   801
 Handcrafted Rubber Towels | Baby        |   945
 Practical Plastic Towels  | Games       |   379
 Handmade Rubber Chicken   | Movies      |   959
 Tasty Rubber Soap         | Tools       |   823
 Incredible Granite Bacon  | Music       |   982
 Handmade Granite Fish     | Electronics |   166
 Licensed Steel Towels     | Industrial  |   939
 Fantastic Cotton Shirt    | Health      |   496
 Licensed Cotton Sausages  | Sports      |   751
 Intelligent Plastic Car   | Shoes       |   628
 Sleek Fresh Gloves        | Clothing    |   919
 Handcrafted Soft Chicken  | Kids        |   720
 Small Fresh Gloves        | Garden      |   991
 Licensed Plastic Salad    | Beauty      |   834
 Tasty Rubber Table        | Computers   |   525
 Refined Metal Tuna        | Jewelery    |   708
 Practical Steel Shoes     | Toys        |   947
(21 rows)
```

```sql
-- Without using JOIN or GrOUP BY, find number of orders for each product
SELECT p.id, p.name, (
	SELECT COUNT(*)
	FROM orders o
	WHERE o.product_id = p.id
) AS num_orders
FROM products p
ORDER BY num_orders DESC
LIMIT 5;

-- RESULT:
 id |           name           | num_orders
----+--------------------------+------------
  6 | Gorgeous Concrete Towels |         12
 52 | Handmade Granite Fish    |         11
 15 | Tasty Metal Cheese       |         11
 60 | Fantastic Cotton Shirt   |         10
 66 | Intelligent Cotton Chips |         10
(5 rows)
```

## SELECT without FROM Clause
In SQL, it is possible to use the SELECT statement without a FROM clause to return constants or expressions.

### Example of SELECT without FROM
```sql
SELECT
	(SELECT MAX(price) FROM products) AS max_price,
	(SELECT MIN(price) FROM products) AS min_price,
	(SELECT AVG(price) FROM products) AS avg_price;

-- RESULT:
 max_price | min_price |      avg_price
-----------+-----------+----------------------
       991 |         1 | 498.7300000000000000
(1 row)
```

## GREATEST and LEAST Functions
The `GREATEST` function returns the largest value from a list of expressions, while the `LEAST` function returns the smallest value.

### Example of GREATEST and LEAST
```sql
SELECT name, price, weight, GREATEST(30, 2 * weight) AS shipping_cost
FROM products
ORDER BY shipping_cost DESC
LIMIT 5;

-- RESULT:
          name           | price | weight | shipping_cost
-------------------------+-------+--------+---------------
 Ergonomic Fresh Pants   |   638 |     30 |            60
 Awesome Fresh Keyboard  |   982 |     30 |            60
 Sleek Granite Towels    |   797 |     30 |            60
 Unbranded Cotton Shoes  |   298 |     29 |            58
 Handcrafted Fresh Bacon |   387 |     29 |            58
(5 rows)
```

```sql
SELECT name, price, weight, LEAST(30, 2 * weight) AS shipping_cost
FROM products
ORDER BY shipping_cost ASC
LIMIT 5;

-- RESULT:
           name           | price | weight | shipping_cost
--------------------------+-------+--------+---------------
 Handcrafted Frozen Shoes |    84 |      1 |             2
 Small Plastic Soap       |   345 |      1 |             2
 Rustic Rubber Soap       |   127 |      2 |             4
 Incredible Granite Mouse |   989 |      2 |             4
 Unbranded Wooden Ball    |   384 |      2 |             4
(5 rows)
```

## CASE Statements
The `CASE` statement is used to create conditional logic in SQL queries. It goes through conditions and returns a value when the first condition is met.

### Example of CASE Statement
```sql
SELECT name, price,
	CASE
		WHEN price < 200 THEN 'Budget'
		WHEN price BETWEEN 200 AND 700 THEN 'Mid-Range'
		ELSE 'Premium'
	END AS price_category
FROM products
LIMIT 5;

-- RESULT:
         name          | price | price_category
-----------------------+-------+----------------
 Practical Fresh Shirt |   876 | Premium
 Gorgeous Steel Towels |   412 | Mid-Range
 Rustic Plastic Bacon  |    10 | Budget
 Tasty Wooden Ball     |   796 | Premium
 Fantastic Soft Fish   |    10 | Budget
(5 rows)
```

```sql
SELECT name, price, (
	CASE
		WHEN price > 700 THEN 'Premium'
		WHEN price > 200 THEN 'Mid-Range'
		ELSE 'Budget'
	END
) AS price_category
FROM products
LIMIT 5;

-- RESULT:
         name          | price | price_category
-----------------------+-------+----------------
 Practical Fresh Shirt |   876 | Premium
 Gorgeous Steel Towels |   412 | Mid-Range
 Rustic Plastic Bacon  |    10 | Budget
 Tasty Wooden Ball     |   796 | Premium
 Fantastic Soft Fish   |    10 | Budget
(5 rows)
```