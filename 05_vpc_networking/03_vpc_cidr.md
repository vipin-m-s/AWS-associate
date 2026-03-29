# CXIDR is classless inter domain routing
- earlier there was class based addressing
- Class A [0] 0 0 0 - 2^24 hosts
- class b [0 0 ] 0 0 - 65536 hosts
- class c [0 0 0] 0 - 256 hosts

# In CIDR we use base address and prefix
Allowed private IP addresses in AWS are
- RFC 1618 IP ranges
- 10.0.0.0/8 => 10.X.0.0/16
- 192.168.0.0/16
- 172.16.0.0/12 => 172.16.0.0 to 172.31.0.0/16

IN AWS allowed prefix is /16 to /28 

# IPV6
- It is different than ipv4
- It is unique in the entire world and all are public
- CIDR with prefix /56 ( 2^72 IPs )
- IPV6 cidr is allocated by AWS
