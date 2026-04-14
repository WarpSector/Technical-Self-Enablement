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
* When running an **`INNER JOIN`** with duplicate columns, you can specify returning just one column by specifying the name of the column in the **`SELECT`** line (For example, if columns A and C both have overlapping data and you don't need both columns displayed in the **`INNER JOIN`**, just specify the name of one column in **`SELECT`** so the result will show only one column).
* If you just use **`JOIN`** without typing "INNER JOIN", PostgreSQL will treat it as an **`INNER JOIN`** by default.

## OUTER JOINS
* **`OUTER JOINS`** allow you to specify how to deal with values only present in one of the tables being joined.
* There are different types of **`OUTER JOINS`**:
  * **`FULL OUTER JOIN`** (the simplest)
  * **`LEFT OUTER JOIN`**
  * **`RIGHT OUTER JOIN`**

### FULL OUTER JOIN
* Example syntax: **`SELECT`** * **`FROM`** Table_A **`FULL OUTER JOIN`** Table_B ON Table_A.col_match = Table_B.col_match; (this basically grabs everything from both tables).
<br><br/>
<img width="1059" height="678" alt="image" src="https://github.com/user-attachments/assets/2199f24a-2a21-4e60-af0b-aa191c30dae5" />
<br><br/>

* Like **`INNER JOINS`**, **`FULL OUTER JOINS`** are symmetrical and the order of the tables don't matter.
* Empty rows in **`FULL OUTER JOINS`** will be populated with **`null`**.
