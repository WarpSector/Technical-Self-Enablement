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

## INNER JOIN
* **`JOINS`** allow the ability to combine multiple tables together.
* The main reason for different **`JOIN`** types is to decide how you want to handle the information present in one of the joined tables.
* **`INNER JOINS`** are the simplest JOIN functions to orchestrate.
* An **`INNER JOIN`** will result with a set of records that match in different tables.
* Example syntax: **`SELECT`** * **`FROM`** Table_A **`INNER JOIN`** Table_B ON Table_A.col_match = Table_B.col_match; (This basically says "grab Table A and Table B and only show the overlapping results between both tables").
* Switching the order of tables on an **`INNER JOIN`** will produce the same result, so the order of the tables does not matter.
