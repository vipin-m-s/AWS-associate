# RDS proxy 
- It is fully managed proxy service provided by aws for rds , aurora
- When there is high number of connections to the database, sometimes the connection might not be terminated due to which it will consume cpu, memory of database
- Proxy will offload the connection pool management to proxy
- Applications can use IAM role for authentication with proxy , proxy will use username, password to authenitcate with rds using AWS KMS
- Due to proxy the failover is imrpvode upto 66%. Since the connections to database needs to be recreated
- With proxy the connections are still existing during fail over
- It can be enabled without fail over
- RDS procy is not publicily accessible, It sits within VPC
- Use case: serverless applications with unpredictable and spiky workloads
