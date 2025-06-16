+++
title = "Thiết lập Cluster"
date = 2020
weight = 1
chapter = false
pre = "<b>4.1 </b>"
+++

Để khởi chạy ECS, ta phải cần tạo cluster để có tài nguyên phục vụ cho việc cài đặt container

#### Khởi tạo cluster

1. Truy cập **ECS**
![cluster](/images/ECS/cluster/1.png)
2. Lựa chọn mục Clusters -> Create cluster
![cluster](/images/ECS/cluster/2.png)
3. Nhập tên Cluster -> chọn AWS Fargate -> Create 
![cluster](/images/ECS/cluster/3.png)
4. Cluster đã được tạo, lúc này chúng ta cần tạo task defination để có thể tạo service khởi chạy trên cluster
![cluster](/images/ECS/cluster/4.png)
