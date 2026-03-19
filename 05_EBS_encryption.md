# Encryption 

When we store data in disk
It is  important to encrypt the data
So that if laptop is lost others cannot access the sensitive information 
Example:- BitLocker, Apple File vault, LUKS

# EBS encryption 
We can encrpyt the ebs volumes
aws uses industry standard AES-256 encryption
Data at rest is encrypted
Data moving from the volume to instance is encypted
Snapshot created from encyrpted volume is encrypted
Volume created from snapshot is also encrypted
We need to use AWS KMS keys for encyption
AWS handles all the encyrption we do not need to worry about it even in applicaiton 
