# Server side encryption KMS 

- S3 uses envelope encryption for SSE-s3, sse-kms and sse-c
  - envelope encyrption :-
  - Write operations :- 
    - We will pass the master key to s3 using various means
    - with the master key , aws will generate data key + encyrpted data key
    - Object is encrypted using data key
    - encrypted object + encyrpted data key is stoed in bucket
  - Read operation :-
    - when reading data , the encrypted data key is retrived and decrypted using master key
    - the data key is then used to decrypt the object

- When readng or writing objects from the bucket when using SSE-KMS we would require the IAM policy
  - Write: kms:generateDatakey
  - Read: kms:decrypt and kms:describeDataKey

- When readfing/writing we might see the "acceess denied" error if kms:decrypt and kms:generateDataKey permission is not provided

 - KMS keys are regional. We need to provide permisson in other regions as well


      <img width="929" height="579" alt="Screenshot 2026-04-02 at 4 45 52 AM" src="https://github.com/user-attachments/assets/f14e49cd-af5d-4a57-be97-b807b20a6d0d" />
