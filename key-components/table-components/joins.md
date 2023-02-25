****

#### JOIN 
#checkLater #goDeeper

Selects a tuples that have **matching** values in **both** tables as long as the condition is satisfied 

Returns all values makes tuples NULL

```sql 

SELECT * FROM customers JOIN orders ON customers.customer_id = orders.customer_id;
```

---

#### INNER JOIN

Selects a tuples that have **matching** values in **both** tables as long as the condition is satisfied 

Returns **only** matching values
Any rows where there is no match in either table are **not** included in the result.

```sql 

SELECT * FROM customers INNER JOIN orders ON customers.customer_id = orders.customer_id;
```

---
#### LEFT JOIN 

Return all values from **left** table and the matching values from the right table.
If no matching value, return **NULL**

```sql 

SELECT table1.column1, table1.column2, table2.column1,....  
FROM table1   
LEFT JOIN table2  
ON table1.matching_column = table2.matching_column;
```


```sql 

SELECT EMPLOYEE.EMP_NAME, PROJECT.DEPARTMENT   
FROM EMPLOYEE  
LEFT JOIN PROJECT  
ON PROJECT.EMP_ID = EMPLOYEE.EMP_ID;
```
----

#### RIGHT JOIN 

Return all values from **right** table and the matching values from the left table.
If no matching value, return **NULL**

```sql 

SELECT table1.column1, table1.column2, table2.column1,....  
FROM table1   
RIGHT JOIN table2  
ON table1.matching_column = table2.matching_column;
```


```sql 

SELECT EMPLOYEE.EMP_NAME, PROJECT.DEPARTMENT   
FROM EMPLOYEE  
RIGHT JOIN PROJECT  
ON PROJECT.EMP_ID = EMPLOYEE.EMP_ID;
```
----

#### LEFT OUTER JOIN 
#### RIGHT OUTER JOIN 

- Which way around you put your tables in the join statement doesn’t matter, so Course LEFT OUTER JOIN Lecturer is equivalent to Lecturer RIGHT OUTER JOIN Course. Standard SQL also supports a full outer join, which means that every row from both tables will be represented in the result. Lecturer FULL OUTER JOIN Course will retrieve all the lecturers (even if they don’t examine a course) and all the courses (even if they don’t have an examiner).

----

#### FULL JOIN 

In SQL, FULL JOIN is the result of a combination of **both** **left** and **right** outer join. Join tables have all the records from both tables. It puts NULL on the place of matches not found.

```sql 

SELECT table1.column1, table1.column2, table2.column1,....  
FROM table1   
FULL JOIN table2  
ON table1.matching_column = table2.matching_column;
```

```sql 

SELECT EMPLOYEE.EMP_NAME, PROJECT.DEPARTMENT   
FROM EMPLOYEE  
FULL JOIN PROJECT   
ON PROJECT.EMP_ID = EMPLOYEE.EMP_ID;
```

