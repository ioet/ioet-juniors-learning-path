---
layout: "../../../../layouts/BlogPost.astro"
title: "What Is a Non-Relational Database?"
pubDate: "2022-09-14"
---

Most databases can be categorized as either relational or non-relational. Non-relational databases are sometimes referred to as “NoSQL,” which stands for Not Only SQL. The main difference between these is how they store their information.

A non-relational database stores data in a non-tabular form, and tends to be more flexible than the traditional, SQL-based, relational database structures. It does not follow the relational model provided by traditional relational database management systems.

## Topics

- [Topics](#topics)
- [Non-relational database](#non-relational-database)
- [The benefits of a non-relational database](#the-benefits-of-a-non-relational-database)
  - [Massive dataset organization](#massive-dataset-organization)
  - [Flexible database expansion](#flexible-database-expansion)
  - [Multiple data structures](#multiple-data-structures)
  - [Built for the cloud](#built-for-the-cloud)
- [Types of NoSQL databases](#types-of-nosql-databases)
- [Dynamic schemas](#dynamic-schemas)
- [Replication](#replication)
- [Non-relational databases and application development](#non-relational-databases-and-application-development)
  - [Reference](#reference)

## Non-relational database

Non-relational databases (often called NoSQL databases) are different from traditional relational databases in that they store their data in a non-tabular form. Instead, non-relational databases might be based on data structures like documents. A document can be highly detailed while containing a range of different types of information in different formats. This ability to digest and organize various types of information side-by-side makes non-relational databases much more flexible than relational databases.
![NoSQL](https://webimages.mongodb.com/_com_assets/cms/ku47c2z5sv9fu26rp-image3.png?auto=format%252Ccompress)
Example MongoDB Document for a Patient in Healthcare.

Non-relational databases are often used when large quantities of complex and diverse data need to be organized. For example, a large store might have a database in which each customer has their own document containing all of their information, from name and address to order history and credit card information. Despite their differing formats, each of these pieces of information can be stored in the same document.

Non-relational databases often perform faster because a query doesn’t have to view several tables in order to deliver an answer, as relational datasets often do. Non-relational databases are therefore ideal for storing data that may be changed frequently or for applications that handle many different kinds of data. They can support rapidly developing applications requiring a dynamic database able to change quickly and to accommodate large amounts of complex, unstructured data.

When starting a project, it is worth considering relational vs non-relational databases, in terms of their differences, to get a better understanding of the right solution for the project. You can also consider different examples of the uses for both, and when you might want to choose one over the other.

## The benefits of a non-relational database

Today’s applications collect and store increasingly vast quantities of ever-more complex customer and user data. The benefits of this data to businesses, of course, lie in their potential for analysis. Using a non-relational database can unlock patterns and value even within masses of variegated data.

There are several advantages to using non-relational databases, including:

### Massive dataset organization

In the age of Big Data, non-relational databases can not only store massive quantities of information, but they can also query these datasets with ease. Scale and speed are crucial advantages of non-relational databases.

### Flexible database expansion

Data is not static. As more information is collected, a non-relational database can absorb these new data points, enriching the existing database with new levels of granular value even if they don’t fit the data types of previously existing information.

### Multiple data structures

The data now collected from users takes on a myriad of forms, from numbers and strings, to photo and video content, to message histories. A database needs the ability to store these various information formats, understand relationships between them, and perform detailed queries. No matter what format your information is in, non-relational databases can collate different information types together in the same document.

### Built for the cloud

A non-relational database can be massive. And as they can, in some cases, grow exponentially, they need a hosting environment that can grow and expand with them. The cloud’s inherent scalability makes it an ideal home for non-relational databases.

## Types of NoSQL databases

- **Document databases**: in these databases each key is paired with a complex data structure called a 'document'. Documents can contain many different key-value pairs, or key-array pairs, or even nested documents.

- **Network stores**: are used to store information about data networks, such as social connections. Examples of graph stores are Neo4J and Giraph.

- **Key-value stores**: these are the simplest NoSQL databases. Each database element is stored as an attribute name (or "key"), along with its value. Examples of key-value stores are Riak and Berkeley DB. In some key-value stores, such as Redis, each value can have a type, such as "integer", which adds functionality.

- **Column-oriented databases**: These databases, such as Cassandra or HBase, allow queries on large data sets and store data in columns, rather than rows.

## Dynamic schemas

In relational databases it is necessary to define schemas before adding data. For example, if you want to store customer data, such as telephone number, first and last name, address, city and province, the SQL database must know in advance the type of data to be stored.

This hinders agility in development, because every time features are added, the database schema must often be modified. So, if after several iterations of development, you decide that you want to store customers' favorite items in addition to their address and phone number, you must add that column to the database and then migrate the entire database to the new schema.

If the database is large, the process will be very slow and the activity will be interrupted for a long time. If you frequently change the data stored in the application - because you iterate quickly - you will also be interrupted frequently. Relational databases also cannot include unstructured or previously unknown data.

NoSQL databases are designed so that data can be inserted without a predefined schema. This makes it easy to make major modifications to applications in real time without service interruptions, so development is faster, code integration is more reliable, and database administrators have less work to do. Traditionally, developers have had to add code to the application to perform data quality checks, such as forcing the presence of specific fields, data types or permissible values. NoSQL databases, being more sophisticated, allow the application of validation rules in the database, so that users can apply governance to the data, taking advantage of the agility offered by a dynamic schema.

## Replication

Most NoSQL databases also support automatic database replication to ensure availability in the event of service interruptions or planned maintenance outages. More sophisticated NoSQL databases are self-healing and offer failover and recovery features, as well as the ability to distribute the database across multiple geographic regions to support regional failures and enable data localization. Unlike relational databases, NoSQL databases do not need to use other applications or expensive plug-ins to implement replication.

## Non-relational databases and application development

Applications must be able to query data efficiently and deliver results almost instantly. Non-relational databases are a natural choice for this kind of environment. They offer both security and agility, allowing for rapid development of applications in an agile environment. Easier and less complex to manage than relational databases, they can also yield lower data management costs while providing superior performance and speed.

Naturals for agile development, non-relational databases can accommodate the complexity of data inputs more efficiently than structured databases. In an age of increasing data complexity, non-relational databases provide the flexibility in database design that has become increasingly indispensable. Especially when paired with the cloud, non-relational databases lift the limits on your data collection, organization, and analysis, allowing you to get the most out of your data.

### Reference

- [MongoDB](https://www.mongodb.com/)
- [Fundamentals of NoSQL databases](https://www.mongodb.com/es/nosql-explained#:~:text=When%20people%20use%20the%20term,format%20other%20than%20relational%20tables.)
- [MongoDB Technical Document](https://www.mongodb.com/es/collateral/top-5-considerations-when-evaluating-nosql-databases)
