## KombyteCompetition
Welcome to the Kombyte Competition! This README provides syntax documentation to assist participants in completing the competition questions.

### Basic SQL Query

Participants in this qualification level would be tasked with executing fundamental SQL queries on the dataset. This could include:

1. **Data Retrieval Tasks**: SELECT statement
2. **Data Filtering and Sorting**: WHERE clause, ORDER BY clause
3. **Aggregate Functions**: SUM(), AVG(), COUNT(), etc.
4. **Subqueries and Derived Tables**: Subqueries, Common Table Expressions (CTEs)

### Advanced SQL Query

Participants in this qualification level would be required to execute more complex SQL queries involving joins, advanced functions, triggers, and stored procedures. Tasks could include:

1. **Data Manipulation and Join Operations**: JOIN operations (INNER JOIN, LEFT JOIN, etc.)
2. **User Defined Functions**: CREATE FUNCTION statement
3. **Trigger**: CREATE TRIGGER statement
4. **Stored Procedure**: CREATE PROCEDURE statement

### Overall Competition Structure

1. Participants would be given a fixed amount of time to complete each qualification level.
2. Each qualification level could consist of multiple tasks, and participants would earn points based on the correctness and efficiency of their queries.
3. The competition could be conducted online, with participants submitting their SQL queries through a platform that evaluates and scores their submissions automatically.
4. The participant with the highest total score across both qualification levels would be declared the winner of the competition

## SQL Quick References

### Query modifiers or Clauses

1. **SELECT**: Specifies the columns to be retrieved from the database.
2. **FROM**: Specifies the table(s) from which to retrieve data.
3. **WHERE**: Filters the rows based on specified conditions.
4. **GROUP BY**: Groups the rows that have the same values into summary rows.
5. **HAVING**: Filters groups of rows returned by the GROUP BY clause.
6. **ORDER BY**: Sorts the result set by specified column(s) in ascending or descending order.
7. **LIMIT**: Limits the number of rows returned by the query.
8. **OFFSET**: Specifies the number of rows to skip before starting to return rows.
9. **JOIN**: Combines rows from two or more tables based on a related column between them.
10. **INNER JOIN**: Returns only the rows that have matching values in both tables.
11. **LEFT JOIN (or LEFT OUTER JOIN)**: Returns all rows from the left table, and the matched rows from the right table.
12. **RIGHT JOIN (or RIGHT OUTER JOIN)**: Returns all rows from the right table, and the matched rows from the left table.
13. **FULL JOIN (or FULL OUTER JOIN)**: Returns all rows when there is a match in either left or right table.
14. **UNION**: Combines the result sets of two or more SELECT statements.
15. **UNION ALL**: Similar to UNION but retains all rows, including duplicates.
16. **DISTINCT**: Removes duplicate rows from the result set.
17. **AS**: Renames a column or table with an alias.
18. **CASE**: Specifies conditional logic within the query.
19. **ORDER BY**: Sorts the result set by specified column(s) in ascending or descending order.
20. **FETCH**: Retrieves rows from a cursor.
21. **FOR**: Specifies locking behavior for rows retrieved by the query.

### SELECT Syntax

```sql
SELECT column1, column2, ...
FROM table_name;
```

### COUNT() Syntax

```sql
SELECT COUNT(column_name)
FROM table_name;
```

### WHERE Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

### AND Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2;
```

### OR Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2;
```

### ORDER BY Syntax

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

### INSERT INTO Syntax

```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

### UPDATE Syntax

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

### DELETE Syntax

```sql
DELETE FROM table_name
WHERE condition;
```

### CREATE DATABASE Syntax

```sql
CREATE DATABASE database_name;
```

### DROP DATABASE Syntax

```sql
DROP DATABASE database_name;
```

### CREATE TABLE Syntax

```sql
CREATE TABLE table_name (
column1 datatype,
column2 datatype,
column3 datatype,
...
);
```

### DROP TABLE Syntax

```sql
DROP TABLE table_name;
```

### ALTER TABLE Syntax

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

### CREATE INDEX Syntax

```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

### DROP INDEX Syntax

```sql
DROP INDEX table_name.index_name;
```

### CREATE View Syntax

```sql
CREATE [ OR ALTER ] VIEW [ schema_name . ] view_name [ (column [ ,...n ] ) ]
[ WITH <view_attribute> [ ,...n ] ]
AS select_statement
[ WITH CHECK OPTION ]
[ ; ]  
  
<view_attribute> ::=
{  
    [ ENCRYPTION ]  
    [ SCHEMABINDING ]  
    [ VIEW_METADATA ]
}
```

### IF-ELSE Syntax

```sql
IF Boolean_expression   
     { sql_statement | statement_block }   
ELSE   
     { sql_statement | statement_block }
```

### TRY-CATCH Syntax

```sql
BEGIN TRY  
     { sql_statement | statement_block }  
END TRY  
BEGIN CATCH  
     { sql_statement | statement_block }
END CATCH;
```

### CASE Syntax

```sql
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    ...
    ELSE result
END;
```

### WHILE Syntax

```sql
WHILE Boolean_expression   
     { sql_statement | statement_block | BREAK | CONTINUE }
```

### GROUP BY Syntax

```sql
SELECT column1, COUNT(column2)
FROM table_name
GROUP BY column1;
```

### HAVING Syntax

```sql
SELECT column1, COUNT(column2)
FROM table_name
GROUP BY column1
HAVING COUNT(column2) > value;
```

### BETWEEN Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column1 BETWEEN value1 AND value2;
```

### IN Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column1 IN (value1, value2, ...);
```

### LIKE Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column1 LIKE pattern;
```

### Data Retrieval Tasks

To retrieve data from a table, use the SELECT statement:

```sql
SELECT column1, column2, ...
FROM table_name;
```

### Data Filtering and Sorting

To filter and sort data, use the WHERE and ORDER BY clauses:

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition
ORDER BY column_name;
```

### Aggregate Functions

To perform aggregate functions such as SUM, AVG, COUNT, MAX, and MIN, use the respective functions:

```sql
SELECT SUM(column_name) AS sum_column
FROM table_name;
```

### Subqueries and Derived Tables

To use subqueries or derived tables, embed a SELECT statement within another SELECT statement:

```sql
SELECT column1, column2, ...
FROM (SELECT column1, column2 FROM table_name) AS derived_table;
```

### Data Manipulation and Join Operations

To manipulate data and perform join operations, use UPDATE, INSERT INTO, DELETE, and JOIN statements:

```sql
UPDATE table_name
SET column1 = value1
WHERE condition;

INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);

DELETE FROM table_name
WHERE condition;

SELECT t1.column1, t2.column2
FROM table1 t1
JOIN table2 t2 ON t1.common_column = t2.common_column;
```

### INNER JOIN Syntax

```sql
SELECT columns
FROM table1
INNER JOIN table2 ON table1.column = table2.column;
```

### LEFT JOIN Syntax

```sql
SELECT columns
FROM table1
LEFT JOIN table2 ON table1.column = table2.column;
```

### RIGHT JOIN Syntax

```sql
SELECT columns
FROM table1
RIGHT JOIN table2 ON table1.column = table2.column;
```

FULL OUTER JOIN Syntax

```sql
SELECT columns
FROM table1
FULL OUTER JOIN table2 ON table1.column = table2.column;
```

### User Defined Functions

To create user-defined functions, use the CREATE FUNCTION statement:

```sql
CREATE FUNCTION function_name (parameters)
RETURNS return_datatype
AS
BEGIN
    -- Function logic here
END;
```

### Trigger

To create triggers, use the CREATE TRIGGER statement:

```sql
CREATE TRIGGER trigger_name
AFTER INSERT ON table_name
FOR EACH ROW
BEGIN
    -- Trigger logic here
END;
```

### Stored Procedure
To create stored procedures, use the CREATE PROCEDURE statement:

```sql
CREATE PROCEDURE procedure_name (parameters)
AS
BEGIN
    -- Procedure logic here
END;
```
