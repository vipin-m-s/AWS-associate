# EBS Encryption

- We can encrypt the ebs volumes using AWS KMS
- we can enable encryption by
  - Default encryption :_ Each region will have the default KMS keys are created with name aws/ebs ( it is regional service )
  - Manually creating encryption keys in KMS. CMK customer managed keys

 Encyrption is present at multiple level
 - If we have encrypted volume
 - The data at rest is encrypted
 - The data transferring from ebs volume to ec2 instance is encyrpted
 - The snapshot creeated from the ebs volume is encyrpted
 - The volume created from snapshot is encrypted

The encryption keys are required for
- Creating a volume
- Creating snapshot
- Creating volume from the snapshot

<img width="651" height="368" alt="Screenshot 2026-03-24 at 5 28 41 AM" src="https://github.com/user-attachments/assets/cd3d1ee5-e52e-446c-9e4c-92444531fb61" />

## We cannot encrypt existing ebs volume directly.
- unencrypted ebs volume -----> Create snapshot ------> Create encyrpted volume from snapshot

## We need to safe guard the CMK
- If the cmk is disabled in KMS the volume will not be accessible since it will not be able to decrypt without keys
- If the cmk is delete, there will be permanent loss of data
  
