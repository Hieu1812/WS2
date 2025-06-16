+++
title = "Phát triển CI/CD cho backend thông qua Docker với các dịch vụ của AWS"
date = 2024
weight = 1
chapter = false
+++
# Phát triển CI/CD cho backend thông qua Docker với các dịch vụ của AWS

### Tổng quan

 Trong bài lab này, bạn sẽ tìm hiểu về các dịch vụ của AWS trong triển khai CI/CD pipeline .

![WS](/images/WS2.png) 

### ECR
- Là một dịch vụ lưu trữ docker image được cung cấp bởi Amazon Web Services (AWS). Sử dụng ECR có thể kết hợp với các dịch vụ khác như ECS,EKS,... một cách thuận tiện hơn với tính sẵn sàng cao  
### CodePipeline
- Là một dịch vụ của AWS giúp ta trong việc xây dựng luồng pipeline cho CI/CD. Trong bài này sẽ có 3 stage: Source, Build, Deploy. Source sẽ được kích hoạt qua lệnh push trong github repo đã được cài đặt. Với Build sẽ kích hoạt CodeBuild, Deploy sẽ kích hoạt CodeDeploy.
### CodeBuild
- CodeBuild sẽ thực hiện vai trò build source code để ứng dụng có thể sẵn sàng deploy. Nó sẽ thực hiện các câu lệnh build thông qua một config file yaml chứa toàn bộ câu lệnh build và các cấu hình liên quan.
### ECS
- Là một dịch vụ điều phối container được quản lý hoàn toàn sẽ giúp việc triển khai, quản lý và mở rộng các ứng dụng được đóng gói một cách hiệu quả hơn. Trong bài này sẽ sử dụng cấu trúc serverless là fargate
### ALB
- Application Load Balancer là Cân bằng tải ở lớp ứng dụng (Layer 7 - HTTP). Giúp điều phối các HTTP Requests tới các máy chủ dịch vụ khác nhau (target groups) hoặc các ứng dụng trên cùng máy chủ.


### Nội dung

 1. [Thiết lập và đẩy image lên ECR](1-SetupECR/)
 2. [Thiết lập VPC ](2-VPC/)
 3. [Thiết lập CodeBuild](3-CodeBuild/)
 4. [Thiết lập và khởi chạy ECS](4-ECS/)
 5. [Thiết lập CodePipeline](5-Portfwd/)
 6. [Dọn dẹp tài nguyên](6-cleanup/)
