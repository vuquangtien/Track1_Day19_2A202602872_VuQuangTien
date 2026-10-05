# Prototype Feedback Note — Bùi Hải Nam (2A202602636)

## Thông tin phiên

| Mục | Ghi nhận |
| --- | --- |
| Tester | Bùi Hải Nam — MSSV 2A202602636 |
| Ngày | 05/10/2026 |
| Bối cảnh kiểm tra | Learner biết thay số trong Gradient Descent nhưng cần hiểu mối liên hệ giữa dấu đạo hàm và hướng cập nhật. |
| Prototype đã kiểm tra | A → B → C, câu transfer và luồng hỏi trợ giảng |
| Facilitator | Vũ Quang Tiến — 2A202602872 |

## Observation theo từng option

### Option A — Tự chẩn đoán

- Tester chọn “Dấu đạo hàm cho biết hàm đang tăng hay giảm” đầu tiên, đọc phần giải thích rồi quay lại danh sách để so sánh với bước “Đi ngược gradient”. Recovery là nút “Đổi bước cần xem lại”.
- Luồng dễ hiểu: danh sách 4 bước kiến thức nền giúp người học biết mình có thể tự chọn phần muốn ôn; thông điệp hệ thống không tự đoán lỗ hổng tạo cảm giác kiểm soát tốt.
- Đã kiểm tra: mỗi bước “Đạo hàm”, “Dấu đạo hàm”, “Đi ngược gradient” và “Learning rate” đều thay đổi đúng tiêu đề và phần giải thích. Lựa chọn của learner hiện được phản hồi rõ ràng.
- Recovery hiện có: có thể quay lại đổi bước hoặc bỏ qua. Đây là cách khôi phục phù hợp khi learner nhận ra mình chọn nhầm chủ đề.
- Điểm cần test thật: người học có tự xác định đúng bước mình thiếu không. A tạo quyền kiểm soát cao, nhưng vẫn đòi hỏi learner gọi đúng tên lỗ hổng.

### Option B — Chẩn đoán cùng AI

- Tester trả lời “Có / Chưa chắc / Một ví dụ trực quan”, đọc evidence có nhắc đến dấu đạo hàm và chọn xem giải thích. Nếu diagnosis không khớp, recovery là “Không đúng, đổi hướng” để sửa câu trả lời.
- Điểm tốt: nêu trước giới hạn “gợi ý một khả năng”, hiển thị độ chắc chắn thấp và có nút “Không đúng, đổi hướng”; đây là các tín hiệu minh bạch hữu ích.
- Đã kiểm tra: kết quả thay đổi theo câu trả lời. Chưa chắc cách tính đạo hàm dẫn tới ôn đạo hàm; chưa hiểu dấu dẫn tới hướng giảm loss; cần ví dụ dẫn tới diễn giải trực quan; chọn ôn nền tảng dẫn tới nhắc lại về độ dốc.
- Bằng chứng hiển thị cũng khớp nhánh chẩn đoán, nên người học có thể kiểm tra AI đã dựa vào thông tin nào. Đây là điểm mạnh hơn A khi learner không gọi tên được lỗ hổng.
- Điểm cần test thật: ba câu hỏi có đủ để tạo cảm giác AI hiểu tình huống không, và người học có dùng “Không đúng, đổi hướng” khi gợi ý không khớp không.

### Option C — AI chủ động phát hiện kẹt

- Tester đọc tín hiệu “dừng 4 phút, sửa 2 lần”, chọn “Xem một hướng hỗ trợ”, sau đó mở preview câu hỏi trợ giảng và hủy thay vì gửi. Recovery gồm “Để sau”, “Đừng nhắc trong bài này” và Hủy preview.
- Điểm tốt: prompt nói rõ các tín hiệu chỉ thuộc phiên hiện tại, không đọc bài khác và không tự gửi trợ giảng. Các lựa chọn “Xem hỗ trợ”, “Để sau”, “Đừng nhắc” và preview trước khi gửi thể hiện quyền kiểm soát tốt.
- Cần làm rõ trong test thật: prototype hiện mở Option C từ màn hình chọn phương án, nên chưa mô phỏng được khoảnh khắc AI tự xuất hiện khi learner thật sự dừng lâu/sửa sai. Người test thật cần đánh giá cả thời điểm prompt xuất hiện có gây ngắt mạch hay không.
- Luồng escalation rõ ràng ở mức prototype: xem bản nháp, sửa nội dung, hủy hoặc gửi. Tuy nhiên trạng thái “Đã gửi” chỉ là màn hình mô phỏng; cần ghi rõ nếu triển khai thật sẽ gửi đến đâu, thời gian phản hồi dự kiến và cách hủy khi chưa được xử lý.

## Kiểm tra chung

- Câu transfer có đáp án và phản hồi đúng: với `f(w) = (w + 2)²`, tại `w₀ = 0` thì `f'(0) = 4 > 0`, nên `w` giảm sau một bước. Câu này kiểm tra được việc hiểu hướng cập nhật, không chỉ nhớ ví dụ ban đầu.
- Đã kiểm tra: khi trở về context bằng Reset hoặc các nút quay lại bài, form B, phản hồi transfer, nội dung nháp gửi trợ giảng và trạng thái tắt nhắc C được đưa về mặc định. Nhãn Reset nay khớp hành vi.
- Cả ba option dùng chung bài toán và câu transfer nên so sánh cơ chế hỗ trợ là khá công bằng.

## So sánh sau khi thử A/B/C

- **Lựa chọn cuối cùng:** Nam chọn **Option C — AI chủ động phát hiện kẹt**.
- **Lý do chọn:** C hỗ trợ đúng lúc learner đang loay hoay, không bắt Nam phải tự gọi tên lỗ hổng như A hoặc trả lời thêm câu hỏi trước như B. Prompt cho biết rõ tín hiệu “dừng 4 phút, sửa 2 lần”, kèm mức chắc chắn thấp, nên Nam hiểu đây là gợi ý thay vì kết luận về năng lực.
- **Trade-off Nam nhận thấy:** A cho quyền chủ động cao nhất nhưng dễ mất thời gian nếu chưa biết mình cần ôn gì. B minh bạch về cách AI đưa ra gợi ý nhưng thêm bước trả lời câu hỏi. C có nguy cơ ngắt mạch học nếu nhắc sai lúc, nhưng các lựa chọn “Để sau”, “Đừng nhắc trong bài này” và preview trước khi gửi trợ giảng giúp Nam vẫn giữ quyền kiểm soát.
- **Pattern/điểm đáng chú ý:** Nam ưu tiên việc được hỗ trợ sớm hơn là tự chẩn đoán hoàn toàn. Nam đọc phần tín hiệu và mức chắc chắn thấp ở C trước khi chọn xem hỗ trợ; điều này làm prompt chủ động bớt cảm giác bị theo dõi hoặc bị AI áp đặt.
- **Điều phiên này không chứng minh:** Việc Nam chọn C không có nghĩa C sẽ phù hợp nhất với mọi learner, prompt chủ động luôn xuất hiện đúng lúc, hoặc C giúp hoàn thành bài nhanh hơn A/B.

## Observation Summary

**Tester/context:** Bùi Hải Nam (2A202602636), learner biết thay số trong Gradient Descent nhưng cần hiểu mối liên hệ giữa dấu đạo hàm và hướng cập nhật.

| Observation | Note |
| --- | --- |
| First action | A: Nam chọn “Dấu đạo hàm…”; B: Nam trả lời `Có / Chưa chắc / Một ví dụ trực quan`; C: Nam đọc tín hiệu “dừng 4 phút, sửa 2 lần” rồi chọn “Xem một hướng hỗ trợ”. |
| Chỗ dừng, do dự hoặc hiểu sai | Không có hành vi do dự hoặc hiểu sai cụ thể được ghi lại trong phiên này. Điểm cần kiểm tra ở tester sau là liệu A có giúp họ tự gọi đúng tên lỗ hổng không. |
| Evidence được đọc hay bỏ qua | Ở B, Nam đọc evidence về dấu đạo hàm. Ở C, Nam đọc tín hiệu và mức chắc chắn thấp trước khi nhận hỗ trợ. A không đưa evidence do AI suy luận. |
| Cách tester sửa hoặc lấy lại control | A: “Đổi bước cần xem lại”; B: có thể dùng “Không đúng, đổi hướng”; C: Nam preview câu hỏi trợ giảng rồi hủy, và thấy “Để sau”/“Đừng nhắc trong bài này”. |
| Option được chọn | **C** |
| Lý do và trade-off | Nam ưu tiên được hỗ trợ sớm, không phải tự gọi tên lỗ hổng hoặc trả lời thêm câu hỏi. Nam chấp nhận rủi ro prompt ngắt mạch vì vẫn có thể để sau, tắt nhắc hoặc hủy escalation. |
| Evidence chống lại kỳ vọng của nhóm | A cho learner quyền chủ động cao nhất, nhưng Nam vẫn chọn C khi C giải thích rõ tín hiệu và mức chắc chắn thấp. Đây là một tín hiệu phản biện cho giả định learner luôn muốn tự khởi động hỗ trợ. |

## Bốn lớp ghi nhận

### OBSERVED

- Nam dùng đủ A → B → C; ở A, Nam chọn bước về dấu đạo hàm và sau đó quay lại đổi bước.
- Ở B, Nam trả lời ba câu, đọc evidence và xem giải thích.
- Ở C, Nam đọc tín hiệu phiên hiện tại, chọn xem hỗ trợ, preview câu hỏi trợ giảng rồi hủy.
- Sau khi thử cả ba, Nam chọn C và nêu khả năng trì hoãn/tắt nhắc/hủy escalation giúp giữ quyền kiểm soát.

### INTERPRETED

Nam có thể ưu tiên được hỗ trợ sớm khi AI nói rõ mình dựa vào tín hiệu nào và không khẳng định chắc chắn. Điều này chưa cho thấy learner khác sẽ chấp nhận prompt chủ động hay AI có thể phát hiện kẹt đúng trong tình huống thực tế.

### DECIDED — NEXT CHANGE

1. Giữ mechanism chính của C cho tester tiếp theo, nhưng mô phỏng trigger sau một hành vi cụ thể thay vì để tester tự mở C từ menu.
2. Test thêm xem learner có thấy thời điểm prompt C gây ngắt mạch, và liệu họ tự chọn đúng bước ở A hay cần AI đặt câu hỏi như B.
3. Ghi thời gian hoàn thành, câu transfer và lý do chấp nhận/từ chối prompt trước khi chọn hướng phát triển tiếp.

### STILL UNPROVEN

- Không thể kết luận C sẽ phù hợp nhất với learner khác hoặc prompt chủ động luôn xuất hiện đúng lúc.
- Không chứng minh learner hoàn thành bài nhanh hơn, hiểu sâu hơn hoặc chuyển được sang dạng bài khác.
- Không xác thực AI có thể suy luận đúng lỗ hổng kiến thức trong tình huống thực tế.
