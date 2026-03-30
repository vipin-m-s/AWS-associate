# Transit gateway 
- disadvantage with vpc peering
  - it is one to one connection
  - if the vpcs have to communicate there has to be a peering between all the vpcs
  - It is difficult to maintain

- Transit gateway
  - We can create one transit gateway per region and connect all VPCs within the region to transit gateway
  - And to connect to VPCs from other region. we can perform Transit gateway peering.
  - We can also connect transit gateway to site to site VPN on premise networks
  - We can connect to on-prem using direct connect as well.

<img width="638" height="578" alt="Screenshot 2026-03-30 at 9 07 00 AM" src="https://github.com/user-attachments/assets/13e1fe16-3975-42dd-a9d2-85f2fda72ee2" />

- It is a regional router, Only can connect vpcs within the same region.
- We can also connect to software defind WAN or third party network appliances

# Advnced features of transit gateway 
- IP multicast
  - single/multiple source and destination
  - UDP protocol / connectionless
  - From one computer we can send to multiple computers
  - sending email to email-list
- AZ affinity of the transit gateway
  - It will try to keep the traffic within the same AZ across the VPCs.
<img width="556" height="490" alt="Screenshot 2026-03-30 at 9 19 21 AM" src="https://github.com/user-attachments/assets/a687a218-0dc6-427e-8a55-686e6aa3d0c6" />

  - But if in the destinaiton AZ there is no ec2 instancce, the there will be asymmetric routing
  - Appliance may reject the traffic.
  - This is not what we want. Hence we can use transit gateway in applicance mode. This will ensure the traffic flows in same AZ
<img width="574" height="486" alt="Screenshot 2026-03-30 at 9 21 07 AM" src="https://github.com/user-attachments/assets/069c9221-51dc-44ad-b245-158089a702c6" />

- It supports sharing of Transit gateway across AWS account using RAM ( resource access manager )
- ANy architecture that requires centralized management requires transit gateway
