# Joins

## Overview
* **`JOINS`** allow combining information from multiple tables.
* Different kind of **`JOINS`** include:
  * **`INNER JOINS`**
  * **`OUTER JOINS`**
  * **`FULL JOINS`**
  * **`UNIONS`**

## AS
* The **`AS`** statement allows you to create an "alias" for a column or a result.
* Example syntax: **`SELECT`** column **`AS`** new_name **`FROM`** table;
* Example syntax: **`SELECT`** **`SUM`**(column) **`AS`** new_name **`FROM`** table;
* **`AS`** statements are helpful for enhancing the readability of a column.
* The **`AS`** operator only executes at the end of a query, so it cannot be used inside of a **`WHERE`** operator or HAVING clause.
* AS operators are useful when using **`JOINS`** so you can rename columns in the output.
