# MySQL Notes

## Table of Contents
- [Installation](#installation)
- [Connecting to MySQL](#connecting-to-mysql)
- [Connecting MySQL with Python](#connecting-mysql-with-python)
- [Connecting MySQL with Workbench](#connecting-mysql-with-workbench)
- [Creating a Database](#creating-a-database)
- [Creating Tables](#creating-tables)
- [Inserting Data](#inserting-data)
- [Querying Data](#querying-data)
- [Updating Data](#updating-data)
- [Deleting Data](#deleting-data)
- [SQL Commands](#sql-commands)

## Installation
To install MySQL, follow these steps:
1. Download the MySQL installer from the official website.
2. Run the installer and follow the on-screen instructions.
3. Choose the desired installation options and complete the installation process.
## Connecting to MySQL

### Connecting MySQL with Python

To connect MySQL with Python, you can use the `mysql.connector` library. Follow these steps:

- Import the required libraries:
    ```python
    import mysql.connector
    ```

- Establish a connection:
    ```python
    connection = mysql.connector.connect(
        host="localhost",
        port=3306,
        user="your_username",
        password="your_password",
        database="your_database"
    )
    ```
    

- Create a cursor object:
    ```python
    cursor = connection.cursor()
    ```
    

- Execute SQL queries:
    ```python
    cursor.execute("SELECT * FROM your_table")
    result = cursor.fetchall()
    ```
    

- Process the retrieved data:
    ```python
    for row in result:
        print(row)
    ```
    

- Close the cursor and connection:
    ```python
    cursor.close()
    connection.close()
    ```
    


### Connecting MySQL with Workbench

To connect to MySQL with Workbench, use the following command:


This code demonstrates the process of connecting MySQL with Workbench and retrieving data.

Steps to connect MySQL with Workbench:
1. Install MySQL and Workbench on your machine.
2. Launch Workbench and click on the '+' icon to create a new connection.
3. Enter the connection details such as hostname, port, username, and password.
4. Click on 'Test Connection' to verify the connection.
5. Once the connection is successful, you can execute SQL queries to retrieve data from the MySQL database.

## Creating a Database

To create a database in MySQL Workbench, follow these steps:
1. Open MySQL Workbench and connect to your MySQL server.
2. Click on the "Database" menu and select "Create Schema".
3. Enter a name for the database and click "Apply" to create it.
```mysql
CREATE DATABASE your_database_name;
```

## Creating Tables

To create tables in a database using MySQL Workbench, follow these steps:
1. Open MySQL Workbench and connect to your MySQL server.
2. Double-click on the database where you want to create the table.
3. Click on the "Table" menu and select "Create Table".
4. Enter the table name and define the columns, their data types, and any constraints.
5. Click "Apply" to create the table.

```mysql
CREATE TABLE your_table_name (
    column1 datatype1,
    column2 datatype2,
    column3 datatype3,
    ...
);
```

## Inserting Data

To insert data into a table using MySQL Workbench, follow these steps:
1. Open MySQL Workbench and connect to your MySQL server.
2. Double-click on the database containing the table.
3. Double-click on the table where you want to insert data.
4. Click on the "Insert" tab and enter the values for each column.
5. Click "Apply" to insert the data into the table.

```mysql
INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...);
```

## Querying Data

To query data from a table using MySQL Workbench, follow these steps:
1. Open MySQL Workbench and connect to your MySQL server.
2. Double-click on the database containing the table.
3. Double-click on the table from which you want to query data.
4. Click on the "Query" tab and write your SQL query to retrieve the desired data.
5. Click "Execute" to run the query and view the results.

```mysql
SELECT column1, column2, column3
FROM table_name
WHERE condition;
```

## Updating Data

To update data in a table using MySQL Workbench, follow these steps:
1. Open MySQL Workbench and connect to your MySQL server.
2. Double-click on the database containing the table.
3. Double-click on the table where you want to update data.
4. Click on the "Query" tab and write your SQL update statement to modify the data.
5. Click "Apply" to execute the update statement and update the data in the table.

```mysql
UPDATE table_name
SET column1 = new_value1, column2 = new_value2, ...
WHERE condition;
```

## Deleting Data

To delete data from a table using MySQL Workbench, follow these steps:
1. Open MySQL Workbench and connect to your MySQL server.
2. Double-click on the database containing the table.
3. Double-click on the table from which you want to delete data.
4. Click on the "Query" tab and write your SQL delete statement to remove the data.
5. Click "Apply" to execute the delete statement and delete the data from the table.

```mysql
DELETE FROM table_name
WHERE condition;
```
## SQL Commands
![Commands](https://media.geeksforgeeks.org/wp-content/uploads/20210920153429/new.png)
- [DDL (Data Definition Language)](#ddl-data-definition-language)
- [DQL (Data Query Language)](#dql-data-query-language)
- [DML(Data Manipulation Language)](#dmldata-manipulation-language)
- [DCL (Data Control Language)](#dcl-data-control-language)
- [TCL (Transaction Control Language)](#tcl-transaction-control-language)

### DDL (Data Definition Language)
----------------------------------
DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema. It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database. DDL is a set of SQL commands used to create, modify, and delete database structures but not data. These commands are normally not used by a general user, who should be accessing the database via an application.

List of DDL commands: 

1. [CREATE](https://www.geeksforgeeks.org/sql-create-table/): This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. [DROP](https://www.geeksforgeeks.org/sql-drop-truncate/): This command is used to delete objects from the database.
3. [ALTER](https://www.geeksforgeeks.org/sql-alter-add-drop-modify/): This is used to alter the structure of the database.
4. [TRUNCATE](https://www.geeksforgeeks.org/sql-drop-truncate/): This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. [COMMENT](https://www.geeksforgeeks.org/sql-comments/): This is used to add comments to the data dictionary.
6. [RENAME](https://www.geeksforgeeks.org/sql-alter-rename/): This is used to rename an object existing in the database.

### DQL (Data Query Language)
----------------------------------
DQL statements are used for performing queries on the data within schema objects.

List of DQL commands: 
* [SELECT](https://www.geeksforgeeks.org/sql-select-query/): It is used to retrieve data from the database.

### DML(Data Manipulation Language)
----------------------------------
The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

List of DML commands: 

1. [INSERT](https://www.geeksforgeeks.org/sql-insert-statement/): It is used to insert data into a table.
2. [UPDATE](https://www.geeksforgeeks.org/sql-update-statement/): It is used to update existing data within a table.
3. [DELETE](https://www.geeksforgeeks.org/sql-delete-statement/): It is used to delete records from a database table.
4. [LOCK](https://www.geeksforgeeks.org/sql-lock-table/): Table control concurrency.
5. [CALL](): Call a PL/SQL or JAVA subprogram.
6. [EXPLAIN PLAN](): It describes the access path to data.

### DCL (Data Control Language)
----------------------------------
DCL includes commands such as GRANT and REVOKE which mainly deal with the rights, permissions, and other controls of the database system. 

List of  DCL commands: 

1. GRANT: This command gives users access privileges to the database.

    Syntax:
    ```
    GRANT SELECT, UPDATE ON MY_TABLE TO SOME_USER, ANOTHER_USER;
    ```

2. REVOKE: This command withdraws the user’s access privileges given by using the GRANT command.

    Syntax:
    ```mysql
    REVOKE SELECT, UPDATE ON MY_TABLE FROM USER1, USER2;  
    ```

### TCL (Transaction Control Language)
----------------------------------
Transactions group a set of tasks into a single execution unit. Each transaction begins with a specific task and ends when all the tasks in the group are successfully completed. If any of the tasks fail, the transaction fails. Therefore, a transaction has only two results: success or failure. You can explore more about transactions here. Hence, the following TCL commands are used to control the execution of a transaction: 

BEGIN: Opens a Transaction.

1. COMMIT: Commits a Transaction.

    Syntax:
    ```
    COMMIT;  
    ```

2. ROLLBACK: Rollbacks a transaction in case of any error occurs.

    Syntax:
    ```
    ROLLBACK; 
    ```
 

3. SAVEPOINT: Sets a save point within a transaction.

    Syntax:
    ```
    SAVEPOINT SAVEPOINT_NAME; 
    ```
 