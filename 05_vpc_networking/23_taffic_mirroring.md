# Traffic mirroring
- vpc flow logs only caputres the metadata about the packaets
- The traffic mirroring collects the actual payload
- It is used for Deep inspection of the packets
- The mirrored data can be sent to 3rd party netowrk applicances for security inspection at real time
- The source for traffic mirrroring is ENI
- The destination for traffic mirroring is ENI or NLB.
 <img width="461" height="190" alt="Screenshot 2026-03-30 at 2 52 50 PM" src="https://github.com/user-attachments/assets/7ee09b7a-f4ff-4db8-ac36-c0b34207017c" />
<img width="547" height="305" alt="Screenshot 2026-03-30 at 2 53 49 PM" src="https://github.com/user-attachments/assets/039cf323-6d11-4a32-8963-dcf6b382216b" />
- source and destination can be within same VPC
- Can be across VPC using VPC peering or transit gateway
- The source and destination can be across AWS account




