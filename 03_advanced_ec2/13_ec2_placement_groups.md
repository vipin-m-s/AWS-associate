# Ec2 placement groups

- AWS provides a way to choosing the underlying AWS infrastructure placement stratgey
- This can be done to increase the perfotmance, latency and avoid hardware level failures
- There are 3 placement grousp
  - clustered placement group
    - all the ec2 instances will be placed on same physical host
    - Reduced the loatency
    - Can be used for hpc workloads
    - fast node to node communication
  - spread placement group
    - When we want instances to not share the underlying hardware
    - to avoid hardware related failure impact
  - paritioin placement group
    - When we have large number of instances
    - We can group the instances and place it on different physiocal hosts. 
  
