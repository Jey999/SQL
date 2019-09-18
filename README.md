#               SQL Revision
 DML - Data Manipulation Language
 DDL - Data Definition Language

| DML    | DDL    |
|--------|--------|
| SELECT | CREATE |
| INSERT | ALTER  |
| UPDATE | DROP   |

## DQL
SELECT  - Is a statement that returns a result set of records from one or more tables

WHERE   - Is used to filter data

OR      - Is used to select either condition 1 or 2

For instance :

| Question : | Select all orders that the Ship City is Rio de Janeiro or Reims?              |
|------------|-------------------------------------------------------------------------------|
| Query    : | Select * FROM Orders WHERE ShipCity = 'Rio de janeiro' OR ShipCity = 'Reims'; |

### DML

The following aggregate functions can be used to calculate totals usually in conjunction with the GROUP BY clause:

| SUM   : | SUM(OrderTotal) for the grand total of a column for all rows selected                    |
|---------|------------------------------------------------------------------------------------------|
| AVG   : | AVG (UnitPrice) for the average of a column for all rows selected                        |
| MIN   : | Min (UnitPrice) for the smallest value in a column for all rows selected                 |
| MAX   : | Max (UnitPrice) for the lagest value in a column for all rows selected                   |
| COUNT : | COUNT(*) for the number of NOT NULL rows selected if * is used then all rows are counted |   

For Example :

SELECT Supplier

#### DDL

CREATE AND ALTER

The CREATE TABLE statement is used to create a new table in a database.

Create a Table that includes a UserID, User_name and contact info for Fullwell cross library:

use my_db
CREATE TABLE Userlib_table               
(
user_ID VARCHAR(50) PRIMARY KEY Not Null,    --Assign field names with it's corresponding data type
User_name VARCHAR(6),
Email VARCHAR(50),
Telephone_no char (11)
);

The ALTER TABLE statement is used to add, delete, or modify columns in an existing table.

use my_db
ALTER TABLE Userlib_Table
ALTER COLUMN User_name VARCHAR (50)      --- In this case the field user_name was edited so its character/length could be increased from 6 to 50.

The INSERT INTO statement is used to insert new records in a table.

If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. The INSERT INTO syntax would be as follows:

use my_db
INSERT INTO Userlib_table
Values ('1','JK Rowling', 'jk@gmail.com', '07508264512');
