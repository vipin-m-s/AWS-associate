# VPC peering

- BY default we will not be able to communicate between resources across VPCs in same region, different region and different account via private IPS. The traffic would flow over the internet.
- If we want to want communication to happen via private network and not via internet.
- We need to enable VPC peering


VPC peering allows private IP communication between
- VPC withoin same region
- VPC across the region
- VPC across the AWS accounts

<img width="1029" height="735" alt="Screenshot 2026-03-19 at 5 40 45 AM" src="https://github.com/user-attachments/assets/45fe93be-947e-41b0-9297-e3cafee806d2" />

private communication is not allowed by default
Traffic goes via the internet using public IP for communication
cannot use private IP for communication


<img width="1026" height="633" alt="Screenshot 2026-03-19 at 5 42 16 AM" src="https://github.com/user-attachments/assets/075ef17d-ad63-400c-b8ed-6b8f8780b88f" />

Now ec2 instances can communicate via private IPS
1) Send a request for the peering connection to the accepter VPC
2) Accept the peering connection
3) Add the appropriate Routing rules for both the subnets
