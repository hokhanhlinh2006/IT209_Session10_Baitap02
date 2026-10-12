
# Bài 2: Đóng gói Web Backend bằng Single-stage Dockerfile

## 1. Thông tin sinh viên
- Họ và tên: Hồ Khánh Linh
- Mã sinh viên: B24DTCN359
- Lớp: CNTT3

## 2. Mục tiêu
Xây dựng REST API bằng Node.js và Express, sau đó đóng gói ứng dụng thành Docker Image bằng Single-stage Dockerfile.

## 3. Cấu trúc thư mục
- Dockerfile: Cấu hình build Docker Image.
- package.json: Khai báo thư viện Express.
- server.js: Mã nguồn REST API.
- README.md: Hướng dẫn thực hiện bài tập.

## 4. Dockerfile
Dockerfile sử dụng image nền node:18-alpine và các chỉ thị:
- FROM: Chọn image nền.
- WORKDIR: Thiết lập thư mục /app.
- COPY: Sao chép file ứng dụng.
- RUN: Cài đặt thư viện.
- ENV: Thiết lập PORT=3000.
- EXPOSE: Khai báo cổng 3000.
- CMD: Chạy node server.js bằng exec form.

## 5. Build và chạy ứng dụng

Build image:

```bash
docker build -t hw-backend:v1 .
<img width="1186" height="416" alt="ex2_ss10" src="https://github.com/user-attachments/assets/6e9aefba-7563-4d95-962c-a7c0ac6c71d3" />
