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

1. Data Definition Language(DDL): It changes a table???s structure by adding, deleting and altering its contents. Its changes are auto-committed(all changes are automatically permanently saved in the database). Some commands that are a part of DDL are:

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

In the above example, we insert the values ???Scaler??? and ???DSA??? in the columns Name and Subject in the STUDENT table.

UPDATE: Used to update value of a table???s column.
Example:

UPDATE STUDENT   
SET User_Name = 'Interviewbit'    
WHERE Student_Id = '2'  
In the above example, we update the name of the student, whose Student_ID is 2, to the User_Name = ???Interviewbit???.

DELETE: Used to delete one or more rows in a table.
Example:

DELETE FROM STUDENT 
WHERE Name = "Scaler";  
In the above example, the query deletes the row where the Name of the student is ???Scaler??? from the STUDENT table.

3. Data Control Language(DCL): These commands are used to grant and take back access/authority (revoke) from any database user. Some commands that are a part of DCL are:

Grant: Used to grant a user access privileges to a database.
Example:

GRANT SELECT, UPDATE ON TABLE_1 TO USER_1, USER_2;  
In the above example, we grant the rights to SELECT and UPDATE data from the table TABLE_1 to users - USER_1 and USER_2.

Revoke: Used to revoke the permissions from an user.
Example:

REVOKE SELECT, UPDATE ON TABLE_1 FROM USER_1, USER_2;  

In the above example we revoke the rights to SELECT and UPDATE data from the table TABLE_1 from the users- USER_1 and USER_2.

4. Transaction Control Language: These commands can be used only with DML commands in conjunction and belong to the category of auto-committed commands. Some commands that are a part of TCL are:

COMMIT: Saves all the transactions made on a database.
Example:

DELETE FROM STUDENTS
WHERE AGE = 16;  
COMMIT;  
In the above database, we delete the row where AGE of the students is 16, and then save this change to the database using COMMIT.

ROLLBACK: It is used to undo transactions which are not yet been saved.
Example:
DELETE FROM STUDENTS 
WHERE AGE = 16;  
ROLLBACK;  
By using ROLLBACK in the above example, we can undo the deletion we performed in the previous line of code, because the changes are not committed yet.

SAVEPOINT: Used to roll transaction back to a certain point without having to roll back the entirity of the transaction.
Example:

SAVEPOINT SAVED;
DELETE FROM STUDENTS 
WHERE AGE = 16;  
ROLLBACK TO SAVED;

In the above example, we have created a savepoint just before performing the delete operation in the table, and then we can return to that savepoint using the ROLLBACK TO command.

5. Data Query Language: It is used to fetch some data from a database. The command belonging to this category is:

SELECT: It is used to retrieve selected data based on some conditions which are described using the WHERE clause. It is to be noted that the WHERE clause is also optional to be used here and can be used depending on the user???s needs.
Example: With WHERE clause,

SELECT Name  
FROM Student  
WHERE age >= 18;  
Example: Without WHERE clause,

SELECT Name  
FROM Student 
In the first example, we will only select those names in the Student table, whose corresponding age is greater than 17. In the 2nd example, we will select all the names from the Student table.

5. SQL Constraints

Constraints are rules which are applied on a table. For example, specifying valid limits or ranges on data in the table etc.

The valid constraints in SQL are:

1. NOT NULL: Specifies that this column cannot store a NULL value.

Example:

CREATE TABLE Student
(
   ID int(8) NOT NULL,
   NAME varchar(30) NOT NULL,
   ADDRESS varchar(50)
);
In the above example, we create a table STUDENT, which has some attributes it has to store. Among these attributes we declare that the columns ID and NAME cannot have NULL values in their fields using NOT NULL constraint.

2. UNIQUE: Specifies that this column can have only Unique values, i.e the values cannot be repeated in the column.

Example:

CREATE TABLE Student
(
   ID int(8) UNIQUE,
   NAME varchar(10) NOT NULL,
   ADDRESS varchar(20)
);
In the above example, we create a table Student and declare the ID column to be unique using the UNIQUE constraint.

3. Primary Key: It is a field using which it is possible to uniquely identify each row in a table. We will get to know about this in detail in the upcoming section.

4. Foreign Key: It is a field using which it is possible to uniquely identify each row in some other table. We will get to know about this in detail in the upcoming section.

5. CHECK: It validates if all values in a column satisfy some particular condition or not.

Example:

CREATE TABLE Student
(
   ID int(6) NOT NULL,
   NAME varchar(10),
   AGE int CHECK (AGE < 20)
);
Here, in the above query, we add the CHECK constraint into the table. By adding the constraint, we can only insert entries that satisfy the condition AGE < 20 into the table.

6. DEFAULT: It specifies a default value for a column when no value is specified for that field.

Example:

CREATE TABLE Student
(
   ID int(8) NOT NULL,
   NAME varchar(50) NOT NULL,
   CLASS int DEFAULT 2
);
In the above query, we set a default value of 2 for the CLASS attribute. While inserting records into the table, if the column has no value specified, then 2 is assigned to that column as the default value.

6. Crud Operations in SQL

CRUD is an abbreviation for Create, Read, Update and Delete. These 4 operations comprise the most basic database operations. The relevant commands for these 4 operations in SQL are:

Create: INSERT
Read: SELECT
Update: UPDATE
Delete: DELETE

![image](https://user-images.githubusercontent.com/81725794/182010294-0a393d37-f1cf-4048-8173-8657e62bc98c.png)

The above image shows the pillars of SQL CRUD operations.

INSERT: To insert any new data ( create operation - C ) into a database, we use the INSERT INTO statement.
SQL Syntax:

INSERT INTO name_of_table(column1, column2, ....)
   VALUES(value1, value2, ....)
Example:

INSERT INTO student(ID, name, phone, class)
   VALUES(1, 'Scaler', '+1234-4527', 12)
For multiple rows,

SQL Syntax:

INSERT INTO name_of_table(column1, column2, ....)
   VALUES(value1, value2, ....),
   (new_value1, new_value2, ...),
   (....), ... ;
   
Example:

INSERT INTO student(ID, name, phone, class)
   VALUES(1, 'Scaler', '+1234-4527', 12),
   (2, 'Interviewbit', '+4321-7654', 11);
The above example will insert into the student table having the values 1, Scaler, +1234-5678 and 12 to the columns ID, name, phone and class columns.

SELECT: We use the select statement to perform the Read ( R ) operation of CRUD.
SQL Syntax:

SELECT column1,column2,.. FROM name_of_table;

Example:

SELECT name,class FROM student;
The above example allows the user to read the data in the name and class columns from the student table.

UPDATE: Update is the ???U??? component of CRUD. The Update command is used to update the contents of specific columns of specific rows.
SQL Syntax:

UPDATE name_of_table
SET column1=value1,column2=value2,...
WHERE conditions...;
Example:

UPDATE customers
SET phone = '+1234-9876'
WHEREID = 2;
The above SQL example code will update the table ???customers??? whose ID is 2 with the new given phone number.

DELETE:
The Delete command is used to delete or remove some rows from a table. It is the ???D??? component of CRUD.

SQL Syntax:

DELETE FROM name_of_table
WHERE condition1, condition2, ...;
Example:

DELETE FROM student
WHERE class = 11;
The above SQL example code will delete the row from table student, where the class = 11 conditions becomes true.

7. Important SQL Keywords

![image](https://user-images.githubusercontent.com/81725794/182010452-e1b77e1d-c533-49c0-82da-15d7329ac7f3.png)

The below table lists some important keywords used in SQL, along with their description and example.
![Screenshot (968)](https://user-images.githubusercontent.com/81725794/182010467-5eb4b5bb-6682-46e8-8f83-666ad44ab83a.png)

![Screenshot (969)](https://user-images.githubusercontent.com/81725794/182010469-4bf32bc2-d040-4e86-8c5c-00b301a86dae.png)

![Screenshot (970)](https://user-images.githubusercontent.com/81725794/182010477-74a7d6e8-3c3a-47d1-aa41-05bed30e4750.png)

8. Clauses in SQL

Clauses are in-built functions available in SQL and are used for filtering and analysing data quickly allowing the user to efficiently extract the required information from the database.

The below table lists some of the important SQL clauses and their description with examples:
![Screenshot (971)](https://user-images.githubusercontent.com/81725794/182010481-20bfa48a-7517-4d6d-aa02-4b236e742e4a.png)

9. SQL Operators

Operators are used in SQL to form complex expressions which can be evaluated to code more intricate queries and extract more precise data from a database.

There are 3 main types of operators: Arithmetic, Comparision and Logical operators, each of which will be described below.

![image](https://user-images.githubusercontent.com/81725794/182010505-0fd447da-39f4-412b-abcb-1fd1a9a2230e.png)

Arithmetic Operators:

Arithmetic Operators allows the user to perform arithmetic operations in SQL. The table below shows the list of arithmetic operators available in SQL:

![Screenshot (972)](https://user-images.githubusercontent.com/81725794/182010577-67288a49-7139-4024-89fd-389f568114e5.png)

Bitwise Operators:

Bitwise operators are used to performing Bit manipulation operations in SQL. The table below shows the list of bitwise operators available in SQL:

![Screenshot (972](https://user-images.githubusercontent.com/81725794/182010585-ccc39125-be23-4585-b264-7424de6ac2a7.png)

Relational Operators:

Relational operators are used to performing relational expressions in SQL, i.e those expressions whose value either result in true or false. The table below shows the list of relational operators available in SQL:

![Screenshot (973)](https://user-images.githubusercontent.com/81725794/182010591-0206a708-dcb2-4dac-ba79-7f6ab3b1df20.png)

Compound Operators:

Compound operators are basically a combination of 2 or more arithmetic or relational operator, which can be used as a shorthand while writing code. The table below shows the list of compound operators available in SQL:

![Screenshot (974)](https://user-images.githubusercontent.com/81725794/182010595-04c2b176-ae77-4b07-8856-b3490219243e.png)

Logical Operators:

Logical operators are used to combining 2 or more relational statements into 1 compound statement whose truth value is evaluated as a whole. The table below shows the SQL logical operators with their description:

![Uploading Screenshot (975).png???]()

10. Keys in SQL
A database consists of multiple tables and these tables and their contents are related to each other by some relations/conditions. To identify each row of these tables uniquely, we make use of SQL keys. A SQL key can be a single column or a group of columns used to uniquely identify the rows of a table. SQL keys are a means to ensure that no row will have duplicate values. They are also a means to establish relations between multiple tables in a database.

Types of Keys:

1. Primary Key: They uniquely identify a row in a table.

Properties:

Only a single primary key for a table. (A special case is a composite key, which can be formed by the composition of 2 or more columns, and act as a single candidate key.)
The primary key column cannot have any NULL values.
The primary key must be unique for each row.
Example:

CREATE TABLE Student (
   ID int NOT NULL,
   LastName varchar(255) NOT NULL,
   FirstName varchar(255),
   Class int,
   PRIMARY KEY (ID)
);
The above example creates a table called STUDENT with some given properties(columns) and assigns the ID column as the primary key of the table. Using the value of ID column, we can uniquely identify its corresponding row.

2. Foreign Key: Foreign keys are keys that reference the primary keys of some other table. They establish a relationship between 2 tables and link them up.

Example: In the below example, a table called Orders is created with some given attributes and its Primary Key is declared to be OrderID and Foreign Key is declared to be PersonId referenced from the Person's table. A person's table is assumed to be created beforehand.

CREATE TABLE Orders (
   OrderID int NOT NULL,
   OrderNumber int NOT NULL,
   PersonID int,
   PRIMARY KEY (OrderID),
   FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
Super Key: It is a group of single or multiple keys which identifies row of a table.
Candidate Key: It is a collection of unique attributes that can uniquely identify tuples in a table.
Alternate Key: It is a column or group of columns that can identify every row in a table uniquely.
Compound Key: It is a collection of more than one record that can be used to uniquely identify a specific record.
Composite Key: Collection of more than one column that can uniquely identify rows in a table.
Surrogate Key: It is an artificial key that aims to uniquely identify each record.
Amongst these, the Primary and Foreign keys are most commonly used.

11. Functions in SQL

The SQL Server has many builtin functions some of which are listed below:

SQL Server String Functions:
The table below lists some of the String functions in SQL with their description:

![Screenshot (976)](https://user-images.githubusercontent.com/81725794/182010679-9210988c-d958-4f27-8850-cea01f73bc4a.png)

SQL Server Numeric Functions:
The table below lists some of the Numeric functions in SQL with their description:

![Screenshot (977)](https://user-images.githubusercontent.com/81725794/182010688-2b276b43-f5eb-48c9-b65f-e8b3b92f9a31.png)

SQL Server Date Functions:
The table below lists some of the Date functions in SQL with their description:

![Screenshot (978)](https://user-images.githubusercontent.com/81725794/182010728-e121f4e2-372b-43fb-ba01-799b42fc644c.png)

SQL Server Advanced Functions:
The table below lists some of the Advanced functions in SQL with their description:

![Screenshot (979)](https://user-images.githubusercontent.com/81725794/182010732-2d5239ea-d642-42e1-b2d7-ac15ac5773a3.png)

12. Joins in SQL

Joins are a SQL concept that allows us to fetch data after combining multiple tables of a database.

The following are the types of joins in SQL:

INNER JOIN: Returns any records which have matching values in both tables.

![image](https://user-images.githubusercontent.com/81725794/182010754-50b71a40-1167-4534-9f31-576abac01b63.png)

Example:

Consider the following tables,

![image](https://user-images.githubusercontent.com/81725794/182010762-3eee5256-dcf1-48d3-a06d-7390d49c97ef.png)

Let us try to build the below table, using Joins,

![image](https://user-images.githubusercontent.com/81725794/182010772-68665642-26d4-4d21-85f8-73951d1b42fd.png)

The SQL code will be as follows,

SELECT orders.order_id, products.product_name,customers.customer_name,products.price
FROM orders
INNER JOIN products ON products.product_id = order.product_id
INNER JOIN customers on customers.customer_id = order.customer_id;
NATURAL JOIN: It is a special type of inner join based on the fact that the column names and datatypes are the same on both tables.
Syntax:

Select * from table1 Natural JOIN table2;
Example:

Select * from Customers Natural JOIN Orders;

In the above example, we are merging the Customers and Orders table shown above using a NATURAL JOIN based on the common column customer_id.

RIGHT JOIN: Returns all of the records from the second table, along with any matching records from the first.

![image](https://user-images.githubusercontent.com/81725794/182010788-5894acbf-45b0-4fd9-b2d0-15680de83156.png)

Example:

Let us define an Orders table first,

![image](https://user-images.githubusercontent.com/81725794/182010794-7452a1d3-fac9-4dfe-8594-536ec70e1af8.png)

Let us also define an Employee table,

![image](https://user-images.githubusercontent.com/81725794/182010801-4112ff04-ce21-4f25-a2fa-4b2b10ac46e1.png)

Applying right join on these tables,

SELECT Orders.OrderID, Employees.LastName, Employees.FirstName
FROM Orders
RIGHT JOIN Employees
ON Orders.EmployeeID = Employees.EmployeeID
ORDER BY Orders.OrderID;
The resultant table will be,

![image](https://user-images.githubusercontent.com/81725794/182010811-b8fee322-2d66-4f78-9e2a-105ec919304c.png)

LEFT JOIN: Returns all of the records from the first table, along with any matching records from the second table.

![image](https://user-images.githubusercontent.com/81725794/182010818-0b6a8fe2-3b0d-4752-a1b1-649f27778183.png)

Example:

Consider the below Customer and Orders table,

![image](https://user-images.githubusercontent.com/81725794/182010832-47f641f3-4336-44b0-8fa6-f21b15781ee0.png)

![image](https://user-images.githubusercontent.com/81725794/182010836-96e38d52-f884-482e-b1bf-5489d56384b5.png)

We will apply Left Join on the above tables, as follows,

SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders
ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
The top few entries of the resultant table will appear as shown in the below image.

![image](https://user-images.githubusercontent.com/81725794/182010850-a638bbed-7023-4aeb-9d15-587ba89bf345.png)

FULL JOIN: Returns all records from both tables when there is a match.

![image](https://user-images.githubusercontent.com/81725794/182010870-96aef906-ebf8-4ff4-904f-d2a256a66309.png)

Example:

Consider the below tables, Customers and Orders,

Table Customers:

![image](https://user-images.githubusercontent.com/81725794/182010874-ebd5a49f-5654-4c23-bd8b-b9d87014b0d6.png)

Table Orders:

![image](https://user-images.githubusercontent.com/81725794/182010880-3d22fdd0-6bdd-4857-ba4d-ac312dd92361.png)

Applying Outer Join on the above 2 tables, using the code:

SELECT  ID, NAME, AMOUNT, DATE
  FROM CUSTOMERS
  FULL JOIN ORDERS
  ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;
We will get the following table as the result of the outer join.

![image](https://user-images.githubusercontent.com/81725794/182010890-3fac544e-797b-41e4-b551-b81a2c4ae25e.png)

13. Triggers in SQL

SQL codes automatically executed in response to a certain event occurring in a table of a database are called triggers. There cannot be more than 1 trigger with a similar action time and event for one table.

Syntax:

Create Trigger Trigger_Name
(Before | After)  [ Insert | Update | Delete]
on [Table_Name]
[ for each row | for each column ]
[ trigger_body ]
Example:

CREATE TRIGGER trigger1
before INSERT
ON Student
FOR EACH ROW
SET new.total = (new.marks/ 10) * 100;
Here, we create a new Trigger called trigger1, just before we perform an INSERT operation on the Student table, we calculate the percentage of the marks for each row.
Some common operations that can be performed on triggers are:

DROP: This operation will drop an already existing trigger from the table.
Syntax:
DROP TRIGGER trigger name;
SHOW: This will display all the triggers that are currently present in the table.
Syntax:
SHOW TRIGGERS IN database_name;

14. SQL Stored Procedures

SQL procedures are stored in SQL codes, which can be saved for reuse again and again.

Syntax:

CREATE PROCEDURE procedure_name AS sql_statement
GO;
To execute a stored procedure,

EXEC procedure_name;
Example:

CREATE PROCEDURE SelectAllCustomers AS SELECT * FROM Customers;
GO;
The above example creates a stored procedure called ???SelectAllCustomers???, which selects all the records from the customer table.

15. SQL Injection
Insertion or ???Injection??? of some SQL Query from the input data of the client to the application is called SQL Injection. They can perform CRUD operations on the database and can read to vulnerabilities and loss of data.

It can occur in 2 ways:

Data is used to dynamically construct an SQL Query.
Unintended data from an untrusted source enters the application.
The consequences of SQL Injections can be Confidentiality issues, Authentication breaches, Authorization vulnerabilities, and breaking the Integrity of the system.

![image](https://user-images.githubusercontent.com/81725794/182010912-d27bd0ce-bfec-4bd5-b237-ab53993315f3.png)

he above image shows an example of SQL injections, through the use of 2 tables - students and library. 

Here the hacker is injecting SQL code - 

UNION SELECT studentName, rollNo FROM students 
into the Database server, where his query is used to JOIN the tables - students and library. Joining the 2 tables, the result of the query is returned from the database, using which the hacker gains access to the information he needs thereby taking advantage of the system vulnerability. The arrows in the diagram show the flow of how the SQL Injection causes the vulnerability in the database system, starting from the hacker???s computer.

Conclusion

Databases are growing increasingly important in our modern industry where data is considered to be a new wealth. Managing these large amounts of data, gaining insights from them and storing them in a cost-effective manner makes database management highly important in any modern software being made. To manage any form of databases/RDBMS, we need to learn SQL which allows us to easily code and manage data from these databases and create large scalable applications of the future, which caters to the needs of millions.



