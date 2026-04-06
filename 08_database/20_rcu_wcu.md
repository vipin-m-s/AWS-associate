# Provisoned capacity mode
- We need to pre-define the RCU/WCU
- Should be used for steady workload and predictable workload
- It will throttle spiky traffic
- Cheaper then capacity mode if workload is consistent

# on demand capacity mode
- It will define the rcu/wcu based on data access pattern
- Should be used for unpredictable workload
- It can handle spiky traffic
- Will be expensive if the workload is steady

It will take 24 hours to change between 2 capacity modes
