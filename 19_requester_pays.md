# Requester pays

In aws s3, The owner is not only charged for storing obejcts in bucket
Owner is also charged for data transfer. data transfer in is 0 , but data transfer out cost is present.

If the owner decides he can enable requester pays
- When this is enabled. The requester AWS account will be charged for data transfer cost.
- The owner still needs to pay for storing the objects.
- The bucket will disable anonymous access Since they need to be charged.
- 
