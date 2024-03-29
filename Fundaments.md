******
#Fundaments #Starting-point

#### Table of content 
Main Content 

 - [Terminology](DBMS-terminology.md)
 - [Tools-software](Tools-software.md)
 - [Design-patterns](design-patterns-index.md)
 
 * [Table-creation](Table-operations.md)
 * [Basic-statements](Basic-statements.md)
 * [Databases](databases/mariandb.md)
 * [Pattern-matching](Pattern-matching.md)
 * [Aggregates](aggregates.md)
 * [Joins](joins.md)
 * [Clauses](clauses.md)
 * [SQL-parts](Patern-matching.md)

Resourcers 
	[W3Schools](https://www.w3schools.com/SQl/sql_and_or.asp)
	[JavaPoint](https://www.javatpoint.com/dbms-sql-joins) 
 
#### Data & Databases

- Data
	- Information stored in a computer or any other device
	- text,number,images,videos
- Databases
	- organized collection of related data ready for manipulation
	- different types of databases
	- allows efficient access and retrieval

#### What is DBMS vs RDBMS

* DBMS (Database Management System)
	* System to manage data stored in database (no-relations)
	* Broader term to refer **any type of dbms**
	* MongoDB,Firebase,Redis etc ..
	
* RDBMS (Relational Database Management System)
	* Based on **relational** model
	* Organizing stored data in table and having relations between data 
	* MySQL,Postgres,MSSQL,Oracle database ...

#### Dialects / Syntax
#Dialects #NOTFinished

* Fill here info about dialects 

#### Schema architecture 

- **External Schema(s)**
	- An external schema describes the part of the database that a particular user group is interested in and hides the rest of the database from that user group.
- **Conceptual Schema**
	- The conceptual schema hides the details of physical storage structures and concentrates on describing entities, data types, relationships, user operations, and constraints. 
	- This is the type of schema, that we use as developers.
- **Internal Schema** 
	- The internal schema uses a physical data model and describes the complete details of data storage and access paths for the database.

![schema|300](assets/schema-arch.png)

#### Data Independency 
- **Logical Data Independency**
	- The ability to change the conceptual schema without affecting the external level.
	- Often hard to accomplice completely.
- **Physical Data Independency**
	- The ability to change the physical schema without affecting the conceptual schema.
	- Typically totally transparent in modern DBMS’s.



  
  
