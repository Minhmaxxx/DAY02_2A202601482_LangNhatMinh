## Scan rộng

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 |Tiêu tốn thời gian, lợi thế của AI | Tìm lại thông tin bài cũ và đọc tài liệu mất thời gian: Khó khăn khi phải lục lọi lại slide bài giảng cũ, hoặc đọc các tài liệu dài để trích xuất thông tin làm báo cáo/đồ án | Sinh viên đại học | Mất 30 đến 45 phút chỉ để tìm trong các thư mục Drive/Zalo lớp để tìm thấy đúng slide cần thiết. Thường xuyên nản chí khi phải đọc và tóm tắt tài liệu từ các file PDF dài hàng chục trang | 
| 2 |Tác vụ lặp lại, Điểm đau | Bỏ sót lịch nộp bài tập và công việc cần làm: Không nhớ hôm nay có deadline nào cần hoàn thành, dẫn đến việc quên nộp bài hoặc làm đối phó vào phút chót | Sinh viên, trưởng nhóm đồ án/dự án | Liên tục nhắn tin hỏi bạn bè trong nhóm chat kiểu như: "Ê hôm nay phải làm gì nhỉ, có nộp cái gì không ?". Từng trễ hạn submit code hoặc nộp bài tập trên hệ thống trường ít nhất 1-2 lần trong tháng |
| 3 |Tiêu tốn thời gian, điểm đau| Onboarding, codebase và xử lý conflict: Người mới thường gặp khó khăn với môi trường mới, chưa thích nghi được dẫn tới đọc hiểu luồng logic code của dự án chưa được tốt. Quá trình chia nhánh và merge code trên git thường xuyên bị xung đột | Lập trình viên mới, thực tập sinh | Mất từ nửa ngày đến một ngày chỉ để setup xong môi trường server chạy local. Tốn 30-45 phút mỗi lần gỡ rối (resolve conflict) khi gộp code từ các thành viên khác |
| 4 |AI có thể tốt hơn, lặp lại | Cân đối lịch trình tập luyện thể thao: Khó khăn trong việc theo dõi và tự động điều chỉnh lịch tập luyện kết hợp nhiều môn, tránh tình trạng quá tải thể lực hoặc chấn thương | Bản thân (người chơi thể thao) | Khá đau đầu và mất thời gian mỗi tuần để tự chia lịch đá bóng sân 7, xen kẽ với các buổi chạy bộ dài (1.5 – 2 tiếng) và lịch tập sức mạnh tại nhà (tạ tay, xà đơn) sao cho hợp lý |
| 5 |Tiêu tốn thời gian, Lợi thế của AI | Thiếu tính năng gợi ý chiến thuật/phân bổ tối ưu: Các game mô phỏng hoặc app quản lý không tự động gợi ý cách phân bổ tài nguyên, kỹ năng tối ưu cho người dùng dựa trên dữ liệu hiện tại | Người chơi game, Người dùng app | Người dùng thường xuyên phải thoát ứng dụng ra ngoài để tra cứu wiki, xem hướng dẫn cách phân bổ skill, luyện rank nhân vật, gây đứt gãy trải nghiệm giải trí |

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Cân đối lịch trình tập luyện thể thao phức hợp | Workflow quen thuộc, pain point diễn ra hàng tuần. Có thể đo lường success metric rõ ràng thông qua tỷ lệ hoàn thành lịch tập và thời gian xếp lịch. | Khó lượng hóa chính xác dữ liệu đầu vào (mức độ mệt mỏi của người tập) vào hệ thống một cách chuẩn xác. |
| 2 | Xử lý Merge Conflict khi làm việc nhóm trên Git | Actor rõ ràng. Bottleneck định lượng được rõ rệt (mất hàng chục phút để hiểu logic). Tác động trực tiếp tiến độ release. | Ranh giới giữa máy đề xuất (draft) và tự động gộp (auto-merge) chưa rõ ràng, rủi ro sinh lỗi logic ẩn cao. |
| 3 | Đứt gãy trải nghiệm khi tra cứu Wiki game/app | Điểm nghẽn rất cụ thể (thao tác chuyển đổi app liên tục). Giải quyết được bằng Computer Vision / Screen Reader. | Cấu hình phần cứng thiết bị di động có chịu được việc chạy nền một AI Agent liên tục hay không. |

---

## Problem Card #1 — Lịch Tập Luyện Thông Minh

**Problem 1 câu:**  
Người chơi thể thao tốn nhiều thời gian và phân vân không biết cách tinh chỉnh khối lượng, dời lịch bài tập (bóng đá, chạy bộ, tạ) sao cho phù hợp với thể trạng mỏi cơ thực tế mỗi ngày để tránh kiệt sức.

**Actor:**  
Bản thân (Người chơi thể thao nghiệp dư, tập luyện đa môn).

**Thời điểm / bối cảnh:**  
Lên lịch cho ngày hôm sau hoặc sáng sớm thức dậy, đặc biệt là sau một buổi tập nặng (như chạy bộ 1.5 - 2 tiếng hoặc đá bóng sân 7) chưa kịp phục hồi.

**Current workflow:**

```text
1. Chốt lịch cố định các môn từ đầu tuần.
2. Thực hiện buổi tập cường độ cao ngày hôm trước.
3. Thức dậy thấy cơ thể đau mỏi, chưa phục hồi kịp.
4. Tự phân vân đánh giá mức độ đau mỏi và tìm cách đổi lịch/bài tập.
5. Cố tập theo lịch cũ (gây chấn thương) hoặc quyết định bỏ tập (mất kiên trì).
```

**Bottleneck:**  
Bước 4 — Tự đánh giá mức độ mỏi cơ và suy nghĩ/tra cứu để xếp lại lịch bài tập thay thế mất khoảng 15 phút, thường dẫn đến nản chí.

**Impact:**  
Dễ gặp chấn thương do tập quá tải, hoặc làm giảm động lực duy trì lịch tập, tỷ lệ hoàn thành kế hoạch tuần (compliance rate) bị thấp.

**Success metric:**  
Giảm thời gian chọn lịch tập thay thế từ khoảng 15 phút xuống dưới 3 phút. Theo dõi compliance rate hằng tuần và đặt mục tiêu >85% sau khi có baseline thực tế.

**Non-AI alternative:**  
Thuê Personal Trainer (PT) chuyên nghiệp theo dõi và điều chỉnh hàng ngày (tốn kém), hoặc tự tạo quy tắc Rule-based trên Excel (quá cứng nhắc, không đo được thể trạng thực tế).

**AI hypothesis:**  
Người dùng log chỉ số mệt mỏi/vị trí đau mỏi vào hệ thống, AI đối chiếu lịch tuần và tự động draft lại lịch: recommend đổi sang bài tập phục hồi (giãn cơ) hoặc giảm khối lượng tạ xuống mức an toàn. Người dùng chỉ việc duyệt.

**Safety boundary:**  
Hệ thống không chẩn đoán chấn thương hoặc thay thế chuyên gia y tế. Người dùng tự quyết định lịch tập; nếu đau bất thường hoặc nghi ngờ chấn thương thì nghỉ tập và hỏi chuyên gia.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — Dễ quá tải, mất thời gian suy nghĩ

[1 Chốt lịch tuần: 5']
→ [2 Tập nặng buổi trước: 120']
→ [3 Thức dậy thấy cơ thể đau mỏi: 5']
→ [4 Phân vân tìm bài thay thế: 15']  <-- bottleneck
→ [5 Cố tập theo lịch cũ hoặc bỏ tập: 5']
```

### Draft future workflow

```text
FUTURE STATE — 3 phút (Linh hoạt, an toàn)

[1 Log mức độ mỏi cơ vào app: 1']
→ [2 AI check lịch trống & draft bài giãn cơ/thay thế: 1']
→ [3 Người dùng review + chốt lịch: 1']  <-- human boundary
→ [4 Tập luyện an toàn theo lịch mới: 45']

Fallback: AI gợi ý bài tập sai mục tiêu/vẫn quá nặng → Người dùng tự chọn nghỉ ngơi hoàn toàn (Rest day).
```

---

## Problem Card #2 — Hỗ Trợ Xử Lý Merge Conflict Trên Git

**Problem 1 câu:**  
Lập trình viên mới mất nhiều thời gian đọc hiểu phần code chồng chéo khi xảy ra merge conflict, dễ sửa nhầm logic hoặc làm chậm tiến độ merge của nhóm.

**Actor:**  
Lập trình viên mới hoặc thực tập sinh trong dự án nhóm; Tech Lead là người hỗ trợ review khi cần.

**Thời điểm / bối cảnh:**  
Khi pull, rebase hoặc merge branch của nhiều thành viên trước khi tạo Pull Request hoặc release.

**Current workflow:**

```text
1. Kéo code mới hoặc merge branch vào nhánh đang làm.
2. Git báo conflict tại một hoặc nhiều file.
3. Mở file có conflict marker và tự đối chiếu hai đoạn code.
4. Đọc history, hỏi tác giả đoạn code hoặc tra cứu tài liệu để hiểu intent.
5. Sửa thủ công, đánh dấu conflict đã resolve và commit lại.
6. Chạy test hoặc nhờ teammate review trước khi merge.
```

**Bottleneck:**  
Bước 3-4 — hiểu intent của các đoạn code chồng chéo và chọn phần cần giữ mất khoảng 15-30 phút mỗi lần.

**Impact:**  
Merge bị chậm, tiến độ branch/release bị ảnh hưởng; nếu resolve sai có thể tạo hidden bug khó phát hiện sau này.

**Success metric:**  
Giảm thời gian xử lý một merge conflict từ khoảng 15-30 phút xuống dưới 10 phút, không tăng số lỗi phát hiện trong test hoặc code review sau merge.

**Non-AI alternative:**  
Quy ước branch rõ ràng, commit nhỏ, rebase sớm, code owner review và pair programming có thể giảm conflict, nhưng không giúp người mới hiểu nhanh intent của phần code đã chồng chéo.

**AI hypothesis:**  
AI đọc hai phía conflict cùng context lân cận, giải thích điểm khác nhau và draft một hoặc vài phương án resolve. Lập trình viên tự chọn phương án, chạy test và gửi review.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — khoảng 15-30 phút / conflict

[1 Pull / merge branch: 1']
→ [2 Git báo conflict: 1']
→ [3 Đọc marker + đối chiếu code: 10']  <-- bottleneck
→ [4 Tìm intent / hỏi teammate: 10']     <-- bottleneck
→ [5 Sửa, test và review: 8']
```

### Draft future workflow

```text
FUTURE STATE — dưới 10 phút / conflict

[1 Git báo conflict: 1']
→ [2 AI tóm tắt khác biệt + draft phương án: 1']
→ [3 Developer chọn và tự resolve: 3']  <-- human boundary
→ [4 Chạy test + code review: 5']

Fallback: AI thiếu context hoặc draft không an toàn → dừng resolve, hỏi tác giả code hoặc Tech Lead.
Không auto-merge hoặc bỏ qua test.
```

---

## Problem Card #3 — Trợ Lý Tra Cứu Wiki Game/App

**Problem 1 câu:**  
Người chơi game hoặc người dùng app phải liên tục rời màn hình hiện tại để tìm Wiki và đối chiếu thông số, làm gián đoạn trải nghiệm và khó áp dụng thông tin đúng với context đang có.

**Actor:**  
Người chơi game hoặc người dùng app có nhu cầu tra cứu chiến thuật, phân bổ tài nguyên, kỹ năng hoặc thông số.

**Thời điểm / bối cảnh:**  
Khi đang chơi hoặc sử dụng app và cần quyết định build, skill, cách phân bổ tài nguyên hay xử lý một tình huống cụ thể.

**Current workflow:**

```text
1. Gặp tình huống cần chọn chiến thuật hoặc phân bổ tài nguyên.
2. Thoát game/app hoặc chuyển sang trình duyệt.
3. Tìm Wiki, video hướng dẫn hoặc bài viết liên quan.
4. Đối chiếu phiên bản, thông số và tình huống hiện tại.
5. Quay lại game/app để áp dụng hoặc điều chỉnh lựa chọn.
```

**Bottleneck:**  
Bước 2-4 — chuyển ứng dụng, tìm đúng nguồn và đối chiếu thủ công mất khoảng 5-10 phút mỗi lần.

**Impact:**  
Trải nghiệm bị đứt gãy; người dùng có thể chọn sai do nguồn cũ, nguồn không phù hợp phiên bản hoặc không đúng tình huống hiện tại.

**Success metric:**  
Giảm thời gian tìm đúng thông tin áp dụng được từ khoảng 5-10 phút xuống dưới 2 phút; người dùng vẫn tự xác nhận nguồn và quyết định cuối.

**Non-AI alternative:**  
Bookmark Wiki chính thức, in-game guide, build calculator hoặc danh sách nguồn tin cậy có thể giúp tra cứu nhanh hơn, nhưng vẫn yêu cầu người dùng tự chuyển ngữ cảnh và đối chiếu nhiều nguồn.

**AI hypothesis:**  
Người dùng cung cấp context cần thiết như tên game/app, phiên bản, nhân vật hoặc screenshot. Trợ lý tìm trong các nguồn Wiki được duyệt, tóm tắt các lựa chọn kèm link nguồn; người dùng tự quyết định áp dụng.

**Quick gut:**  
Agent.

### Draft current workflow

```text
CURRENT STATE — khoảng 5-10 phút / lần tra cứu

[1 Gặp tình huống cần quyết định: 0.5']
→ [2 Rời game/app hoặc chuyển tab: 0.5']
→ [3 Tìm Wiki/guide: 3']                 <-- bottleneck
→ [4 Đối chiếu phiên bản và thông số: 4'] <-- bottleneck
→ [5 Quay lại áp dụng: 1']
```

### Draft future workflow

```text
FUTURE STATE — dưới 2 phút / lần tra cứu

[1 Người dùng cung cấp context hoặc screenshot: 0.5']
→ [2 Trợ lý truy vấn Wiki đã duyệt: 0.5']
→ [3 Trợ lý tóm tắt lựa chọn kèm nguồn: 0.5']
→ [4 Người dùng kiểm tra và tự chọn: 0.5']  <-- human boundary

Fallback: Không có nguồn đúng phiên bản hoặc confidence thấp → mở Wiki chính thức, không tự động thao tác trong game/app.
```

---

## Card tôi muốn pitch nhất

**Card tôi muốn pitch nhất:** Lịch Tập Luyện Thông Minh.

**Vì sao:** Đây là workflow bản thân trực tiếp trải nghiệm hằng tuần, có bottleneck và thời gian nền tương đối rõ; đồng thời có thể so sánh process fix, Rule và Workflow trước khi quyết định có cần AI hay không.

**Câu hỏi tôi muốn nhóm challenge:** Rule dựa trên lịch tập, mức đau mỏi và Rest Day có đủ an toàn/hiệu quả chưa, hay AI thực sự tạo thêm giá trị ở bước điều chỉnh lịch?

