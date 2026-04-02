# object lock 

- It helps in preveting objects being deleted or overwritten
- Useful for meeting WORM write once read many for compliance purposes in financcne etc
- S3 bucket versioning should be enabled for obejct lock
- Object retention
  - retention period
    - Fixed Duration upto which the object should be retained
    - It can be applied to the bucket level and to individual object level
  - retention modes
    - compliance mode - It cannot be delted/overwritten by anyone even root user until retention period finishes
    - goverenance mode - It can be deleted/overwritten with permisssion s3:BypassGoverenanceRetention
  - legalhold
    - No expiration date
    - Remains in place until deleted from the onbject version using permission s3:PutObjectLegalHold
