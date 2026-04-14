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
<div align="center"><img width="80%" height="80%" alt="image" src="https://github.com/user-attachments/assets/7396bb84-7911-4e46-83e4-e51844011e1d" /></div>

## Logical Operators (that allow you to combine Comparison Operators in the SQL Syntax)
* **`AND`** (re: Condition 1 has to be TRUE **AND** Condition 2 has to be TRUE)
* **`OR`** (re: Condition 1 is TRUE **OR** Condition 2 is TRUE)
* **`NOT`** (re: means the **opposite** of whatever Condition you're specifying)

## ORDER BY
* **`ORDER BY`** syntax is used to sort rows based on a value in the column either in ascending (ASC) or descending (DESC) order.
* **Example syntax:** **`SELECT`** column1_name, column2_name **`FROM`** table_name **`ORDER BY`** column1_name ASC/DESC
* **`ORDER BY`** is always at the end of the statement since we want to do our selections and sorting first - moving the **`ORDER BY`** statement higher in the syntax will return an error.
* Use **`ASC`** and **`DESC`** to sort in ascending or descending order - if left blank, **`ASC`** is the default.

## LIMIT
* **`LIMIT`** allows you to limit the number of rows returned for a query.
* **`LIMIT`** is useful for not wanting every single row in a table returned, but only the top few rows or so giving you an idea of the layout.
* **`LIMIT`** becomes useful when used in combination with **`ORDER BY`**.

## BETWEEN
* **`BETWEEN`** is used to match/find a value(s) between a range of values.
* **`BETWEEN`** finds values between the lowest and highest values within a range - you set the lowest and highest values to define the range (re: value >= low AND <= high. In other words, a value BETWEEN a low value AND a high value, re: BETWEEN 3 (low value) AND 9 (high value) will return all values greater than and equal to 3 + values less than and equal to 9).
* **`BETWEEN`** is used in conjunction with **`WHERE`**.
* You can also combine **`BETWEEN`** with the NOT logical operator and ask to match/find a value NOT in between a low value and a high value (re: value < low OR value > high; value NOT BETWEEN low AND high; re: value NOT BETWEEN 3 (low value) and 9 (high value) will return all values NOT BETWEEN 3 and 9)).
* **`BETWEEN`** can also be used for dates using YYYY-MM-DD (re: date **`BETWEEN`** '2007-01-01' AND '2007-02-01').
* When using **`BETWEEN`** for dates that also include timestamps, pay attention to how you are using the **`BETWEEN`** operator since the timestamps start at 00:00.
  * For example, if you want dates between '2007-01-01' and '2007-02-01', the **`BETWEEN`** will give you all the dates up to '2027-02-01 00:00 hrs.'. If you wanted the actual timestamps for 2007-02-01, you need to set the **`BETWEEN`** operator for '2007-01-01 and '2007-02-02' so it gives you all the timestamps for 2007-02-01 starting 00:00 through 23:59 hrs.
* Example syntax: **`SELECT`** * **`FROM`** table_name **`WHERE`** column1_name **`BETWEEN`** low value **`AND`** high value;

## IN
* **`IN`** is used for checking multiple possible values in a data table (ex: if a user's name shows up IN a list of known names).
* Example syntax: value **`IN`** (option1, option2,...,option_n)
* **`NOT IN`** can also be used to check for multiple possible values excluded from a data set.

## LIKE and ILIKE
* We can perform direct comparisons against strings, such as: **`WHERE`** first_name = 'John'.
* We can do more than that with **`LIKE`** and **`ILIKE`** operators.
* If we want to match against a general pattern in a string (such as all emails ending with @gmail.com or all names that begin with 'A'), we can use **`LIKE`** and **`ILIKE`**.
* **`LIKE`** allows us to use wildcard characters to perform pattern matching in the data.
* Use % to match any sequence of characters in the string.
* Use _ (underscore) to match any single character.
* Example syntax: **`WHERE`** name **`LIKE`** 'A%' (returns all names that begin with 'A' with any sequence of characters after 'A').
* Example syntax: **`WHERE`** name **`LIKE`** '%a' (returns all names that end with 'a' with any sequence of characters before 'a').
* **NOTE:** **`LIKE`** is case-sensitive, while **`ILIKE`** is not case-sensitive.
* Using the underscore allows you to replace just a single character.
* For example, if we want to check the database to retrieve all Mission Impossible films, our syntax could be something like: **`WHERE`** title **`LIKE`** 'Mission Impossible _'. This provides all film titles staring with "Mission Impossible" and whatever single character that comes after.
* You can also use multiple underscores. So in our previous example, we could also use: **`WHERE`** title **`LIKE`** 'Mission Impossible Version#__', to find all titles with 2 different characters at the end such as "Version 01", "Version 02", etc.
* You can also combine operators for more complex pattern matching using % and _ together (re: WHERE name LIKE '_her%').
