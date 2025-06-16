+++
title = "Thiết lập CodeBuild"
date = 2020
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

Phần này, bạn sẽ thiết lập Codebuild để khởi chạy dockerfile và lưu trữ chúng trên ECR

{{% notice info %}}
Bạn sẽ cần phải bổ sung thêm buildspec.yaml để codebuild hoạt động theo ý muốn.  [File buildspec tham khảo](https://github.com/Hieu1812/book-server/blob/main/buildspec.yml)
{{% /notice %}}

### Tạo Codebuild

1. Truy cập **Codebuild**
![Codebuild](/images/Codebuild/1.png)
2. Chọn Create project
![Codebuild](/images/Codebuild/2.png)
3. Nhập tên dự án, loại dự án mình chọn default.
4. Ở mục Source: Codebuild sẽ được kích hoạt thông qua lệnh push repo của github nên mình sẽ chọn thẳng source từ github của mình.
![Codebuild](/images/Codebuild/3.png)
![Codebuild](/images/Codebuild/4.png)
5. Với các thông số môi trường (evironment) mình sẽ để mặc định. Sau đó chọn tạo service role mới và chọn sử dụng file buildspec.yml.
![Codebuild](/images/Codebuild/5.png)
6. Mục Artifact sẽ chọn no artifacts và điền group name nhằm dễ quản lý logs. Sau đó Create build project
![Codebuild](/images/Codebuild/6.png)
Lúc này việc thiết lập Codebuild hoàn tất nhưng ta cần cấp quyền cho service role vừa tạo để codebuild có quyền push image lên ECR
7. Truy cập service role ở ngay trang chi tiết Codebuild
8. Ở trang chi tiết role, chọn Add permissions -> Attach policies
![Codebuild](/images/Codebuild/8.png)
9. Thực hiện tìm kiếm EC2Container, ở đây mình sẽ lựa chọn quyền hạn phù hợp cho role này là PowerUser. Sau đó chọn Add permissions.
![Codebuild](/images/Codebuild/9.png)
10. Codebuild đã có thể hoạt động, bạn có thể kích hoạt thông qua git push hoặc chọn start build
![Codebuild](/images/Codebuild/10.png)
![Codebuild](/images/Codebuild/11.png)