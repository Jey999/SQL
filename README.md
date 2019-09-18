#               SQL Revision
 DML - Data Manipulation Language
 DDL - Data Definition Language

| DML    | DDL    |
|--------|--------|
| SELECT | CREATE |
| INSERT | ALTER  |
| UPDATE | DROP   |

##DML EXAMPLES
SELECT - Is a statement that returns a result set of records from one or more tables

COUNT() - is an aggregate function that returns the number of items found in a set.  

WHERE  - Is used to filter data

OR  - Is used to select either condition 1 or 2

For instance :
Q1) Select all orders that the Ship City is Rio de Janeiro or Reims?

Query: Select * FROM Orders WHERE ShipCity = 'Rio de janeiro' OR ShipCity = 'Reims';
