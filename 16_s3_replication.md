# s3 replication  

- Autommatic and asynchronous replication of objects from one bucket to another bucket
- After enabling repliation , only new objects will be automatically replicated
- Older objects will not be, We need to perform on-demand replication using bathc operations
- It supports Same Region Replication (SRR) CrossRegion Replication (CRR)
- RTC - replication time control - If we want to have SLA of 15 minutes. 15 minutes for replicaiton objects
- Bucket versiojning has to be enabled for bucket replication 
- Use cases
  - Store data closer to user and reduce latency (CRR)
  - Store objects into one bucket from man y bucket (SRR)
  - Replicate production in test env ( SRR ) 
