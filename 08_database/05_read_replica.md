# Read replica
- It is an scaling solution where we can scale the read requests
- It is also used to reduce then stress on the primary db
- We create 1 primary databnase which can serve both read/write requests
- Then create upto 15 read replicas which can serve read requests
- We can place read replicas in same or different region ( cross region data transfer cost is applicable )
- It is responsibility of the application to redirect the read requests to read replica
- There is asynchronous replication from primary to read replicase
- So the read reploicas will store the stale entry and there is a lag/ read consistency is not present
- If latest data is needed it can be read from primary database
- It also acts as a disaster recovery solution,. if primary fails we can promtre one of them to priamry and it will act as a standalone database
<img width="864" height="480" alt="Screenshot 2026-04-05 at 2 51 57 PM" src="https://github.com/user-attachments/assets/9eb0dc9c-356e-442c-ba2e-9c763c0c4055" />


