---
title : "Create VPC"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1 </b> "
---

#### Create VPC

1. Access **AWS Management Console**

   - Find **VPC**
   - Select **VPC**

   ![create VPC](/aws-fcj-workshop01/images/2-createVPC/1CreateVPC/0001.png?width=90pc)

2. In the **VPC** interface

   - Select **Your VPCs**
   - Select **Create VPC**

   ![create VPC](/aws-fcj-workshop01/images/2-createVPC/1CreateVPC/0002.png?width=90pc)

3. **Name tags** VPC 
   - Import **```lambda-start-stop```**
   - IPv4 CIDR enter **```10.0.0.0/16```**
   - Select **Create VPC**

   ![create VPC](/aws-fcj-workshop01/images/2-createVPC/1CreateVPC/0003.png?width=90pc)


4. VPC successfully created **lambda-start-stop**

   ![create VPC](/aws-fcj-workshop01/images/2-createVPC/1CreateVPC/0004.png?width=90pc)

5. Proceed to activate **DNS server name**

   - Select **VPC lambda-start-stop**
   - Select **Actions**
   - Select **Edit VPC settings**
   
   ![create VPC](/aws-fcj-workshop01/images/2-createVPC/1CreateVPC/0005.png?width=90pc)

6. Enable **DNS server name**
   - Check the box **Enable DNS server names**
   - Select **Save**
  
   ![create VPC](/aws-fcj-workshop01/images/2-createVPC/1CreateVPC/0006.png?width=90pc)