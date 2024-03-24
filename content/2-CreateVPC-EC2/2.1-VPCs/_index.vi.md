---
title : "Tạo VPC"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---
#### Tạo VPC

1. Truy cập **AWS Management Console**

   - Tìm **VPC**
   - Chọn **VPC**

   ![create VPC](/images/2-createVPC/1CreateVPC/0001.png?width=90pc)

2. Trong giao diện **VPC**

   - Chọn **Your VPCs**
   - Chọn **Create VPC**

   ![create VPC](/images/2-createVPC/1CreateVPC/0002.png?width=90pc)

3. **Name tags** của VPC 
   - Nhập **```lambda-start-stop```**
   - IPv4 CIDR nhập **```10.0.0.0/16```**
   - Chọn **Create VPC**

   ![create VPC](/images/2-createVPC/1CreateVPC/0003.png?width=90pc)

4. Tạo thành công VPC **lambda-start-stop**

   ![create VPC](/images/2-createVPC/1CreateVPC/0004.png?width=90pc)

5. Tiến hành bật **DNS hostnames**

   - Chọn **VPC lambda-start-stop**
   - Chọn **Actions**
   - Chọn **Edit VPC settings**
   
   ![create VPC](/images/2-createVPC/1CreateVPC/0005.png?width=90pc)

6. Bật **DNS hostnames**
   - Tích vào ô **Enable DNS hostnames**
   - Chọn **Save**
  
   ![create VPC](/images/2-createVPC/1CreateVPC/0006.png?width=90pc)