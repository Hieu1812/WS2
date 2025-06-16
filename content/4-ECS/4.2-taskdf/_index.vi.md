+++
title = "Thiết lập Task definition"
date = 2020
weight = 1
chapter = false
pre = "<b>4.2 </b>"
+++


Trong bước này, chúng ta sẽ tạo task definition cho cluster vừa tạo.

#### Tạo **Task definition**

1. Truy cập Task definition -> Create new task definition
![taskdf](/images/ECS/taskdf/1.png)

2. Tại trang **Create bucket** 
    - Nhập tên Task definition.
    - Lựa chọn Launch type, ở đây mình chọn fargate.
    - Hệ điều hành,CPU,Ram lựa chọn theo nhu cầu sử dụng của ứng dụng.
    - Task roles hãy lựa chọn các role có sẵn hoặc tạo mới ở mục đó.
    ![taskdf](/images/ECS/taskdf/2.png)
3. Trong mục container, ta thiết lập như sau
    - Nhập tên của container.
    - Image URI ta cần nhập chính xác URI cùng với tag của image. Bạn cũng có thể truy cập ECR -> Repository cần lấy -> Copy URI với image có tag ta cần lấy.
    - Mở port cho container, trong code mình có mở cổng 3005 nên mìnhh sẽ để cổng 3005
    - Ở phần giới hạn tài nguyên, mình sẽ để theo mặc định. Các bạn có thể chỉnh theo nhu cầu với cpu và giới hạn max, min cho RAM
    - Cài đặt biến môi trường cho container mình khuyến khích sử dụng Secrets manager hơn. 
    - Chọn create để hoàn tất thiết lập
    ![taskdf](/images/ECS/taskdf/3.png)
4. Sau khi thiết lập sẽ hiển thị chi tiết task definition với trạng thái active là đã hoàn thành và chuyển sang bước tiếp theo.
    ![taskdf](/images/ECS/taskdf/4.png)
