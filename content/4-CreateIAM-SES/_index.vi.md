---
title : "Tạo cảnh báo về Email khi Instance thay đổi trạng thái"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---
Dưới đây là mô hình bạn có thể tham khảo:

![1-intrduce sendmail](/aws-fcj-workshop01/images/1-introduce/Workshop01-EC2SendMail.png?width=50pc)

**Nội dung:**
1. [Tạo Role](4.1-CreateRoleSendMail)
2. [Tạo Lambda gửi cảnh báo](4.2-CreateLambdaSendmail)
3. [Tạo Rule EventBridge](4.3-CreateRuleStateEC2)
