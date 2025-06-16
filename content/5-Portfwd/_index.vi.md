+++
title = "Thiết lập CodePipeline"
date = 2020
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

Chúng ta sẽ cấu hình **Code Pipeline** để tự động hóa quá trình deploy container với trigger là git push.

#### Tạo CodePipeline

1. Truy cập vào **Code Pipeline**
  ![cluster](/images/Codepl/1.png)
2. Chọn Pipeline -> Create Pipeline
  ![cluster](/images/Codepl/2.png)
  - Chọn build custom pipeline -> next
  ![cluster](/images/Codepl/3.png)
  - Nhập tên pipeline, mình sẽ chọn tạo role mới luôn rồi chọn next
  ![cluster](/images/Codepl/4.png)
  - Tới phần Source mình chọn github -> chọn connection -> tên repo -> nhánh. Chọn Webhook để có thể trigger pipeline thông qua lệnh push
  {{% notice info %}}Nếu bạn chưa thiết lập kết nối thì có thể tham khảo [đây](URL "https://docs.aws.amazon.com/dtconsole/latest/userguide/connections-create-github.html#connections-create-github-console"){{% /notice %}}
  ![cluster](/images/Codepl/5.png)
  - Tới phần build mình chọn Other build providers -> AWS Codebuild -> chọn project đã tạo ở trang 3 và next
  ![cluster](/images/Codepl/6.png)
  - Phần test mình sẽ bỏ qua
  ![cluster](/images/Codepl/7.png)
  - Phần deploy mình chọn ECS -> Chọn cluster -> Service -> Next
  ![cluster](/images/Codepl/8.png)
  - Xem lại rồi chọn Create pipeline
  ![cluster](/images/Codepl/9.png)
1. Sau khi tạo xong pipeline sẽ chạy và trả về kết quả thành công.
  ![cluster](/images/Codepl/10.png)

#### Khởi chạy pipeline
- Thực hiện lệnh git push hoặc chọn release change để khởi chạy pipeline.

Chúc mừng bạn đã hoàn tất bài thực hành hướng tạo pipeline CI/CD. Hãy nhớ thực hiện bước dọn dẹp tài nguyên để tránh sinh chi phí ngoài ý muốn nhé.