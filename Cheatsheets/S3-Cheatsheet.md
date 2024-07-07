# S3 Cheatsheet
- There are generally 2 ways to interact with the S3 service using CLI.
 1. ```aws s3``` (Beginner Friendly)
  - "aws s3" is great for quick, common tasks with simplified outputs
  
 2. ```aws s3api``` (Good for developers & advanced tasks)
 - "aws s3api" is designed for tasks requiring JSON outputs, verbose details (or) advanced operations.

This cheatsheet contains commands that have both variations (s3 and s3api), you can use the ```aws s3``` based commands whenever possible as they are simpler to use unless you need JSON Output or have specific requirements.

## Creating a Bucket

### 1.1 Create a bucket using ```aws s3```
```text
aws s3 mb s3://my-bucket-name123
```

### 1.2 Create a bucket using ```aws s3api```
```text
aws s3api create-bucket --bucket my-bucket-name123
```
This will create a bucket in the default region 'us-east-1'

### 2.1 Create a bucket in a specified region using ```aws s3```
```text
aws s3 mb s3://mybucket --region us-west-2
```
### 2.2 Create a bucket in a specified region using ```aws s3api```
```text
aws s3api create-bucket --bucket my-bucket-name123 --region us-west-2 --create-bucket-configuration LocationConstraint=us-west-2
```
If you want to creating a bucket in the us-east-1 region (N. Virginia), you can simply run the previous command since it is the default:
```text
aws s3 mb s3://my-bucket-name123
```

## Listing

### work in progress..
