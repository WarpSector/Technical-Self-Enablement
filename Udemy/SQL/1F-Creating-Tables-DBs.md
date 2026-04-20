# Creating Tables and Databases

## Data Types
* When creating tables using SQL, you must first determine the DATA TYPE.
* These are the COMMON Data Types:
  * Boolean (True/False)
  * Character (char, varchar, and text)
  * Numeric (integer and floating-point number)
  * Temporal (date, time, timestamp, and interval).
* These are some UNCOMMON Data Types:
  * UUID (Universally Unique Identifiers)
  * Array (Stores an array of strings, numbers, etc.)
  * JSON
  * Hstore key-value pair
  * Special types such as network address and geometric data.
* You should carefully consider the data type to use (do a Google search to determine the best practices for storing data and the data types to use).
* Choose data types keeping long term storage in mind (re: cannot add in historical data, so always default to storing as much information as possible to start - you can always delete what you don't need later).
