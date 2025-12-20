# SQL Constraints and Data Migration

## What is it?
This note covers SQL constraints, data migration using pgloader, and some useful pgCLI tricks.

## SQL Constraints

### Auto Generated Primary Key

```sql
CREATE TABLE users (
   id BIGINT PRIMARY KEY GENERATED ALWAYS AS IDENTITY,
   username VARCHAR(50) NOT NULL
);
```

#### Key Points:
- We can also create a primary key using `SERIAL` data type, but `GENERATED ALWAYS AS IDENTITY` is the SQL standard way.
- Declaring a table with a serial primary keys is similar to the following:
```sql
CREATE TABLE users (
   id SERIAL PRIMARY KEY,
   username VARCHAR(50) NOT NULL
);
```
- It is equivalent to execute the following statements:
```sql
CREATE SEQUENCE users_id_seq;
CREATE TABLE users (
   id INTEGER NOT NULL DEFAULT nextval('users_id_seq'),
   username VARCHAR(50) NOT NULL,
   PRIMARY KEY (id)
);
ALTER SEQUENCE users_id_seq OWNED BY users.id;
```
- As we can see, creating a SERIAL field is a shortcut to create:
   - A int column and arrange for its default values to be assigned from a sequence generator.
   - A NOT NULL constraint applied to ensure that a null value cannot be inserted.
   - Mark the sequence as owned by the column, so that it will be dropped if the column or table is dropped.


### Foreign Key Constraint

```sql
CREATE TABLE photos (
   id BIGINT PRIMARY KEY GENERATED ALWAYS AS IDENTITY,
   user_id BIGINT REFERENCES users(id),
   url VARCHAR(255) NOT NULL
);
```

```sql
CREATE TABLE photos (
   id BIGINT PRIMARY KEY GENERATED ALWAYS AS IDENTITY,
   user_id BIGINT REFERENCES users(id) ON DELETE CASCADE,
   url VARCHAR(255) NOT NULL
);
```

#### Key Points:
- The `REFERENCES` keyword is used to create a foreign key constraint.
- By Default, foreign key is created with `ON DELETE NO ACTION`. So if we try to delete a user that has photos, it will raise an error.
- We can specify different actions for foreign keys using `ON DELETE` and `ON UPDATE` clauses:
   - `ON DELETE CASCADE`: When the referenced row is deleted, delete the rows that reference it.
   - `ON DELETE SET NULL`: When the referenced row is deleted, set the foreign key column to NULL.
   - `ON DELETE SET DEFAULT`: When the referenced row is deleted, set the foreign key column to its default value.
   - `ON DELETE NO ACTION`: Default behavior


## Data Migration using pgloader

### Installing pgloader
```bash
# On Ubuntu
sudo apt-get install pgloader
```

### Basic Usage
```bash
pgloader kaggle_eu_soccer.sqlite postgresql://root:root@localhost/kaggle_eu_soccer

pgloader mysql://user:password@localhost/source_db postgresql://user:password@localhost/target_db
```