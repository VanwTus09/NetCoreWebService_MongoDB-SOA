# Tổng Quan

Dự án này triển khai một API sử dụng ASP.NET Core để quản lý danh sách công việc cần làm (To-Do Items), kết nối với cơ sở dữ liệu. Dưới đây là các chức năng và mô tả kết quả đạt được:

## 1. Khởi tạo và cấu hình dự án
- `Program.cs` cấu hình các dịch vụ và pipeline cho ứng dụng.
- Kết nối cơ sở dữ liệu thông qua `DatabaseSettings` từ `appsettings.json`.
- Swagger được cấu hình giúp kiểm tra và thử nghiệm API dễ dàng.

## 2. Dịch vụ ToDoService
- `ToDoService.cs` là lớp chứa các phương thức để tương tác với cơ sở dữ liệu.
- Các phương thức chính bao gồm:
  - `GetAsync()`: Trả về danh sách tất cả công việc.
  - `GetAsync(string id)`: Trả về công việc theo `id`.
  - `CreateAsync(ToDoItem newItem)`: Thêm một công việc mới vào cơ sở dữ liệu.
  - `UpdateAsync(string id, ToDoItem updatedItem)`: Cập nhật thông tin một công việc.
  - `RemoveAsync(string id)`: Xóa một công việc theo `id`.

## 3. Controller
- `ToDoController.cs` cung cấp các endpoint cho API để quản lý công việc, bao gồm các phương thức HTTP:

| HTTP Method | Endpoint            | Mô tả                                    |
|------------|--------------------|------------------------------------------|
| GET        | /todoitems         | Lấy danh sách tất cả công việc.         |
| GET        | /todoitems/{id}     | Lấy thông tin chi tiết một công việc.   |
| GET        | /todoitems/complete | Lấy danh sách công việc đã hoàn thành.  |
| POST       | /todoitems         | Thêm một công việc mới.                 |
| PUT        | /todoitems/{id}     | Cập nhật thông tin một công việc.       |
| DELETE     | /todoitems/{id}     | Xóa một công việc khỏi danh sách.       |
![swagger](https://github.com/user-attachments/assets/f0890c7c-dc03-4d4b-8eca-844e75b6c3e4)


## 4. Hướng dẫn sử dụng
1. Chạy ứng dụng trên `https://localhost:7186`.
2. Sử dụng công cụ như Postman, Insomnia hoặc REST Client trong VS Code để gửi request đến API.
3. Kiểm tra kết quả trả về để xác nhận chức năng hoạt động đúng như mong đợi.
## 5. Kết quả
![getapis](https://github.com/user-attachments/assets/665d5bf7-3cda-49f5-9281-cdb5c8ac64da)
dữ liệu 
![mongodb](https://github.com/user-attachments/assets/0eee9afc-7d0d-4ca5-8703-a4d830730ceb)


