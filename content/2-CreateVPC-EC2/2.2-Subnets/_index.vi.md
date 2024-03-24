---
title : "Tạo Subnet"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo Subnet

1. Trong giao diện **VPC**

   - Chọn **Subnets**
   - Chọn **Create Subnet**
  
   ![create subnet](/aws-fcj-workshop01/images/2-createVPC/2CreateSubnet/0001.png?width=90pc)


2. Giao diện **Create subnet**

   - VPC ID Chọn **lambda-start-stop**
   - Subnet name nhập **```subnet-start-stop```**
   - Availability Zone chọn **ap-southeast-1a**
   - IPv4 CIDR chọn **10.0.0.0/16**
   - IPv4 subnet CIDR block nhập **```10.0.10.0/24```**
  
   ![create subnet](/aws-fcj-workshop01/images/2-createVPC/2CreateSubnet/0002.png?width=90pc)

3. Kéo xuống và chọn **Create subnet**

   ![create subnet](/aws-fcj-workshop01/images/2-createVPC/2CreateSubnet/0003.png?width=90pc)

4. **Subnet** được tạo thành công

   ![create subnet](/aws-fcj-workshop01/images/2-createVPC/2CreateSubnet/0004.png?width=90pc)