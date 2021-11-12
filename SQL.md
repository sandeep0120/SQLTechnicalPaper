# Structured Query Language

### Abstract:- 
SQL (Structured Query Language) is a standardized programming language that's used to manage relational databases and perform various operations on the data in them. Initially created in the 1970s, SQL is regularly used not only by database administrators, but also by developers writing data integration scripts and data analysts looking to set up and run analytical queries. The uses of SQL include modifying database table and index structures; adding, updating and deleting rows of data; and retrieving subsets of information from within a database for transaction processing and analytics applications. Queries and other SQL operations take the form of commands written as statements -- commonly used SQL statements include select, add, insert, update, delete, create, alter and truncate. SQL became the de facto standard programming language for relational databases after they emerged in the late 1970s and early 1980s. Also known as SQL databases, relational systems comprise a set of tables containing data in rows and columns. Each column in a table corresponds to a category of data -- for example, customer name or address -- while each row contains a data value for the intersecting column. 

![Build Status](https://www.databasezone.com/images/SQLServerSimplified.gif)

### Introduction:-

 SQL commands are divided into several different types, among them data manipulation language (DML) and data definition language (DDL) statements, transaction controls and security measures. The DML vocabulary is used to retrieve and manipulate data, while DDL statements are for defining and modifying database structures. The transaction controls help manage transaction processing, ensuring that transactions are either completed or rolled back if errors or problems occur. The security statements are used to control database access as well as to create user roles and permissions. 
SQL syntax is the coding format used in writing statements. ![Build Status](https://cdn.ttgtmedia.com/rms/editorial/sSQLServer_Figure1_082516_desktop.png) 

Above figure shows an example of a DDL statement written in Microsoft's T-SQL to modify a database table in SQL Server 2016:

### Commands:- 

##### Alter Table
 *lets you add columns to a table in a database.*_

```sh
ALTER TABLE table_name 
ADD column_name datatype;
```

##### AND
 _AND is an operator that combines two conditions. Both conditions must be true for the row to be included in the result set._
  ```sh
SELECT column_name(s)
FROM table_name
WHERE column_1 = value_1
AND column_2 = value_2;
```
   
##### AS
_AS is a keyword in SQL that allows you to rename a column or table using an alias._
```sh
SELECT column_name AS 'Alias'
FROM table_name;
```
 
##### AVG()
_AVG() is an aggregate function that returns the average value for a numeric column._
```sh
SELECT AVG(column_name)
FROM table_name;
```

##### BETWEEN
_The BETWEEN operator is used to filter the result set within a certain range. The values can be numbers, text or dates._
```sh
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value_1 AND value_2;
```

##### CASE
_CASE statements are used to create different outputs (usually in the SELECT statement). It is SQL’s way of handling if-then logic._
```sh
SELECT column_name,
CASE
WHEN condition THEN 'Result_1'
WHEN condition THEN 'Result_2'
ELSE 'Result_3'
END
FROM table_name;
```
   

##### COUNT()
_COUNT() is a function that takes the name of a column as an argument and counts the number of rows where the column is not NULL._
```sh
SELECT COUNT(column_name)
FROM table_name;
```

##### CREATE TABLE
_CREATE TABLE creates a new table in the database. It allows you to specify the name of the table and the name of each column in the table._
```sh
CREATE TABLE table_name (
column_1 datatype, 
column_2 datatype, 
column_3 datatype
);
```

##### DELETE
_DELETE statements are used to remove rows from a table._
```sh
DELETE FROM table_name
WHERE some_column = some_value;
```

##### GROUP BY
_GROUP BY is a clause in SQL that is only used with aggregate functions. It is used in collaboration with the SELECT statement to arrange identical data into groups._
```sh
SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name;
```
 
##### INNER JOIN
_An inner join will combine rows from different tables if the join condition is true._
```sh
SELECT column_name(s)
FROM table_1
JOIN table_2
ON table_1.column_name = table_2.column_name;
```

**OUTER JOIN**
_An outer join will combine rows from different tables even if the join condition is not met. Every row in the left table is returned in the result set, and if the join condition is not met, then NULL values are used to fill in the columns from the right table._
```sh
SELECT column_name(s)
FROM table_1
LEFT JOIN table_2
ON table_1.column_name = table_2.column_name;
```


##### INSERT
_INSERT statements are used to add a new row to a table._
```sh
INSERT INTO table_name (column_1, column_2, column_3) 
VALUES (value_1, 'value_2', value_3);
```

##### IS NULL / IS NOT NULL
_IS NULL and IS NOT NULL are operators used with the WHERE clause to test for empty values._
```sh
SELECT column_name(s)
FROM table_name
WHERE column_name IS NULL;
```

##### ORDER BY
_ORDER BY is a clause that indicates you want to sort the result set by a particular column either alphabetically or numerically._
```sh
SELECT column_name
FROM table_name
ORDER BY column_name ASC | DESC;
```

##### UPDATE
_UPDATE statements allow you to edit rows in a table._
```sh
UPDATE table_name
SET some_column = some_value
WHERE some_column = some_value;
```

##### WHERE
_WHERE is a clause that indicates you want to filter the result set to include only rows where the following condition is true._
```sh
SELECT column_name(s)
FROM table_name
WHERE column_name operator value;
```

##### WITH
_WITH clause lets you store the result of a query in a temporary table using an alias. You can also define multiple temporary tables using a comma and with one instance of the WITH keyword.
The WITH clause is also known as common table expression (CTE) and subquery factoring._
```sh
WITH temporary_name AS (
SELECT *
FROM table_name)
SELECT *
FROM temporary_name
WHERE column_name operator value;
```



### Conclusion:- 
The Structured Query Language (SQL) is the main programing language designed to manage data stored in database systems. While SQL was initially used only with relational database management systems (RDBMS), its use has been significantly extended with the advent of new types of database systems. Specifically, SQL has been found to be a powerful query language in highly distributed and scalable systems that process Big Data, i.e., datasets with high volume, velocity and variety. While traditional relational databases represent now only a small fraction of the database systems landscape, most database courses that cover SQL consider only the use of SQL in the context of traditional relational systems.


### References:- 
| Name | source |
| ---------- | ------ |
| Codecademy  | https://www.codecademy.com/articles/sql-commands?r=master
| Research Gate | https://www.researchgate.net/publication/311488672_SQL_From_Traditional_Databases_to_Big_Data
| Tutorials Point| https://www.tutorialspoint.com/sql-programming/index.asp
| DataCamp| https://www.datacamp.com/community/tutorials/sql-tutorial-query
