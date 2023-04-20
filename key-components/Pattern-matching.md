#Pattern-matching #LIKEOperator #WHERE-OPERATOR
*****

#### What is pattern matching 

* It is possible to match the string and check for its **matching** with different patterns using the **LIKE** operator in SQL 
* LIKE operator => compares the part that satisfies and matched the pattern that is specified using a collection of various regular and widcard characters.
* The **LIKE** operator return **true** if match is found and if the string does **NOT** match with the specified pattern then it return **FALSE**

#### How does it work ? 

* The pattern with which we have to match the expression can be a sequence of the regular characters and wildcard characters
* The wildcard characters provide flexibility and variety in matching the expressions.

### Examples 

Table *Employees

| Id | LastName  | FirstName | Address   | City      | NumOfCars |
| :--------| :-------- | :-------- | :-------- | :-------- | :-------- |
|    1     |  Peterson |  Jordan     |   Empty Street       |   Prague  |  5
	|    2     |  Brave |  Adam     |   Empty Street       |   Viena    |  4
|    3     |  Jake |  Paul     |   Empty Street       |   Brusel        | 1
|    4     |  Charles |  Prince     |   Empty Street       |   London  | 4


* In simple way 
	* if looking for everything **after**  = '{letter}**%**'
	* if looking for everything **before**  = '**%**{letter}'
	* if looking everything **whenever**  = '**%**{letter}**%**'
#1

Display the employee names where firstName **starts** with 'A'
```sql 

SELECT firstName from empl
WHERE firstName LIKE 'A%';

# % means that rest 
# after the A it can be anything 

Output : true/false 
```

#2

Display the employee firstName **ends** with letter 'N'
```sql 

SELECT firstName from empl
WHERE firstName LIKE '%n';

# % means that rest 
# before the n it can be anything 

Output : true/false 
```

#3

Display all the names of all employees having 'P' in **any position** in their name 
```sql 

SELECT firstName from empl
WHERE firstName LIKE '%P%';

# % means that the letter can be after or before in the word 
```

#4

Display the names of all employees where whose firstName does **not** contain 'P' anywhere 
```sql 

SELECT firstName from empl
WHERE firstName NOT LIKE '%P%';

# NOT LIKE means that that the letter P is not included in these searched tuples 
```

