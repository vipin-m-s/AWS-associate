# IAM roles and efs storage

## IAM roles 
There are 2 types of IAM roles
- ec2 instance profile
  - ecs agent to pull container image
  - Send logs to cloudwatch
- ecs task role
  - For ecs task to download/upload to s3
  - create entry in dynamodb

<img width="476" height="501" alt="Screenshot 2026-04-05 at 9 59 49 AM" src="https://github.com/user-attachments/assets/24196d86-946e-4f0e-aa44-297686ec502d" />


## Persistent storage for ecs
- Each ec2 instance contains the EBS volume
- But if ecs task stop and starts in another ec2 instance, the task will not have access to storage
- And AWS fargate does not have EBS

#### EFS
- EFS is managed linux file system service with AWS
- It supports multi AZ, multi region, hence durable
- EFS can be mounted to each ecs task and to fargate
- We can persist our data in EFS by mounting
- If ecs task stop and start in anoyhert ec2 instance it can still mount to efs
- We connect ecs and efs via the task definition file

<img width="525" height="323" alt="Screenshot 2026-04-05 at 10 04 08 AM" src="https://github.com/user-attachments/assets/dc6a61b0-883f-41e6-9c43-457f8a5a6ba5" />
