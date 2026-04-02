# s3 bucket versioning

- Without the bucket versioning,
  - If the user uploads a object, modifies the object and reuploads it. The object will get overwritten
  - If the user deletes the object, The obecjt is lost

- With bucket versioning
  - S3 maintains versions of the object
  - new version of the object is created when a modified object is reuploaded
  - The new version of the object will have a new version ID
  - It can be used for rollback to older version of the object
  - When deleting the object we need to specift the object version
  - If we delte without object version , A delete marker is added to the object as a new version. We can get the object back by removing the delete marker.

### Lifecycle rules
- It is used for automatic transitioning of the objects among different storage classes.
- We can transistion the current and non-current objects as well
- We can move the non-current objects to infrequrnt access

## Cost for versions
- EDvery version of the object is cost associated

## Featires
- Bucket versioning should be enables for below features
- bucket replication
- object lock
- MFS delete
