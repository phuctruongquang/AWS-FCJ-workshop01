---
title : "Tạo Schelude EventBridge Stop EC2"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 3.4 </b> "
---

#### Tạo lịch tự động tắt instance

1. Truy cập **AWS Management Console**

   - Tìm **Amazon EventBridge**
   - Chọn **Amazon EventBridge**

   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0001.png?width=90pc)

2. Trong giao diện **Amazon EventBridge**

   - Chọn **Schedules**
   - Chọn **Create Schedule**

   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0002.png?width=90pc)

3. Trong **Specify schedule detail**

   - Schedule name nhập **```ScheduleEC2Stop```**
   - Chọn **Recurring schedule**
   - Chọn **(UTC+07:00) Asia/BangKok**

   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0003.png?width=90pc)

4. Tiếp theo

   - Chọn **Cron-based schelude**
   - Phần **Cron experssion** phần này chúng ta sẽ nhập giờ thực tế mà bạn mong muốn Instance Stop nhé. Tham khảo tại [Schedule types on EventBridge Scheduler](https://docs.aws.amazon.com/scheduler/latest/UserGuide/schedule-types.html?icmpid=docs_console_unmapped)
   - Chọn **OFF**

   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0004.png?width=90pc)

   - **Minutes** -> Nhập phút bạn muốn tắt instance
   - **Hours** -> Nhập giờ mà bạn muốn tắt instance
   - **Day of moth** -> Nhập ? thì sẽ chạy tất cả các ngày trong tháng
   - **Month** -> Nhập * sẽ chạy tất cả tháng trong năm
   - **Day of the week** -> Nhập Mon-Sat thì sẽ chạy thừ thứ 2 đến thứ 7
   - **Year** -> Nhập * sẽ lấy năm theo mốc hiện tại

   - Kéo xuống và chọn **Next**

   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0005.png?width=90pc)


5. Tiếp theo

   - Chọn **Templated targets**
   - Chọn **AWS Lambda Invoke**

   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0006.png?width=90pc)

6. Kéo xuống bên dưới
   - Phần **Invoke**
   - **Lambda function** nhập **```LambdaEC2Stop```**
   - Thêm đoạn mã sau vào phần **Payload**
   - Chọn **Next**

         {
            "action": "stop"
         }
            
   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0007.png?width=90pc)

6. Tiếp theo và kéo xuống cuối trang

   - **Role name** nhập **```Amazon_EventBridge_Scheduler_LAMBDA_StopEC2```**

   - Chọn **Next**

   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0008.png?width=90pc)

   {{% notice note %}}
   Ở phần Role name này sẽ được tạo ra và nằm tại [CloudWatch](https://us-east-1.console.aws.amazon.com/cloudwatch/home?region=us-east-1#logsV2:log-groups) Log group, bạn có thể xem thêm
   {{% /notice %}}

   - Kéo xuống và chọn **Create schedule**

   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0009.png?width=90pc)

   - Lịch tự động đã được tạo thành công

   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0010.png?width=90pc)

   - Bạn chờ tới thời gian đã đặt trước đó, và quay lại EC2 kiểm tra instance
   - Trạng thái instance đã **Stopping**
   
   ![create Schedule Stop](/images/4-CreateLambda/3CreateEventBridgeStop/0011.png?width=90pc)

   {{% notice note %}}
   Nếu đã đến giờ mà instance chưa thay đổi trạng thái thì bạn hãy ấn refresh và chờ thêm 1-3p nữa nhé!
   {{% /notice %}}