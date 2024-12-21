## Git Ignore

Khi chia sẻ mã nguồn với người khác, thường có những tệp hoặc phần của dự án mà bạn không muốn chia sẻ.

### Ví dụ

- Tệp nhật ký (log files)
- Tệp tạm thời (temporary files)
- Tệp ẩn (hidden files)
- Tệp cá nhân (personal files)
- v.v.

Git có thể chỉ định các tệp hoặc phần nào của dự án nên bị bỏ qua bằng cách sử dụng tệp `.gitignore`.

Git sẽ không theo dõi các tệp và thư mục được chỉ định trong `.gitignore`. Tuy nhiên, bản thân tệp `.gitignore` vẫn được Git theo dõi.

---

### Tạo tệp .gitignore

Để tạo tệp `.gitignore`, đi đến thư mục gốc của kho Git cục bộ và tạo tệp này:

```bash
touch .gitignore
```

Sau đó mở tệp bằng một trình soạn thảo văn bản.

#### Ví dụ:
Chúng ta sẽ thêm hai quy tắc đơn giản:

1. Bỏ qua bất kỳ tệp nào có phần mở rộng `.log`.
2. Bỏ qua mọi thứ trong bất kỳ thư mục nào có tên là `temp`.

**Nội dung của `.gitignore`:**

```plaintext
# Bỏ qua tất cả các tệp .log
*.log

# Bỏ qua tất cả các tệp trong bất kỳ thư mục nào có tên temp
temp/
```

Bây giờ tất cả các tệp `.log` và bất kỳ thứ gì trong các thư mục `temp` sẽ bị Git bỏ qua.

> **Lưu ý:** Trong trường hợp này, chúng ta sử dụng một tệp `.gitignore` áp dụng cho toàn bộ kho. 
> Cũng có thể có thêm các tệp `.gitignore` trong các thư mục con, chúng chỉ áp dụng cho các tệp hoặc thư mục trong thư mục đó.

---

### Quy tắc cho .gitignore

Quy tắc cho .gitignore

Dưới đây là các quy tắc chung cho việc khớp mẫu trong các tệp .gitignore:

Dòng trống: Các dòng trống bị bỏ qua.

Dòng bắt đầu bằng #: Đây là các dòng chú thích và bị bỏ qua.

name: Khớp với tất cả các tệp và thư mục có tên name.

Ví dụ: /name.log, /lib/name.log

name/: Khớp với tất cả các tệp và thư mục trong bất kỳ thư mục nào có tên name.

Ví dụ: /name/file.txt, /name/log/name.log

*.file: Khớp với tất cả các tệp có phần mở rộng .file.

Ví dụ: /name.file, /lib/name.file

name?.file: ? khớp với một ký tự bất kỳ.

Ví dụ: /name1.file, /namea.file

name[a-z].file: [range] khớp với một ký tự trong phạm vi được chỉ định (ví dụ: a-z).

Ví dụ: /namea.file, /nameb.file

name[!abc].file: [!set] khớp với một ký tự ngoại trừ các ký tự được chỉ định trong tập hợp (ví dụ: a, b, c).

Ví dụ: /names.file, /namex.file

!name/*.file: ! chỉ định một ngoại lệ.

Ví dụ: Khớp với tất cả các tệp .file trừ những tệp trong thư mục name.

**/name: Khớp với tất cả các thư mục name, và các tệp/thư mục trong bất kỳ thư mục nào tên name.

Ví dụ: /name/log.file, /lib/name/log.file

!name/secret.log: Khớp với mọi thứ trong thư mục name trừ name/secret.log.

Ví dụ: /name/file.txt, nhưng KHÔNG khớp /name/secret.log.

### Quy tắc bỏ qua tệp cục bộ và cá nhân

Cũng có thể bỏ qua các tệp hoặc thư mục mà không hiển thị trong tệp `.gitignore` được phân phối.

Loại bỏ qua này được chỉ định trong tệp `.git/info/exclude`. Nó hoạt động giống như `.gitignore` nhưng không được hiển thị cho người khác.

---

### Kiểm tra bản thân với bài tập

**Bài tập:**

Trong tệp `.gitignore`, thêm một dòng để bỏ qua tất cả các tệp `.temp`:

**Giải pháp:**

```plaintext
# Bỏ qua tất cả các tệp .temp
*.temp
```

