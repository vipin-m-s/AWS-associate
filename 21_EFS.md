# Elastic FIle System

EFS is a fully managed file storage service offered by AWS
It can automatically scale from gigabyte to petabyte of data.
We do not need to manually scale the storage.

Imagine a scenario where ec2 instances are using EBS volumes of size 100 GB
If the storage is full 100 GB then ec2 instances cannot access store data. 
But if we use EFS then we do not need to worry about backend storage. 
AWS automatically Scales storage for us. 

We can attach EFS to multiple targets
EC2, lambda etc

# Cost
EFS 1 TB - 300 dollars
EBS 1 TB - 100 dollars
s3 1 TB - 23 dollars

# Advantages 
- We will be charged for how much storage we use per month in EFS , unlike EBS where we are charged for 1 TB of storage we have created.
- In EFS it will automatically scale, In EBS we need to manually extend the volume.
- If performance is a concern, Then EBS has to be used.
- EFS can be accessed from on prem via AWS direct or AWS VPN.
