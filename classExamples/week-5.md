***

### SELECT 

Assignments examples 

1. Read a list of all employees working in the ‘Administration’ department.

```sql

SELECT *
FROM employee
WHERE Dno = (SELECT Dnumber FROM department WHERE Dname = 'Administration');
```


2. Read a list of ssn, fname, lname and salary for all employee.

```sql

SELECT ssn,fname,lname,salary  
FROM employee
```
