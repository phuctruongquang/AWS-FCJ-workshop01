---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

#### Giới thiệu về AWS Lambda

   ![introduce lambda](/images/1-introduce/0001-lambda.png?width=30pc)

**AWS Lambda** (tạm gọi tắt là Lambda) là một dịch vụ điện toán phi máy chủ (serverless), dựa trên mô hình FaaS (Function-as-a-service). Khi sử dụng dịch vụ này, người dùng sẽ không cần quan tâm đến hạ tầng hệ thống bên dưới. Lambda sẽ thực thi các đoạn code do người dùng quy định khi được yêu cầu. Điều này giúp người dùng, đặc biệt là các lập trình viên (developer) sẽ có nhiều thời gian hơn để tập trung vào phát triển ứng dụng của mình.

Các ngôn ngữ lập trình đang được hỗ trợ bao gồm:
- Java
- Python
- C#
- Node.js
- Go
- PowerShell
- Ruby

Người dùng sử dụng các ngôn ngữ lập trình được hỗ trợ phía trên để tạo ra các Lambda function. Các function này sẽ tính phí dựa vào thời gian xử lý (duration time) ứng với dung lượng memory của function. Và mỗi khu vực mà function được tạo ra sẽ có mức phí khác nhau, hay xem để tham khảo chi phí từng khu vực tại [AWS Lambda Pricing](https://aws.amazon.com/lambda/pricing/) 


#### Giới thiệu về Amazon EventBridge

   ![introduce EventBridge](/images/1-introduce/0002-eventbridge.png?width=30pc)

**Amazon EventBridge** là dịch vụ cho phép bạn xây dựng các ứng dụng phản ứng với các sự kiện một cách nhanh chóng, dễ dàng và an toàn. EventBridge cung cấp một bus sự kiện phi tập trung, cho phép bạn truyền sự kiện giữa các ứng dụng, dịch vụ và tài nguyên AWS.

**Lợi ích của Amazon EventBridge:**

- Dễ sử dụng: EventBridge cung cấp một giao diện đơn giản để tạo, gửi và nhận sự kiện.

- Khả năng mở rộng: EventBridge có thể xử lý hàng triệu sự kiện mỗi giây.

- Bảo mật: EventBridge cung cấp bảo mật cấp doanh nghiệp.

- Tích hợp: EventBridge tích hợp với hơn 200 dịch vụ AWS và các ứng dụng SaaS phổ biến.

**Một số trường hợp sử dụng phổ biến cho Amazon EventBridge:**

- Tự động hóa các tác vụ: EventBridge có thể được sử dụng để tự động hóa các tác vụ như chuyển đổi dữ liệu, phân tích dữ liệu và quản lý quy trình.

- Xây dựng các ứng dụng theo sự kiện: EventBridge có thể được sử dụng để xây dựng các ứng dụng theo sự kiện như luồng dữ liệu, hệ thống cảnh báo và các ứng dụng IoT.

- Kết nối các dịch vụ AWS: EventBridge có thể được sử dụng để kết nối các dịch vụ AWS với nhau, giúp bạn dễ dàng xây dựng các kiến trúc ứng dụng phức tạp.

#### Giới thiệu về Amazon Simple Email Service

   ![introduce SES](/images/1-introduce/0003-SES.png?width=30pc)

**Amazon Simple Email Service (SES)** là dịch vụ gửi email với số lượng lớn, tiết kiệm chi phí và được xây dựng trên cơ sở hạ tầng đáng tin cậy, có quy mô linh hoạt do Amazon phát hành. Với Amazon SES, bạn có thể sử dụng nhiều giải pháp khác nhau như: gửi email giao dịch, thư tiếp thị, thử trả lời tự động hay bất kỳ nội dung nào khác.

Hiện nay, Amazon SES có hai mô hình định giá: Một là cho việc nhận email (đây là trọng tâm của dịch vụ này) và hai là cho việc gửi email.

Chi phí nhận email của Amazon SES phụ thuộc vào hai yếu tố: Số lượng email và kích thước của email bạn nhận được.


Chi phí gửi email của Amazon SES phụ thuộc vào hai yếu tố: Số lượng email, kích thước của email và kích thước của tệp đính kèm mà bạn gửi.

Ví dụ: Nếu email bạn nhận được dưới **256KB và không có tệp đính kèm**, thì việc nhận email là miễn phí. Ngoài ra, Amazon SES còn giới hạn 1.000 email hàng tháng cho bậc miễn phí của dịch vụ.

Xem thao khảo chi phí tại [Amazon SES pricing](https://aws.amazon.com/ses/pricing/)