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
<br><br/>
<div align="center"><img width="60%" height="60%" alt="image" src="https://github.com/user-attachments/assets/b3775b68-2df6-4eaf-bad0-42d6b0bfce58" /></div>
<br><br/>

  
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
<div align="center"><img width="60%" height="60%" alt="image" src="https://github.com/user-attachments/assets/2199f24a-2a21-4e60-af0b-aa191c30dae5" /></div>
<br><br/>

* Like **`INNER JOINS`**, **`FULL OUTER JOINS`** are symmetrical and the order of the tables don't matter.
* Empty rows in **`FULL OUTER JOINS`** will be populated with **`null`**.

### FULL OUTER JOIN with WHERE
* Using **`WHERE`** with **`FULL OUTER JOIN`** leaves out any overlapping data between the tables being joined - you will only see results unique to each table.
<br><br/>
<div align="center"><img width="60%" height="60%" alt="image" src="https://github.com/user-attachments/assets/cf61400f-4210-47f2-a9de-3fac60f549d9" /></div>
<br><br/>

* Essentially, we use the same syntax for **`FULL OUTER JOIN`**: **`SELECT`** * **`FROM`** table_A **`FULL OUTER JOIN`** Table_B ON Table_A.col_match = Table_B.col_match
* Except now we add the **`WHERE`** operator: **`WHERE`** Table_A.id IS null OR Table_B.id IS null
* As usual, this is also symmetrical and the order of tables don't matter.

### LEFT OUTER JOIN
* **`LEFT OUTER JOINS`** results in a set of records that are in the LEFT table.
* If there are no matches with the RIGHT table, the results returned are null.
* The results will return everything in Table A and whatever overlaps in Table B, but will not return anything unique in Table B.
* **`LEFT OUTER JOINS`** are not symmetrical, so the order of the tables matters (the LEFT table will be referred to first).
* Example syntax: **`SELECT`** * **`FROM`** Table_A **`LEFT OUTER JOIN`** Table_B ON Table_A.col_match = Table_B.col_match;
* Can also use **`LEFT JOIN`** instead of **`LEFT OUTER JOIN`**.
<br><br/>
<div align="center"><img width="60%" height="60%" alt="image" src="https://github.com/user-attachments/assets/85117373-9729-4827-9f7a-e8e969e8f819" /></div>
<br><br/>

### LEFT OUTER JOIN with WHERE
* **`LEFT OUTER JOINS`** with **`WHERE`** will return everything in Table A, but nothing overlapping with Table B and nothing in Table B (essentially, it's everything in Table A less the overlapping data with Table B).
<br><br/>
<div align="center"><img width="60%" height="60%" alt="image" src="https://github.com/user-attachments/assets/7b796637-0236-4dbd-b149-e662b68bea6e" /></div>
<br><br/>

* Example syntax: **`SELECT`** * **`FROM`** Table_A **`LEFT OUTER JOIN`** Table_B ON Table_A.col_match = Table_B.col_match **`WHERE`** Table_B.id IS null;

### RIGHT JOINS
* **`RIGHT JOINS`** are basically **`LEFT JOINS`** but flipped in the opposite direction.
* **`RIGHT JOINS`** are the same as switching the table order in a **`LEFT JOIN`**.
<br><br/>
<div align="center"><img width="60%" height="60%" alt="image" src="https://github.com/user-attachments/assets/46f9f6ed-ffd4-47b6-89c6-e15b0a745140" /></div>
<br><br/>







