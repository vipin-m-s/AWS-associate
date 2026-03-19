# NAT gateway

- Ec2 instances in private subnet will not be able to access internet to download security patches and security updates.
- Hence we need to involve a NAT gateway
- Ec2 instance will be able to access to the internet via NAT gateway.
- All request from ec2 instance will go to internet and response will flow back to the ec2
- But From the internet any new connection to private ec2 instance will be blocked by the NAT gateway
<img width="679" height="567" alt="Screenshot 2026-03-18 at 7 29 31 PM" src="https://github.com/user-attachments/assets/bd69f2b3-7250-433f-a7c4-6b9405eafd68" />
