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

### Simple Example for **`CASE`** Expression:
* **`CASE`** expression syntax first evaluates an expression then compares the result with each value in the **`WHEN`** clauses sequentially.
<br><br/>
<div align="center"><img width="70%" height="70%" alt="image" src="https://github.com/user-attachments/assets/8477a931-f64f-4667-80d4-73094c9c0c3f" /></div>
<br><br/>
