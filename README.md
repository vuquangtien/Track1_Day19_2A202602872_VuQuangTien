# Day 19 — Hicarus | Case A: AI Tutor Diagnostic Refresher

## 1. Thông tin cá nhân và nhóm

| Mục | Thông tin |
| --- | --- |
| Họ và tên | Vũ Quang Tiến |
| MHV | 2A202602872 |
| Tên nhóm | Hicarus |
| Thành viên | Vũ Quang Tiến (2A202602872), Trần Đức Quân (2A202602922), Đoàn Quang Thanh (2A202602841) |
| Case | Case A — AI Tutor: Diagnostic Refresher cho VLearn |

## 2. Hypothesis Problem

## Chặng 1 — Evidence Snapshot + Hypothesis Problem

### Đầu vào từ Day 17

Nhóm tiếp tục **Case A — AI Tutor: Diagnostic Refresher** cho VLearn, với learner đang học/làm bài và bị kẹt ở một nội dung. Nhóm không đổi case để chọn giải pháp dễ build hơn.

| Artifact cần có | Nguồn đã đối chiếu | Cách dùng trong Day 18/19 |
| --- | --- | --- |
| Hypothesis Problem | `DAY17_Hicarus_BanGiao.md`, mục 2 | Giữ problem làm phạm vi chung cho cả A/B/C. |
| Ba Practice Notes | Bàn giao Day 17, mục 3: Nam; Gradient Descent; Backpropagation/Attention | Tổng hợp evidence và các điểm còn chưa chắc. |
| Solution Parking Lot | Bàn giao Day 17, mục 4, gồm 6 hướng | Mở lại solution space; không coi các ý tưởng là evidence user đã yêu cầu. |
| Conversation Guide cuối | Bàn giao Day 17, mục 5 ghi các câu hỏi đã bổ sung về tình huống, nguồn, thời gian, chẩn đoán nguyên nhân và kiểm tra mức hiểu | Chỉ dùng để tham khảo context và những câu hỏi còn mở; Day 18/19 không tiếp tục problem interview. |

Practice interview Day 17 là input để thiết kế và kiểm tra prototype, chưa đủ để chứng minh pain đã được xác thực.

### Evidence Snapshot

**User và tình huống:** Learner đang học hoặc làm bài, gặp một đoạn không hiểu và cần xử lý để tiếp tục học. Ba câu chuyện đều thuộc bối cảnh học kiến thức Machine Learning/cơ bản và xảy ra gần đây.

| Evidence từ Practice Notes | Ý nghĩa tạm thời |
| --- | --- |
| Nam nói gặp kiến thức khó khi làm bài vì chưa nắm kiến thức cơ bản; không bỏ qua mà bỏ thời gian tìm hiểu vì phần sau phụ thuộc vào nó. | Điểm kẹt có thể làm gián đoạn mạch học và learner có động lực xử lý ngay. Chưa rõ cách tìm hiểu, thời gian và chi phí cụ thể. |
| Một learner mất khoảng 30–45 phút khi học Gradient Descent: đọc slide, xem ví dụ, Google, YouTube, hỏi ChatGPT rồi làm bài tương tự. Learner nói phần tốn thời gian nhất là tìm đúng tài liệu/cách giải thích. | Learner có nhiều nguồn hỗ trợ nhưng vẫn tốn công chọn đúng nguồn và đúng kiểu giải thích. |
| Khi học Backpropagation, learner ban đầu tìm video về thuật toán nhưng sau đó nhận ra bị thiếu Chain Rule. Sau 15–20 phút ôn Chain Rule và làm ví dụ một neuron, họ quay lại làm được phần lớn bài. | Lỗ hổng kiến thức nền có thể là nguyên nhân trong một số tình huống; một ví dụ đơn giản giúp nối kiến thức nền với bài hiện tại. |
| Với Attention, learner từng tự cho rằng mình thiếu Matrix Multiplication. Sau khi ôn vẫn không hiểu và chỉ phát hiện ra mình nhầm Query/Key/Value khi hỏi bạn. | Learner có thể tự chẩn đoán sai nguyên nhân; hệ thống không nên khẳng định chắc chắn một nguyên nhân duy nhất. |
| ChatGPT cho phép hỏi lại nhưng đôi khi trả lời dài hoặc mở rộng sang nhiều kiến thức khiến learner rối. Learner cũng không chắc mình hiểu sâu hay chỉ hiểu một ví dụ. | Hỗ trợ cần ngắn, bám đoạn đang học, cho phép hỏi lại/đổi hướng và có cách để learner tự kiểm tra mức hiểu. |

### Evidence huddle

| Practice Note | User đã thực sự làm/nói gì? | Điều nhóm đang diễn giải |
| --- | --- | --- |
| 1 — Bùi Hải Nam | Khi gặp kiến thức khó do chưa nắm kiến thức cơ bản, Nam không bỏ qua mà “bỏ thời gian ra tìm hiểu”, vì không hiểu phần đó thì không hiểu kiến thức sau. | Điểm kẹt có thể liên quan kiến thức nền và đủ quan trọng để xử lý ngay. Chưa rõ Nam tìm bằng cách nào, mất bao lâu và workaround có gây khó khăn đáng kể không. |
| 2 — Gradient Descent | Learner đọc slide, xem ví dụ, tự làm ví dụ đơn giản, Google, YouTube, hỏi ChatGPT nhiều lần rồi tự làm lại bài tương tự. Learner nói: “Phần tốn thời gian nhất không hẳn là học, mà là tìm đúng tài liệu hoặc đúng cách giải thích.” | Rào cản có thể là tìm đúng loại hỗ trợ, thay vì thiếu hoàn toàn một nguồn giải thích. |
| 3 — Backpropagation/Attention | Learner tưởng mình không hiểu Backpropagation, sau đó nhận ra quên Chain Rule; ôn lại khoảng 15–20 phút rồi làm được phần lớn bài. Trong một lần học Attention, learner lại đoán sai nguyên nhân và chỉ phát hiện khi hỏi bạn. | Thiếu kiến thức nền có thể là một nguyên nhân, nhưng learner có thể chẩn đoán sai; một giải pháp cần xử lý cả sự không chắc chắn về nguyên nhân. |

**Điểm lặp lại:** Cả ba learner đều không bỏ qua điểm kẹt và dùng các bước tìm hiểu/ôn lại để tiếp tục bài. Hai notes nêu rõ việc tự tìm đúng nguyên nhân hoặc đúng cách giải thích là khó.

**Evidence mâu thuẫn hoặc bất ngờ:** Workaround hiện tại đôi khi hiệu quả: Nam nói cuối cùng hiểu được; learner Backpropagation quay lại làm được phần lớn bài. Với Attention, ôn kiến thức nền không giúp vì nguyên nhân ban đầu bị đoán sai.

**Điều vẫn là suy đoán:** Tần suất xảy ra, mức chi phí phổ biến và việc thiếu kiến thức nền có phải nguyên nhân chính hay không; chưa có bằng chứng rằng AI Tutor sẽ tốt hơn workaround hiện tại.

### Điều nhóm biết và điều còn cần kiểm tra

- Có tín hiệu rằng learner gặp điểm kẹt, dùng workaround nhiều bước và đôi khi mất đáng kể thời gian để tìm đúng sự hỗ trợ.
- Ôn kiến thức nền **có thể** giúp, nhưng không giải quyết mọi trường hợp; nhu cầu về ví dụ, diễn giải, ngữ cảnh hoặc hỏi lại cũng xuất hiện.
- Workaround hiện tại đôi khi vẫn hiệu quả, nên ba feedback ở Day 17 chưa cho phép kết luận nhu cầu hoặc giá trị sản phẩm đã được xác thực.
- Cần tiếp tục quan sát: tần suất điểm kẹt; chi phí thực tế; cách learner biết mình chẩn đoán sai; và cách họ kiểm tra đã hiểu khi đổi dạng bài.

### Hypothesis Problem nhóm tiếp tục

> Khi đang học hoặc làm bài và gặp một phần không hiểu, **learner** gặp khó khăn trong việc **xác định điều mình thiếu và chọn cách xử lý để tiếp tục bài** vì **chưa rõ nguyên nhân là lỗ hổng kiến thức nền hay cần một cách giải thích/ví dụ khác**, dẫn đến **phải dùng các workaround rời rạc, mất thời gian tìm đúng hỗ trợ và có thể đứt mạch học**.

**Evidence ban đầu hỗ trợ giả thuyết:** Trong note Gradient Descent, learner dùng slide, ví dụ, Google, YouTube và ChatGPT trong khoảng 30–45 phút; họ nói phần tốn thời gian nhất là tìm đúng tài liệu/cách giải thích. Note Backpropagation cho thấy learner chỉ nhận ra cần ôn Chain Rule sau khi đã tìm nội dung Backpropagation.

**Điều vẫn chưa được chứng minh:** Các tình huống này xảy ra thường xuyên đến đâu; workaround có luôn tốn kém hay không; và AI có thể giúp learner chẩn đoán/giải quyết điểm kẹt tốt hơn các cách hiện có hay không.

### Hypothesis Problem gốc từ Day 17

> Khi đang học và gặp một phần không hiểu, learner cần xác định và xử lý điểm bị kẹt để tiếp tục bài học. Nhóm giả định rằng một phần learner bị kẹt vì không tự xác định được kiến thức nền còn thiếu; hiện họ dùng các workaround rời rạc như xem lại, tìm kiếm hoặc hỏi người khác, có thể làm gián đoạn việc học. Cần kiểm tra liệu tình huống này có xảy ra đủ thường xuyên, đủ tốn kém, và liệu thiếu kiến thức nền có thực sự là nguyên nhân chính hay không.

**JTBD:** Khi bị kẹt ở một nội dung trong bài học, tôi muốn xác định điều mình chưa hiểu và có cách xử lý phù hợp, để có thể tiếp tục học mà không mất quá nhiều thời gian hoặc đứt mạch.

## 3. Three Solution Options

Design Sheet chi tiết: [three-option-design-sheet.md](three-option-design-sheet.md). Cách mở prototype: [prototype-link.md](prototype-link.md).

## Chặng 2 — Ba Solution Options + Comparison Contract

### Solution Parking Lot được mở lại

| Hướng | Cơ chế | Nguồn |
| --- | --- | --- |
| P1. Nút “Tôi vẫn chưa hiểu” → chẩn đoán → giải thích → quay lại bài | User + AI co-create | Case directive Day 17 |
| P2. Đưa ví dụ/cách diễn giải khác thay vì ôn kiến thức nền | AI tạo nội dung, user chọn | Giả thuyết cạnh tranh B, Day 17 |
| P3. Câu kiểm tra ở dạng khác để biết đã hiểu thật chưa | Kiểm tra transfer | Practice Note Gradient Descent |
| P4. Learner tự đánh dấu bước chưa hiểu trên chuỗi kiến thức soạn sẵn | User-led, no-inference | Bổ sung vì pool thiếu hướng user-led |
| P5. AI phát hiện learner bị kẹt từ bài làm, đề xuất chỗ hổng và chuyển trợ giảng khi cần | AI initiates, user reviews + human escalation | Bổ sung vì pool thiếu AI-initiated/human escalation |

P1–P3 cùng bắt đầu bằng learner báo kẹt và AI giải thích, nên P4 và P5 được bổ sung để tạo ba cơ chế thực sự khác nhau. P3 được dùng làm bước kết thúc chung nhằm đo desired outcome, không thành option riêng.

### Những quyết định chung cho A/B/C

| Thành phần | Quyết định chung |
| --- | --- |
| Target user | Learner đang tự làm bài tập môn kỹ thuật, đã có slide/bài giảng nhưng bị kẹt ở một khái niệm. |
| Situation | Đang làm bài, biết áp dụng công thức nhưng không hiểu vì sao công thức đúng nên không làm tiếp được. |
| Task | Xác định đúng chỗ mình đang hổng và hiểu đủ khái niệm đó để quay lại làm bài. |
| Desired outcome | Learner quay lại bài trong 10 phút và trả lời đúng một câu kiểm tra ở dạng khác với ví dụ vừa học. Đây là mục tiêu test, chưa phải kết quả đã được xác thực. |
| Content/data fixture | Gradient Descent: `f(w) = (w − 3)²`, `w₀ = 0`, learning rate `0.1`; tính `w₁` và giải thích vì sao cập nhật `w = w − lr·f'(w)`. Chuỗi nền: đạo hàm là độ dốc → dấu đạo hàm cho biết hướng hàm tăng → đi ngược gradient để giảm loss → learning rate điều chỉnh độ dài bước. Câu transfer: Với `f(w) = (w + 2)²`, `w₀ = 0`, w tăng hay giảm sau một bước, và vì sao? |

### Ba solution hypotheses

| Thành phần | Option A — Tự chẩn đoán theo chuỗi kiến thức | Option B — Hỏi chẩn đoán cùng AI | Option C — AI chủ động phát hiện kẹt |
| --- | --- | --- | --- |
| Solution mechanism | Learner tự đi qua chuỗi 4 bước kiến thức nền, tự đánh dấu bước chưa hiểu và xem giải thích soạn sẵn. | AI hỏi 2–3 câu ngắn để suy luận chỗ hổng; learner xác nhận hoặc sửa trước khi AI giải thích. | AI phân tích bài làm để phát hiện tín hiệu kẹt, đề xuất chỗ hổng và giải thích; chuyển trợ giảng khi AI không chắc. |
| User làm gì? | Đọc từng bước, tự đánh giá hiểu/chưa hiểu, chọn bước cần xem lại và làm câu transfer. | Báo đang kẹt, trả lời câu hỏi, xác nhận/sửa chẩn đoán và làm câu transfer. | Làm bài bình thường; đồng ý xem, bỏ qua hoặc yêu cầu trợ giảng khi AI đề xuất; làm câu transfer. |
| AI làm gì? | Không suy luận nguyên nhân; hiển thị nội dung theo lựa chọn của learner và chấm câu transfer theo đáp án có sẵn. | Sinh câu hỏi chẩn đoán, suy luận chỗ hổng, sinh giải thích ngắn trong phạm vi learner đã xác nhận và chấm câu transfer. | Phân tích đáp án sai, thời gian dừng và số lần sửa; suy luận chỗ hổng, sinh giải thích, đánh giá độ tự tin và chuyển người thật khi thấp hoặc learner sai transfer hai lần. |
| Trigger | Learner chủ động mở chuỗi kiến thức khi thấy kẹt. | Learner chủ động báo “Tôi vẫn chưa hiểu”. | AI tự kích hoạt khi phát hiện tín hiệu kẹt từ bài làm. |
| Trade-off chính | Dễ kiểm soát, không sai do AI; nhưng learner phải tự đánh giá đúng chỗ hổng và nội dung cần được soạn sẵn. | Xử lý trực tiếp barrier xác định chỗ hổng; nhưng tốn thêm bước hỏi đáp và AI vẫn có thể chẩn đoán sai. | Giảm thời gian loay hoay sớm; nhưng có thể ngắt quãng sai lúc, phát hiện nhầm, tạo cảm giác bị theo dõi và tốn nguồn lực trợ giảng. |

### Distance check

- **A khác B vì:** A để learner tự chẩn đoán trên nội dung cố định, không có AI suy luận; B để AI suy luận qua câu hỏi, learner xác nhận hoặc sửa kết quả.
- **B khác C vì:** B bắt đầu khi learner chủ động báo kẹt; C bắt đầu khi AI phát hiện kẹt từ hành vi bài làm và có đường chuyển trợ giảng.
- **A khác C vì:** A đặt quyền khởi động và chẩn đoán ở learner; C để AI khởi động và đưa đề xuất, learner duyệt hoặc bỏ qua.

```text
USER CREATES / INITIATES             → Option A
        ↓
USER + AI CO-CREATE                  → Option B
        ↓
AI CREATES / INITIATES, USER REVIEWS → Option C
```

### Comparison Contract

Ba prototype dùng chung bối cảnh, bài Gradient Descent, chuỗi kiến thức nền và câu transfer. Cùng một task được giao cho tester: xử lý điểm kẹt để quyết định bước tiếp theo trước khi quay lại bài. Chỉ thay cơ chế hỗ trợ, quyền khởi động, cách phân chia việc user–AI–trợ giảng và trade-off; không dùng khác biệt màu sắc, layout hoặc wording làm option.

## Chặng 3 — Human–AI Design Pass

**Critical interaction được review:** điểm learner chọn hoặc nhận một hướng hỗ trợ sau khi bị kẹt ở bài Gradient Descent. Prototype chỉ cần thể hiện interaction này và bước quay lại bài/câu transfer, không thiết kế toàn bộ VLearn.

### Human–AI Decision Table

| Human–AI decision | Option A — Tự chẩn đoán | Option B — Chẩn đoán cùng AI | Option C — AI chủ động phát hiện kẹt |
| --- | --- | --- | --- |
| User làm gì? AI làm gì? | User đọc chuỗi bốn bước, tự đánh dấu bước chưa hiểu, chọn xem lại và làm câu transfer. Hệ thống hiển thị nội dung tương ứng; không kết luận learner hổng ở đâu. | User báo kẹt, trả lời 2–3 câu và xác nhận/sửa nhận định. AI tổng hợp câu trả lời, đề xuất một khả năng nguyên nhân và tạo giải thích ngắn sau khi user chọn. | User tiếp tục làm bài hoặc chọn phản hồi đề xuất. AI nhận tín hiệu kẹt, nêu tín hiệu đã thấy và mời user nhận trợ giúp; chỉ sau khi user đồng ý AI mới đưa hướng ôn hoặc mở đường hỏi trợ giảng. |
| AI Act / Ask / Don't Act? Vì sao? | **Don't Act.** Không có đủ dữ liệu để hệ thống kết luận chỗ hổng; learner giữ quyền tự nhận định. | **Ask, rồi Act sau xác nhận.** Chẩn đoán có thể sai và ảnh hưởng hướng học, nên learner cần sửa hoặc bác bỏ trước khi AI tạo hỗ trợ. | **Ask.** AI được phép chủ động nhận ra tín hiệu nhưng không tự ngắt bài hay tự chuyển coach. Sai ở thời điểm này dễ gây phiền và làm learner mất mạch. |
| User hiểu capability/limit bằng gì? | Dòng giới thiệu: “Bạn tự chọn bước cần xem lại. Hệ thống không đoán bạn đang thiếu kiến thức nào.” | Trước câu hỏi: “Tôi sẽ hỏi 3 câu về đoạn đang học để gợi ý một khả năng, không xác định chắc chắn nguyên nhân.” | Prompt nêu rõ: “Tôi thấy bạn dừng lâu/chỉnh đáp án nhiều lần. Đây chỉ là tín hiệu, không có nghĩa bạn chưa hiểu.” Đồng thời nói AI không đọc nội dung ngoài bài và không tự gửi gì cho trợ giảng. |
| Evidence/uncertainty được thể hiện thế nào? | Hiển thị chuỗi kiến thức như tài liệu hỗ trợ, không gắn nhãn một bước là nguyên nhân. User chọn bước nào thì hệ thống nói đó là lựa chọn của user. | Card nhận định ghi “Có thể bạn đang cần xem lại: dấu đạo hàm và hướng giảm loss”, kèm các câu trả lời mà AI đã dựa vào và nút “Không đúng, đổi hướng”. | Prompt liệt kê tín hiệu phiên hiện tại: thời gian dừng, số lần sửa/đáp án sai. Gắn nhãn “độ chắc chắn thấp”; khi tín hiệu không đủ, AI chỉ cho user nút tự mở trợ giúp, không nêu nguyên nhân. |
| User kiểm soát và recovery thế nào? | User đổi bước đã chọn, bỏ qua trợ giúp, quay lại bài hoặc mở câu transfer bất cứ lúc nào. Không có nhận định AI cần sửa. | User sửa câu trả lời, chọn “Không đúng”, chọn một hướng khác, bỏ qua giải thích hoặc quay lại bài. Sau câu transfer sai, user có thể xem lại giải thích, quay về chuỗi kiến thức hoặc tiếp tục bài mà không bị khóa. | User chọn “Xem hỗ trợ”, “Để sau”, hoặc “Đừng nhắc trong bài này”; có nút tắt phát hiện chủ động. User xem/chỉnh nội dung trước khi gửi trợ giảng và có thể hủy gửi. Dù từ chối prompt, learner vẫn quay lại bài hoặc tự mở Option A/B. |
| Feedback và dữ liệu | Lựa chọn bước và đáp án transfer chỉ dùng trong phiên prototype để hiển thị nội dung/câu tiếp theo; không dùng để suy luận hồ sơ năng lực hoặc ghi nhớ sang lần sau. | Câu trả lời chẩn đoán và lựa chọn “đúng/không đúng” chỉ dùng cho lần hỗ trợ hiện tại; không ghi nhớ sang lần sau trong prototype. User có thể bắt đầu lại để xóa câu trả lời hiện tại. | Chỉ dùng dữ liệu tương tác của **phiên bài hiện tại**: thời gian dừng, số lần sửa và đáp án. Không đọc tab/bài khác, không ghi nhớ sang lần sau, không gửi coach nếu learner chưa preview và bấm gửi. User có thể tắt phát hiện chủ động và xóa tín hiệu phiên hiện tại. |

### Quyết định chung khi AI sai

- AI không được khóa learner vào hướng ôn hoặc buộc hoàn thành câu transfer mới cho quay lại bài.
- “Không đúng”, “Đổi hướng”, “Bỏ qua/Để sau” và “Quay lại bài” phải hiện ngay ở trạng thái AI đưa đề xuất.
- Câu transfer là tín hiệu tự kiểm tra, không phải phán quyết rằng learner đã hiểu hoặc chưa hiểu.

## Chặng 4 — Ba micro-prototype

Prototype chạy bằng HTML/CSS/JavaScript tại [index.html](index.html). Tester tự mở file này, chọn A/B/C từ cùng một common context và có nút **Reset về bài tập chung** ở cuối trang.

### Scope chung

- **Common context:** bài Gradient Descent, điểm kẹt “vì sao đi ngược gradient lại giảm loss?”, và cùng data fixture/câu transfer ở Chặng 2.
- **Critical interaction:** A chọn bước kiến thức; B trả lời chẩn đoán rồi review gợi ý; C review tín hiệu AI phát hiện trước khi chọn hỗ trợ.
- **Result/user decision:** mỗi option dẫn tới câu transfer hoặc quay lại bài; learner luôn có thể bỏ qua, đổi hướng hay reset.

### Prototype annotation — không hiện cho tester

| Option | We expect the tester to | Watch for | Do not explain |
| --- | --- | --- | --- |
| A | Tự chọn một bước nền mà họ muốn ôn và quyết định có làm câu transfer không. | Họ có hiểu hệ thống không đoán thay; có biết chọn bước nào; có đổi bước khi chọn không phù hợp không. | Ý nghĩa từng bước của chuỗi kiến thức hoặc đáp án bài tập. |
| B | Trả lời ba câu, đọc mức chắc chắn/lý do và chọn chấp nhận, sửa hoặc từ chối gợi ý AI. | Họ có hiểu AI chỉ gợi ý; có xem evidence; có dùng “Không đúng, đổi hướng” không. | Vì sao AI ra kết luận hoặc đáp án của câu transfer. |
| C | Nhận ra prompt chỉ là tín hiệu, sau đó chọn xem hỗ trợ, để sau, tắt nhắc hoặc preview trước khi gửi trợ giảng. | Prompt có gây gián đoạn; họ có hiểu dữ liệu AI dùng; họ có thấy quyền từ chối và hủy gửi không. | Tại sao AI phát hiện kẹt hoặc phải chọn phương án nào. |

## Chặng 5 — Chuẩn bị test

### Relevant context

> Gần đây bạn có từng đang làm bài, biết cách áp dụng một công thức nhưng chưa hiểu vì sao công thức đó đúng hoặc vì sao nó hoạt động không?

Chỉ hỏi một lần, tối đa hai phút. Nếu tester chưa có trải nghiệm tương tự, vẫn mời họ làm task để phát hiện interaction breakdown; không dùng phản hồi đó để đưa ra value claim mạnh.

### Outcome task

> Trong tình huống này, hãy dùng từng phương án để tìm một bước giúp bạn hiểu vì sao Gradient Descent cập nhật w theo hướng ngược gradient, rồi quyết định bạn sẽ làm gì tiếp theo để quay lại bài tập.

Facilitator mở từng option từ common context; task và content fixture giữ nguyên cho A/B/C. Không hướng dẫn tester bấm nút nào hay phải chọn phương án nào.

### Observation focus

Chỉ ghi hành vi và lời nói trước; diễn giải sau. Quan sát tối đa năm điểm sau:

1. **First action:** Tester làm gì đầu tiên ở mỗi option.
2. **Hesitation:** Tester dừng, do dự hoặc tìm cách nào; điều gì tạo ra khoảng dừng đó.
3. **Evidence read/ignored:** Tester có đọc giới hạn, tín hiệu hoặc độ chắc chắn AI đưa ra không.
4. **Misunderstanding và correction/recovery:** Tester hiểu sai điều gì; có tự tìm được “Không đúng”, đổi hướng, bỏ qua, để sau, tắt nhắc hoặc quay lại bài không.
5. **Option được chọn và trade-off:** Sau khi thử đủ A/B/C, tester chọn gì cho tình huống này và nêu điều họ chấp nhận đánh đổi.

### Luật facilitation

1. Tester tự điều khiển prototype.
2. Mỗi tester làm cùng Outcome task qua cả A/B/C.
3. Không narrate, giải thích icon hoặc pitch giải pháp.
4. Không lấp khoảng im lặng.
5. Không hỏi “Bạn có thích không?”.
6. Khi tester hỏi cách hoạt động, hỏi lại: “Theo bạn, nó nên hoạt động như thế nào?”

**Ba câu cứu hộ duy nhất:**

- “Bạn cứ nói to suy nghĩ của mình nhé.”
- “Bạn sẽ làm gì tiếp theo?”
- “Theo bạn, nó nên hoạt động như thế nào?”

## 4. Đóng góp của tôi trong nhóm

Tôi phụ trách **Option C — AI chủ động phát hiện điểm kẹt, learner review**. Phần tôi thực hiện gồm:

- Xác định critical interaction cho Option C: AI chỉ nêu tín hiệu của phiên hiện tại và hỏi learner có muốn nhận hỗ trợ hay không.
- Thiết kế expectation, uncertainty, quyền từ chối, tắt gợi ý chủ động, preview/chỉnh/hủy trước khi gửi trợ giảng và đường quay lại bài.
- Build flow Option C trong prototype chung: prompt tín hiệu → nhận/trì hoãn/tắt gợi ý → hướng hỗ trợ → tùy chọn preview câu hỏi gửi trợ giảng → câu transfer/quay lại bài.
- Tham gia chuẩn hóa shared context, data fixture Gradient Descent và outcome task dùng chung cho A/B/C.
- Facilitate một phiên test với Bùi Hải Nam (2A202602636), sau đó ghi observation vào [prototype-feedback-note.md](prototype-feedback-note.md).

## 5. Prototype Feedback

- Feedback Note của phiên tôi facilitate: [prototype-feedback-note.md](prototype-feedback-note.md).
- Tổng hợp ba phiên của nhóm: [group-feedback-synthesis.md](group-feedback-synthesis.md).
- **Trạng thái:** Đã có Feedback Note của phiên do tôi facilitate. Group Feedback Synthesis chỉ hoàn tất khi nhóm có đủ ba Feedback Notes, mỗi tester đã trải nghiệm đầy đủ A/B/C. Không kết luận solution đã được validated.

## 6. AI Support Log

Xem [ai-support-log.md](ai-support-log.md). Đây là log riêng của người nộp và cần được tôi rà lại, bổ sung phần tự sửa sau khi test.

### Khai báo sử dụng AI

AI được dùng để tổng hợp các Practice Notes đã có thành Evidence Snapshot và hỗ trợ cấu trúc tài liệu. Mọi facts, quote và quan sát trong phần này đều bám theo tài liệu Day 17; không tạo thêm phản hồi người dùng hoặc dữ liệu phỏng vấn.
