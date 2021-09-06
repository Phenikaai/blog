---
layout: post
title: Chuỗi hướng dẫn về NVIDIA NGC
subtitle: Chạy Docker Container sử dụng Nvidia-Container-Toolkit trên Ubuntu
date:       2021-09-1
author:     "Mai Xuan Trang"
background: '/img/posts/nvidia-ngc.jpg'
---

Khi đọc báo tôi thường hay phải chạy lại các thí nghiệm (code) của các bài báo đó. Code cung cấp bởi các tác giả thường cũ và không được cập nhật. Tác giả thông thường cũng không viết chi tiết hoặc có rất it thông tin về môi trường họ chạy code. Việc tìm kiếm và cài đặt được các thư viện cho đúng để chạy được code thực sự là một ác mộng. Đặc biệt là khi chạy các mô hình học sâu trên NVIDIA GPU, việc cài đặt đúng phiên bản CUDA, đúng CUDA driver và đúng phiên bản các frameworks (Pytorch, Tensorflow, ...) là công việc tốn rất nhiều thời gian. Chưa kể đến việc cài đặt lại trên môi trường máy chủ lại có thể gây ảnh hưởng đến người khác.

Tôi ghi chú ra đây phương pháp sử dụng Docker và NVIDIA NGC để chạy các docker images phù hợp với yêu cầu của mình cho từng dự án.

Các bước tôi thường thực hiện để sử dụng Docker vàn NVIDIA NGC như sau:

### Bước 1: Cài đặt Docker và nvidia-container-toolkit

Trên Ubuntu terminal chạy lệnh sau đây để cài đặt Docker và nvidia-container-toolkit:

```> sudo apt-get install -y docker.io nvidia-container-toolkit```

Sau khi cài đặt xong bạn có thể kiểm tra docker có chạy đúng hay không bằng cách chạy lệnh:

```> sudo systemctl status docker```

Nếu docker đang chạy lỗi, hoặc không active bạn có thể restart lại docker như sau:

`> sudo systemctl daemon-reload`
`> sudo systemctl restart docker`

### Bước 2: Lấy container từ NVIDIA NGC về

NVIDIA NGC là một private docker registry, bạn muốn tải container từ NGC về trước hết cần tạo tài khoản trên NGC và login vào tài khoản với '`docker login`' như hướng dẫn sau: [NGC User Guide](https://docs.nvidia.com/dgx/ngc-registry-for-dgx-user-guide/index.html).

Sau khi đăng ký tài khoản, và đăng nhập bạn có thể vào [NGC Catalog](https://ngc.nvidia.com/catalog) để tìm hiểu và lựa chọn container phu hợp với yêu cầu của mình.

Sau khi chon được container phù hợp, bạn chạy lệnh sau đây để tải container về:

`> sudo docker pull nvcr.io/nvidia/pytorch:21.08-py3`

Lệnh này sẽ tải về docker một container đã được cài đặt sẵn các thư viện, framework, drivers cần thiết. Ví dụ thông tin môi trường của container trong lệnh trên bạn có thể tìm thấy ở đây: [Pytorch Release 21.08](https://docs.nvidia.com/deeplearning/frameworks/pytorch-release-notes/rel_21-08.html#rel_21-08)

### Bước 3: Chạy docker với interactive mode

Sau khi tải container về rồi, bạn có thể khởi tạo một "interactive session" để chạy và làm việc với container như sau:

```sudo docker run --gpus all -it --rm -v `pwd`/codes:/codes/ nvcr.io/nvidia/pytorch:21.08-py3```

Lệnh này sẽ khởi chạy container và gắn thư mục `codes` ở thư mục hiện tại trên máy của bạn với thư mục `/codes` trên container. (dữ liệu được chia sẽ giữa máy chủ và container).

Chi tiết hơn về các cờ khi chạy lệnh này bạn có thể xem chi tiết hơn trên: [NGC Container](https://ngc.nvidia.com/catalog/containers/nvidia:pytorch)

### That's it: Enjoy running you code on the container

Bạn đã thành công tải và chạy một GPU docker container từ NVIDA NGC. Việc dùng docker này giup bạn giảm nhiều thời gian trong việc tìm kiếm và cài đặt các thư viện, framworks để chạy code.

