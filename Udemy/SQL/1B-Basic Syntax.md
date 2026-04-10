# Basic SQL Syntax 

## SELECT
* **`SELECT`** is the most common statement used.
* **`SELECT`** retrieves information from a table.
* **`SELECT`** is used with other SQL statements to perform complex queries.
* **Example syntax:** **`SELECT`** column_name **`FROM`** table_name;
* You **`SELECT`** the specific data you want FROM a specific table in the DB.
* Use **`*`** (SELECT * FROM table_name;) to retreive everything from the table.
* The **`;`** ends the statement.
* Capitalization of the syntax is necessary for complex queries.

## DISTINCT
* **`DISTINCT`** is a statement that retrieves unique and distinct values (if you have a table that contains duplicate values, you may need to use this statement to find the unique value).
* **`DISTINCT`** retrieves only the distinct values in the column.
* **`DISTINCT`** operates only on columns, not rows.
* **Example syntax:** **`SELECT`** **`DISTINCT`** column_name **`FROM`** table_name;
* You may also need to add parenthesis for clarity when conducting complex queries - example: **`SELECT`** **`DISTINCT`** (column_name) **`FROM`** (table_name);

## COUNT
* **`COUNT`** returns the number of input rows when matched to a specific query.
* **`COUNT`** can be applied on a specific column, or you can use * - either way, this will return the same result.
* **Example syntax:** **`SELECT`** **`COUNT`**(column_name), **`FROM`** table_name;
* **Example syntax:** **`SELECT`** **`COUNT`**(choice) **`FROM`** table_name;
* **Example syntax:** **`SELECT`** **`COUNT`**(*) **`FROM`** table_name;

## SELECT WHERE
* **`WHERE`** statements allows you to specify conditions on columns and for the rows that are returned.
* Along with **`SELECT`**, **`WHERE`** statements are the most fundamental SQL syntax statements you will use.
* **Example syntax:** **`SELECT`** column1_name, column2_name **`FROM`** table_name **`WHERE`** (whatever conditions you apply);
* The **`WHERE`** statement appears immediately after the **`FROM`** statement.
* Conditions are used to filter the rows retrieved by the **`SELECT`** statement (re: you **`SELECT`** the target column or columns **`FROM`** a specified table **`WHERE`** you apply the conditions you want - these conditions act on the rows).

## Common Comparison Operators used in SQL Syntax
<img width="1783" height="1006" alt="image" src="https://github.com/user-attachments/assets/7396bb84-7911-4e46-83e4-e51844011e1d" />

## Logical Operators (that allow you to combine Comparison Operators in the SQL Syntax)
* **`AND`** (re: Condition 1 has to be TRUE **AND** Condition 2 has to be TRUE)
* **`OR`** (re: Condition 1 is TRUE **OR** Condition 2 is TRUE)
* **`NOT`** (re: means the **opposite** of whatever Condition you're specifying)

## ORDER BY
* **`ORDER BY`** syntax is used to sort rows based on a value in the column either in ascending (ASC) or descending (DESC) order.
* **Example syntax:** **`SELECT`** column1_name, column2_name **`FROM`** table_name **`ORDER BY`** column1_name ASC/DESC
* **`ORDER BY`** is always at the end of the statement since we want to do our selections and sorting first - moving the **`ORDER BY`** statement higher in the syntax will return an error.
