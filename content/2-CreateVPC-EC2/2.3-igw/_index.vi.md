---
title : "Tạo Internet gateway"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Tạo Internet gateway

1. Trong giao diện **VPC**

   - Chọn **Internet gateways**
   - Chọn **Create Internet gateway**

   ![create igw](/images/2-createVPC/3CreateIGW/0001.png?width=90pc)

2. Giao diện **Create subnet**

   - Name tag nhập **```igw-start-stop```**
   - Chọn **Create**

   ![create igw](/images/2-createVPC/3CreateIGW/0002.png?width=90pc)

3. **Attach to VPC**
   - Chọn **Actions**
   - Chọn **Attach to VPC**
  
   ![create igw](/images/2-createVPC/3CreateIGW/0003.png?width=90pc)

4. **Attach to VPC**

     - Available VPCs chọn **lambda-start-stop**
     - Chọn **Attach internet gateway**
  
   ![create igw](/images/2-createVPC/3CreateIGW/0004.png?width=90pc)

5. **Attach** thành công tới VPC

   ![create igw](/images/2-createVPC/3CreateIGW/0005.png?width=90pc)