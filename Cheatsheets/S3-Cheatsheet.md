# S3 Cheatsheet
- There are 2 ways to interact with the S3 service using CLI.
 1. ```aws s3``` - Use this command for straightforward file operations like copying, moving, removing, and syncing files between your local system and S3, ideal for everyday use without dealing with API complexities.
 
 2. ```aws s3api``` - Use this command for finer control over S3 operations like setting bucket policies, configuring access controls, managing bucket versioning, or other advanced configurations, suitable for administrators or developers leveraging the full power of the S3 API.

- The cheatsheet contains a mix of both approaches, you can use the ```aws s3``` based commands whenever possible as they are simpler to use when getting started.

## Creating Bucket

### Create a bucket
```text
aws s3api create-bucket --bucket my-bucket-name123
```
This will create a bucket in the default region 'us-east-1'

### Create a bucket in a specified region
```text
aws s3api create-bucket --bucket my-bucket-name123 --region us-west-2 --create-bucket-configuration LocationConstraint=us-west-2
```
If you want to creating a bucket in the us-east-1 region (N. Virginia), you can simply run the previous command since it is the default region:
```text
aws s3api create-bucket --bucket my-bucket-name123
```

## Listing

### Work in progress..
