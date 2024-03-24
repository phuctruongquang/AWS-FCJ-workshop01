---
title : "Tạo Lambda Start"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

#### Tạo Start instance

1. Trong giao diện **Lambda**

   - Chọn **Create Function**
  
   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0011.png?width=90pc)

2. Tiếp theo

   - Chọn **Author from scratch**
   - Function name nhập **```LambdaEC2Start```**
   - Runtime chọn **Python 3.9**
   - Chọn vào mũi tên **Change default execution role**
   - Chọn **Use an existing role**
   - Chọn **LambdaEC2Role**
   - Và kéo xuống chọn **Create function**

   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0012.png?width=90pc)


3. Tiếp theo

   - Chọn **Code**
   - Xóa đoạn mã cũ và dán đoạn mã mới bên dưới và chỉnh sửa **Region, Instance**
   - Chọn Deploy
   - **Instance** thì bạn qua EC2 copy ID nhé
  {{% notice note %}}
   Bạn nhớ chỉnh lại **Region** nhé. Ở bài này mình đang ở Region **Singapore** nên nhập **```ap-southeast-1```**
   {{% /notice %}}

   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0013.png?width=90pc)


            import boto3
            region = 'ap-southeast-1'
            instances = ['ID instance Linux']
            ec2 = boto3.client('ec2', region_name=region)

            def lambda_handler(event, context):
               ec2.start_instances(InstanceIds=instances)
               print('started your instances: ' + str(instances))
         

1. Bước tiếp theo chúng ta thực hiện thử bật instance

   - Chọn **Test**
   - Chọn **Create new event**
   - Eventname nhập **```EC2Start```**
   - Chọn **Private**
   - Chọn **Save**
   - Chọn **Test**

   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0014.png?width=90pc)


   - Quay lại EC2 xem lại trạng thái của instance đã **Running**

   ![create lambda start](/aws-fcj-workshop01/images/4-CreateLambda/2LambdaStart/0015.png?width=90pc)