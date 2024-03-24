---
title : "Demo bài Lab"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

### Chúng ta sẽ tạo ra một lịch tự động để tắt instance nhé

1. Truy cập vào **EC2**
    - Xem trạng thái của instance đang là **Running**

    ![combine together](/images/7-CombineTogether/0001.png?width=90pc)

2. Truy cập vào **Amazon EventBridge**

    - Chọn **ScheduleEC2Stop**
    - Chọn **Edit**

    ![combine together](/images/7-CombineTogether/0003.png?width=90pc)

3. Tiếp theo chúng ta sẽ sửa lại giờ

    ![combine together](/images/7-CombineTogether/0004.png?width=90pc)

    - Chọn **Next**

    ![combine together](/images/7-CombineTogether/0005.png?width=90pc)

    - Chọn **Next**

    ![combine together](/images/7-CombineTogether/0006.png?width=90pc)

    - Chọn **Next**

    ![combine together](/images/7-CombineTogether/0007.png?width=90pc)

    - Chọn **Save schedule**

    ![combine together](/images/7-CombineTogether/0008.png?width=90pc)

4. Quay lại **EC2** và chờ tới giờ instance của bạn sẽ tự động chuyển trạng thái thành **Stopped**

    ![combine together](/images/7-CombineTogether/0009.png?width=90pc)

    {{% notice note %}}
   Nếu đã đến giờ mà instance chưa thay đổi trạng thái thì bạn hãy ấn refresh và chờ thêm 1-3p nữa nhé!
    {{% /notice %}}

    - Sau khi trạng thái đã **Stopped** bạn sẽ nhận được một Email thông báo

    ![combine together](/images/7-CombineTogether/0010.png?width=90pc)