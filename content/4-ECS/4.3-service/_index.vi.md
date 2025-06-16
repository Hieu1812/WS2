+++
title = "Thiết lập service"
date = 2020
weight = 1
chapter = false
pre = "<b>4.3 </b>"
+++

Để khởi chạy ECS, ta phải cần tạo cluster để có tài nguyên phục vụ cho việc cài đặt container

#### Khởi tạo cluster

1. Truy cập cluster trong **ECS**, chọn đầu mục Service và Create
![cluster](/images/ECS/service/1.png)
2. Tại trang create service:
    - Chọn task definition, phiên bản mới nhất của task df sẽ được tự động chọn.
    - Trong environment, mình sẽ chọn options là launch type với fargate và platform mới nhất.
    ![cluster](/images/ECS/service/2.png)
    - Desired tasks sẽ lựa chọn theo nhu cầu. Số tasks sẽ được khởi chạy dựa trên thông số cài đặt sẵn.
    - Lựa chọn VPC giống với VPC đã chọn trong task definition. Chọn subnet phù hợp (ở đây mình chọn 2 subnet public)
    ![cluster](/images/ECS/service/3.png)
    - Chọn security group vừa tạo ở Trang 2
    - Phần bài của mình có sử dụng Load balancing nên sẽ tick chọn sử với cổng 80 và phương thức HTTP
    ![cluster](/images/ECS/service/4.png)
    - Đặt tên cho load balancer và target group, sau đó kiểm tra lại và chọn Create
    ![cluster](/images/ECS/service/5.png)
3. Truy cập load balancer để lấy DNS truy cập. 
    - khi truy cập vào trang, ta có thể thấy địa chỉ ip của container đang khởi chạy. Sau khi load lại trang thì sẽ thay đổi địa chỉ ip mới từ container khác
    ![cluster](/images/ECS/service/6.png)
    ![cluster](/images/ECS/service/7.png)

{{%notice tip%}}
Bạn có thể điều chỉnh thuật toán của load balencing trong **Edit target group attributes** ở target group đã tạo.
Bật stickness nhằm liên kết và duy trì phiên giữa máy khách và container
{{%/notice%}}
