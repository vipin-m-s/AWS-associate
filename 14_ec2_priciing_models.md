# ec2 pricing models

## on demand instances
- When we want to be charged hourly or based on seconds, we can opt for on demand instanced
- If we stop or terminate the instances we will not be charged
- But if AWS has resource shortages, we might get error when creeating on demand instances

## Reserved instances
- If we provide a commitment of running servers for say 1 year or 3 year
- We can get ec2 instances with 70% off from AWS.
- But we have to pay upfront cost to AWS for 1 year or 3 years
- Even if instances are stopped

## Spot instances
- AWS provides spare instances for discounted price of 70%-80% thorugh bidding
- But there a caveat, These instances will be terminated at anytime by AWS
- When other customers provision on demand instances or if someone else has made a highewr price bid.

## Saving plans
- Of we have commitment of running ec2 instances for dollar per hour.
- We can opt for savings plan
- They will offer instances for 1 year or 3 year commitment at discounter price

## dedicated hosts
- Usually in the physical hosts, there will be VMs created for multiple customers
- If we want the entire host for our use, we can opt for dedicated hosts
- no other VMs will be provisioned on those host
- It can be ondemand and reserved instances as well
