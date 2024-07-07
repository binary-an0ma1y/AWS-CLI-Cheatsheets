# S3 Cheatsheet
There are generally two ways to interact with the S3 service using CLI:
 1. ```aws s3``` is great for quick, common tasks with simplified outputs.
 2. ```aws s3api``` is designed for tasks requiring JSON output, verbose details or advanced operations.

<small>This cheatsheet contains commands that have both variations (s3 and s3api), you can use the ```aws s3``` based commands whenever possible as they are simpler to use unless you need JSON output or have specific requirements.</small>

## 1. Creating Buckets

#### 1.1 Create a bucket:
- using 'aws s3'
```text
aws s3 mb s3://my-bucket-name123
```
- using 'aws s3api'
```text
aws s3api create-bucket --bucket my-bucket-name123
```
Using any one of these two commands will create a bucket in the default region 'us-east-1'.

#### 1.2 Create a bucket in a specified region
- using 'aws s3'
```text
aws s3 mb s3://mybucket --region us-west-2
```
- using 'aws s3api'
```text
aws s3api create-bucket --bucket my-bucket-name123 --region us-west-2 --create-bucket-configuration LocationConstraint=us-west-2
```

## Listing
### work in progress..
