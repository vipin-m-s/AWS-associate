# S3 event notificaiton 
- When an event occurs in s3 bucket, we can send the event to aws services using s3 event notificaiton
- Currently 3 services are supported
  - SNS sns:push 
  - SQS sqs:sendMessage
  - lambda lambda:invokeFunction
- Notifcation is snet on below operaiotns
  - objectCreatwed
  - objectRemoved
  - objectRetrieval from glacier started / completed
  - lifecycle has moved object from one storage class to another or expiration of objects
  - intelligent tiering - move objects from one class to another
  - bucket replication - when replication completed
- We should use this carefully since all above events can be sent in millions and lambda function is triggered
- We can specify the objects for which we watn to notify using object prefix, suffix and tags
- If bucket versioning is enabled, the event notification is sent for all versions
- Ordering is not guaranteed. If obj1 and obj2 is created. obj2 notification might be sent first
- The notification is sent one guarantteed tiome, it can be sent more than once, In that case application must handle
- The notification wil lcontain only the metadata and not the data itself. 
  <img width="447" height="398" alt="Screenshot 2026-04-03 at 7 04 22 AM" src="https://github.com/user-attachments/assets/e5c6c519-409c-41fb-9a75-cd0849a21eb5" />
