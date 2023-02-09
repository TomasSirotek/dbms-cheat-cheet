****


##### DO MORE EXAMPLES FROM THAT WEEK

```sql

SELECT *
FROM employee
WHERE Dno = (SELECT Dnumber FROM department WHERE Dname = 'Administration');
```
