#Basic-statements

Example table **user**

| Id | LastName  | FirstName | Address   | City      | 
| :--------| :-------- | :-------- | :-------- | :-------- |
|    1     |  Peterson |  Adam     |   Empty Street       |   Prague        | 

******
#### SELECT 
More about select
#clauses 
*  [Clauses](table-components/clauses)
*  [Joins](table-components/joins)

Basic select statements to select **Id** and **FirstName** from table **user**

```sql

SELECT Id, FirstName  
FROM user;
```

Asterix symbol lets you select all columns from table **user**

```sql

SELECT * FROM user;
```

More examples in practice 
#classExamples  
 - [ClassExamplesWeek5](classExamples/week-5)
 - [ClassExamplesWeek6](classExamples/week-6)

#### SELECT DISTINCT
Return only disctinct (different) values.

```sql 

SELECT DISTINCT Id, City,   
FROM user;
```

****
#### INSERT
Multiple selective columns insert

```sql

INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)  
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');
```

Insert name 'Hamilton' into table **user** field **FirstName**

```sql

INSERT INTO user(FirstName) VALUES ('Hamilton')
```


****
#### UPDATE
Basic update statements 

```sql

UPDATE user  
SET FirstName = 'Cardinal', City= 'Frankfurt'  
WHERE id = @id;

```


***
#### DELETE
Deletes user where id  from table **user**

```sql
DELETE FROM user
WHERE id = @id;
```
