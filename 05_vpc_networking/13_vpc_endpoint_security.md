# VPC endpoint security 
<img width="843" height="542" alt="Screenshot 2026-03-30 at 8 16 07 AM" src="https://github.com/user-attachments/assets/e5939e13-c0b6-4ac5-8afd-9f05cd300405" />

There are 2 types of security which can be provided 
1) netowrk level
2) Policy level

## netowkr level security 

### The ec2 instance security group 
- port 443 outbound rule has to be enabled to security group of ENI

### the eni securiyt group 
- port 443 inbound rule has to be enabled from the ec2 security group

## Policy based security

<img width="830" height="236" alt="Screenshot 2026-03-30 at 8 23 33 AM" src="https://github.com/user-attachments/assets/89a7eaae-4701-44a5-9fe6-c10d90b5cfee" />

## identity based policy 
- With identity based policy on iam user/role
- We can specify to which s3 bucket the user/role has access to

## endpoint policy 
- By default if we do not specify the endpoint policy. The policy applied is
```
{
    "Principal" : "*",
    "Affect" : "Allow", 
    "Action" : "*",
    "Resource": "*"
}
```
- means all the policy applicable to the user it can continue using same permissisons

### we can specify policy for specific s3 bucekt via the endpoint
```
{
    "Principal" : "*",
    "Affect" : "Allow", 
    "Action" : [
        "s3:getObject",
        "s3:putObject"
    ],
    "Resource": [
        "arn:aws:s3:::my_bucket",
        "arn:aws:s3:::my_bucket/*"
    ]
}
```
### We can also specify policy to allow only certiain aws account / role access
```
{
    "Principal" : "*",
    "Affect" : "Allow", 
    "Action" : "*",
    "Resource": "*",
    "Condition": {
        "ArnEquals" : {"aws:PrincipalAccount": "12345678"}
    }
}
```

for roles
```
{
    "Principal" : "*",
    "Affect" : "Allow", 
    "Action" : "*",
    "Resource": "*",
    "Condition": {
        "ArnEquals" : {"aws:PrincipalArn": "arn:aws:iam:::Role/test"}
    }
}
```

## Resource based policy 
We can also attach resource based policy on s3 bucket to allow
- Access Only from the endpoint
- Access Only from the vpc
