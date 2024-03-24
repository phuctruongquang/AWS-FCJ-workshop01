---
title : "Xác minh email vào SES"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b> 2.7 </b> "
---

#### Xác thực Email vào SES

1. Truy cập **AWS Management Console**

   - Tìm **SES**
   - Chọn **Amazon Simple Email Service**

    ![SES](/aws-fcj-workshop01/images/2-createVPC/7CreateSES/0001.png?width=90pc)


2. Trong giao diện **Amazon SES**

   - Chọn **Identities**
   - Chọn **Create indentity**

    ![SES](/aws-fcj-workshop01/images/2-createVPC/7CreateSES/0002.png?width=90pc)

3. **Identity details**
   
   - Chọn **Email address**
   - Mục Email address nhập email của bạn vào
   - Chọn **Create identity**

    ![SES](/aws-fcj-workshop01/images/2-createVPC/7CreateSES/0003.png?width=90pc)

4. Thông báo chờ xác minh **email**

    ![SES](/aws-fcj-workshop01/images/2-createVPC/7CreateSES/0004.png?width=90pc)

5. Mở email của bạn và sẽ thấy có một email từ Amazon Web Service gửi về cho bạn

    - Ấn vào đường dẫn
    
    ![SES](/aws-fcj-workshop01/images/2-createVPC/7CreateSES/0005.png?width=90pc)

6. Xác minh đã thành công

    ![SES](/aws-fcj-workshop01/images/2-createVPC/7CreateSES/0006.png?width=90pc)

    - Quay lại và kiểm tra

    ![SES](/aws-fcj-workshop01/images/2-createVPC/7CreateSES/0007.png?width=90pc)