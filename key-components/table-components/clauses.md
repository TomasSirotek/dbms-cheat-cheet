******

### AND
#operator 
* The `WHERE` clause can be combined with `AND`, `OR`, and `NOT` operators.
``` sql

SELECT _column1_, _column2, ..._  
FROM _table_name_  
WHERE _condition1_ AND _condition2_ AND _condition3 ..._;
```

---

### OR
#operator 

-   The `OR` operator displays a record if any of the conditions separated by `OR` is TRUE.
``` sql

SELECT _column1_, _column2, ..._  
FROM _table_name_  
WHERE _condition1_ AND _condition2_ AND _condition3 ..._;
```

-----

### NOT
#operator 

* The `NOT` operator displays a record if the condition(s) is NOT TRUE.
``` sql

SELECT _column1_, _column2, ..._  
FROM _table_name_  
WHERE _condition1_ AND _condition2_ AND _condition3 ..._;
```

*****

### SELECT TOP 

The `SELECT TOP` clause is used to specify the number of records to return.

**SQL Server**
``` sql 

SELECT TOP 1000
FROM _table_name  
_WHERE _condition_;
```

**MySQL**
``` sql 

SELECT _column_name(s)_  
FROM _table_name  
_WHERE _condition_  
LIMIT _number_;
```

*****

#NOTFinished 

### Sub-query in the FROM-clause

* Must use a tuple-variable to name tuples of the sub-query
``` sql 

SELECT Fname, Lname 
FROM Employee, (SELECT Essn 
				FROM Works_On WHERE Pno= 10) Project10 #Tuple-variable 
WHERE Employee.SSN = Project10.Essn


```

### Sub-Query in the WHERE-clause

* In place of a relation in the FROM clause, we can use a subquery and then query its result.
* The IN-operator is often used with sub-select in the WHERE-clause
``` sql 

SELECT Fname, Lname 
FROM Employee 
WHERE Employee.SSN IN (SELECT Essn 
					   FROM Works_On 
					   WHERE Pno= 10)
```

### Sub-query returning one tuple 

* If a subquery is guaranteed to produce ONE tuple, then the subquery can be used as a value.
``` sql 

SELECT Fname, Lname 
FROM Employee 
WHERE Dno = ( SELECT Dnumber 
			 FROM Department 
			 WHERE Dname = ‘Research’)
```

### HAVING-clause

* HAVING may follow a GROUP BY clause
``` sql 

SELECT Dname, COUNT(*) AS ‘#Employees’ 
FROM Department 
JOIN Employee ON Dnumber = Dno 
GROUP BY Dname 
HAVING COUNT(*) > 1
```

### ORDER BY-clause

* Ascending or ASC for asceding ordering 
* Descending or DESC for desceding ordering
``` sql 

SELECT SSN, Lname + ‘, ‘ + Fname AS Name, Address, Salary 
FROM Employee 
ORDER BY Salary 
DESC, Lname, Fname
```


### IN-operator
#operator

* The IN operator is used to test for membership of a set.
``` sql 

SELECT DO SOME EXAMPLE

```

### NOT IN-operator
#operator

* Find the names of all employees having no dependents.
``` sql 

SELECT Fname, Lname 
FROM Employee 
WHERE SSN NOT IN (SELECT Essn 
				  FROM Dependent)

```


### EXISTS
#operator

* EXISTS() is true if and only if the subquery result is not empty.
* Often used with correlated sub-queries, where the sub-query uses values from the outermost query.
``` sql 

SELECT Fname, Lname 
FROM Employee AS e
WHERE NOT EXISTS (SELECT * 
				  FROM Dependent AS d 
				  WHERE d.Essn = e.SSN)

```

### ANY/ALL
#operator

* Input text 
``` sql 

SELECT DO EXAMPLES

```

### UNION, INTERSECTION and DIFFERENCE
#NOTFinished 


### SET Semantic vs. BAG Semantic
#NOTFinished 


