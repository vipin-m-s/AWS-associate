# No sql vs sql database
## sql 
- When the schema is fixed
- When the workload is predictable
- When there are ad-hoc queries
- Example oracle, msserver, mysql
- Banking, flight booking

## No sql 
- When each item has different attributes
- When the workload is unpredictable
- When the 90-95% of queries are fixed
- Mongodb, dynamodb
- Ecommerce product catalog

# Dynamo db 
- It is a fully managed no sql key value database service
- Performance:- It provides consistent single digit millisecond read and write performance at any scale
  100TB of storage, trillions of rows, million requests/second.
- Serverless :- No provisionging or capacity management.
- Encryption :- provides encryption at rest
- Availability :- 5 9s of availability
- Data types:- supports multiple data types such as scalar ( number, string ) , JSON document and set 

# Structure
- It contains a table which is a container for storing data
- Each table will have an item ( similar to row  in sql )
- Each item will have partition key , optionally sort key and the attributes
- partition key + sort key = primary key ( needs to be unique )
- If sort key is not provided then parition key will be primary key.

# Dyamodb operations
## query
- We need to use parition key or optionally sort key to fetch items
- We can apply filters on the returned items
- We can use conditions like >, >= etc on sort key
- We can use only = for parition key 
  
## scan 
- It will fetch all the items and hence expensive.
- We can apply filters on the returned items
- It is slow and expensive
