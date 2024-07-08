# serverless-DU-student-data

## aws services :- lambda, s3, dynamodb, api gateway, iam , cloudfront ( ohio )

### step-1 :-

Create dynamoDB table

```sh
studentData
```

partition key

```sh
studentid
```

3. Create IAM role for lambda

4. Create lambda function and update code
   
---> lambada function = insertStudentData  , run time = python 3.12 , apply new role  , upload code

---> lambada function = getstudentdata  , run time = python 3.12  , apply new role  , upload code


4. Create API Gateway

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
