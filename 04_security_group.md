# Security group

- This is a virtual firewall, most basic firewall for ec2 instance
- There are 2 firewalls the reqwuest mist pass through to reach ec2 instance
- NACL -> Security group -> ec2 instance
- NACL is subnet level
- Security group is instance level

# COmmon ports
http 80 
ssh 22 
ftp 21
SFTP 22
https 443 
rdp 3389 

# IPv6 traffix 
::/0 
Inbound rule and outbound rule

return traffic is always enabled by default
It is statefukl 
It remembers the return trafficx iss wlaways allowed
It is different than outbound rukes

# default behaviour
- by default all inbound traffic is not allowed
- All outbound traffic is allowed

# behaviour
- Multiple ec2 instance can use single SG
- Single EC2 can have multiple SG

# Authorises both ip4 and ipv6 traffic
# rules can be added and removed at any time. We do not have to wait for 5 minutes or reboot instances
# Max 16 securioty group can be attached to ec2 instancwe with 1000 rules currently
