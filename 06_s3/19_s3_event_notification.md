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
  <img width="447" height="398" alt="Screenshot 2026-04-03 at 7 04 22 AM" src="https://github.com/user-attachments/assets/e5c6c519-409c-41fb-9a75-cd0849a21eb5" />
