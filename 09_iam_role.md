# IAM role

- IAM roles can be used when
  - AWS service wants to access other AAWS services such as ec2, lkambda
  - It cna be used by IAM users for cross account access
  - It can be used by external users which are federated user. google, facebook and active directory login

- SUppose consider a scenario where
- We have ec2 instance and app inside ec2 instance need access to s3 bucket
- We typicaly create an IAM user and attach policy and create access and secret keys
- and we can configure the keys inside the ec2 instance
- But the problem is there keys will not expire. They are long term credentials.
- If hacker hacks into the ec2 instance he can get access to the keys and perform actions.
- The keys are never rotated


## IAM role:-
With the help of IAM role. There is a expiry for the Access keys.
- These are short lived access keys and they keep rotating
- They use another aws service calles STS security token service for rotating the access keys.
- The keys are rotated every 1 hour by default
- We can attach the IAM role to the ec2 instance, And the access key + secret access key + session token. The session token keeps on rotating.

### IAM Role - access key + secret access key + session token ( from STS ) 
### IAM user - access key + secret access key 
