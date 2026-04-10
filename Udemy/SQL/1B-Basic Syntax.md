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
* **Example syntax:** **`SELECT`** **`DISTINCT`** column_name, **`FROM`** table_name;
* You may also need to add parenthesis for clarity when conducting complex queries - example: **`SELECT`** **`DISTINCT`** (column_name), **`FROM`** (table_name);
