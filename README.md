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

Numeric Datatypes:

The table below lists all the Numeric Datatypes in SQL along with their descriptions:

![Screenshot (967)](https://user-images.githubusercontent.com/81725794/181933407-9b17826c-e95b-4013-89fb-816ee8ea7fba.png)

Date/Time Datatypes:

The datatypes available in SQL to handle Date/Time operations effectively are called the Date/Time datatypes. The below table lists all the Date/Time variables in SQL along with their description:


![Screenshot (967)](https://user-images.githubusercontent.com/81725794/181933419-bada0478-a17b-402a-bbee-5f08b3c2a621.png)

4. SQL Commands

SQL Commands are instructions that are used by the user to communicate with the database, to perform specific tasks, functions and queries of data.

Types of SQL Commands:

![image](https://user-images.githubusercontent.com/81725794/181933434-3e663ddc-b476-4838-9526-6d36019ac007.png)

The above image broadly shows the different types of SQL commands available in SQL in the form of a chart.

1. Data Definition Language(DDL): It changes a table’s structure by adding, deleting and altering its contents. Its changes are auto-committed(all changes are automatically permanently saved in the database). Some commands that are a part of DDL are:

1. CREATE: Used to create a new table in the database.
Example:

CREATE TABLE STUDENT(Name VARCHAR2(20), Email VARCHAR2(100), DOB DATE);  

2. ALTER: Used to alter contents of a table by adding some new column or attribute, or changing some existing attribute.
Example:

ALTER TABLE STUDENT ADD(ADDRESS VARCHAR2(20));  
ALTER TABLE STUDENT MODIFY (ADDRESS VARCHAR2(20));  

3. DROP: Used to delete the structure and record stored in the table.
Example:

DROP TABLE STUDENT;  

4. TRUNCATE: Used to delete all the rows from the table, and free up the space in the table.
Example:
TRUNCATE TABLE STUDENT;

2. Data Manipulation Language(DML): It is used for modifying a database, and is responsible for any form of change in a database. These commands are not auto-committed, i.e all changes are not automatically saved in the database. Some commands that are a part of DML are:

INSERT: Used to insert data in the row of a table.
Example:

INSERT INTO STUDENT (Name, Subject) VALUES ("Scaler", "DSA"); 



