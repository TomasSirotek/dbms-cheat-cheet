****
#### Domain 

* A **domain** is a unique set of values that can be assigned to an attribute in a database. For example, a domain of strings can accept only string values.

* **Range** of **Values**

- A domain is a set of values allowed for an attribute or field (ALL FIELDS FOR EACH COLUMN - (example => id,age,name - domain of chars or binary values ))

- Each field in a database has a specific domain

**Examples**
	- Name : A string of char of varying length
	- Age: A whole number between 0 and 120
	- Email : A string of characters that includes an "@" symbol

#### Constraints 

- Constraint means a limitation to something or someone. 
- Constraints only allow a partifuclar kind of data 

**Types**
#constraints-types

- *Domain Constraints*
	- The ones on the domain ensuring for example that age is between 0 and 120
	- **Examples**
		- Not null
		- Check (if valid then will be entered else not)
* *Key Constraints* 
	* Constraining PK not NULL and primary key 
* *Entity Integrity Contraints*
	* Same as the key contraint 
	* Sub set of the key constraints 
	* The key constraint states that the Primary Key attributes should be unique and must not contain null values.
* *Referential Integrity Constraints* 
	*  Each value in FK field must exist as values in the PK filed
	*  This constraint can be summarized in one line i.e. the referencing attribute must be the subset of referred attribute.
	*  This means that a record or a tuple cannot be inserted in the referencing relation if it is not present in the referenced relation.
	*  Also, any record that is present in the referencing relation cannot be updated or deleted from the referenced relation.
* *Tuple Uniquenes Constrains* 
	* Simple constrain ensuring that the tuple is unique (so no duplicates)
	
#### Tuple 

- Tuple in DBMS means a **row** or a **record**
- Basically any of the row or records are called Tuples 

#### Primary key 

* A unique identifier for each record (or row) in a table.
* Ensures that each record in the table has a unique value

#### Foreign key 

* A foreign key is a field in one table that refers to the primary key of another table. The foreign key creates a relationship between two tables, allowing data to be retrieved from one table based on the data in another table.

#### Intersect 

* Select both rows that choses where table.name = 'tomas'

#### Union

* Select either subject  

#### Except

*  Select row where table.name = 'tomas' but not 'adam'
