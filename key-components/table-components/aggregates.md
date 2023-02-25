****

**Aggregation**  is a process of combining **two** or more **entities** to form a more meaningful new entity.

Treated as a **single entity**

*Example table* user

| Id | LastName  | FirstName | Address   | City      | NumOfCars |
| :--------| :-------- | :-------- | :-------- | :-------- | :-------- |
|    1     |  Peterson |  Jordan     |   Empty Street       |   Prague  |  5
	|    2     |  Brave |  Adam     |   Empty Street       |   Viena    |  4
|    3     |  Jake |  Paul     |   Empty Street       |   Brusel        | 1
|    4     |  Charles |  Prince     |   Empty Street       |   London  | 4

----

### SUM

A function to **calculate** the **sum** of all selected tuples 

```sql 

SUM()  
or  
SUM( [ALL|DISTINCT] expression )
```

Using WHERE 

```sql 

SELECT SUM(COST)  
FROM user  
WHERE numOfCars >3;
```

Using HAVING

```sql

SELECT COMPANY, SUM(COST)  
FROM PRODUCT_MAST  
GROUP BY COMPANY  
HAVING SUM(COST)>=170;
```

-----

## AVG

A function to  calculate **avarage** value of all selected tuples of all non-Null values 

```sql 

AVG()  
or  
AVG( [ALL|DISTINCT] expression )
```


```sql 

SELECT AVG(NumOfCars)  
FROM ;

# Output : 3.5
```

-----

### COUNT()

A function used to **count** the number of rows in a database table.
Works for both numeric and non-numeric data types.

```sql 

COUNT(*)
OR
COUNT( [ALL|DISTINCT] expression )
```

Selecting from table 

```sql 

SELECT COUNT(*)
FROM user

# Output : 4
```

Select distinct City from table user

```sql 

SELECT COUNT(DISTINCT City)
FROM user
```

Select  COUNT()  with Having

```sql 

SELECT numOfCars, COUNT(*)  
FROM user  
GROUP BY numOfCars  
HAVING COUNT(*)>2;
```

------

### MIN

A function to  calculate **minimum** value of a certain column.
Determines the largest value of all selectes values of a column

```sql 

MIN()  
or  
MIN( [ALL|DISTINCT] expression )
```


```sql 

SELECT MIN(NumOfCars)  
FROM user;

# Output: 1
```

-----

### MAX 

A function to  calculate **maximum** value of a certain column.
Determines the largest value of all selectes values of a column.


```sql 

MAX()  
or  
MAX( [ALL|DISTINCT] expression )
```


```sql 

SELECT MAX(NumOfCars)  
FROM user;

# Output: 5
```

------

