****


**JOIN VS INNER JOIN**
		- inner join only returns rows that have matching values in both tables
	- **LEFT OUTER JOIN  | RIGHT OUTER JOIN | FULL JOIN** 
		- Which way around you put your tables in the join statement doesn’t matter, so Course LEFT OUTER JOIN Lecturer is equivalent to Lecturer RIGHT OUTER JOIN Course. Standard SQL also supports a full outer join, which means that every row from both tables will be represented in the result. Lecturer FULL OUTER JOIN Course will retrieve all the lecturers (even if they don’t examine a course) and all the courses (even if they don’t have an examiner).
	- **Sets operation** 
		- used on two tables that have the same number and type of columns.
		- retrieve the rows that appear in both these tables 
		- or "Retrieve the rows that are in this table but not that one.”
	- I**ntersect | union | except**
		- interect - select both rows that choses where table.name = 'tomas'
		- union - select either subject 
		- except - select row where table.name = 'tomas' but not 'adam'
