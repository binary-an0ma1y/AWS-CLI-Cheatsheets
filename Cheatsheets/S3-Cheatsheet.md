# S3 Cheatsheet
- There are 2 ways to interact with the S3 service using CLI.
 1. ```aws s3``` - Use this command for straightforward file operations like copying, moving, removing, and syncing files between your local system and S3, ideal for everyday use without dealing with API complexities.
 
 2. ```aws s3api``` - Use this command for finer control over S3 operations like setting bucket policies, configuring access controls, managing bucket versioning, or other advanced configurations, suitable for administrators or developers leveraging the full power of the S3 API.

## Creating Bucket

### Create a bucket in a specified region
```text
aws s3api create-bucket --bucket my-bucket --region us-east-1
```
