# dynamodb ttl 
- It deletes the expired items from the dynamo db table based on timestamp attreibute
- It uses UNIX epoch time
- If the current time is greater then the stored epoch the item is deleted.
- THere is no additional cost of using the feature, Standard read/write charges are applicable
- dynamodb table keeps checking the items in background and removes them asynchronmojusly
- It helps in reducing storage cost and keeps the table clean

# use cases
- User token/ session management - automatically delete the session takes after TTL
- Rate limit counter - Keep a counter of how many times the API has been hit with TTL
- OTP validation - store OTP for 1 minute and then delete it automatically after TTL

