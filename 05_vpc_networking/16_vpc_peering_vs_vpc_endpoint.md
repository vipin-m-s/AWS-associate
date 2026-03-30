# VPC peering vs VPC endpoint

- VPC peering creates full layer 3 connectivity between the 2 VPCs
- So any resource in 1 VPC can access any resoure in the other VPC
- But we want only the application to be accessible and not the servers
<img width="691" height="277" alt="Screenshot 2026-03-30 at 9 48 48 AM" src="https://github.com/user-attachments/assets/ef373be2-b7a0-486d-934b-79e64b8c8491" />

- There is also bi directional connection with vpc peering
- Any resource in vpc1 can access any reosurce in vpc2 and vvice versa
- Only the clients should be able to connect with the service
<img width="710" height="223" alt="Screenshot 2026-03-30 at 9 50 01 AM" src="https://github.com/user-attachments/assets/31bc1bd2-4252-40f4-8070-4a82d80e9135" />


- For VPC peering 2 vpcs cannot have the same CIDR blocks. It should be different
- The SAAS cidr is not in our hand, it can have same CIDR range
<img width="717" height="280" alt="Screenshot 2026-03-30 at 9 50 59 AM" src="https://github.com/user-attachments/assets/221b8562-3d12-4aa3-b426-75ecef986578" />

- IN VPC peering there is a limitation on the number of VPC peering connection there can exist ( max 125 )
- For a SAAS service provider, they might want to expose their application to mny clients
<img width="585" height="296" alt="Screenshot 2026-03-30 at 9 53 11 AM" src="https://github.com/user-attachments/assets/78f27ab5-fe4d-4147-9a92-408d57809707" />


- IN VPC endpoint ( private link ), There is no full layer 3 connectivity. We expose only the service and not the servers.
- There is a one way communication, hence only clients can access service
- The service can only be exposed via VPC service endpoint and in other vpc we need to create VPC endpoint
- There is no limitation on number of vpc endpoint connection.
- PrivateLink supports having same CIDR ranges.
