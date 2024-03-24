---
title : "Tạo role"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1 </b> "
---

#### Tạo Policy

1. Truy cập giao diện **AWS Management Console**

   - Tìm **IAM**
   - Chọn **IAM**

   ![create IAM policy](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0001.png?width=90pc)

2. Trong giao diện **IAM**

   - Chọn **Policies**
   - Chọn **Create Policy**

   ![create IAM policy](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0002.png?width=90pc)

3. Bước tiếp theo

   - Chọn **JSON**
   - Xóa đoạn mã cũ trong **Policy editor** và sao chép đoạn mã bên dưới dán vào
   - Chọn **Next**

               {  "Version": "2012-10-17",
         "Statement": [
            {
               "Effect": "Allow",
               "Action": [
               "logs:CreateLogGroup",
               "logs:CreateLogStream",
               "logs:PutLogEvents"
               ],
               "Resource": "arn:aws:logs:*:*:*"
            },
            {
               "Effect": "Allow",
               "Action": [
               "ec2:Start*",
               "ec2:Stop*"
               ],
               "Resource": "*"
            }
         ]
         }


   

   ![create IAM policy](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0003.png?width=90pc)

4. **Policy details**

   - Policy name nhập **```LambdaEC2Policy```**
   - Chọn **Create Policy**

   ![create IAM policy](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0004.png?width=90pc)

   - Vậy là chúng ta đã tạo thành công Policy

#### Bước tiếp theo chúng ta sẽ tạo Roles

1. Trong giao diện **IAM**
   
   - Chọn **Roles**
   - Chọn **Create Role**

   ![create IAM policy](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0005.png?width=90pc)

2. Tiếp theo

   - Chọn **AWS service**
   - Use case chọn **Lambda**
   - Chọn **Next**.

   ![create IAM policy](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0006.png?width=90pc)

3. Tiếp theo

   - Nhập vào thanh tìm kiếm mà chúng ta đã tạo ra ở phần Policies **```LambdaEC2Policy```**
   - **Tích chọn Policy**
   - Chọn **Next**

   ![alt text](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0007.png?width=90pc)

4. Tiếp theo

   - Role name nhập  **```LambdaEC2Role```**

   ![create IAM policy](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0008.png?width=90pc)

   
   - Chọn **Create Role**

   ![create IAM policy](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0009.png?width=90pc)

5. Tạo thành công **Role**

   ![create IAM policy](/aws-fcj-workshop01/images/3-CreateIAMPolicy-Role/0010.png?width=90pc)