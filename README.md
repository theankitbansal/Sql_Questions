# Sql_Questions

Introduction: What is SQL?

To get introduced to SQL, we first need to know about Databases and Database Management Systems(DBMS).
Data is basically a collection of facts related to some object. A Database is a collection of small units of data arranged in a systematic manner. A Relational Database Management System is a collection of tools that allows the users to manipulate, organize and visualize the contents of a database while following some standard rules that facilitate fast response between the database and the user side.

After getting introduced to the concept of data, databases and DBMS/RDBMS, we can finally learn about SQL. SQL or Structured Query Language is basically the language that we (the user) use to communicate with the Databases and get our required interpretation of data out of it. It is used for storing, manipulating and retrieving data out of a database.

SQL Features

SQL allows us to interact with the databases and bring out/manipulate data within them. Using SQL, we can create our own databases and then add data into these databases in the form of tables.

The following functionalities can be performed on a database using SQL:

1. Create or Delete a Database.
2. Create or Alter or Delete some tables in a Database.
3. SELECT data from tables.
4. INSERT data into tables.
5. UPDATE data in tables.
6. DELETE data from tables.
7. Create Views in the database.
8. Execute various aggregate functions.

Learn SQL: Basic to Advanced Concepts

1. Installation
To get started with using SQL, we first need to install some Database Management System server. After installing the RDBMS, the RDBMS itself will provide all the required tools to perform operations on the database and its contents through SQL. Some common RDBMS which is highly in use are:

Oracle
MySQL
PostgreSQL
Heidi SQL

To install any RDBMS, we just need to visit their official website and install the setup file from there, by following the instructions available there. With the server setup, we can set up a Query Editor, on which we can type our SQL Queries.

2. Tables

All data in the database are organized efficiently in the form of tables. A database can be formed from a collection of multiple tables, where each table would be used for storing a particular kind of data and the table by themselves would be linked with each other by using some relations.

SQL-Create Table:

We use the CREATE command to create a table. The table in the above example can be created with the following code:

CREATE TABLE student(
   ID INT NOT NULL,
   Name varchar(25),
   Phone varchar(12),
   Class INT
);

SQL-Delete Table:

To delete a table from a database, we use the DROP command.

DROP TABLE student;

3. SQL DataTypes

To allow the users to work with tables effectively, SQL provides us with various datatypes each of which can be useful based on the type of data we handle.

![image](https://user-images.githubusercontent.com/81725794/181932725-04ac6df5-026f-4775-9697-095861182a26.png)

The above image is a chart that shows all the datatypes available in SQL along with some of their examples.

The next section describes various most popular SQL server datatypes categorised under each major division.

String Datatypes:

The table below lists all the String type datatypes available in SQL, along with their descriptions:

![Screenshot (965)](https://user-images.githubusercontent.com/81725794/181933343-6b7af41d-5422-457e-ada3-851b6c341ef7.png)




