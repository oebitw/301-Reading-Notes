# SQL

![](https://www.freetutorialsplus.com/sql-tutorial/images/sql-illustration.png)

## What is SQL

SQL is a standard language for storing, manipulating and retrieving data in databases.


SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.




## Basic SQL
Each record has a unique identifier or primary key. SQL, which stands for Structured Query Language, is used to communicate with a database. Through SQL one can create and delete tables. Here are some commands:

* CREATE TABLE - creates a new database table.

* ALTER TABLE - alters a database table
DROP TABLE - deletes a database table.

* CREATE INDEX - creates an index (search key).

* DROP INDEX - deletes an index.

* SQL also has syntax to update, insert, and delete records.

* SELECT - get data from a database table
UPDATE - change data in a database table.
* DELETE - remove data from a database table.

* INSERT INTO - insert new data in a database table.

## SQL SELECT Statement

The `SELECT` statement is used to select data from a database.

The data returned is stored in a result table, called the result-set.

SELECT Syntax:
```
SELECT column1, column2, ...
FROM table_name;
```

## The SQL SELECT DISTINCT Statement

The SELECT DISTINCT statement is used to return only distinct (different) values.

Inside a table, a column often contains many duplicate values; and sometimes you only want to list the different (distinct) values.

```
SELECT DISTINCT Syntax
SELECT DISTINCT column1, column2, ...
FROM table_name;
```


## The SQL WHERE Clause
The WHERE clause is used to filter records.

It is used to extract only those records that fulfill a specified condition.

WHERE Syntax
```
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```


## The SQL AND, OR and NOT Operators

The WHERE clause can be combined with AND, OR, and NOT operators.

The AND and OR operators are used to filter records based on more than one condition:

The AND operator displays a record if all the conditions separated by AND are TRUE.

The OR operator displays a record if any of the conditions separated by OR is TRUE.

The NOT operator displays a record if the condition(s) is NOT TRUE.

AND Syntax:
```
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
```

OR Syntax:
```
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
```
NOT Syntax:
```
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```

## CREATE TABLE
The CREATE TABLE statement is used to create a new table. The format is:
```
CREATE TABLE tablename
(column1 data type,
column2 data type,
column3 data type);
```

* char(size): Fixed length character string.

* varchar(size): Variable-length character string, Max size is specified in parenthesis.

* number(size): Number value with a max number of columns specified in parenthesis.

* date: Date value.

* number(size,d): A number with a maximum number of digits of “size” and a maximum number of “d” digits to the right of the decimal.

## INSERT VALUES
Once a table has been created data can be inserted using INSERT INTO command.
```
INSERT INTO tablename
(col1, ... , coln)
VALUES (val1, ... , valn)
```
