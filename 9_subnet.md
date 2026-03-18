# sub networking

- Subnetworking is creating sub divisions of the network
- VPC spans across all the availability zones
- We can create an EC2 instance in a availability zone
  
<img width="1105" height="720" alt="Screenshot 2026-03-18 at 6 57 03 AM" src="https://github.com/user-attachments/assets/94d9d118-5048-4047-9168-403527a927a1" />

- Since the VPC spans across all availabiliuty zone
- We cannot create ec2 instance in VPC
- Each subnet lives within an availability zone
- We create ec2 instance within a subnet and behind the scenes we are creating within that availability zone


<img width="1130" height="658" alt="Screenshot 2026-03-18 at 6 59 06 AM" src="https://github.com/user-attachments/assets/6263ec97-2a72-46e7-ab1b-24d792eed9f6" />

- In each region we have default VPC
- Default VPC will have default subnet
- number of default subnet = number of availability zone in the region
- By default 4090 IPs per default subnet
