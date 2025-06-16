+++
title = "Thiết lập và đẩy image lên ECR"
date = 2020
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

Ở phần này, bạn sẽ tạo một private repository nhằm lưu trữ image file của phần mềm
### Tạo ECR
1. Truy cập vào **ECR**.
![ECR](/images/ECR/1.png)
2. Ở thanh điều hướng bên trái, chọn **Private repositories**.
3. Chọn  **Create repositories**.
![ECR](/images/ECR/2.png)
4. Nhập tên repositories. Khuyến khích cùng tên với tag đã đặt lúc build docker để dễ quản lý hơn :v,  chọn create để tạo.
5. Nếu bạn chưa từng sử dụng AWS CLI thì từ bước này sẽ hướng dẫn cài đặt và tạo IAM user cho CLI.
   1. Thực hiện tải AWS CLI ở link sau [AWS CLI]( https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) và cài đặt như thông thường
   2. Thực hiện tạo user để đăng nhập vào CLI, trong phạm vi workshop này, mình chỉ thêm quyền cơ bản để có thể push image lên ECR. Truy cập **IAM**
    ![ECR](/images/ECR/6.png)
   3. Chọn User => create user
    ![ECR](/images/ECR/7.png)
   4. Nhập tên user.
    ![ECR](/images/ECR/8.png)
   5.  Chọn Attach policies directly => tìm kiếm và chọn **AmazonEC2ContainerRegistryPowerUser** => next
    ![ECR](/images/ECR/9.png)
   6.  Chọn create. Tài khoản mới sẽ được tạo ngay lập tức, truy cập tới chi tiết tài khoản => create access key.
    ![ECR](/images/ECR/10.png)
   7.  Chúng ta sẽ sử dụng trong phạm vi CLI nên sẽ chọn CLI => tick đồng ý => next
    ![ECR](/images/ECR/11.png)
   8.  Mình sẽ bỏ qua bước này để tạo luôn access key
    ![ECR](/images/ECR/12.png)
   9.  Access key đã được tạo thành công, nên tải về dưới dạng csv để có thể xem lại dễ hơn vì nó chỉ được xem, tải một lần duy nhất.
    ![ECR](/images/ECR/13.png)
   10. Sau đó ta truy cập vào cmd gõ ```aws configure``` và đăng nhập bằng key đã tải ở bước trước cùng với region.
6.  Lúc này ta đã có thể sử dụng dụng các câu lệnh có sẵn của AWS trên IDE
![ECR](/images/ECR/4.png) 
1.  Sau khi đã thực hiện các bước có sẵn, image được build sẽ xuất hiện trên ECR
![ECR](/images/ECR/5.png)