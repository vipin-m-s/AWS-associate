# gateway endpoint

- We can use gateway endpoint to access s3 and dynamodb via pricate aws network instead of public network via NAT/IGW
- NAT gateway is charged service and if we want to consume hughe amount of data using s3 using bucket via nat gateway it will be hevaily charged.
- Instead we can setup gateway endpoint whcih is free service
- It can connect only to s3 and dynamodb

Steps
- We need to create an gateway endpoint in the required vpc
- We need to add a Route table rule to send traffic to S3
- We need to allow Security group outbound traffic 80 and 443 port to s3

Prefix list
- We know that s3 and dynamodb is managed service
- it will not expose its IP address to us
- Hence we cannot add to security group and route table
- Hence when we attach gateway endpoint. Prefix list is createdd
- These are collection of IP address of the services using which we can add security group and route table.

<img width="979" height="629" alt="Screenshot 2026-03-30 at 5 26 09 AM" src="https://github.com/user-attachments/assets/3fb2448a-65df-4fca-a64f-9ec57bb39560" />

VPC peering and VPN 
- The gateway endpoint is only accessible within the VPC its created in
- We cannot access it from Peered VPC or on-prem network via VPN.

<img width="1254" height="613" alt="Screenshot 2026-03-30 at 5 28 33 AM" src="https://github.com/user-attachments/assets/a5d8535f-aabf-4b9d-836e-a159f5a3755e" />

Routing rule in prviate subnet
- Routing rule needs to be added - prefix list -> vpce ( gateway endpoint )

Security group outbound rule for ec2
- We need to allow port 8/443 from ec2 to the vpce if not all allow is added

# Gateway endpoint demo
- create vpc
- create public subnet and ec2 as bastion host
- create private subnet and ec2
- Create s3 buckets
- We will not be able to access s3 using aws s3 ls
- Then attach IAM role to private ec2 instance
- Try aws s3 ls we will not be able to access
- Create gateway vpc endpoint
- Validate route table rule is created for prefix list -> VPCe
- check aws s3 ls

