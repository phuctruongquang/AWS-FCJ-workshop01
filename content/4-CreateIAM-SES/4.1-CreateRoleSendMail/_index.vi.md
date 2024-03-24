---
title : "Tạo Role"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

#### Tạo Role

1. Truy cập **AWS Management Console**

   - Tìm **IAM**
   - Chọn **IAM**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0001.png?width=90pc)

2. Trong giao diện **IAM**

   - Chọn **Roles**
   - Chọn **Create role**
  
    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0002.png?width=90pc)

3. Tiếp theo

   - Chọn **AWS service**
   - **Use case** chọn **Lambda**
   - Chọn **Next**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0003.png?width=90pc)


4. Tiếp theo

   - Nhập vào thanh tìm kiếm **```CloudWatchFullAccess```**
   - **Tích chọn CloudWatchFullAccess**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0004.png?width=90pc)

    - Nhập vào thanh tìm kiếm **```AmazonSESFullAccess```**
    - **Tích chọn AmazonSESFullAccess**
    - Chọn **Next**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0005.png?width=90pc)

5. Tiếp theo

   - Role name nhập  **```StateChangeEC2Role```**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0006.png?width=90pc)


   - Kéo xuống bên dưới chọn **Create Role**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0007.png?width=90pc)
6. Tạo thành công **Role**

    ![create role IAM](/aws-fcj-workshop01/images/5-CreateRole-IAMSendMail/0008.png?width=90pc)