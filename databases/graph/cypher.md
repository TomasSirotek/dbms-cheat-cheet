***

#### Querying 

*Match* being uset to select nodes 
```cypher

MATCH 
```

*(n)* selecting the node (it is just simple variable)
can be named how ever we want to 
```cypher

MATCH () // node reference ()
MATCH (n) // naming it n for better naming 
```

returning all nodes matched in the database 
```cypher 

MATCH (n) RETURN n
```

selecting specific **label** of the nodes

```cypher 

MATCH (n:PLAYER) RETURN n
// matching n (variable) with the label 
// and returning n 
```

specifing the properties on the nodes

```cypher 

MATCH (player:PLAYER) RETURN player.name
// matching player (variable) with the label 
// and returning player.name

// selecting multiple properties 
// simply just inputing another comma and specifiyng 

MATCH (player:PLAYER) RETURN player.name, player.height


// can use aliases AS

MATCH (player:PLAYER) RETURN player.name AS bestName 


```

Result : 

![schema|400](assets/graphDb/select-property.png)


#### Filtering 

Simple selecting with WHERE clause 
```cypher

MATCH (player:PLAYER)
WHERE player.name = 'LeBron James'
RETURN player

```

Same thing shorter syntax 
Can use multiple properties of the node 
```cypher

MATCH (player:PLAYER 
{name: "LeBron James",height:2.1})
RETURN player
``` 

Selecting all that are not with the use of diamond brackets 

--> **<>** <--

```cypher

MATCH (player:PLAYER)
WHERE player.name <> 'LeBron James'
RETURN player
```

Simple grater a less 

```cypher

MATCH (player:PLAYER)
WHERE player.height < 2 // <,>
RETURN player

```

#### Arithmetic 


Calculatin BMI of the player 

```cypher

MATCH (player:PLAYER)
WHERE (player.weight / (player.height * player.height)) > 25
RETURN player
```


Filtering with **AND** and **>=** or ****