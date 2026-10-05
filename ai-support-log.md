# AI Support Log — Vũ Quang Tiến

> Rà lại và chỉnh phần reflection này bằng trải nghiệm làm bài của chính bạn trước khi nộp.

| Hạng mục | AI đã hỗ trợ | Tôi đã kiểm tra/sửa gì |
| --- | --- | --- |
| Tổng hợp Day 17 | Sắp xếp ba Practice Notes thành Evidence Snapshot và tách fact khỏi diễn giải. | Giữ giới hạn evidence: không coi practice interview là validation; không dùng quote chưa được notes ghi nhận. |
| Thiết kế A/B/C | Chuyển Parking Lot thành ba cơ chế khác nhau và soạn Comparison Contract. | Dùng hướng Option C do nhóm phân công; kiểm tra A/B/C khác nhau ở agency/mechanism, không chỉ UI. |
| Human–AI Design | Gợi ý expectation, uncertainty, recovery và chính sách dữ liệu phiên cho từng option. | Điều chỉnh Option C: AI chỉ hỏi trước khi hỗ trợ, không tự ngắt bài hay tự gửi coach. |
| Prototype | Tạo HTML/CSS/JavaScript với canned output cho common context và A/B/C. | Kiểm tra flow reset, đường từ chối/hủy và nội dung fixture; không dùng model/API thật. |
| Chuẩn bị test | Soạn context question, outcome task, observation focus và template feedback. | Không dùng AI tạo observation, quote, feedback note hoặc reflection từ tester. |
| Sau phiên test | Sắp xếp Feedback Note theo các lớp Observed, Interpreted, Next Change và Still Unproven. | Chỉ dùng hành vi, lựa chọn và trade-off do tester/facilitator đã ghi; không để AI tạo thêm quote hoặc preference. |

## Chỗ AI có thể hời hợt/sai và cách tôi xử lý

- AI có thể suy luận quá mạnh từ ba notes. Tôi giữ mục “Still Unproven” và không viết solution đã được xác thực.
- AI có thể làm Option C thành một prompt gây gián đoạn. Tôi thêm “Để sau”, “Đừng nhắc trong bài này”, tắt phát hiện chủ động và quay lại bài.
- AI không có mặt trong buổi test. Tôi tự ghi hành vi và lựa chọn thực tế của tester vào Feedback Note; chỉ tổng hợp cùng nhóm sau khi có đủ ba phiên.

## Reflection sau test của tôi

Điểm AI hỗ trợ hữu ích:
Cung cấp khung quan sát và cấu trúc bóc tách phản hồi (Observed vs. Interpreted) rất rõ ràng, giúp tôi tập trung ghi nhận hành vi thao tác của tester thay vì vội vàng suy diễn cảm xúc của họ trong lúc dẫn test.
Bộ canned output chuẩn bị sẵn giúp phiên test diễn ra trơn tru, ổn định, giúp tester tương tác đúng ngữ cảnh mà không bị phân tâm bởi độ trễ hay lỗi phản hồi ngẫu nhiên từ mô hình thật.

Điểm AI gợi ý không khớp với thực tế:
AI giả định người dùng hoặc sẽ nhận toàn bộ trợ giúp hoặc bấm bỏ qua ngay lập tức. Thực tế thao tác của Nam diễn ra nhiều tầng hơn: bạn ấy đọc tín hiệu can thiệp, chủ động chọn xem hỗ trợ, mở phần preview câu hỏi gửi trợ giảng nhưng sau khi cân nhắc lại quyết định bấm hủy để tự làm tiếp.
Gợi ý ban đầu của AI về việc hiển thị lý do can thiệp còn dài dòng, khiến luồng thao tác preview trước khi xác nhận gửi trợ giúp chưa đủ gọn gàng.

Tôi đã xử lý và đề xuất chỉnh sửa:
Trong buổi test: Tôi giữ im lặng quan sát toàn bộ chuỗi hành động và chuỗi thao tác của Nam khi mở preview rồi bấm hủy, chỉ ghi nhận thao tác thực tế chứ không mớm ý hay giải thích thay cho giao diện.
Đề xuất thay đổi cho bản tiếp theo: Rút gọn tối đa thông điệp can thiệp thành dạng vi mô (micro-copy) súc tích, tối ưu lại màn hình preview câu hỏi trợ giảng để người dùng nắm nhanh nội dung trước khi quyết định gửi hay hủy, đồng thời tôn trọng quyền kiểm soát của người học khi họ muốn quay lại tự xử lý bài làm.
