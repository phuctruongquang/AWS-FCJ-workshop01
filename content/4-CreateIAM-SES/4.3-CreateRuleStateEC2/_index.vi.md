---
title : "Tạo rule EventBridge"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 4.3 </b> "
---

#### Tạo Rule EventBridge

1. Truy cập **AWS Management Console**

   - Tìm **Amazon EventBridge**
   - Chọn **Amazon EventBridge**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0001.png?width=90pc)

2. Trong giao diện **Amazon EventBridge**

    - Chọn **Rules**
    - Chọn **Create rule**
  
    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0002.png?width=90pc)

3. Tiếp theo **Rule detail**

   - Name nhập **```RuleEventBridgeEC2StartStop```**
   - Chọn **Rule with an event pattern**
   - Chọn **Next**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0003.png?width=90pc)


4. Bước tiếp theo kéo xuống phần **Event pattern**

   - Event source chọn **AWS service**
   - AWS service chọn **EC2**
   - Event type chọn **EC2 Instance State-change Notification**
   - Event type Specification 1 Chọn **Specific state(s)** ấn dấu mũi tên chọn **stopped** và **pending**
   - Event type Specification 2 chọn **Specific instance id(s)** Specific instance id(s) nhập ID của instance Linux
   - Tiếp theo chọn **Next**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0004.png?width=90pc)

5. Tiếp theo

   - Chọn **Lambda function**
   - Chọn **LambdaSendMail**
   - Chọn **Next**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0005.png?width=90pc)

    - Chọn **Next**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0006.png?width=90pc)

    - Chọn **Create rule**

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0007.png?width=90pc)

    - Rule đã được tạo thành công

    ![create rule eventbridge](/aws-fcj-workshop01/images/6-CreateFunctionLambdaToMail/2CreateRuleEvent/0008.png?width=90pc)