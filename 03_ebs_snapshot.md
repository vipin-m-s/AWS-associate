# SNAPSHOT

- point in time backup of the ebs volume
- They are stored in s3 bucket in backend ( highly durable 11 9s of durability )
- They are regional service
- We can copy the snapshot to different region
- They are incremental in nature - one full snapshot + incremental changes ( useful for cost saving ) 
- Tey can be shared across different AWS accounts
- When we delete the ebs snapshot, it will be stored in reccycle bin for 30 days.
- We can also control the lifecycle of ebs volume using ADLM amazon data lifecycle manager. To Create snapshot weekly and to delete the snapshot after certain duration.
- EC2 instance ---> ebs volume ----> ebs snapshot 
