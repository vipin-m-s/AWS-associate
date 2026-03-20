# Storage gateway

When organization want to keep using their on premises infra for running webservers. 
But they want to use AWS for storage services. They can use storage gateway. 
The AWS storage services are exposed via standard protocols for access. 
This way the organization do not need to modify their legacy application to use AWS APIs.
 They can mount the volume and use it. 

 - File storage gateway
The File system is made accessible via the NFS/SMB protocol

- VOlume storage gateway
The block storage is made accessible via isci protocol

- tape storage gateway
tape storage services is made accessible vvia iscsi vtl protocol

<img width="1198" height="661" alt="Screenshot 2026-03-20 at 7 18 04 AM" src="https://github.com/user-attachments/assets/15b5075f-961f-49d4-aec9-b27c0fa8eb79" />
