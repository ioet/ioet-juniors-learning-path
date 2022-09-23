---
layout: "../../../../layouts/BlogPost.astro"
title: "SQL most used operations"
---

## Contributors

- [Josué Cando](https://github.com/JosueOb)

## Content

- [Contributors](#contributors)
- [Content](#content)
- [Introduction](#introduction)
- [SQL Commands](#sql-commands)
  - [Data Definition Language](#data-definition-language)
  - [Data Manipulation Language](#data-manipulation-language)
  - [Data Control Language](#data-control-language)
  - [Data Query Language](#data-query-language)
- [CRUD operations](#crud-operations)
  - [Create](#create)
    - [Notes](#notes)
  - [Read](#read)
  - [Update](#update)
    - [Notes](#notes-1)
  - [Delete](#delete)
    - [Notes](#notes-2)
  - [Example](#example)
- [Join Operations](#join-operations)
  - [Types of SQL join](#types-of-sql-join)
  - [Advantages and disadvantages](#advantages-and-disadvantages)
- [References](#references)

## Introduction

SQL is easy to learn, as the statements are composed of descriptive words in English and are not case-sensitive. Also,
you can create and interact with a database using SQL efficiently and easily. you don't have to specify how to get the
data from the database. Rather, you simply specify what to retrieve, and SQL does the rest.

SQL provides statements for defining the structure of the data, manipulating data in the database, declare constraints
and retrieve data from the database in various ways, depending on our requirements.

## SQL Commands

The standard SQL commands to interact with relational databases are `CREATE`, `SELECT`, `INSERT`, `UPDATE`, `DELETE`
and `DROP`. These commands can be classified into groups based on their nature:

### Data Definition Language

SQL provides commands for defining the relation schemas, modifying relation schemas and deleting relations. These are
called **Data Definition Language (DDL)** that help to define the database structure or schemas.

| Command   | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| CREATE    | Creates a new table, a view of a table, or other object in database.        |
| ALTER     | Modifies an existing database object, such as a table.                      |
| DROP      | Deletes an entire table, a view of a table or other object in the database. |
| TRUNCATE  | Deletes all the rows from the table and free the space.                     |

### Data Manipulation Language

The **Data Manipulation Language (DML)** is the language that gives users the ability to access, or manipulate the
condition that the appropriate data model has inherited.

| Command | Description       |
|---------|-------------------|
| INSERT  | Creates a record. |
| UPDATE  | Modifies records. |
| DELETE  | Deletes records.  |

### Data Control Language

The **Data Control Language (DCL)** is used for controlling user access in a database. This commands is related to the
security issues.

| Command | Description                              |
|---------|------------------------------------------|
| GRANT   | Gives a privilege to user.               |
| REVOKE  | Takes back privileges granted from user. |

### Data Query Language

The **Data Query Language (DQL)** is used for performing queries on the data within schema objects. The purpose of the
DQL Command is to get some schema relation based on the query passed to it.

| Command | Description                                        |
|---------|----------------------------------------------------|
| SELECT  | Retrieves certain records from one or more tables. |

## CRUD operations

### Create

In this operation, it is expected to insert a new record using the SQL insert statement. SQL uses `INSERT INTO`
statement to create new records within the table. Then specify the table name and the columns that you want to insert.
The columns go inside the parentheses and, then you specify a `VALUES` clause.

```
INSERT INTO <table_name> (column1, column2, column3 ) VALUES (value1, value2, value3);
```

To insert multiple rows, follow the below syntax:

```
INSERT INTO <table_name> (column1, column2,….) 
VALUES(value1, value2, ...),( value1 ,value2, ...),(value1, value2, ...)
```

#### Notes

* SQL Insert statement only works against a single table unlike select which can work against multiple tables.
* A column that is an auto-increment field will be generated automatically when a new record is inserted in the table.

### Read

In this operation, it refers to `SELECT` statement to retrieve the data from a listed table(s). To read related data
from the specified table, refer to the below syntax:

```
SELECT * FROM <TableName>
```

It allows you to retrieve specific data, one or more rows from one or more tables. The wildcard character (*) or
asterisk is used to populate all the columns of the table(s). Also, you can specify names of columns from the table(s)
that you would like to get data from.

```
SELECT column1m column2, column3 FROM <TableName>
```

### Update

In this operation, it refers to `UPDATE` statement to brings a change to an existing record(s) of the table. When
performing an update, you’ll need to define the target table and the columns that need to update along with the
associated values, and you may also need to know which rows need to be updated. In general, you want to limit the number
of rows in order to avoid lock escalation and concurrency issues.

```
UPDATE <TableName>
SET column1=value1, column2=value2,…
WHERE <Expression/Conditional>
```

#### Notes

* There are several ways to update records in a database, such as row-by-row, bulk and small batch updates.
* Always make sure you use a `WHERE` clause unless you want to update the entire table.
* If you have indexes that are not being used for the table, removing them could help optimize the update.

### Delete

In this operation, it refers to `DELETE` statement to remove the record(s) from the table. In this case, you’ll define
the target table and also which rows you need to delete from the table. The syntax in its simplest form is the DELETE
keyword followed by the table name. In some case without a `WHERE` clause in the query deletes all existing rows from
the table.

```
DELETE FROM <TableName>
WHERE <Expression/Conditional>
```

#### Notes

* It is recommended to manage record status changes (logical delete) instead of deleting them.
* Before you decide to perform mass **deletes** or **updates** of data in your database, it would be good that you back
  up all tables where changes are expected. After changes are performed, you should compare the old and the new table.
  If everything went OK, you can delete the backup tables. If there were errors, you should revert things (replace the
  'live' table with the one previously backed up) and try again (with corrected code).

### Example

In this case, a table is created to record the products with the following columns (`id`, `name`, `price`
and `category`). Remember that you must first create a database and create the product table in it. Make sure you have
admin privileges before creating any database. Once a database is created, you can check it in the list of databases
with the following SQL command: `SHOW DATABASES`;

```
CREATE DATABASE db;
 
CREATE TABLE db.products (
    id INT IDENTITY (1, 1) PRIMARY KEY,,
    name VARCHAR(255) NOT NULL, 
    price money NOT NULL, 
    category VARCHAR(255) NOT NULL 
);
```

This table is going to be used to perform the CRUD operations reviewed above:

* Create a new product record.

```
INSERT INTO db.products (name, price, category) VALUES ('phone A', 375.50, 'technology');
```

* Create multiple product records.

```
INSERT INTO db.products (name, price, category) 
VALUES ('phone A', 375.50, 'technology'),
       ('phone B', 575.50, 'technology'),
       ('phone C', 775.50, 'technology');
```

* List all product records, including all product data.

```
SELECT * FROM db.products
```

* List a specific product with specific data (columns).

```
SELECT name, price FROM db.products WHERE id=1
```

* Update a product record.

```
UPDATE db.products SET price=350.75 WHERE id=1
```

* Delete a specific product record.

```
DELETE FROM db.products WHERE id=1
```

## Join Operations

By using joins, you can retrieve data from two or more tables based on logical relationships between the tables. Joins
indicate how SQL Server should use data from one table to select the rows in another table. A join condition defines the
way two tables are related in a query by:

* Specifying the column from each table to be used for the join. A typical join condition specifies a foreign key from
  one table and its associated key in the other table.
* Specifying a logical operator (for example, = or <>,) to be used in comparing values from the columns.

### Types of SQL join

![SQL joins](https://ingenieriadesoftware.es/wp-content/uploads/2018/07/sqljoin.jpeg)

| Type              | Description                                                                       |
|-------------------|-----------------------------------------------------------------------------------|
| Inner Join        | Returns rows that have a matching value in both tables.                           |
| Left Join         | Returns all rows from the left table and matching rows from the right table.      |
| Right Join        | Returns all rows from the right table and matching rows from the left table.      |
| Full (Outer) Join | Returns all rows when there's a match on either the left or right table.          |
| Cross Join        | Returns all rows from the left table combined with the rows from the right table. |

### Advantages and disadvantages

* The main advantage of a join is that it executes faster. because the columns are specifically named and indexed and
  optimized by the database engine, the retrieval time almost always will be faster than that of a subquery.
* A disadvantage of using joins is that they are not as easy to read as subqueries.
* Another disadvantage is that it can be confusing as to which join is the appropriate type of join to use to yield the
  correct desired result set.

## References

* [SQLite online](https://sqliteonline.com/)