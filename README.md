#                                      *SQL Revision*

 Structured Query Language(SQL) as we all know is the database language by the use of which we can perform certain operations on the existing database and also we can use this language to create a database. SQL uses certain commands like Create, Drop, Insert etc. to carry out the required tasks.

 These SQL commands are mainly categorized into four categories:

 DDL – Data Definition Language
 DQl – Data Query Language
 DML – Data Manipulation Language
 DCL – Data Control Language

The three we are mainly going to focus on includes : DDL, DML & DQL


 |   *DDL*   |   *DML*   |   *DQL*   |
 |---------|---------|---------|
 | CREATE  | INSERT  | SELECT  |
 | ALTER   | UPDATE  |         |
 | RENAME  | DELETE  |         |
 | DROP    |         |         |

## *DQL*
DML statements are used for performing queries on the data within schema objects.
The purpose of DQL Command is to get some schema relation based on the query passed to it.

SELECT  - Is a statement that returns a result set of records from one or more tables

WHERE   - Is used to filter data

OR      - Is used to select either condition 1 or 2

For instance :

| Question : | Select all orders that the Ship City is Rio de Janeiro or Reims?              |
|------------|-------------------------------------------------------------------------------|
| Query    : | Select * FROM Orders WHERE ShipCity = 'Rio de janeiro' OR ShipCity = 'Reims'; |



### *DDL*

DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.

*CREATE AND ALTER*

The CREATE TABLE statement is used to create a new table in a database.

Example :

Create a Table that includes a UserID, User_name and contact info for Fullwell cross library

Query:

use my_db

CREATE TABLE Userlib_table          

(

user_ID VARCHAR(50) PRIMARY KEY Not Null,    --Assign field names with it's corresponding data type

User_name VARCHAR(6),

Email VARCHAR(50),

Telephone_no char (11)

);

The ALTER TABLE statement is used to add, delete, or modify columns in an existing table.

Example :

use my_db

ALTER TABLE Userlib_Table

ALTER COLUMN User_name VARCHAR (50)      --- In this case the field user_name was edited so its character/length could be increased from 6 to 50.


#### *DML*

The INSERT INTO statement is used to insert new records in a table.

If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query.
However, make sure the order of the values is in the same order as the columns in the table.

Example:

use my_db

INSERT INTO Userlib_table

Values ('1','JK Rowling', 'jk@gmail.com', '07508264512');
