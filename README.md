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

 
## Indexes 
### An Index is a data structure that increase retrieval speed at the expense of using more storage space and decreasing the write spped.
### It requires at most n reads when quering on a table with n records by a field which known as a table scan. Instead, when querying by a key, it takes average n/2 reads because the scan will stop when the first record is found. Note. Index is not required to be set on a key. 
### Each record in the index has a pointer to the original data in the table.
## Composite Indexes
### A data structure sort on a concatenation of multiple fields. Note. the order of constituent columns in composite index is important
### It is a good idea to create a composite index on fields which often appear together.
