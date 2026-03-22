# AWS IAM permission boundary

- It is a guardrail against the granted IAM policy
- It restricts the resources the user can access
- If user has a policy which allows s3:* ec2:*
- And the permission boundary has only ec2:*
- Then the permission is just ec2:*
- Permission boundary does not grant permissions
- IAM policy IAM permission boundary
<img width="408" height="333" alt="Screenshot 2026-03-22 at 10 43 50 AM" src="https://github.com/user-attachments/assets/38e062d6-411b-443c-919f-753d15872944" />
