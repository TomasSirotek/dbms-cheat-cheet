******

### AND

* The `WHERE` clause can be combined with `AND`, `OR`, and `NOT` operators.
``` sql

SELECT _column1_, _column2, ..._  
FROM _table_name_  
WHERE _condition1_ AND _condition2_ AND _condition3 ..._;
```

### OR

-   The `OR` operator displays a record if any of the conditions separated by `OR` is TRUE.
``` sql

SELECT _column1_, _column2, ..._  
FROM _table_name_  
WHERE _condition1_ AND _condition2_ AND _condition3 ..._;
```

### NOT

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

``` sql 




```

``` sql 




```
