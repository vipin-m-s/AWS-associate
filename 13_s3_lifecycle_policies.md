# s3 lifecycle policies

If the objects are created and it remains in s3 standard storage then it will be heavilty charged
we want automated system which will move the objects in such a fashion
- Object creation - s3 standard
- After 30 days of object creation - s3 standrd IA
- After 60 days of objeect creation - s3 glacier

In this way organizations can save cost, 
By moving objects to different storage classes

NOTE:- If there are obejcts present in bucket, before applying lifecycle rules. Those object will continue to remain in standard storage.

