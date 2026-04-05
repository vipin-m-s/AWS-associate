# There are 3 securiyt - access/authentication , data and network

## 1. access/authenticaion
- rds supports authentication using username and password.
- These should not be stored in plain text format
- They should be stored in aws secrets manager
- IAM role authentication is supported only for mysql and postgres databases

## 2. data encyrption 
- encyrption at rest can be enabled at creation time. It uses AWS KMS
- encyrption at trnasit is supported by http over tls by default
- If we have enrypted database and if we take snapshot the snapshot is also encyrpted
- If we have no encyrpted databse and we want encrypted.
    1. Create snapshot from non encrypted databaase
    2. Copy the snapshot with encryption
    3. Now create a database from encrypted snapshot
    4. now the databsae is encrypted

# network 
- RDS lives within the vpc and subnet, Hence we can use all the network security feature such as NACL and security group.
