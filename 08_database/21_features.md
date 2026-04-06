# Dynamodb global table
- The same table will be made available in multiple region
- All the replicas support read/write operatons unlike aurora db where 1 was primary other was secondary
- It is useful in providding low latency access for the customers as data is close to them
- It is also useful in region level failure / disaster recovery

# Dynamo db DAX
- Dynamo db accelerator is a in memeory cache for the dynamo db
- It provides microsecond low latency access to the cached items
- It is a eventual consistency, the data may be lagging in cache.
- use case :- high read operations
- anti pattern :- when we need read consistency

# Dynamo db streams
- When there is any update to the dynamo db tables, the change is captured in dynamodb streams
- Other AWS services can then read from the dynamodb stream and act on the messages
- It is an optional feature. Can be enabled/disabled any time
- Stores the changes in the logs exactly once and stricylt ordered for 24 hours
- Use case:-
  - sensor data, real time monitoring
  - connected car
  - Backup of table -> When change occurs in table -> Data sent to streams -> backup the data/table
