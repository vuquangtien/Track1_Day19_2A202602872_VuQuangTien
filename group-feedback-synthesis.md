# Group Feedback Synthesis

## Nguồn feedback

|Feedback|Facilitator|Tester|Thứ tự option|Option chọn|Note|
|---|---|---|---|---|---|
|**1**|Trần Đức Quân|Đặng Văn Thái Anh (2A202602407)|A → B → C|**B**|Feedback Note do Quân lưu trong repo cá nhân/nhóm chung|
|**2**|Đoàn Quang Thanh|Nguyễn Văn Thăng (2A202602835)|B → C → A|**A**|Feedback Note do Thanh lưu trong repo cá nhân/nhóm chung|
|**3**|Vũ Quang Tiến|Bùi Hải Nam (2A202602636)|C → A → B|**C**|[Feedback Note cá nhân](prototype-feedback-note.md)|

Nhóm xoay vòng thứ tự để mỗi option được test đầu tiên đúng một lần, giảm hiệu ứng "option sau dễ hơn vì đã biết bài".

## Bảng tổng hợp

|Nội dung đối chiếu|Feedback 1 (Thái Anh)|Feedback 2 (Thăng)|Feedback 3 (Nam)|Pattern hoặc khác biệt|
|---|---|---|---|---|
|**First action:** điểm chạm đầu tiên|**A:** thử gõ phần (b), khựng lại rồi tự bấm "Ôn lại kiến thức nền". **B:** gõ ngay mô tả điểm vướng. **C:** đọc tín hiệu "dừng 4 phút, sửa 2 lần", chững lại rồi chọn xem hỗ trợ.|**B:** trả lời đủ 3 câu. **C:** đọc tín hiệu rồi chọn **"Để sau"**. **A:** chọn "Dấu đạo hàm", mở thêm "Learning rate".|**C:** đọc tín hiệu, chọn "Xem một hướng hỗ trợ". **A:** chọn "Dấu đạo hàm", quay lại so với "Đi ngược gradient". **B:** trả lời câu hỏi, đọc evidence.|**Pattern:** ở A, cả 3 đều đi thẳng vào **bước dấu đạo hàm / đi ngược gradient**; ở C, cả 3 đều **đọc tín hiệu trước khi quyết định**; ở B, cả 3 đều **trả lời câu hỏi chẩn đoán mà không bỏ ngang**. **Khác biệt:** ở C, Thăng từ chối ngay ("Để sau"), Thái Anh và Nam chấp nhận.|
|**Major breakdown:** điểm tắc nghẽn lớn nhất|**C:** lo bị thu thập dữ liệu hoặc bị báo cho giảng viên, "hơi giật mình" khi prompt xuất hiện. **A:** khựng ~15 giây ở bước dấu đạo hàm.|**C:** lo prompt xuất hiện khi đang suy nghĩ. **A:** do dự giữa "Dấu đạo hàm" và "Đi ngược gradient". **B:** không muốn trả lời thêm khi đã biết cần ôn gì.|**A:** phải tự gọi đúng tên lỗ hổng, do dự giữa "Dấu đạo hàm" và "Đi ngược gradient". **B:** thêm bước trả lời câu hỏi. **C:** nguy cơ ngắt mạch nếu nhắc sai lúc.|**Pattern:** cả 3 đều nêu **lo ngại về gián đoạn/bị theo dõi ở C**; 2/3 (Thăng, Nam) **do dự giữa "Dấu đạo hàm" và "Đi ngược gradient"** ở A; 2/3 (Thăng, Nam) thấy **câu hỏi của B là bước thêm**. Breakdown nằm ở **khả năng tự gọi tên chỗ hổng**, không nằm ở giao diện.|
|**Control taken:** cách lấy lại quyền kiểm soát|Tự đánh dấu và quay lại đúng ô (b); yên tâm vì B có "Chưa đúng, sửa hướng tìm" dù không dùng; **chỉnh bản nháp rồi gửi** trợ giảng ở C.|**"Để sau"** ở C, sẽ dùng "Đừng nhắc" nếu lặp lại; "Đổi bước cần xem lại" ở A; biết có "Không đúng, đổi hướng" ở B nhưng không dùng.|**Mở preview hỏi trợ giảng rồi hủy** ở C; "Đổi bước cần xem lại" ở A; biết có "Không đúng, đổi hướng" ở B nhưng không dùng.|**Pattern:** cả 3 đều **dùng hoặc chỉ ra được đường thoát** ở mọi option. **Khác biệt:** chưa ai dùng "Không đúng, đổi hướng" ở B vì không ai gặp chẩn đoán sai.|
|**Selected option:** phương án được chọn|Option **B** (test thứ 2)|Option **A** (test thứ 3)|Option **C** (test thứ 1)|**Không có pattern về lựa chọn**, và lựa chọn **không trùng với vị trí test**: mỗi tester chọn một option ở một vị trí khác nhau. Lựa chọn đi theo việc learner **có tự gọi tên được chỗ hổng hay không** và mức chấp nhận việc AI chủ động.|
|**Key trade-off:** sự đánh đổi then chốt|B thu hẹp đúng chỗ vướng mà không phải tự đoán như A, không bị theo dõi như C; đổi lại mất thêm 1–2 phút trả lời câu hỏi.|A cho tự chọn và tự kiểm tra; đổi lại learner phải tự gọi tên lỗ hổng. B là phương án dự phòng tốt. C có nguy cơ ngắt mạch lớn hơn lợi ích.|C hỗ trợ sớm, không phải tự gọi tên lỗ hổng hay trả lời câu hỏi; đổi lại có nguy cơ ngắt mạch, được bù bằng "Để sau", "Đừng nhắc" và preview.|**Trục đánh đổi chung:** **quyền tự khởi động** (A) ↔ **AI giúp thu hẹp chỗ hổng** (B) ↔ **được hỗ trợ sớm** (C). B là option duy nhất **không bị tester nào từ chối**: Thái Anh chọn, Thăng coi là dự phòng tốt, Nam chỉ chê thêm bước trả lời câu hỏi.|

## Quyết định hành động tiếp theo của cả nhóm

- **Đúng MỘT Next Change duy nhất nhóm chốt cho vòng tiếp theo:** Chọn **Option B — Cùng AI chẩn đoán** làm cơ chế chính và sửa một interaction: thêm lối tắt **"Mình biết cần ôn bước nào"** ở màn hình đầu của B, để learner đã biết chỗ hổng bỏ qua câu hỏi chẩn đoán và chọn thẳng bước cần ôn.

- **Dữ kiện thực tế cụ thể từ 3 cuộc thử nghiệm dẫn dắt nhóm đến quyết định này:**
  - **B giải quyết đúng barrier của Hypothesis Problem** ("không xác định được mình đang hổng ở đâu"): Thái Anh chọn B vì B **"thu hẹp đúng chỗ vướng mà không phải tự đoán danh mục kiến thức như A"**; ở A, Thăng và Nam đều do dự giữa "Dấu đạo hàm" và "Đi ngược gradient", tức là tự chẩn đoán vẫn khó.
  - **Nhu cầu của người chọn C được B đáp ứng mà không cần AI tự xuất hiện:** Nam chọn C vì không phải tự gọi tên lỗ hổng; B cũng làm được việc này. Trong khi đó **cả 3 tester đều nêu lo ngại ở C** (Thái Anh "hơi giật mình", Thăng chọn "Để sau", Nam nhắc nguy cơ nhắc sai lúc).
  - **Lối tắt đến từ người chọn A:** Thăng thấy câu hỏi của B "có ích khi không biết bắt đầu từ đâu" nhưng **không muốn trả lời thêm khi đã tự nhận diện được phần cần ôn**; Nam cũng chê B thêm bước trả lời câu hỏi. Lối tắt giữ quyền tự chọn của A ngay trong B.

- **Điều quan trọng vẫn CHƯA THỂ CHỨNG MINH ĐƯỢC (Still Unproven) sau 3 phiên test:**
  - **Nhánh phục hồi khi AI chẩn đoán sai:** không ai gặp chẩn đoán sai ở B, nên chưa biết "Không đúng, đổi hướng" có giúp quay về đúng chỗ hổng không. Đây là rủi ro lớn nhất khi chọn B làm cơ chế chính.
  - **Learner có tự chọn đúng giữa lối tắt và câu hỏi chẩn đoán không:** chưa biết learner có nhận ra mình "đã biết cần ôn bước nào" hay sẽ chọn lối tắt rồi chọn sai bước (như Thăng và Nam từng do dự ở A).
  - **Thời điểm prompt C xuất hiện:** cả 3 phiên đều mở C từ màn hình chọn phương án, nên việc không chọn C dựa trên lo ngại của tester, chưa dựa trên hành vi khi AI tự xuất hiện thật.
  - **Hiệu quả học:** chưa đo thời gian hoàn thành so với mức 30–45 phút trong evidence ban đầu, và chưa đo mức hiểu khi đổi sang dạng bài khác.
  - **Cỡ mẫu:** chỉ 3 tester, mỗi người chọn một option khác nhau; quyết định chọn B dựa trên việc B không bị ai từ chối và khớp barrier, chưa phải vì đa số tester ưu tiên B.
