# Three-Option Design Sheet

> Case A — AI Tutor: Diagnostic Refresher. Xuất phát từ Hypothesis Problem đã chốt trong [README.md](README.md#2-chốt-hypothesis-problem).

## 1. Mở lại Solution Parking Lot

|#|Hướng đã park / bổ sung|Cơ chế|Nguồn|
|---|---|---|---|
|1|Nút "Tôi vẫn chưa hiểu" → hệ thống hỏi ngắn để chẩn đoán → chọn nội dung nền → giải thích → đưa learner trở lại bài|User + AI co-create (AI chẩn đoán, user xác nhận)|Directive Case A|
|2|Đưa ví dụ/cách diễn giải khác thay vì ôn kiến thức nền|AI tạo nội dung, user chọn|Giả thuyết cạnh tranh B|
|3|Bổ sung bước kiểm tra "đã hiểu thật chưa" bằng bài dạng khác|Kiểm tra transfer|I01: "không chắc mình hiểu thật hay chỉ hiểu đúng ví dụ"|
|4 *(bổ sung)*|Learner tự đánh dấu bước mình chưa hiểu trên chuỗi kiến thức soạn sẵn, không có AI suy luận|User-led / no-inference|Bổ sung vì pool thiếu hướng user-led|
|5 *(bổ sung)*|AI chủ động phát hiện learner bị kẹt từ bài làm, đề xuất chỗ hổng; chuyển cho trợ giảng khi AI không chắc|AI initiates, user reviews + human escalation|Bổ sung vì pool thiếu hướng AI-initiated và human escalation|

**Lý do bổ sung:** Hướng 1–3 đều cùng cơ chế "user báo kẹt → AI giải thích", chỉ khác nội dung giải thích. Nhóm thêm hướng 4 (user-led, không suy luận) và hướng 5 (AI chủ động + human escalation) để có ba cơ chế thực sự khác nhau cho cùng một task. Hướng 3 không thành option riêng mà được dùng làm bước kết thúc chung, vì nó đo desired outcome.

## 2. Chọn ba cách giải

**Những thứ phải giữ nguyên:**

|Thành phần|Quyết định chung cho A/B/C|
|---|---|
|**Target User**|Learner đang tự làm bài tập môn kỹ thuật, đã có slide/bài giảng nhưng bị kẹt ở một khái niệm|
|**Situation**|Đang làm bài tập, biết áp dụng công thức nhưng không hiểu vì sao công thức đúng nên không làm tiếp được|
|**Task**|Xác định đúng chỗ mình đang hổng và hiểu đủ khái niệm đó để quay lại làm bài|
|**Desired Outcome**|Learner quay lại bài trong ≤ 10 phút (so với 30–45 phút hiện tại) và trả lời đúng một câu kiểm tra ở dạng khác với ví dụ vừa học|
|**Content/data fixture**|Bài gradient descent: *"Cho f(w) = (w − 3)², w₀ = 0, learning rate = 0.1. Tính w₁ và giải thích vì sao cập nhật w = w − lr·f'(w)."* Chuỗi kiến thức nền: (1) đạo hàm là độ dốc → (2) dấu đạo hàm cho biết hướng hàm tăng → (3) đi ngược gradient để giảm loss → (4) learning rate điều chỉnh độ dài bước. Câu kiểm tra transfer: *"Với f(w) = (w + 2)² và w₀ = 0, w sẽ tăng hay giảm sau một bước? Vì sao?"*|

**Những thứ được phép khác:**

|Thành phần|Option A — Tự chẩn đoán theo chuỗi kiến thức|Option B — Hỏi chẩn đoán cùng AI|Option C — AI chủ động phát hiện kẹt|
|---|---|---|---|
|**Solution mechanism**|User-led, no-inference: learner tự đi qua chuỗi 4 bước kiến thức nền soạn sẵn, tự đánh dấu bước chưa hiểu, nhận giải thích soạn sẵn cho bước đó|User + AI co-create: AI hỏi 2–3 câu ngắn để đoán chỗ hổng, learner xác nhận hoặc sửa, AI giải thích đúng phạm vi chỗ hổng đó|AI initiates, user reviews: AI theo dõi bài làm, tự nhận ra learner bị kẹt và đề xuất chỗ hổng + giải thích; learner chấp nhận/bỏ qua; chuyển cho trợ giảng khi AI không chắc|
|**User làm gì?**|Đọc từng bước, tự đánh giá "hiểu/chưa hiểu", chọn bước cần xem lại, làm câu kiểm tra|Báo mình đang kẹt, trả lời câu hỏi chẩn đoán, xác nhận/sửa chẩn đoán của AI, làm câu kiểm tra|Làm bài như bình thường; khi được AI đề xuất thì đồng ý xem, bỏ qua, hoặc yêu cầu gặp trợ giảng; làm câu kiểm tra|
|**AI làm gì?**|Không suy luận; hệ thống chỉ hiển thị nội dung đã soạn theo lựa chọn của learner và chấm câu kiểm tra theo đáp án có sẵn|Sinh câu hỏi chẩn đoán, suy luận chỗ hổng, sinh lời giải thích ngắn chỉ trong phạm vi chỗ hổng đã được learner xác nhận, chấm câu kiểm tra|Phân tích bài làm (đáp án sai, thời gian dừng, số lần sửa) để phát hiện kẹt, suy luận chỗ hổng, sinh giải thích; đánh giá độ tự tin và chuyển cho người khi thấp hoặc learner sai câu kiểm tra 2 lần|
|**Trigger**|Learner chủ động mở chuỗi kiến thức khi thấy mình kẹt|Learner chủ động báo "vẫn chưa hiểu"|AI tự kích hoạt khi phát hiện tín hiệu kẹt từ bài làm|
|**Trade-off chính**|Dễ kiểm soát, không sai do AI, rẻ để build; nhưng phụ thuộc việc learner tự đánh giá đúng — điều evidence cho thấy learner đang làm không tốt — và chỉ áp dụng cho nội dung đã soạn chuỗi sẵn|Giải quyết trực tiếp barrier "không biết mình hổng ở đâu" và có learner xác nhận; nhưng tốn thêm bước hỏi-đáp, AI có thể chẩn đoán sai, và vẫn cần learner tự nhận ra mình kẹt|Learner không phải tự nhận ra mình kẹt, giảm thời gian loay hoay sớm nhất; nhưng có rủi ro ngắt quãng sai lúc, phát hiện nhầm, cảm giác bị theo dõi, và tốn chi phí trợ giảng khi escalation|

**Distance check:**

- **A khác B vì:** A để learner tự chẩn đoán chỗ hổng trên nội dung cố định và không có suy luận của AI; B để AI suy luận chỗ hổng qua câu hỏi, learner chỉ xác nhận hoặc sửa kết quả chẩn đoán.
- **B khác C vì:** B bắt đầu khi learner chủ động báo kẹt và learner quyết định chẩn đoán cuối cùng; C bắt đầu khi AI tự phát hiện kẹt từ hành vi làm bài, AI đưa ra đề xuất trước và có thêm đường chuyển sang người thật.
- **A khác C vì:** A đặt toàn bộ quyền khởi động và quyền chẩn đoán vào learner, không có AI; C đặt quyền khởi động và chẩn đoán vào AI (kèm trợ giảng), learner chỉ duyệt đề xuất.

**Vị trí trên spectrum:**

```text
USER CREATES / INITIATES            → Option A (tự chẩn đoán theo chuỗi kiến thức)
        ↓
USER + AI CO-CREATE                 → Option B (hỏi chẩn đoán cùng AI)
        ↓
AI CREATES / INITIATES, USER REVIEWS → Option C (AI chủ động phát hiện kẹt + human escalation)
```


## 3. Human–AI Design pass

**Critical interaction cần test:** khoảnh khắc **xác định chỗ hổng** của learner trên bài gradient descent, tức đoạn từ lúc learner bị kẹt đến lúc nhận giải thích cho đúng một bước kiến thức nền. Không thiết kế các phần khác của sản phẩm.

### 3.1. Bốn quyết định thiết kế

**Expectation:**

- Trước khi bắt đầu, learner cần biết: hệ thống sẽ giúp tìm *một* bước kiến thức đang hổng và giải thích ngắn bước đó, **không** giải toàn bộ bài thay learner.
- Limit cần nói rõ: chỉ hỗ trợ trong chuỗi kiến thức của bài hiện tại; chẩn đoán có thể sai; giải thích không thay thế giảng viên/trợ giảng.

**Role and Agency:**

- Learner luôn là người quyết định cuối cùng về "mình hổng ở đâu"; AI chỉ đề xuất.
- Tại critical moment: A — AI *Don't Act*; B — AI *Ask*; C — AI *Act* ở mức đề xuất, nhưng *Ask* trước khi mở giải thích.
- Nếu AI chẩn đoán sai, learner mất thời gian đọc giải thích không liên quan và có thể rối thêm, giống trải nghiệm với ChatGPT trong I01. Sai dễ phát hiện nếu giải thích ngắn, gắn với đúng một bước, và có câu kiểm tra ở cuối.

**Evidence and Uncertainty:**

- Learner cần thấy AI dựa vào đâu: câu trả lời chẩn đoán của chính họ (B) hoặc dấu hiệu từ bài làm, ví dụ "bạn đã dừng ở bước tính w₁ và đổi dấu gradient 2 lần" (C).
- Khi AI không chắc: B hỏi thêm một câu thay vì đoán; C không tự mở giải thích mà đưa 2 bước khả nghi để learner chọn, hoặc gợi ý gặp trợ giảng.

**Control and Recovery:**

- Learner có thể bỏ qua đề xuất, chọn bước khác trong chuỗi, yêu cầu giải thích theo cách khác, hoặc tắt chế độ tự phát hiện (C).
- Sau khi AI sai: learner quay về chuỗi 4 bước để tự chọn bước khác (đường dự phòng chung của cả ba option) hoặc quay lại bài tập ngay, không mất phần bài đã làm.

### 3.2. Human–AI Decision Table

|Human–AI decision|Option A — Tự chẩn đoán theo chuỗi kiến thức|Option B — Hỏi chẩn đoán cùng AI|Option C — AI chủ động phát hiện kẹt|
|---|---|---|---|
|**User làm gì? AI làm gì?**|User: tự đánh giá từng bước "hiểu/chưa hiểu", chọn bước cần xem, làm câu kiểm tra. AI: không có; hệ thống hiển thị nội dung soạn sẵn và chấm theo đáp án.|User: báo kẹt, trả lời 2–3 câu chẩn đoán, xác nhận/sửa chẩn đoán, làm câu kiểm tra. AI: sinh câu hỏi, đề xuất chỗ hổng, giải thích trong phạm vi đã được xác nhận.|User: làm bài bình thường, duyệt đề xuất (xem / chọn bước khác / bỏ qua / gặp trợ giảng), làm câu kiểm tra. AI: phát hiện kẹt từ bài làm, đề xuất chỗ hổng, giải thích, escalation khi không chắc.|
|**AI Act / Ask / Don't Act? Vì sao?**|**Don't Act.** Option này kiểm tra liệu learner có tự chẩn đoán được khi có cấu trúc rõ ràng; hậu quả sai chỉ là learner chọn nhầm bước, dễ tự sửa.|**Ask.** Chẩn đoán dễ sai và evidence cho thấy giải thích lệch chỗ hổng làm learner rối hơn, nên AI phải hỏi và được xác nhận trước khi giải thích.|**Act → Ask.** AI chủ động lên tiếng để learner không phải tự nhận ra mình kẹt, nhưng chỉ ở mức đề xuất; mở giải thích cần learner đồng ý vì ngắt lời sai lúc gây phiền và mất mạch.|
|**User hiểu capability/limit bằng gì?**|Một dòng mở đầu: "Đây là 4 bước kiến thức của bài này, hãy tự đánh dấu bước bạn chưa chắc." Không cần giải thích AI.|Câu mở đầu: "Mình sẽ hỏi 2–3 câu để tìm bước bạn đang kẹt, sau đó giải thích ngắn bước đó. Mình có thể đoán sai, bạn có thể sửa."|Lần đầu bật: thông báo AI sẽ theo dõi đáp án và thời gian làm bài để gợi ý khi bạn có vẻ kẹt; chỉ gợi ý, không tự sửa bài; có thể tắt.|
|**Evidence/uncertainty được thể hiện thế nào?**|Không có suy luận nên không có uncertainty từ AI; kết quả câu kiểm tra là bằng chứng duy nhất cho learner biết đã chọn đúng bước hay chưa.|Hiển thị chẩn đoán kèm lý do lấy từ câu trả lời của learner ("Vì bạn trả lời gradient âm thì w giảm…"). Không chắc → hỏi thêm một câu hoặc đưa 2 khả năng để learner chọn.|Hiển thị tín hiệu đã dùng (bước dừng lâu, đáp án sai, số lần sửa). Độ tự tin thấp → đưa 2 bước khả nghi để chọn; sai câu kiểm tra 2 lần → gợi ý gặp trợ giảng.|
|**User kiểm soát và recovery thế nào?**|Đổi bước đã đánh dấu bất cứ lúc nào; sai câu kiểm tra → quay lại chuỗi để chọn bước khác; có thể đóng chuỗi để quay về bài.|Sửa chẩn đoán trước khi nhận giải thích; yêu cầu "giải thích cách khác"; chuyển sang tự chọn trong chuỗi 4 bước nếu AI hỏi vẫn sai; quay lại bài bất cứ lúc nào.|Bỏ qua đề xuất; chọn bước khác; yêu cầu trợ giảng; tắt chế độ tự phát hiện; bài làm không bị thay đổi nên quay lại task ban đầu ngay.|

### 3.3. Feedback and data check

|Câu hỏi|Option A|Option B|Option C|
|---|---|---|---|
|**Feedback ảnh hưởng phiên hiện tại, lần sau hay không ghi nhớ?**|Chỉ trong phiên hiện tại; không ghi nhớ.|Xác nhận/sửa chẩn đoán chỉ ảnh hưởng phiên hiện tại; không dùng để cá nhân hoá lần sau trong prototype.|Việc bỏ qua đề xuất có thể làm AI giảm tần suất gợi ý trong phiên; nếu muốn ghi nhớ cho lần sau phải hỏi learner trước.|
|**Dữ liệu nào được dùng và user có cách rút quyền không?**|Chỉ lựa chọn learner tự đánh dấu.|Câu trả lời chẩn đoán của learner trong phiên.|Đáp án, thời gian dừng, số lần sửa trong bài hiện tại. Learner tắt chế độ tự phát hiện là ngừng thu tín hiệu; dữ liệu của trợ giảng chỉ gửi khi learner chủ động yêu cầu.|
