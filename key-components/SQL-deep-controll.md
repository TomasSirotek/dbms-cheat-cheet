*****

##### Important !

- All **DDL** statements are commited **automatically** at end of the statement excution 
- Explicit COMMIT or ROLLDBACK is not needed for DDL

* All changes done by **DML's** need explicitly commit or rollback to make changes permament or to revert back 

#### What is DDL 
( Data Definition Language )

* Language to **manage** of the **objects** in the RDMS 
* Used for **defining** and **managing** db structure like
	* table,viewsequence,users
 
 Common commands 
 
```sql
 * CREATE 
 * ALTER
 * DROP
 * TRUNCATE

 More exapmples 
 * CREATE SEQUENCE 
 * ALTER SEQUENCE 
 * CREATE PROCEDURE 
 * CREATE FUNCTION
```

* [Table-operation](Pattern-matching.md)

#### What is DML
( Data Manipulation Language )

* Language to **manage** of the **data** that is stored in the RDMS 

```sql
 Common commands 
 * INSERT
 * UPDATE
 * DELETE
 * MERGE
```

* [Basic-statements](Basic-statements.md)
 
#### What is DCL
( Data Control Language )

* Language to **control** of the **data** that is stored in the RDMS 

```sql
 Common commands 
 * GRANT
 * REVOKE 
```

#### What is TCL
( Transaction Control Language )

* Langugage to **control** transaction in RDMS

```sql
 Common commands 
 * COMMIT
 * ROLLBACK
 * SAVEPOINT
```

#### What is DRL
( Data Retrieval Language )

* Languge to **retrieve** the data in RDMS

```sql
 Common commands 
 * SELECT
```

[Basic-statements](Basic-statements.md)


