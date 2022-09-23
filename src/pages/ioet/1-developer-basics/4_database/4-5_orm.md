---
layout: "../../../../layouts/BlogPost.astro"
title: "ORM Object Relational Mapping"
pubDate: "2022-09-14"
---

## Contributor

- [Josué Cando](https://github.com/JosueOb)

## Content

- [Contributor](#contributor)
- [Content](#content)
- [Introduction](#introduction)
- [The Impedance Mismatch](#the-impedance-mismatch)
  - [Problems of an O-R Impedance Mismatch](#problems-of-an-o-r-impedance-mismatch)
- [ORM Frameworks](#orm-frameworks)
  - [Popular ORM tools/frameworks](#popular-orm-toolsframeworks)
    - [Python](#python)
    - [Java](#java)
    - [PHP](#php)
    - [Javascript/Typescript](#javascripttypescript)
- [ORM Terminology](#orm-terminology)
- [Advantages](#advantages)
- [Disadvantages](#disadvantages)
- [Conclusions](#conclusions)
- [References](#references)

## Introduction

Object relational mapping (ORM) is an established programming technique that has emerged as a solution to the
[**Object-Relational Impedance
Mismatch**](https://medium.com/booleanbhushan/object-relational-impedance-mismatch-28fc2440dee4) problem. ORM provides
an object-oriented interface to relational databases.

In this way, program objects can be easily saved and retrieved from secondary storage without the need to use repetitive
code to map application data to database records. ORM not only boosts developer productivity and reduces maintenance
costs, but also promotes portability because it abstracts away differences of [**Database Management
Systems**](https://www.bmc.com/blogs/dbms-database-management-systems/) (DBMS).

## The Impedance Mismatch

The impedance mismatch problem is a well-known problem in persistence objects in relational databases between both the
object model and the relational model and between the object programming language and the relational query language.
Object-oriented paradigm and relational databases have different concepts that can in practice make it difficult to
integrate them together. While object-oriented development is based on the concept of data and their behaviours,
relational databases are based on purely data.

* The object-oriented paradigm views data mainly as behaviours, that is, objects are important not just because of the
  data they contain, but because of their ability to perform tasks on the data and exchange hand.
* The relational paradigm places emphasis on the data itself and its structural (not behaviour) relationship with other
  data.

So to resolve this problem, there is usually a process of modeling both the object-oriented and relational paradigms
such that they are often subjected to some bending and twisting of the object-oriented paradigm until it matches the
underlying relational database technology.

### Problems of an O-R Impedance Mismatch

| Problem          | Concern                                                                                                                                                                                         |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Structure        | The structure problem theme is refers to any difference of data structure between the schema of an object-oriented program and the schema of a relational database.                             |
| Instance         | It is about data ownership and accountability.                                                                                                                                                  |
| Encapsulation    | In a database, the value of a column in a row has no such protection. Consequently, once stored in a database, data may be changed without the protection of the semantics encoded in a method. |
| Identity         | The essence of an identity problem is how to identify uniquely a collection of data values between both object- oriented program and a relational database.                                     |
| Processing Model | The essence of a processing model problem is how to represent in, maintain and retrieve from a database a sufficient set of objects for processing.                                             |
| Schema Ownership | The essence of the schema ownership problem is that the team who design and implement an object-oriented program can be different from the team who design and implement a relational database. |

## ORM Frameworks

ORM frameworks provide a middle layer between object-oriented code and database operations. They take the task of
adapting typical objects to forms that can be understood by database engines, and they perform operations at both sides
of the equation. These tools create a set of virtual object database that map classic database structures, can be
understood by developers, and behave as expected in an OOP environment. In a typical three-tier application where there
is a separation between the presentation, the business, and the data layers, ORM frameworks lie inside the data layer
and, contrary to the common presentation in books and articles, ORM frameworks can handle multiple database sources.

### Popular ORM tools/frameworks

#### Python

* [django ORM](https://www.fullstackpython.com/django.html)
* [SQLAlchemy](https://www.sqlalchemy.org/)
* [Peewee](https://peewee.readthedocs.io/en/latest/)
* [Pony ORM](https://ponyorm.org/)

#### Java

* [Hibernate](https://docs.jboss.org/hibernate/orm/current/userguide/html_single/Preface.html)
* [jOOQ](https://www.jooq.org/)
* [Top Link](https://docs.oracle.com/middleware/1213/toplink/solutions/index.html)
* [Eclipse Link](https://www.eclipse.org/eclipselink/documentation/2.7/concepts/toc.htm)
* [Open JPA](https://openjpa.apache.org/builds/3.0.0/apache-openjpa/docs/main.html)
* [MyBatis](https://mybatis.org/mybatis-3/index.html#)

#### PHP

* [RedBeanPHP](https://redbeanphp.com/index.php)
* [Eloquent ORM](https://laravel.com/docs/9.x/eloquent)
* [Doctrine ORM](https://www.doctrine-project.org/projects/orm.html)
* [Propel](http://propelorm.org/)
* [Cycle ORM](https://cycle-orm.dev/)
* [Solr](https://solr.apache.org/)

#### Javascript/Typescript

* [Knex.js: SQL Query Builder ](http://knexjs.org/)
* [Sequelize](https://sequelize.org/)
* [Bookshelf](https://bookshelfjs.org/)
* [Waterline](https://waterlinejs.org/)
* [Objection.js](https://vincit.github.io/objection.js/)
* [Mongoose](https://mongoosejs.com/)
* [Typegoose](https://typegoose.github.io/typegoose/)
* [TypeORM](https://typeorm.io/)
* [MikroORM](https://mikro-orm.io/)
* [Prisma](https://www.prisma.io/)

## ORM Terminology

There are a number of terms that we come across repeatedly. Many terms originate from the ORM designers, and others are
borrowed from the world of databases. This section provides a summary of the most commonly used terms in ORM solutions.

| Term         | Description                                                                                                                                                                                                                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entity       | Entity An entity is the complete set of data held by an application object  as defined by the developer in order to serve the needs of a specific  application. This data set replicates the data found in the underlying  database.                                                                                                                                      |
| Properties   | Entity’s data is stored in properties in the same way that classic objects  use properties to hold data. Entities match database  tables and table records; therefore, those instances should be uniquely  identifiable by the ORM framework at the entity level. This is resolved by  assigning a property to act as unique identifier.                                  |
| Associations | Entities make sense in a  model when they form relationships that represent logical and conceptual  notions. These relationships are called associations in ORM frameworks, and they are formed between one or more properties.                                                                                                                                           |
| Criteria     | At ORM level, queries are built based  on conditions that are passed to the underlying database engine. These  conditions, which can be generic or specific, are formed by attaching  criteria together.                                                                                                                                                                  |
| Projections  | Although you can retrieve all the properties (columns) of a table data from  a database using ORM criteria, common programming practice indicates  that you should only fetch the properties that are required in each  situation. This type of queries is managed differently by ORM packages  than the typical criteria-based queries, and they are called projections. |
| Container    | The framework  loads the relevant data in the memory in the form of entities or other  relevant data structures, performs the instructed operations, and then, many times, pushes back the changes to the database. This snapshot of the  data is managed by an entity container.                                                                                         |

## Advantages

* It abstracts away the database system so that switching from MySQL to PostgreSQL, or whatever flavor you prefer, is
  easy-peasy.
* Depending on the ORM you get a lot of advanced features out of the box, such as support for transactions, connection
  pooling, migrations, seeds, streams, and all sorts of other goodies.
* Many of the queries you write will perform better than if you wrote them yourself.

## Disadvantages

* There is overhead involved in learning how to use any given ORM.
* The initial configuration of an ORM can be a headache.

## Conclusions

* ORM represents a set of techniques in computer programming, which attempt to make incompatible systems cooperate,
  communicate, and exchange information. At the same time, they attempt to make the life of developers easier.
* ORM avoids the inclusion of embedded SQL statements in the application code, which in turn facilitates migration to
  another database management system, incorporating an abstraction layer between the physical relational model and the
  business layer of the application.
* In certain cases the use of an ORM is not recommended, especially when minimum response times are imposed or less
  overhead is required. In these cases it is better to use a microORM, avoiding inline SQL injections whenever possible.

## References

* [ORM for Python](https://medium.com/pragmatech/orm-for-python-b63cfbc39e7f)
* [What is ORM?](https://javabydeveloper.com/orm-object-relational-mapping/)
* [What are the best PHP ORMs?](https://www.slant.co/topics/5639/~php-orms)
