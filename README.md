# postman-api-testing
# BÁO CÁO BÀI TẬP: TÌM HIỂU VÀ THỰC HÀNH CÔNG CỤ POSTMAN

## 1. Thông tin sinh viên
- **Họ và tên:** Dương Thiện Hùng  
- **Mã sinh viên:** 23010601
- **Lớp:** K17-CNTTVJ
- **Môn học:** Đánh giá kiểm định
---

## 2. Tổng quan về công cụ Postman
Qua việc học tập từ video hướng dẫn và tài liệu mở rộng, em đã nắm được các kiến thức cốt lõi về Postman:
- **Postman là gì:** Là một trong những API Client phổ biến nhất thế giới, hỗ trợ đắc lực cho Developer và QA trong việc gửi request, kiểm thử, quản lý và tự động hóa quy trình test API.
- **Các thành phần cơ bản:** Phương thức HTTP (GET, POST, PUT, DELETE), Base URL, Endpoint, Query Parameters, Headers và Body dữ liệu (thường dùng định dạng JSON).
- **Kiểm thử tự động (Automation Testing):** Postman hỗ trợ viết mã kiểm thử bằng ngôn ngữ JavaScript trong tab *Tests* kết hợp với *Collection Runner* để chạy kiểm thử hàng loạt nhanh chóng.

---

## 3. Kết quả thực hành chi tiết

### Thao tác 3.1: Gửi Request GET và phân tích phản hồi
- **API sử dụng:** `https://random-data-api.com/api/v2/users` (API lấy thông tin người dùng ngẫu nhiên).
- **Kết quả:** Request gửi đi thành công, máy chủ phản hồi mã trạng thái `200 OK` và trả về body dạng JSON chứa dữ liệu chi tiết của user (id, password, first_name, last_name,...).

*Hình minh họa gửi Request GET thành công:*
![Gửi Request GET](./anh1_get_request.png)

### Thao tác 3.2: Viết mã khẳng định (Assertion) tự động
Em đã sử dụng các đoạn mã mẫu (Snippets) JavaScript của Postman để cấu hình kiểm tra tự động 2 điều kiện:
1. Xác thực mã trạng thái phản hồi phải bằng `200`.
2. Xác thực thời gian phản hồi (Response time) phải nhỏ hơn `200ms`.

*Hình minh họa mã script và kết quả Test Results (PASS):*
![Viết Test Script](./anh2_test_script.png)

### Thao tác 3.3: Chạy kiểm thử tự động hàng loạt với Collection Runner
Để đảm bảo API hoạt động ổn định khi chạy lặp lại, em sử dụng tính năng Collection Runner của Postman để thực thi tự động toàn bộ kịch bản test.

*Hình minh họa kết quả chạy bằng Runner:*
![Kết quả Runner](./anh3_runner_results.png)
