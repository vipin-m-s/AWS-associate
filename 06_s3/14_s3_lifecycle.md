# s3 lifecycle 
- It will help us in transitioning the objects from one storage class to another to save the cost
- It follows the waterfall model .
  - From standard it can go to any other class
  - But it cannot move upwards
- Transition action
  - We can move from standard s3 to standard s3 IA after 30 days
- Transitiion period
  - We can also specify after how many days we need to move
  - We cannot move it in 1 days
  - from standard s3 -> standard s3 IA / one zone IA => 30 days
  - In glacier => 90 days
  - In glacier deep archieve => 180 days before transition
- We cannot transition smaller objects. It will cost more.
  - S3 does not support transitioning 128KB or lesser objects
- Expiration period
  - We can also specify when the objects needs to be deleted from the bucket

- Rules
  - We need to filter the objects based on prefix, tags and min size and max size
  - Such objects will be eligible for transition

- Transition is supported within the bucket objects itself, we cannot mvoe one object to another object. For that we have bucket replication

