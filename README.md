# SQL Exercises

## Topics

- Structured Query Language (SQL)
- Relational Databases
- SQLite
- Writing Basic Queries

## Assignments

### Create a Database Table

- use DB Browser for SQLite to create a database, name it anything you want.
- add an _accounts_ table with the following _schema_:

  - `id`, numeric value with no decimal places that should autoincrement.
  - `name`, string, add whatever is necessary to make searching by name faster.
  - `budget` numeric value.

- constraints
  - the `id` should be the primary key for the table.
  - account `name` should be unique.
  - account `name`, required.

# Inside the DB Browser

- when creating the table
  CREATE TABLE `accounts` (
  `id` INTEGER PRIMARY KEY AUTOINCREMENT,
  `name` TEXT NOT NULL UNIQUE,
  `budget` REAL
  );
- save the table by cliking on _Write Changes_
- Execute SQL
  select \* from accounts
  this command shows all accounts

_id_ _name_ _budget_
"1" "ice cream" "399.99"
"2" "IPhone X" "1279.66"
"3" "IPad" "499.99"
"4" "Airpods" "199.99"

### Write Basic Queries

- Visit [SQL Try Editor at W3Schools.com](https://www.w3schools.com/Sql/tryit.asp?filename=trysql_select_top) and write the following queries:

  - find all customers with a particular first name.
    SELECT \* FROM Customers where CustomerName like 'Antonio%'

  - find all customers that live in London.
    SELECT \* FROM Customers where city='London'

  - find the phone number for a particular supplier (provide id, or supplier name).
    SELECT PHONE FROM Suppliers where SupplierName='Exotic Liquid' OR SupplierID='4'

  - find all customers in a particular postal code.
    SELECT \* FROM Customers where PostalCode='12209'

  - find all suppliers who have names with more than 20 characters.
    SELECT \* FROM Suppliers where length(SupplierName) > 20

  - list customers descending by the number of orders.
    SELECT customerID, count(\*) as orders FROM [Orders] group by customerid order by orders desc

  - list orders descending by the order date.
    SELECT \* from Orders order by OrderDate desc

  - list orders grouped by customer showing the number of orders per customer.
  - list orders grouped by customer's city showing number of orders per city.

  - add a customer using your information.
  - add 2 products.
  - add 2 orders with you as the customer.
  - delete all customers that have no orders.

Clicking the `Restore Database` in that page will repopulate the database with the original data and discard all changes you have made.
