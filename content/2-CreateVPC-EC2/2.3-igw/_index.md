---
title : "Create Internet gateway"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 2.3 </b> "
---

#### Create Internet gateway

1. In the **VPC** interface

   - Select **Internet gateways**
   - Select **Create Internet gateway**

   ![create igw](/aws-fcj-workshop01/images/2-createVPC/3CreateIGW/0001.png?width=90pc)

2. Interface **Create subnet**

   - Enter tag name **```igw-start-stop```**
   - Select **Create**

   ![create igw](/aws-fcj-workshop01/images/2-createVPC/3CreateIGW/0002.png?width=90pc)

3. **Attach to VPC**
   - Select **Actions**
   - Select **Attach to VPC**
  
   ![create igw](/aws-fcj-workshop01/images/2-createVPC/3CreateIGW/0003.png?width=90pc)

4. **Attach to VPC**

     - Available VPCs select **lambda-start-stop**
     - Select **Attach internet gateway**
  
   ![create igw](/aws-fcj-workshop01/images/2-createVPC/3CreateIGW/0004.png?width=90pc)

5. **Attach** successfully to VPC

   ![create igw](/aws-fcj-workshop01/images/2-createVPC/3CreateIGW/0005.png?width=90pc)