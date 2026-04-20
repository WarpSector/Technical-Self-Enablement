# Creating Tables and Databases

## Data Types
* When creating tables using SQL, you must first determine the DATA TYPE.
* These are the **COMMON** Data Types:
  * Boolean (True/False)
  * Character (char, varchar, and text)
  * Numeric (integer and floating-point number)
  * Temporal (date, time, timestamp, and interval).
* These are some **UNCOMMON** Data Types:
  * UUID (Universally Unique Identifiers)
  * Array (Stores an array of strings, numbers, etc.)
  * JSON
  * Hstore key-value pair
  * Special types such as network address and geometric data.
* You should carefully consider the data type to use (do a Google search to determine the best practices for storing data and the data types to use).
* Choose data types keeping long term storage in mind (re: cannot add in historical data, so always default to storing as much information as possible to start - you can always delete what you don't need later).

## Primary and Foreign Keys

### Primary Keys
* A Primary Key is a column or group of columns used to identify a row uniquely in a table.
* Primary Keys are important for easily discerning which columns should be used for joining tables together.
* Primary Keys are identified in tables with the `[PK]` designation and they are non-null (meaning every row under this column has an entry in it).
* Primary Keys are also integer-based and unique.

### Foreign Keys
* A Foreign Key is a field or group of fields in a table that uniquely identifies a row in another table.
* Foreign Keys are defined in a table that references to the Primary Key of the other table.
* The table with the Foreign Key(s) is called: "`Referencing Table`" or "`Child Table`".
* The table which the Foreign Key references is called: "`Referenced Table`" or "`Parent Table`".
* A (referencing/child) table can have multiple foreign keys depending on its relationships with other tables.
* Foreign Keys are not identified like Primary Keys are. A column in a table that's not identified as `[PK]` is a Foreign Key in the table, however, that column could be a `[PK]` in a different table.
* Foreign Keys can be ID'ed in pgAdmin by clicking the table >> constraints >> and seeing which keys are marked as "fkey".
