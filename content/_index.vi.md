---
title : "Giảm chi phí vận hành hệ thống với AWS Lambda"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---

# Giảm chi phí vận hành hệ thống với AWS Lambda

#### Tổng quan

Bài viết này sẽ hướng dẫn cách sử dụng Lambda Function để tối ưu hóa chi phí cho hệ thống của bạn trên môi trường Cloud AWS. Chúng ta sẽ lên lịch tự động bật và tắt máy chủ chỉ cần hoạt động trong vài tiếng mỗi ngày.

Đối với các máy chủ hoạt động 24/7, **Saving Plan** là một cách hiệu quả để tối ưu hóa chi phí cho các máy chủ các bạn có thể tham khảo thêm tại đây [AWS Savings Plans](https://docs.aws.amazon.com/savingsplans/latest/userguide/what-is-savings-plans.html)

Dưới đây là mô hình triển khai bạn có thể tham khảo:

   ![1-introduce sodo](/aws-fcj-workshop01/images/1-introduce/Workshop01-Introduce.png?width=70pc)

#### Nội dung
1. [Giới thiệu](1-introduce/)
2. [Các bước chuẩn bị](2-createvpc-ec2/)
3. [Tạo AWS Lambda và Amazon EventBridge](3-createlambdastartstop/)
4. [Tạo cảnh báo về email khi instance thay đổi trạng thái](4-createiam-ses/)
5. [Demo lab](5-combinetogether/)
6. [Xóa tài nguyên](6-delete/)