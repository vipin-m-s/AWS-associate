# Network ACL 

Imagine a scenario where a attacker is using an IP address to attack the servers
 
- Security groups are assocuiated at ec2 instance level
- Network ACLs are associated at the subnet level

- Security groups can all allow traffic to the ec2 instance
- With Network ACLs we can allow/deny traffic to the entire subnet

- Every region will have default ACL
- Every subnet should be associated with network ACL
- If not specified it will use the default network ACL
- The default network acl will allow all ipv4, ipv6 traffic to the subnets
- We can add inbound/outbound rules to the network acl
