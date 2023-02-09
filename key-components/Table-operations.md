****
#### Create database 

```sql 
CREATE DATABASE _databasename_;
```

Create statement to create **new database** by name
******
#### Create table 

```sql

CREATE TABLE _table_name_ (  
    _column1 datatype_,  
    _column2 datatype_,  
    _column3 datatype_,  
   ....  
);
```

Create table statement to specify _table_name_ and each **column**  and **datatype**

```sql

CREATE TABLE Persons (  
    PersonID int,  
    LastName varchar(255),  
    FirstName varchar(255),  
    Address varchar(255),  
    City varchar(255)  
);
```

- caps does not matter 
- make it easily readable and clean naming  (depends also on comapny policies)
- datatype differes depending on #Dialects
- in datatype depending on type specifing attributes 

| PersonId | LastName  | FirstName | Address   | City      | 
| :--------| :-------- | :-------- | :-------- | :-------- |
|    1     |  Peterson |  Adam     |           |           | 

#### Copy table 

The new table gets the same column definitions. All columns or specific columns can be selected.

```sql 

CREATE TABLE _new_table_name_ AS  
    SELECT _column1, column2,..._  
    FROM _existing_table_name_  
    WHERE ....;
```

Inputs **new_table_name** and lets select columns from **existing_table_name** and creates copy example use below

```sql 

CREATE TABLE copyCustomers AS  
SELECT customername, contactname  
FROM customers;
```

#### Back up database 

```sql

BACKUP DATABASE _databasename_  
TO DISK = '_filepath_';
```

Backs up database to disk 

```sql

BACKUP DATABASE _databasename_  
TO DISK = '_filepath_'  
WITH DIFFERENTIAL
```

Backs up only difference from last backup

#### Alter Data 

Add "Email" column to the "Customers" table

```sql

ALTER TABLE _table_name_  
ADD _column_name datatype_;
```

```sql

ALTER TABLE Customers  
ADD Email varchar(255);

```

Drop column 

```sql

ALTER TABLE _table_name_  
DROP COLUMN _column_name_;
```

Rename column 

```sql

ALTER TABLE _table_name_  
RENAME COLUMN _old_name_ to _new_name_;

```

Alter/modify datatype

```sql

ALTER TABLE _table_name_  
ALTER COLUMN _column_name datatype_;

```


##### Drop / Truncate 

```sql 

DROP DATABASE _databasename_;
```

Deletes table with content inside

```sql

TRUNCATE TABLE _table_name_;
```

Delete only data **inside** a table but not the table itself



