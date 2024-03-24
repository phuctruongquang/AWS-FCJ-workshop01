---
title : "Tạo Stop instance"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

#### Tạo Stop instance

1. Truy cập **AWS Management Console**

   - Tìm **Lambda**
   - Chọn **Lambda**

   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0001.png?width=90pc)

2. Trong giao diện **Lambda**

   - Chọn **Create Function**
  
   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0002.png?width=90pc)

3. Tiếp theo

   - Chọn **Author from scratch**
   - Function name nhập **```LambdaEC2Stop```**
   - Runtime chọn **Python 3.9**
   - Chọn vào mũi tên **Change default execution role**
   - Chọn **Use an existing role**
   - Chọn **LambdaEC2Role**

   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0003.png?width=90pc)

   - Kéo xuống và chọn **Create function**

   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0004.png?width=90pc)

   - Tạo thành công Lambda function Stop

   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0005.png?width=90pc)

4. Tiếp theo

   - Chọn **Code**
   - Xóa đoạn mã cũ và dán đoạn mã mới bên dưới và chỉnh sửa **Region, Instance**
   - Chọn Deploy
   - **Instance** thì bạn qua EC2 copy ID nhé
   {{% notice note %}}
   Ở bài này mình đang ở Region **Singapore** nên sẽ nhập **```ap-southeast-1```**
   {{% /notice %}}

   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0006.png?width=90pc)

         import boto3
         region = 'ap-southeast-1'
         instances = ['instance Linux ID']
         ec2 = boto3.client('ec2', region_name=region)

         def lambda_handler(event, context):
            ec2.stop_instances(InstanceIds=instances)
            print('stopped your instances: ' + str(instances))
   
   - Deploy thành công

   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0007.png?width=90pc)

5. Bước tiếp theo chúng ta thực hiện thử tắt instance

   - Chọn **Test**
   - Chọn **Create new event**
   - Eventname nhập **```EC2Stop```**
   - Chọn **Private**
   - Chọn **Save**
   - Chọn **Test**

   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0008.png?width=90pc)

   - Thông báo thành công

   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0009.png?width=90pc)

   - Quay lại EC2 xem lại trạng thái của instance đã **Stopped**

   ![create lambda stop](/aws-fcj-workshop01/images/4-CreateLambda/1LambdaStop/0010.png?width=90pc)