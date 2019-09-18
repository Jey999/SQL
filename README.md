Q1 - How many orders in NWDB?
Query: SELECT COUNT (*) From Orders
Response: 830
Q2 - How many order that the Ship City is Rio de Janeiro?
Query: SELECT COUNT(*) FROM Orders Where ShipCity= 'Rio de Janeiro';

SELECT COUNT(*) AS ‘Order Ship’ FROM Orders Where ShipCity lIKE 'Rio de Janeiro';
Response: 34
Q3 - Select all orders that the Ship City is Rio de Janeiro or Reims?
Query: Select * FROM Orders WHERE ShipCity = 'Rio de janeiro' OR ShipCity = 'Reims';
Select * FROM Orders WHERE ShipCity IN (‘Rio de janeiro','Reims');
Response:
Q4 - Select all of the entries where the Company name has a z or a Z in the table of Customers
Query: Select * FROM  Customers WHERE CompanyName LIKE '%z%'
Select * FROM customers WHERE CHARINDEX (‘z’, CompanyName) > 0  //
Response:
Q5 - We need to update all of our FAX information! This Day and age it is a must! 😅😅😅 Find me the Name of All of the companies that we do not have their FAX numbers! I would also like to know with whom I need to speak with, their contact numbers and what city they are base in.
Query: Select CompanyName,ContactName,Phone,City,Fax FROM  Customers WHERE Fax is NULL
Why can’t I do ?
SELECT CompanyName,Name,Telephone,City * FROM company Where FAX = NULL
Response:
Q6 - Ahh there you are! My prize ⭐️⭐️SPARTANTS⭐️⭐️! MY MARES AND MY STALLIONS! We need to re-target all of our Customers is Paris! Get me information on these clients.
Query: Select * FROM Customers WHERE City = 'Paris' ;
Response:
Q7 - WAIT! Where are you going? (...) These clients are hard to sell too! We need more intel.. Can you find out, from these clients from Paris/London, whom orders the most by quantity? Who are our top 5 clients?
Query:
SELECT SupplierID,
Sum (UnitsOnOrder)AS 'Total Order'
From Products
Group BY SupplierID
ORDER BY 'Total Order' DESC
---SELECT * From customers Where Customer ID = 37
The dot separates the table from the column

use Northwind
SELECT TOP 5 OrderID,UnitPrice,Quantity,Discount, UnitPrice*Quantity AS 'Gross Total'
FROM [Order Details]
Join Customers ON Customers.CustomerID= [Order Details].ProductID
where City = 'Paris'
ORDER BY [Gross Total] DESC
Select * From customers
Need details about customers but don’t know their orders
Look at orders by select * FROM orders
Don’t know the quantity customers ordered

So we go to order details we have quantity but we don’t know who ordered
So lets start by
Select * FROM Customers
Join Orders
ON customers.customerID = Orders.CustomerID
Join [Order Details]
ON Orders.OrderID = [Order Details].OrderID
Where City = ‘London’
Group BY – Customers.CustomerID, Customer
When u groupby mention everything u put what your looking for at the start i/















 * From Orders
Join [Order Details]
On Orders.OrderID = [Order Details].OrderID
Join Customers
ON Customers.CustomerID = Orders.CustomerID
---Where Shipcity LIKE london

Response:
Q8 - OMG What are you? Some kind of SQL Guardian Angel? THIS IS AMAZING! May God pay you handsomely 😸 because I have no cash on me!.. I do have one more request. I need to know more about these these Paris client. Can you find out which ones their deliveries took longer than 10 days? Display the Business/client name, contact name, all their contact details (don't forget the fax!), as well as the number of deliveries that where overdue! Just add a column named: 'Number overdue orders'! simple, thank you!
Query:
SELECT  Customers.CompanyName, Customers.ContactName, Customers.Phone, Customers.City,
CASE WHEN DATEDIFF(dd, OrderDate, ShippedDate) >10 THEN 'OVERDUE'
ELSE 'ONTIME'
End AS 'Status'
FROM Orders
Join Customers ON Customers.CustomerID= Orders.CustomerID
where City = 'Paris'

Response:
