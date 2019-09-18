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

COUNT() - is an aggregate function that returns the number of items found in a set.  

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
