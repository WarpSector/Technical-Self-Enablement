# Conditional Expressions and Procedures

## CASE
* **`CASE`** statements can be implemented to only execute SQL code when certain conditions are met.
* The way **`CASE`** statements work is similar to IF/ELSE statements in other programming languages.
* Two main ways to use a **`CASE`** statement:
    * General **`CASE`** statement
    * **`CASE`** expression
* General Syntax: **`CASE`** **`WHEN`** condition1 **`THEN`** result1 **`WHEN`** condition2 **`THEN`** result2 **`ELSE`** some_other_result **`END`**

### Simple Example for **`CASE`** Statement:
<br><br/>
<div align="center"><img width="70%" height="70%" alt="image" src="https://github.com/user-attachments/assets/7153e973-73d1-4e12-8356-bd44c58dbd94" /></div>
<br><br/>
<br><br/>
<div align="center"><img width="70%" height="70%" alt="image" src="https://github.com/user-attachments/assets/3f9d2126-9754-4a4f-a19a-4cbde42a1b3c" /></div>
<br><br/>

### Simple Example for **`CASE`** Expression:
* **`CASE`** expression syntax first evaluates an expression then compares the result with each value in the **`WHEN`** clauses sequentially.
<br><br/>
<div align="center"><img width="70%" height="70%" alt="image" src="https://github.com/user-attachments/assets/8477a931-f64f-4667-80d4-73094c9c0c3f" /></div>
<br><br/>
<br><br/>
<div align="center"><img width="70%" height="70%" alt="image" src="https://github.com/user-attachments/assets/961c8d25-c8ac-4336-b5e1-38a816c33d43" /></div>
<br><br/>

## COALESCE
* **`COALESCE`** accepts an unlimited number of arguments and returns the first argument that is NOT null.
* If all arguments are null, then the **`COALESCE`** function returns null.
* Example syntax: **`SELECT COALESCE`** (1,2) returns 1 as the first NOT null argument.
* Example syntax: **`SELECT COALESCE`** (NULL, 2,3) returns 2 as the first NOT null argument.
* **`COALESCE`** becomes useful when querying a table that contains null values and you want to replace the null value with another value.

## CAST
* **`CAST`** lets you convert from one data type into another.
* Not every instance of a data type can be CAST to another data type - it has to be reasonable. For example, '5' to an integer will work while 'five' to an integer will not.

### CAST Function Calls
<br><br/>
<div align="center"><img width="70%" height="70%" alt="image" src="https://github.com/user-attachments/assets/b715f5eb-fea9-4a16-9647-e284a2740ea9" /></div>
<br><br/>

## NULLIF
* **`NULLIF`** takes 2 inputs and returns NULL if both inputs are equal.
* If both inputs are not equal, it returns the first argument passed.
* Example syntax: **`NULLIF`** (10,10) - this returns NULL.
* This function is useful in cases where a NULL value would cause an error or unwanted result.
