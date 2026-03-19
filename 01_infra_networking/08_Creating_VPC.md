# Creaating vpc

Amazon virtual private cloud ( VPC ) provides us a virtual network to create servers 

- every region has 1 default VPC
- Default VPC will always have a CIDR block of 172.31.0.0/16
- every region default VPC will have same CIDR

When creating a new VPC, we provide
- name of the VPC
- CIDR block :- The ec2 instances we create within the VPC, The private IP of the instances will be in the range of this CIDR
