# s3 lifecycle vs intelligent tiering

## transition 
- lifecycle has user defined rules for moving objects between the storage classes
- intelligent tiering will automaticlly move objects based on access pattern

## Water fall model
- lifecycle follows lifecycle model where data moves from standard -> IA -> glacier and has 1 way movement
- IT does not follow waterfall mode supports 2 way movement

## Object expiration 
- lifecycle supports expiration where objects can be deleted
- IT doesd not support object deletion

## use case
- lifecycle can be used when we know the data access pattern
- IT is used when we do not know the data access pattern

## example 
- lifecycle -> logs, backups
- IT -> data lake, analytics

## duration 
- In lifecycle we can specify the duration for object in each Storage class
- In IT, we cannot specify the duration, it will automatically move objects

