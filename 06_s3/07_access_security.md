# block all public acceess
- we can block all public access
- It can be used in enterprise
- To prevent data leaks
- we can then provide granular access
- By default all the public access is blocked

# ACL 
- iit is legacy
- it is recommended to use bucket policy
- With ACL we can provide list, read, write permissions
- owner of bucket will have all permissions
- Owner can enable / disable ACL

# Bucket policy - iam security 
- It is a JSON document where we specify the principal, resource, action, affect and condition
- In order for IAM user, group and role to access s3 bucket there are 2 things required
  - The IAM user, group and role should have identity based policy which will allow the user/group/role to access s3 bucket
  - Additionally There should be a resource based policy in s3 bucket which will allow access from the user/group/role
<img width="617" height="324" alt="Screenshot 2026-04-01 at 7 27 57 AM" src="https://github.com/user-attachments/assets/c402cde5-3374-4824-ba68-2694d12b6c8d" />

- Allow aaccess from certain iam user
- Allow access from certain iam role
- Allow access form iam user from other aws account
<img width="751" height="479" alt="Screenshot 2026-04-01 at 7 30 12 AM" src="https://github.com/user-attachments/assets/bc68c770-7b55-4de1-ac9d-dacc8275b9bc" />


# bucket policy - network security 
- We can allow or deny the access from specific VPC
- We can allow or deny the access from specific vpc endpoint
- We can allow or deny the access from specific IP address using condition 
- We can alloww or deny the access from speific IP cidr range 
- We can allow or deny the access from public IP address range using condition 
