# Joins in MySQL

In MySQL, joins are used to combine rows from two or more tables based on a related column between them. 

There are different types of joins available in MySQL:

- **INNER JOIN**: Returns only the matching rows from both tables.
- **LEFT JOIN**: Returns all the rows from the left table and the matching rows from the right table.
- **RIGHT JOIN**: Returns all the rows from the right table and the matching rows from the left table.
- **FULL OUTER JOIN**: Returns all the rows from both tables, including the unmatched rows.


### MySQL INNER JOIN Keyword
The INNER JOIN keyword selects records that have matching values in both tables.

![MySQL INNER JOIN](https://www.w3schools.com/mysql/img_inner_join.png)

Syntax:
```
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

Example:
```
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

## Natural Join

The NATURAL JOIN is such a join that performs the same task as an INNER or LEFT JOIN, in which the ON or USING clause refers to all columns that the tables to be joined have in common.

![Natural_Join](https://www.w3resource.com/w3r_images/mysql-natural-join.gif)

Example:
```
SELECT id,aval1,cval1
FROM table111
NATURAL JOIN table113;
```

