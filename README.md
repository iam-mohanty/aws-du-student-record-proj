# serverless-DU-student-data

## aws services :- lambda, s3, dynamodb, api gateway, iam , cloudfront , route53 ( ohio )

### step-1 :-

Create dynamoDB table

```sh
studentData
```

partition key

```sh
studentid
```

### step-2 :-

Create IAM role for lambda

AWS service = lambda

policy

```sh
AmazonDynamoDBFullAccess
```

```sh
CloudWatchFullAccess
```

role name = du_student_lambada_role

### step-3 :-

Create lambda function and update code
   
#### lambada function-1

```sh
insertStudentData
```

run time = python 3.12  ---->  apply new role  ---->  upload code

#### lambada function-2

```sh
getstudentdata
```

run time = python 3.12  ---->  apply new role  ---->  upload code

### step-4 :-

Create API Gateway

5. Create s3 bucket

6. Test this 👇😎

copy bucket website endpoint  ,  http://devbucket2024project.s3-website.ap-south-1.amazonaws.com

paste it on browser

7. Create cloudfront distribution

---> Origin domain = s3bucketurl

---> Origin access = Origin access control settings  ,  Create new OAC

---> Do not enable security protections  , Default root object = index.html

---> create distribution

---> copy cloudfront policy , go to s3 bucket , block public access and paste policy

9. Now test again 👍⛳

copy cloudfront " Distribution domain name "
