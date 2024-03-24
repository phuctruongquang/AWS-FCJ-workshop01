---
title : "Tạo Schelude EventBridge start EC2"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 3.5 </b> "
---

#### Tạo lịch tự động bật instance

1. Trong giao diện **Amazon EventBridge**

   - Chọn **Schedules**
   - Chọn **Create Schedule**

   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0001.png?width=90pc)

2. Trong **Specify schedule detail**

   - Schedule name nhập **```ScheduleEC2Start```**
   - Chọn **Recurring schedule**
   - Chọn **(UTC+07:00) Asia/BangKok**

   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0002.png?width=90pc)

3. Tiếp theo

   - Chọn **Cron-based schelude**
   - Phần **Cron experssion** phần này chúng ta sẽ nhập giờ thực tế mà bạn mong muốn Instance Start nhé. Tham khảo tại [Schedule types on EventBridge Scheduler](https://docs.aws.amazon.com/scheduler/latest/UserGuide/schedule-types.html?icmpid=docs_console_unmapped)
   - Chọn **OFF**

   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0003.png?width=90pc)

   - **Minutes** -> Nhập phút bạn muốn tắt instance
   - **Hours** -> Nhập giờ mà bạn muốn tắt instance
   - **Day of moth** -> Nhập ? thì sẽ chạy tất cả các ngày trong tháng
   - **Month** -> Nhập * sẽ chạy tất cả tháng trong năm
   - **Day of the week** -> Nhập Mon-Sat thì sẽ chạy thừ thứ 2 đến thứ 7
   - **Year** -> Nhập * sẽ lấy năm theo mốc hiện tại

   - Kéo xuống và chọn **Next**

   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0004.png?width=90pc)


4. Tiếp theo

   - Chọn **Templated targets**
   - Chọn **AWS Lambda Invoke**

   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0005.png?width=90pc)

5. Kéo xuống bên dưới
   - Phần **Invoke**
   - **Lambda function** nhập **```LambdaEC2Start```**
   - Thêm đoạn mã sau vào phần **Payload**
   - Chọn **Next**

         {
            "action": "start"
         }
            
   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0006.png?width=90pc)

6. Tiếp theo và kéo xuống cuối trang

   - **Role name** nhập **```Amazon_EventBridge_Scheduler_LAMBDA_StartEC2```**
   
   - Chọn **Next**

   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0007.png?width=90pc)

   {{% notice note %}}
   Ở phần Role name này sẽ được tạo ra và nằm tại [CloudWatch](https://us-east-1.console.aws.amazon.com/cloudwatch/home?region=us-east-1#logsV2:log-groups) Log group, bạn có thể xem thêm
   {{% /notice %}}

   - Kéo xuống và chọn **Create schedule**

   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0008.png?width=90pc)

   - Lịch tự động đã được tạo thành công

   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0009.png?width=90pc)

   - Bạn chờ tới thời gian đã đặt trước đó, và quay lại EC2 kiểm tra instance
   - Trạng thái instance đã **Pending**

   ![create EventBridge Start](/aws-fcj-workshop01/images/4-CreateLambda/4CreateEventBridgeStart/0010.png?width=90pc)

   {{% notice note %}}
   Nếu đã đến giờ mà instance chưa thay đổi trạng thái thì bạn hãy ấn refresh và chờ thêm 1-3p nữa nhé!
   {{% /notice %}}