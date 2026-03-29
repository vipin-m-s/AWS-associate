# Regional NAT 

# traditional nat pain points
- We need to create public subnet
- We need to maintain public subnet
- We need to create route table for NAT gateway to send traffic to IGW
- We need to create route table for private subnet to send traffic to NAT
- If its high availability setup we need to replicate the same setup in another AZ.

# Regional NAT
- This is a fully managed service by AWS
- We do not need to create public Subnet and route table
- It automatically creates the route table
- It can automatically support new AZs based on our workloads
- Or we can manually select AZs
- Traffic within each AZ is sent to NAT gateway within the same AZ to reduce the cross zonal cost
- We just need to add route in Private subnet route table 
- <img width="701" height="477" alt="Screenshot 2026-03-29 at 9 56 38 AM" src="https://github.com/user-attachments/assets/2e2924a5-137e-40d9-8c76-7351abdb8a91" />
