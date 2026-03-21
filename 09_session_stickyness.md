# sticky sessions ( session affinity ) 

- It is possible to implment session affinity or sticky sessions
- THe client requests are sent to the same instane behind the load balancer
- It is possible to implement this is classis load balancer, application load balancer and network load balancer
- The cookie used for session stickyness has anm expiration date you can control
- Use case:- make the user doesnt loose thier session data

<img width="435" height="526" alt="Screenshot 2026-03-21 at 6 36 45 PM" src="https://github.com/user-attachments/assets/c1f219ff-7ab4-40fa-8e72-36d38833cae8" />

# Sticky session cookie names
There are basically 2 types of cookies
1) Application cookie
   - Custom cookie
     - Created by the application itself
     - Cannot use AWSALB, AWSALBAPP, AWSALBTG, AWSELB 
   - Application cookie
     - created by load balabncer itself
3) Duration based cookie
   - Created by load balancer itself
   - ALB -> AWSALB
   - CLB -> AWSELB
  
