# Contents

# Class Exercise
TASK - Use the Northwind Database to answer the following questions:
1. How many employees have a home in London?
**Query**
```sql
SELECT COUNT(*) FROM Employees WHERE City='London'
```
*Response**  
4

2. Which employee is a Doctor?

**Query**
```sql
SELECT FirstName, LastName FROM Employees WHERE TitleOfCourtesy='Dr.'
```
*Response**  
Andrew Fuller

3. How many products are discontinued? 
**Query**
```sql
SELECT COUNT(*) FROM Products WHERE Discontinued = 0
```
*Response**  
69

4. What are the names and product IDs of the prodcts with a unit price below 5.00? 
**Query**
```sql
SELECT ProductName, CategoryID FROM Products WHERE UnitPrice < 5.00
```
*Response**
![question4]()

5. Which categories have a category name with initials beginning with B or S?
**Query**
```sql
SELECT CategoryName FROM Categories WHERE CategoryName LIKE 'B%' or CategoryName LIKE 'S%' 
```
*Response**  
Beverages, Seafood

6. How many orders are there for EmployeeIDs 5 and 7 (The total for both)?
**Query**
```sql
SELECT COUNT(*) FROM Orders WHERE EmployeeID =5 OR EmployeeID=7
```
*Response**  
114

7. Write a SELECT using the Employees table and concatenate First Name and Last Name together. Use a column alias to rename the column to Employee Name.
**Query**
```sql
Select FirstName +' ' + LastName AS 'Employee Name' FROM Employees
```
*Response**
![question7]()

8. Write a SELECT statement to list the six countries that have Region Codes in the Customers Table. 
**Query**
```sql
SELECT Distinct Country FROM Customers WHERE Region IS NOT NULL
```
*Response**
![question8]()


