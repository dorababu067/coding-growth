---
title: "SQL Basics First Part"
date: 2022-05-20T18:24:38+05:30
tags: ["SQL"]
categories: ["SQL"]
---

## Create Database 

Create new database in postgresql, for sql syntax we can use upper case or lower case letters But I preffer the `UPPERCASE` syntax for sql commands.

```sql
postgres=# CREATE DATABASE test;
CREATE DATABASE

```

## Connect to database 

How to use newly created database in postgresql

```sql
postgres=# \c test;
psql (14.0 (Ubuntu 14.0-1.pgdg20.04+1), server 12.9 (Ubuntu 12.9-0ubuntu0.20.04.1))
You are now connected to database "test" as user "postgres".
test=# 

```

```sql
postgres=# CREATE DATABASE test;
CREATE DATABASE

```

## Drop Database 

`Delete` the existing database, Here `test` is my `DATABASE` name

```sql
postgres=# DROP DATABASE test;
DROP DATABASE

```

## Create table with postgresql

create table syntax

```sql
CREATE TABLE table_name ( column_name + data_type + constraints if any)

```
Create person table, Here datatypes is you wish, here i have used what datatypes i needed.

[Postgresql Datatypes](https://www.postgresql.org/docs/current/datatype.html)

```sql
CREATE TABLE person (
    id INT,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    gender VARCHAR(6),
    date_of_birth DATE
);

```


## Describe the tables

How to see all tables in postgresql database

```sql
test=# \d

          List of relations
 Schema |  Name   | Type  |  Owner   
--------+---------+-------+----------
 public | person  | table | postgres
 public | person2 | table | postgres
(2 rows)

```
How to see individual table structure

```sql
test=# \d person;

                         Table "public.person"
    Column     |         Type          | Collation | Nullable | Default 
---------------+-----------------------+-----------+----------+---------
 id            | integer               |           |          | 
 first_name    | character varying(50) |           |          | 
 last_name     | character varying(50) |           |          | 
 gender        | character varying(6)  |           |          | 
 date_of_birth | date                  |           |          | 

```
## Create table with constraints postgresql

In the below `PRIMARY KEY, NOT NULL` are the constraints

[Postgresql Constraints](https://www.postgresql.org/docs/current/ddl-constraints.html)

```sql
CREATE TABLE person (
    id BIGSERIAL NOT NULL PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    gender VARCHAR(6) NOT NULL,
    date_of_birth DATE NOT NULL
);

```
## Insert Records into tables

syntax

```sql
INSERT INTO table(column1, column2, ...) VALUES (value1, value2, ...);

```

Insert new record into table

```sql
INSERT INTO person (
    first_name,
    last_name,
    gender,
    date_of_birth)
VALUES('Anne','Smith','FEMALE', DATE '1998-01-09');

```
Insert command output

```sql
test=# INSERT INTO person (
    first_name,
    last_name,
    gender,
    date_of_birth)
VALUES('Anne','Smith','FEMALE', DATE '1998-01-09');
INSERT 0 1

```
## Insert the data using the file

[Generate Random Data](https://www.mockaroo.com/)

```sql
test=# \i path/file.sql

```

## ALTER TABLE

introduction to PostgreSQL ALTER TABLE statement
To change the structure of an existing table, you use PostgreSQL ALTER TABLE statement.

The following illustrates the basic syntax of the ALTER TABLE statement:

[ALTER Full Description](https://www.postgresqltutorial.com/postgresql-tutorial/postgresql-alter-table/)

```sql

ALTER TABLE table_name 
ADD COLUMN column_name datatype column_constraint;

```


## Updated Records

Using the `UPDATE` command we can update the existing record values

```sql
test=# SELECT * FROM person WHERE id = 200;
 id  | first_name | last_name |            email             | gender | date_of_birth |   country   
-----+------------+-----------+------------------------------+--------+---------------+-------------
 200 | Romona     | Issac     | rissac5j@businessinsider.com | Female | 2021-12-25    | Philippines
(1 row)

test=# UPDATE person set email = 'updated@email.com' WHERE id =200;
UPDATE 1

test=# SELECT * FROM person WHERE id = 200;
 id  | first_name | last_name |       email       | gender | date_of_birth |   country   
-----+------------+-----------+-------------------+--------+---------------+-------------
 200 | Romona     | Issac     | updated@email.com | Female | 2021-12-25    | Philippines
(1 row)

```
## Delete Records

Remove all the records from the table 

```sql
DELETE FROM person;

```
Remove selected records, here i have selected id is `1000`

```sql
DELETE FROM person WHERE id = 1000;
DELETE 1

```