# Application load balancer
- It operates at layer 7 of the OSI model
- every load balcner has some components
- listener :- we can configure multiple listeners for a load balancer.
- Listeners can listen on ports such as 80,443,8080 etc
- Each listener has target group. We can route traffic to target group.
- It can parse the http headers, and perform
  - path based routing
  - host based routing
  - query parameter based routing
  - source IP based routing
- It supports dualstack ( ipv4 and ipv6 )
- It can connect with ec2, ecs , ip address and lambda as target group
- It can perform tls/ssl terminataion to secure communication between the clients and load balancer
- The communication between load baalancer and ec2 isntances are via http since it occurs internally via private network so it is secure
- It performs health check of the backend target group and send traffic only to the instances which are healthy by performing regualr health checks

- Load balancer is a regional service
- Ec2 instances are within subnet ( AZ )

Simple network architecture
<img width="674" height="715" alt="Screenshot 2026-03-28 at 9 44 52 AM" src="https://github.com/user-attachments/assets/d4838355-6290-4bc4-9f58-6e10a590dd4b" />

Custom domain 

<img width="669" height="698" alt="Screenshot 2026-03-28 at 9 47 34 AM" src="https://github.com/user-attachments/assets/fff51f86-b458-4861-9217-2345aae0a000" />


Securing the communication between the client and the server
<img width="606" height="607" alt="Screenshot 2026-03-28 at 2 10 32 PM" src="https://github.com/user-attachments/assets/fbce4db1-abe4-472b-a942-414fb66aba6a" />

Stiky sessions
 - Duratio nbased - AWSALB
 - application based sticky session - AWSALBAPP
<img width="612" height="619" alt="Screenshot 2026-03-28 at 2 11 54 PM" src="https://github.com/user-attachments/assets/5cd99753-64bc-4f52-8ad0-8b8e85709fa2" />

