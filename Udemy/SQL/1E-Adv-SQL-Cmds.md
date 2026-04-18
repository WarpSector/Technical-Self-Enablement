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
