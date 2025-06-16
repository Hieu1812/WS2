+++
title = "Thiết lập VPC"
date = 2020
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

Ở phần này, bạn sẽ thiết lập VPC và security group cho các cluster
### Thiết lập VPC
<!-- {{% notice info %}}
{{% /notice %}} -->
1. Truy cập vào **VPC**.
!["VPC"](/images/VPC/6.png)
2. Chọn **Create VPC**.
!["VPC"](/images/VPC/7.png)
3. Ta chọn VPC and more nhằm đồng thời thiết lập subnet
4. Nhập các thông tin cần thiết ở khung 2 và 3, chọn số lượng AZ cần thiết, ở workshop này sẽ sử dụng ALB nên mình chọn từ 2 AZ trở lên
!["VPC"](/images/VPC/1.png)
5. Lựa chọn số lượng Public subnet và Private Subnet. Sau đó chọn create để hoàn tất việc thiết lập VPC
!["VPC"](/images/VPC/2.png)
6. Sau khi thiết lập, truy cập vào VPC -> chọn subnet sẽ sử dụng
!["VPC"](/images/VPC/3.png)
7. Chọn actions -> Edit subnet settings
!["VPC"](/images/VPC/4.png)
8. Tick chọn Enable auto-assign public ipv4 address và save. Tiếp tục thực hiện với các subnet sẽ sử dụng còn lại
!["VPC"](/images/VPC/5.png)