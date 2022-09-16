# DB-Note

## Optimization
### Prepared statement
#### The workflow of using prepared statement is Prepare, Compile and Execute
#### Advantages
##### Precompilation and DB-side caching of the SQL statement leads to overall faster execution 
##### SQL injection can be eliminated by disabling literals, effectively requiring the use of prepared statements
### Avoid using SELECT *
#### It is better to specify the columns you need in the select statement rather than SELECT *
#### Advantages
##### If saves the network traffic by not retrieving unused data.
##### When you select* and table join, you may get two same column name from the different tables.
