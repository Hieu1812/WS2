+++
title = "Thiết lập ECS"
date = 2020
weight = 4
chapter = false
pre = "<b>4. </b>"
+++


Cluster là một nhóm logic của các service hoặc các task độc lập. Trong đó sẽ có số lượng service đang hoạt động và trạng thái triển khai của tất cả các task trong cluster.

Task definitions liệt kê các task definition family mà bạn đã tạo. Bạn có thể thực hiện các hành động sau:

- Triển khai task definition dưới dạng service hoặc task.

- Tạo một phiên bản mới

Trong phần này chúng ta sẽ tiến hành tạo ECS với serverless infrastructure (fargate) cluster và khởi chạy ứng dụng.



### Nội dung:

  - [Khởi tạo cluster](./4.1-cluster/)
  - [Thiết lập và khởi tạo task trong cluster](./4.2-taskdf/)
  - [Thiết lập service khởi chạy ](./4.3-service/)
