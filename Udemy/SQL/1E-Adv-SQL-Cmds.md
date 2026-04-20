# Advanced SQL Commands

## Timestamps and Extracts
* Timestamps and Extracts are useful when creating your own tables and DBs.
* PostgreSQL can hold date and time information:
  * **`TIME`** (contains only time HH:MM:SS)
  * **`DATE`** (contains only date MM-DD-YYYY)
  * **`TIMESTAMP`** (contains both time and date)
  * **`TIMESTAMPTZ`** (contains date, time, and timezone).

* Careful considerations need to be made when designing a table and DB and choosing a time data type - remember you can remove historical data, but you cannot add it if you realize later you need additional information.
* Functions and Operations:
  * **`TIMEZONE`**
  * **`NOW`**
  * **`TIMEOFDAY`**
  * **`CURRENT_TIME`**
  * **`CURRENT_DATE`**
* Use the **`SHOW`** command to run the **`TIMEZONE`** function and operation.
* Example syntax:
  * **`SELECT NOW()`** to retrieve your current timestamp.
  * **`SELECT TIMEOFDAY()`** to retrieve your current timestamp as a string.
  * **`SELECT CURRENT_TIME`** to retrieve your current time with time zone.
  * **`SELECT CURRENT_DATE`** to retrieve your current date.   

### Commands
* Commands to extract time information from time based data types:
  * **`EXTRACT ()`**
  * **`AGE ()`**
  * **`TO_CHAR ()`** (formats time information).

* **`EXTRACT ()`** allows you to extract a sub-component of the date value:
  * YEAR
  * MONTH
  * DAY
  * WEEK
  * QUARTER

* Example syntax: **`EXTRACT`**(**`YEAR FROM`** date_column)
* **`AGE ()`** calculates and returns the current age given a timestamp.
* Example syntax: **`AGE`**(date_column) (returns 13 years 1 mon 5 days 01:34:!3.003423)
* **`TO_CHAR()`** is a general function used to convert data types into text, which can be useful for timestamp formatting.
* Usage: **`TO_CHAR`**(date_column, 'mm-dd-yyy').

## Mathematical Functions and Operators
* Mathematical Operators example syntax: **`SELECT`** column_A (mathematical operator) column_B **`FROM`** table
* You would type out the equation based on how the mathematical operator is listed in the documentation.
* Reference the documentation for these: https://www.postgresql.org/docs/current/functions-math.html

## String Functions and Operators
* String Concatenation example syntax: **`SELECT`** column_A | | column_B **`FROM`** table
* Use || '  ' || to add spaces in between the concatenated strings. 
* Reference the documentation for these: https://www.postgresql.org/docs/current/functions-string.html

## Sub Queries
* A sub query allows you to construct complex queries where you can perform a query on the results of another query.
* Example Scenario: How can we get a list of students who scored better than the average grade?
* We would normally do this in 2 steps: **`SELECT`** **`AVG`**(grade) **`FROM`** test_scores (then write that result down somewhere and then run another query).
* Instead of doing it in 2 steps, we can use sub queries: **`SELECT`** student, grade **`FROM`** test_scores **`WHERE`** grade > (**`SELECT`** **`AVG`**(grade) **`FROM`** test_scores)
* The query inside the parenthesis is run first and then the rest of the query is run. That way, the avergae grade is first found and then the query will use that result to run the query to find the students above the average grade.
* We can also use the **`IN`** operator in conjunction with a sub query to check against multiple results returned. In other words, if your sub query is going to return more than 1 value, you'll need to pair it with an **`IN`** operator.

### EXISTS
* The **`EXISTS`** operator tests for the existence of rows in a sub query.
* A sub query is passed in the **`EXISTS()`** function to check if any rows are returned with the sub query.
* Typical syntax: **`SELECT`** column_name **`FROM`** table_name **`WHERE`** **`EXISTS`** (**`SELECT`** column_A **`FROM`** table **`WHERE`** condition);
