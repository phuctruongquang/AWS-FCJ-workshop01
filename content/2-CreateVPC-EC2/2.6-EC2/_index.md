---
title : "Create EC2 Instance"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 2.6 </b> "
---

#### Create EC2 Instance

1. Go to **AWS Management Console**

   - Find **EC2**
   - Select **EC2**

    ![create ec2](/images/2-createVPC/6CreateEC2/0001.png?width=90pc)


2. In interface **EC2**

   - Select **Intances**
   - Select **Launch intances**

    ![create ec2](/images/2-createVPC/6CreateEC2/0002.png?width=90pc)

3. **Name and tags** of EC2 
   - Enter **```EC2-start-stop```**
   - Select **Amazon Linux**
   - Select **Amazon Linux 2023 AMI**

    ![create ec2](/images/2-createVPC/6CreateEC2/0003.png?width=90pc)

4. Scroll down to **Instance type**

   - Select **t2.micro**

- **Key pair**

   - Select **Create new key pair**

    ![create ec2](/images/2-createVPC/6CreateEC2/0004.png?width=90pc)

 - **Key pair name**
   - Enter **```keypairlab```**
 - **Key pair type**
   - Select **RSA**
 - **Private key pair file format**
   - Select **.pem**
- Select **Create keypair**
  
    ![create ec2](/images/2-createVPC/6CreateEC2/0005.png?width=90pc)

5. Scroll down to **Network settings**
   - Select **Edit**
  
    ![create ec2](/images/2-createVPC/6CreateEC2/0006.png?width=90pc)

   - VPC Select **lambda-start-stop**
   - Subnet Select **subnet-start-stop** ap-southeast-1a
   - Auto-assing public ip **Disable**
   - Select **Select existing security group**
   - Select **SG-start-stop**
   - Select **Launch instance**
  
    ![create ec2](/images/2-createVPC/6CreateEC2/0007.png?width=90pc)

6. Successfully created **Instance**

    ![create ec2](/images/2-createVPC/6CreateEC2/0008.png?width=90pc)
