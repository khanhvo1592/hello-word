# Clone repository
**Mục tiêu**
Clone repository từ URL https://abc.com/x/y.git về máy cục bộ và kiểm tra trạng thái của repository sau khi clone.

Hướng dẫn chi tiết
Mở terminal hoặc Git Bash.

Clone repository về máy cục bộ.
Sử dụng lệnh sau để clone repository:

`git clone https://abc.com/x/y.git`

Kết quả: Repository sẽ được tải về trong thư mục hiện tại với tên thư mục mặc định là y.

Xác nhận repository đã được clone.
Dùng lệnh ls để kiểm tra:

bash
Sao chép mã
ls
Kết quả: Bạn sẽ thấy một thư mục mới tên là y.

Chuyển vào thư mục mới:

bash
Sao chép mã
cd y
Kiểm tra trạng thái repository:

bash
Sao chép mã
git status
Kết quả: Bạn sẽ thấy thông báo như sau:

vbnet
Sao chép mã
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
Xem lịch sử commit:

bash
Sao chép mã
git log
Kết quả: Danh sách các commit trước đó sẽ hiển thị, xác nhận rằng bạn có đầy đủ dữ liệu của repository.

Tùy chọn nâng cao
Nếu bạn muốn clone vào một thư mục cụ thể, sử dụng lệnh sau:
bash
Sao chép mã
git clone https://abc.com/x/y.git <ten_thu_muc>
Ví dụ:

bash
Sao chép mã
git clone https://abc.com/x/y.git my-folder
