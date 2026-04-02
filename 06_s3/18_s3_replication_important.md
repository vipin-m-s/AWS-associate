# Important points on s3

- Cross region replication incurs cross region data trnasfer cost
- Same region replication does not
- Replication chaining is not supported . A->B->C. The objects ar enot copied from A->C. We need to add new rule A-> C or batch operation from B->C
- RTC provides 15 minutes of SLA - within 15 minutes 99.99% of objects are copied
- We can view the replication data via cloudwatch
- Events are also shared to s3 event notificaitons
- We can filter objects using object prefix, tags etc
- When using SSE-KMS the IAM persmissions hsould be provided in both source and dest region

# Delteion behaviour

## When deleting without version ID. 
- The object in source bucket will get delete marker
- THe object in dest bucket will not get delete marker
- Because dest bucekt is considered backup and might be accidental deletion

## whwen deleting with version ID
- In source bucket the version is delted
- In dest bucekt the version is not deletefd
- The dest bucket is to prevent accidental deletions
