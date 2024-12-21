# GitHub Flow

GitHub Flow là một quy trình làm việc được thiết kế để phù hợp với Git và GitHub. Nó tập trung vào việc sử dụng nhánh (branch) giúp nhóm làm việc có thể thử nghiệm tự do và triển khai thường xuyên. Quy trình GitHub Flow bao gồm các bước sau:

1. Tạo một nhánh mới
Nhánh (branch) là một khái niệm cốt lõi trong Git. Quy tắc quan trọng nhất là nhánh chính (master/main) luôn sẵn sàng để triển khai.

Khi muốn thử nghiệm hoặc thay đổi, hãy tạo một nhánh mới để đảm bảo bạn không ảnh hưởng đến nhánh chính.

Sau khi hoàn thành nhánh mới, bạn có thể:
Được xem xét (review).
Thảo luận.
Hợp nhất (merge) với nhánh chính khi sẵn sàng.
Lưu ý:

Khi tạo nhánh mới, hầu như luôn bắt đầu từ nhánh chính.
Đặt tên nhánh có ý nghĩa, để đồng đội dễ hiểu nội dung và mục đích.
2. Thực hiện thay đổi và thêm Commit
Sau khi tạo nhánh mới, bạn có thể thực hiện thay đổi: thêm, chỉnh sửa, hoặc xóa file.

Khi đạt được mốc nhỏ (milestone), hãy commit thay đổi để lưu lại.

Commit giúp ghi lại quá trình làm việc.
Mỗi commit cần có thông điệp rõ ràng để giải thích:
Đã thay đổi gì?
Lý do thay đổi.
Lưu ý: Commit thông minh sẽ giúp bạn và nhóm dễ dàng theo dõi và hiểu các thay đổi.

3. Tạo Pull Request
Pull Request (PR) là một phần quan trọng trong GitHub. PR thông báo rằng bạn đã sẵn sàng để người khác xem xét hoặc tích hợp thay đổi của bạn.

Bạn có thể yêu cầu đồng đội xem xét thay đổi hoặc tích hợp vào nhánh của họ.
4. Review (Xem xét và đánh giá)
Khi một Pull Request được tạo, nhóm có thể xem xét thay đổi:

Thảo luận về các cải tiến.
Đánh giá mã nguồn (code review).
Nếu nhận được phản hồi, bạn có thể thực hiện thay đổi và tiếp tục commit. GitHub sẽ tự động hiển thị các commit mới trong Pull Request để tiếp tục đánh giá.

5. Deploy (Triển khai thử nghiệm)
Khi Pull Request được xem xét và mọi thứ đều ổn, đã đến lúc kiểm tra cuối cùng.

GitHub cho phép bạn triển khai từ nhánh để kiểm tra trong môi trường sản xuất.
Nếu có vấn đề, bạn có thể triển khai lại nhánh chính để hoàn nguyên.
Lưu ý: Các nhóm thường có môi trường thử nghiệm riêng để triển khai các nhánh.

6. Merge (Hợp nhất)
Sau khi kiểm tra kỹ lưỡng, bạn có thể merge nhánh vào nhánh chính.

Pull Request sẽ lưu lại lịch sử thay đổi, giúp dễ dàng hiểu tại sao các quyết định được đưa ra.
Lưu ý: Hãy sử dụng từ khóa trong Pull Request để tìm kiếm dễ dàng hơn sau này.

