# Aggregate Functions
## "Group By" & "Having" Operators

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


## GROUP BY
* **`GROUP`** BY allows you to aggregate columns per some category.
* We first choose a categorical column to **`GROUP BY`**.
* Categorical columns are non-continuous (meaning values in the column may not be in order or related and even then, the **`GROUP BY`** function will aggregate them together and return an aggregate value).
* * **`GROUP BY`** allows you to aggregate columns per some category.
* We first choose a categorical column to **`GROUP BY`**.
* Categorical columns are *non-continuous* (meaning values in the column may not be in order or related and even then, the **`GROUP BY`** function will aggregate them together and return an aggregate value).
* Example syntax: **`SELECT`** category_column, *`AGGREGATE FUNCTION`*(data_column) **`FROM`** table_name GROUP BY category_column;
* **`GROUP BY`** must appear right after a **`FROM`** or **`WHERE`** statement (where you can insert a **`WHERE`** statement before the **`GROUP BY`** clause).
* **`WHERE`** statements should not refer to the aggregation results.

### Example of how GROUP BY aggregates the SUM of a Category:
<img width="2628" height="1419" alt="image" src="https://github.com/user-attachments/assets/13bc9d24-063b-4425-8663-967d8221fde6" />

### Example of how GROUP BY aggregates the AVG of a Category:
<img width="2625" height="1396" alt="image" src="https://github.com/user-attachments/assets/a79e6cbf-40eb-4f80-a207-f4fd540485d2" />

### Example of how GROUP BY aggregates the COUNT of a Category:
<img width="2623" height="1411" alt="image" src="https://github.com/user-attachments/assets/09b6d299-082c-4e5b-bae4-698ff55805c4" />

### Matching the SELECT and GROUP BY statements:
#### In the SELECT statement, columns must either have an aggregate function OR both the SELECT column and GROUP BY columns must match:
<img width="2125" height="519" alt="image" src="https://github.com/user-attachments/assets/227cd39c-be78-4fe1-89e2-9457c027ab11" />
<img width="2158" height="490" alt="image" src="https://github.com/user-attachments/assets/627f5b0c-2d90-485e-81e6-f351312f9c03" />

