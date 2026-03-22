# aAWS users

There are different types of users in our AWS account
- root user
  - This user does not have any restriction on the account
  - IAM policies does not apply to root user, hence no permissions are required
  - people should use root user only for special type of operations such as changing aws support plans, updating user permissions, closing aws account etc
  - FOr regular day to dat activities. iam user should be used

- IAM user
  - This user can map to employees in the org
  - THey will have restrcited access to the AWS account
  - THeir access are managewd via IAM policies

- IAM group
  - instead of adding iam policy for each user
  - WE can create iam group ( developer group )
  - We can attach policy to iam group
  - It will apply to all the iam usersw within that group

- iam role
  - THis is applicable for other aws services
  - lambda function will use iam role to access s3 buckets
<img width="733" height="724" alt="Screenshot 2026-03-22 at 6 24 01 AM" src="https://github.com/user-attachments/assets/da241c51-47d2-412a-beef-ada4bfb99445" />
