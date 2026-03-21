# cross zonal lb

- Crosszonal load balancing is enabled by default for ALB and cannot be disabled
- Cross zonal LB is disabled for NLB, GWLB, CLB but can be enabled

# Use case
Consider a scenario where you have diferent number of servers in different AZ
With the help of cross zonal load balancing , the traffic is evenly distributed among all the ec2 instances present in all the AZs
<img width="696" height="711" alt="Screenshot 2026-03-21 at 7 19 55 PM" src="https://github.com/user-attachments/assets/898766cc-20ea-4c94-9645-4af7fa7a197e" />
<img width="696" height="711" alt="Screenshot 2026-03-21 at 7 19 55 PM" src="https://github.com/user-attachments/assets/898766cc-20ea-4c94-9645-4af7fa7a197e" />

With out cross zonal lb 
The traffic woul;d be unevenly distributed among the ec2 instances as below
<img width="772" height="702" alt="Screenshot 2026-03-21 at 7 21 27 PM" src="https://github.com/user-attachments/assets/5f3b9f8c-b36f-4dc6-996d-38f784de4fad" />
<img width="772" height="702" alt="Screenshot 2026-03-21 at 7 21 27 PM" src="https://github.com/user-attachments/assets/5f3b9f8c-b36f-4dc6-996d-38f784de4fad" />
