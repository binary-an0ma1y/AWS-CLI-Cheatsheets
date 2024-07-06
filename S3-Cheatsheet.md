# S3 Cheatsheet
- There are 2 ways to interact with s3 service using CLI.
 1. ```text aws s3``` command
 Use this when you need to perform straightforward file operations like copying, moving, removing, and syncing files between    your local system and S3. It's ideal for everyday use and for users who need to manage files without dealing with the complexities of the underlying API.
 
 2. ```text aws s3api``` command
 Use this when you need finer control over S3 operations, such as setting bucket policies, configuring access controls, managing bucket versioning, or any other advanced S3 configurations. This is suitable for administrators or developers who need to leverage the full power of the S3 API.

## Creating Bucket

### create a bucket in a specified region
```text
aws s3api create-bucket --bucket my-bucket --region us-east-1
```

## Listing


