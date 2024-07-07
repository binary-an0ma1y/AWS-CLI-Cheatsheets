# S3 Cheatsheet
There are generally two ways to interact with the S3 service using CLI:
 1. ```aws s3``` is great for quick, common tasks with simplified outputs.
 2. ```aws s3api``` is designed for tasks requiring JSON output, verbose details or advanced operations.

This cheatsheet contains commands that have both variations (s3 and s3api), you can use the ```aws s3``` based commands whenever possible as they are simpler to use unless you need JSON output or have specific requirements.

## 1. Creating Buckets

#### 1.1 Create a bucket:
- using 'aws s3'
```text
aws s3 mb s3://my-bucket-name
```
- using 'aws s3api'
```text
aws s3api create-bucket --bucket my-bucket-name
```
Using any of these two commands will create a bucket in the default region which is generally "us-east-1".

#### 1.2 Create a bucket in a specified region:
- using 'aws s3'
```text
aws s3 mb s3://my-bucket-name --region us-west-2
```
- using 'aws s3api'
```text
aws s3api create-bucket --bucket my-bucket-name --region us-west-2 --create-bucket-configuration LocationConstraint=us-west-2
```

## 2. Listing

#### 2.1 : Listing buckets:
- using 'aws s3'
```text
aws s3 ls
```
- using 'aws s3api'
```text
aws s3api list-buckets
```

#### 2.2 : Check if a bucket with specified name exists:
- using 'aws s3api'
```text
aws s3api list-buckets --query "Buckets[?Name == 'my-bucket-name'].Name"
```
It prints back the bucket name "my-bucket-name" if it exists, else it returns empty "[]".

#### 2.3 : Listing objects in a bucket:
- using 'aws s3'
```text
aws s3 ls s3://my-bucket-name
```
- using 'aws s3api'
```text
aws s3api list-objects --bucket my-bucket-name
```
Note that folder names are also included along with object names in the output.

## 3. File Transfers

#### 3.1 : Copy a localfile to a bucket:
- using 'aws s3'
```text
aws s3 cp local-filename.txt s3://my-bucket-name/filename.txt
```
- using 'aws s3api'
```text
aws s3api put-object --bucket my-bucket-name --key filename.txt --content-type plain/txt --body local-filename.txt
```

#### 3.2 : Copy/sync multiple files from a local folder into a S3 bucket at once:
- using 'aws s3'
```text
aws s3 sync local-foldername/ s3://my-bucket-name
```
This will copy contents of the local folder into the bucket.

-----work in progress-----

#### 3.3 : :
- using 'aws s3'
```text

```
- using 'aws s3api'
```text

```
