# Aurora features

## global database
- support multi region deployment
- Where primary database used for write operations
- Read replicas can be present closer to customers.
- It can also act as fail over when primary database fail
- replication happens within 1 second almost realtime

## CLoning
- Aurora supports database cloning, where we can clone a database
- It is fast since it uses copy on write technology. data is copied only when there is modification to data. 
- We can create upto 15 clones.
- Cloning is faster than snapshots due to COW

## serverless
- We just need to create database and capacity of database and connect application
- We do not have to worry about scaling during peak workloads
- It handles starting, stopping, scaling of the database
- We are charges per second usage of the database capacity
- Use cases for dev/test environment or even bbusiness critical applications
- Supports all rds features
