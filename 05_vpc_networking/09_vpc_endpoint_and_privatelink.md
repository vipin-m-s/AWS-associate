# VPC endpoint
- If an ec2 instance in prviate subnet wants to connect to AWS services or service in another VPC
- It can communicate via NAT gateway and IGW through the internet
- disadvantages are
  - NAT will charge processing charges  ( IF huge amounts of data has to be access from s3, then bill will be high )
  - Traffic will flow thorugh public internt and hence not safe and secure

<img width="703" height="639" alt="Screenshot 2026-03-29 at 5 14 58 PM" src="https://github.com/user-attachments/assets/368ee408-8ffc-40dd-b2eb-a7795ca90376" />

hence we can make use of VPC endpoint
- gateway endpoint
  - free service
  - We can communicate to s3 and dynamodb only using proivate network
  
- interface endpoint
  - Charged service
  - It will create an ENI with private IP in same subnet as private ec2 instance
  - Using the private IP of eni ec2 instance can aaccess other aws service ssych as kms, sqs etc
  - It can communicate with Network load balancer in other VPC or in other  aws accounts
  - It makes use of aws privatelink

<img width="734" height="550" alt="Screenshot 2026-03-29 at 5 16 36 PM" src="https://github.com/user-attachments/assets/a7024c66-de08-447c-96bf-70cd28400883" />

