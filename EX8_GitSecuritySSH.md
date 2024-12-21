## Git Security SSH

### Sử dụng HTTPS

Cho tới điểm này, chúng ta đã sử dụng HTTPS để kết nối với kho động tác từ xa.

HTTPS thường hoạt động tốt, nhưng bạn nên sử dụng SSH nếu làm việc với mạng không an toàn.

Ngoài ra, một số dự án có thể yêu cầu bạn sử dụng SSH.

---

### SSH là gì?

SSH là một giao thức mạng vỏ bọc bảo mật được sử dụng cho quản lý mạng, chuyển tệp từ xa, và truy cập hệ thống từ xa.

SSH sử dụng cặp khóa SSH để thiết lập giao thức mạng bảo mật đã được xác thực và mã hóa.

Nó cho phép truyền thông an toàn trên các mạng mở không an toàn.

#### Cách hoạt động của SSH:

SSH keys được sử dụng để khởi tạo "bát tay" bảo mật. Khi tạo cặp khóa, bạn sẽ tạo:

- **Khóa công khai (public key):** Chia sẻ với bên từ xa (giống như ổ khoá).
- **Khóa riêng (private key):** Bảo mật và chỉ bạn biết (giống như chìa khoá).

Khóa công khai có thể được suy ra từ khóa riêng, nhưng ngược lại thì không thể.

---

### Tạo Cặp SSH Key

Trên dòng lệnh cho Linux, MacOS hoặc Git Bash trên Windows, bạn có thể tạo khóa SSH.

#### Các bước thực hiện:

1. Tạo khóa mới, sử dụng email làm nhãn:

   ```bash
   ssh-keygen -t rsa -b 4096 -C "test@w3schools.com"
   ```
   
   **Dòng lệnh sẽ xuất ra:**

   ```plaintext
   Generating public/private rsa key pair.
   Enter file in which to save the key (/Users/user/.ssh/id_rsa):
   Created directory '/Users/user/.ssh'.
   Enter passphrase (empty for no passphrase):
   Enter same passphrase again:
   Your identification has been saved in /Users/user/.ssh/id_rsa
   Your public key has been saved in /Users/user/.ssh/id_rsa.pub
   The key fingerprint is:
   SHA256:******************************************* test@w3schools.com
   The key's randomart image is:
   +---[RSA 4096]----+
   |                 |
   |                 |
   |                 |
   |                 |
   |                 |
   |                 |
   |                 |
   |                 |
   |                 |
   +----[SHA256]-----+
   ```

2. Nhập file để lưu khóa (hoặc nhấn `Enter` để sử dụng vị trí mặc định).

3. **Nhập passphrase:**
   - Nhập mật khẩu bảo vệ (để tăng cường bảo mật).
   - Passphrase sẽ phục vụ ngăn ai đó sử dụng khóa nếu họ truy cập vào máy tính.

4. Thêm cặp SSH Key vào SSH-Agent:

   ```bash
   ssh-add /Users/user/.ssh/id_rsa
   ```

   **Dòng lệnh sẽ hiển thị:**

   ```plaintext
   Enter passphrase for /Users/user/.ssh/id_rsa:
   Identity added: /Users/user/.ssh/id_rsa (test@w3schools.com)
   ```

Bây giờ cặp khóa SSH sẽ sẵn sàng để sử dụng.

