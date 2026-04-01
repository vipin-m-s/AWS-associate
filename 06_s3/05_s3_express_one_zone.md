# S3 express one zone 
- It is stored in 1 Availability zone
- In contrast with s3 one zone IA we can choose which AZ our bucket will be create. We could not select in s3 one zone IA
- It uses directory bucket ( these are low latency bucket high optimized )
- It can serve  2 million requests per second
- 10x faster than s3 standard and 80% less cost then s3 standard
- We can choose to add this s3 bucket in same AZ as our ec2 instance application or EKS. Hence we can get good performance and low latency
<img width="917" height="603" alt="Screenshot 2026-04-01 at 6 43 09 AM" src="https://github.com/user-attachments/assets/1323e88a-00e2-4d7a-b33a-854ecb1c0a51" />
