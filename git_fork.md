# GIT FORK 
[text](https://github.com/khanhvo1592/w3schools-test.github.io.git)

1. Fork một Repository
Fork là cách để tạo bản sao của một repository vào tài khoản GitHub của bạn. Điều này rất hữu ích khi bạn muốn:

Đóng góp vào dự án của người khác.
Bắt đầu một dự án dựa trên mã nguồn của họ.
Thực hiện Fork trên GitHub:
Đăng nhập vào GitHub.

Tìm repository mà bạn muốn fork, ví dụ:
https://github.com/w3schools-test/w3schools-test.github.io.

Nhấn nút "Fork" (ở góc trên bên phải).

Sau khi fork, bạn sẽ có một bản sao của repository trong tài khoản của mình.

2. Tạo một bản sao cục bộ của repository (Clone)
Sau khi fork xong, bạn cần sao chép repository đó về máy tính để làm việc:

Mở terminal (hoặc giao diện dòng lệnh Git).

Clone repository vừa fork:
Lấy URL của repository từ trang GitHub của bạn và chạy lệnh sau:

bash
Sao chép mã
git clone https://github.com/your-username/w3schools-test.github.io.git
(Thay your-username bằng tên tài khoản GitHub của bạn.)

Đi vào thư mục dự án vừa clone:

bash
Sao chép mã
cd w3schools-test.github.io
3. Chỉnh sửa và Commit thay đổi
Thực hiện thay đổi:
Chỉnh sửa file hoặc thêm file mới trong dự án.

Thêm thay đổi vào staging area:

bash
Sao chép mã
git add <ten_file>
Hoặc thêm tất cả thay đổi:

bash
Sao chép mã
git add .
Commit thay đổi:

bash
Sao chép mã
git commit -m "Mô tả ngắn gọn thay đổi"
4. Đẩy thay đổi lên GitHub
Push nhánh lên repository fork của bạn:

bash
Sao chép mã
git push origin main
Kiểm tra lại trên GitHub:
Repository của bạn trên GitHub sẽ được cập nhật với thay đổi mới.

5. Gửi Pull Request để đóng góp
Quay lại trang repository gốc:
https://github.com/w3schools-test/w3schools-test.github.io
Nhấn nút "Compare & pull request".
Thêm mô tả chi tiết về thay đổi bạn muốn đóng góp.
Gửi Pull Request (PR).
Làm việc với Fork giúp bạn:
Dễ dàng đóng góp vào các dự án mã nguồn mở.
Bảo toàn nhánh chính của repository gốc.
Quản lý các thay đổi trong repository của riêng bạn trước khi đóng góp.