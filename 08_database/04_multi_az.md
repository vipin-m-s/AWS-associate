# Multi AZ
- RDS supports multi az deployment
- Where it creates a primary database in one az
- Secondary datanase in second az
- All read/write requests are sent to primary DB
- If the primary db/az fails then all the read/write requests are sent to secondary DB
- The DNS for accessing the primary database now redirects to secondayr db
- There is no code changes required from application side, fail over is automatic from AWS side
- The replication for primary -> secondary is synchronous
- Only after data is replicated, the qrite request is complete. 
- Both db will have same data at any moment. For fail over reasons
- Multi AZ is for high availabiluty na dnot scalability ( 2 databases cannot server read/write only 1 db supports read/write requests )
![Uploading Screenshot 2026-04-05 at 2.40.15 PM.png…]()
