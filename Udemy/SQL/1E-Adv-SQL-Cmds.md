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
