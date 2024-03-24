---
title : "Tạo Lambda gửi cảnh báo"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 4.2 </b> "
---

#### Tạo Lambda gửi cảnh báo

1. Truy cập **AWS Management Console**

   - Tìm **Lambda**
   - Chọn **Lambda**

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0001.png?width=90pc)

2. Trong giao diện **Lambda**

   - Chọn **Create Function**
  
    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0002.png?width=90pc)

3. Tiếp theo

   - Chọn **Author from scratch**
   - Function name nhập **```LambdaEC2SendMail```**
   - Runtime chọn **Python 3.9**
   - Chọn vào mũi tên **Change default execution role**
   - Chọn **Use an existing role**

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0003.png?width=90pc)



    - Kéo xuống và chọn role **StateChangeEC2Role**
    - Chọn **Create function**

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0004.png?width=90pc)

4. Tiếp theo

   - Chọn **Code**
   - Xóa đoạn mã cũ và dán đoạn mã mới bên dưới và chỉnh sửa **Email** mà bạn đã xác minh ở **SES**
   - Chọn Deploy

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0005.png?width=90pc)

            import json
            import boto3

            def lambda_handler(event, context):
                subject = 'Attention Please'
                client = boto3.client("ses")
                body = """
                            <br>
                Your server is changing status: Start/Stop
                    """
                message = {"Subject": {"Data": subject}, "Body": {"Html": {"Data": body}}}
                response = client.send_email(Source = "Enter your email address here", Destination = {"ToAddresses": ["Enter your email address here"]}, Message = message) 
                print("The mail is sent successfully")
   
   - Deploy thành công

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0006.png?width=90pc)

5. Bước tiếp theo chúng ta thử nghiệm

   - Chọn **Test**
   - Chọn **Create new event**
   - Eventname nhập **```EC2SendMail```**
   - Chọn **Private**
   - Chọn **Save**
   - Chọn **Test**

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0007.png?width=90pc)

   - Mở **Email** kiểm tra. Sẽ có một thông báo được gửi về

    ![Lambda send mail](/images/6-CreateFunctionLambdaToMail/1CreateLambdaToMail/0008.png?width=90pc)