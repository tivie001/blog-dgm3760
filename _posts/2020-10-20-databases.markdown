---
layout: post
title:  "Blog Post #7 - Databases"
---
![Databases](/assets/databases.png)

## SQL vs. NoSQL vs. Object Relational Databases

--------------------------------------------------------------------------------

### SQL 
- They are relational meaning, it is a database structured to have the stored items of information related to each other or
have the ability to.
- Uses a structured query language and have a pre-defined schema (database blueprint)
- They can be vertically scalable as in adding more power to your existing database

Initially, I would use SQL database when the queries are complex because it is backed by the highly effective SQL query languages. 
I also think it was mentioned in class, that this is the type of database if you are dealing with lots of related transactions.

Some advantages are SQL databases is a widely-used option, making it safe and secure. And it is backed by the query language (SQL)
to manipulate the data you have. However, the disadvantages, it can be restrictive seeing you have to abide by their pre-defined
schemas (you have to structure things in the way they are given to you).   

![Database scalability](/assets/Scale-up-scale-out.png)

### NoSQL
- They are non-relational.
- They have dynamic schemas for unstructured data.
- Are widely popular when key-value pair data, or wide-column stores are needed.
- They can be horizontally scalable as in adding more machines or nodes (see graphic above) to give it more power.

NoSQL is beneficial when the use cases and features of your app are constantly changing, and grow rapidly! 

Some advantages to NoSQL databases the schema is highly flexible and easier to make changes to your database/data in contrary to SQL databases. NoSQL 
also makes it nice ot store many types of data without pre-defining them. However, some disadvantages are, Data integrity can be not 100% at times unlike SQL.
Also, running queries on a NoSQL database can be slower. And more importantly NoSQL does not support relations between data types.

### PostgresSQL
- Is a relational database as well, but it can also be defined as an Object Relational (OR) database which means 
that PostgresSQL stores complex data and relationships directly instead just rows and columns like a normal relational database.
- It supports: triggers, foreign keys, and stored procedures which are all ways to organize your data.

Again I would use an OR database like PostgresSQL if I was dealing with transactions, and user data related to each other. I actually worked for a 
accounting software company that used Postgres! 

Some disadvantages with OR databases is they can get quite a bit complicated too difficult to handle and update retroactively. This is due to it
not being relational to rows and columns.
