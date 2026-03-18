# VPC 

- When a new persion is migrating to a new city
- He has to look for a new house
- Similarly when server is being migratated to the cloud
- We need to look for a new housr for the servers, Which is VPC
- Each server lives within the VPC
- Each AWS region will have a default VPC

<img width="535" height="653" alt="Screenshot 2026-03-18 at 5 46 33 AM" src="https://github.com/user-attachments/assets/bd98852a-65b2-48d0-a6c2-4f595e083342" />

# subnet 

- Suppose John wants to earn extra money
- So he partitioned his house into 2 parts
- Similary VPC is paritioned into multiple paritions.
- Where the servers can live
- 3 servers live in parition1 ( subnet1 )
- 2 servers live in partition2 ( subnet2 )
- Based on the size of the housr, we can fit number of people
- If housr is small then less people
- Similarly If subnet is small , less number of servers

<img width="489" height="565" alt="Screenshot 2026-03-18 at 5 48 39 AM" src="https://github.com/user-attachments/assets/e4f71df1-7dd7-4d96-b94b-7aa0a4470123" />

# Routes

- Suppose there is 2 doors for partition1
- With which the person can go out and inside the house
- Similarly we can create routes for subnet1
- So that outside world can reach the servers in subnet1
- And subnet1 server can reach the outside servers
- Subnet2 does not have any doors. So no1 can enter partition2 or can go out of partition2
- This is the 0.0.0.0/0 route in route table

<img width="580" height="578" alt="Screenshot 2026-03-18 at 5 50 35 AM" src="https://github.com/user-attachments/assets/59a52f65-400b-4890-8a46-d9e2ea912bf3" />

- If we want the people to move within the partiitons.
- We need to create door between the 2 paritions within the house
- Similarly to communicate between the 2 subnets, we need to add route
- This is the local route in route table
  
<img width="616" height="578" alt="Screenshot 2026-03-18 at 5 52 00 AM" src="https://github.com/user-attachments/assets/73125c58-e356-47d5-b12a-9da8026d75ad" />


