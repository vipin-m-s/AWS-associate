
- launch 2 ec2 instances
- Add a index.html
- Create ALB load balancer
- Create target group
- Balance load between the ec2 instances
- View their health status
- Stop 1 instace
- Check their health sttatus
- Start again
- and check load balancing
<img width="540" height="719" alt="Screenshot 2026-03-21 at 10 00 42 AM" src="https://github.com/user-attachments/assets/e4dfe176-8252-4b18-a17e-29796dde6ba8" />



## Handon 2

- Allow only the traffic from Security group of load balancer to the ec2 instances
- IP of instances will not fetch website, only DNS of the load balancer will getch website ( security increases )
- We can also Add rules for Application load balancer, We can forward request based on http headers, paths, request method etc.

 
