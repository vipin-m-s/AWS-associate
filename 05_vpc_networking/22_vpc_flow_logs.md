# flow logs 

- It is used to caputre infomration about IP network going in/out your ENI 
- Flow logs can be attached to ENI, subnet or entire VPC level
- It can send the collected logs to S3, kinesis datahose, cloudwatch etc.
- It is used for debugging purposes such as
  - ec2 cannot talk to rds
  - traffic blocked by nacl and sedurity group
  - detect suspicious traffic
- It can also caputre information from RDS, ELB, elastic cache, redshift
- There is no network performance inpact because of flow logs
- It is a charged service
- It stores logs such as source ip, source port, dest ip , dest port, protocol, status etc
