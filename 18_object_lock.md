# Object lock 

When a randomware attack occurs.
All  the files in the computer/VM will be modified and encrypted.
Unless we pay for attackers. we will not be able to dec rpyt without the keys.

So, we ccan make use of WORM in s3.
Write once read many. The objects once uploaded cannot be modified or deleted.

There are 2 methods
1. Governance mode
here the IAM user with appropriate rules can modify/delete the retention policy and delete the objects
This is still a problem. If the access, secret kjeys of the IAM user is compromised then hacker can delete/moidfy objects

2. Compliance mode
In this mode no1 will be able to modify or delete the objects. Even the root user will not be able to
Until the retention period is over.
