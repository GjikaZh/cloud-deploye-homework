# Cloud Deployment Homework

## 🌐 Description
This repository is used to deploy a simple index.html page using AWS cloud provider

## ☁️ Cloud Provider
The cloud provider used in this assignment is the Amazon Web Services (AWS) - S3

## 🚀 Deployment Steps

1. Created a GitHub repository and added an `index.html` file.
2. Logged into AWS and navigated to the S3 service.
3. Created a new bucket named `cloud-deploy-homework`.
4. Unchecked **Block all public access** while creating the bucket.
5. Uploaded the `index.html` file to the bucket.
6. Enabled **Static Website Hosting** in the bucket properties and set:
   - Index document: `index.html`
7. Set up a **Bucket Policy** to make all files public:
   ```json
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Sid": "PublicReadGetObject",
         "Effect": "Allow",
         "Principal": "*",
         "Action": "s3:GetObject",
         "Resource": "arn:aws:s3:::cloud-deploy-homework/*"
       }
     ]
   }
   
8. Copied the link from bucket properties and opened it
## ⚠️ Issues Faced
I couldn’t make the file public using ACLs because "bucket owner enforced" was enabled. Which I resolved it by adding a public-read bucket policy manually.

## 🔗 Public URL
http://cloud-deploy-homework.s3-website.eu-west-3.amazonaws.com  

### 📄 In the repository is also a file containing screenshots for each step
