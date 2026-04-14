# Aggregate Functions
## Group By & Having Operators

## Aggregate Functions
* SQL provides aggregate functions where you can take multiple inputs and return a single output.
* **Common Functions:**
  * **`AVG`** (returns average value)
  * **`COUNT`** (returns total number of values)
  * **`MAX`** (returns maximum value)
  * **`MIN`** (returns minimum value)
  * **`SUM`** (returns the sum of all values)
* Aggregate Functions only happen in the **`SELECT`** clause and **`HAVING`** clause.
* Example syntax: **`SELECT`** **`MIN`**(column1_name) **`FROM`** table_name;
* **`AVG`** returns a floating point value with lots of significant digits, use the ROUND operator to define the number of significant digits you want; example syntax: **`SELECT`** **`ROUND`**(**`AVG`**(column1_name), # of sig figs) **`FROM`** table_name;
* Example syntax: **`SELECT`** **`SUM`**(column1_name) **`FROM`** table_name;
