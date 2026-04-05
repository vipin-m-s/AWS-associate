# RDS autoscaling
- rds instances use ebs volumes for storage purposes.
- It supports automatic autoscaling of ebs volumes
- condition for autoscaling are
  - storage remaining is less than 10% of the provisioned storage. Example it has crosses 900GB if 1TB is proviosioned
  - It should be for atleast 5 minutes in the above conditionm
  - Of there was a autoscaling activity, then 6 hours must be passed before another autoscaling activity
- it is supported for gp2, gp3 and provissioned IO and not supported for magnetic voluems
- Supported for all database types
- We can also configure maximum storage threshold, above which the rds waill not autosccale the stprage.
