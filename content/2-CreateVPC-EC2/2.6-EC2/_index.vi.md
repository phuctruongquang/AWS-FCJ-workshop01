---
title : "Tạo EC2 Instance"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 2.6 </b> "
---

#### Tạo EC2 Instance

1. Truy cập **AWS Management Console**

   - Tìm **EC2**
   - Chọn **EC2**

    ![create ec2](/images/2-createVPC/6CreateEC2/0001.png?width=90pc)


2. Trong giao diện **EC2**

   - Chọn **Intances**
   - Chọn **Launch intances**

    ![create ec2](/images/2-createVPC/6CreateEC2/0002.png?width=90pc)

3. **Name and tags** của EC2 
   - Nhập **```EC2-start-stop```**
   - Chọn **Amazon Linux**
   - Chọn **Amazon Linux 2023 AMI**

    ![create ec2](/images/2-createVPC/6CreateEC2/0003.png?width=90pc)

4. Kéo xuống **Intance type**

   - Chọn **t2.micro**

- **Key pair**

   - Chọn **Create new key pair**

    ![create ec2](/images/2-createVPC/6CreateEC2/0004.png?width=90pc)

 - **Key pair name**
   - Nhập **```keypairlab```**
 - **Key pair type**
   - Chọn **RSA**
 - **Private key pair file format**
   - Chọn **.pem**
- Chọn **Create keypair**
  
    ![create ec2](/images/2-createVPC/6CreateEC2/0005.png?width=90pc)

5. Kéo xuống **Network settings**
   - Chọn **Edit**
  
    ![create ec2](/images/2-createVPC/6CreateEC2/0006.png?width=90pc)

   - VPC Chọn **lambda-start-stop**
   - Subnet Chọn **subnet-start-stop** ap-southeast-1a
   - Auto-assing public ip **Disable**
   - Chọn **Select existing security group**
   - Chọn **SG-start-stop**
   - Chọn **Launch instance**
  
    ![create ec2](/images/2-createVPC/6CreateEC2/0007.png?width=90pc)

6. Tạo thành công **Instance**

    ![create ec2](/images/2-createVPC/6CreateEC2/0008.png?width=90pc)



