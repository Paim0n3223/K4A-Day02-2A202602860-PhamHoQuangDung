# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Phạm Hồ Quang Dũng
- Mã học viên: 2A202602860
- Nhóm: A1
- Candidate problem nhóm chọn: Phát hiện và sửa ID switch giữa các frame — người làm multi-object tracking phải xem và đối chiếu hàng nghìn frame để tìm vị trí xảy ra ID switch trước khi sửa annotation (một vòng QA ~50 phút, có thể kéo dài nhiều ngày với dataset lớn)

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Scan 8 problems từ trải nghiệm thật (di chuyển xe bus, ghi chép lớp học, thông báo nhiều kênh, họp nhóm, lên lịch), đủ 4 lăng kính, mỗi dòng kèm số thật do tôi tự ước lượng từ sinh hoạt hằng tuần. Chọn top 3 theo tiêu chí tự đặt: mức khó chịu + khả năng tôi kiểm soát được. Loại #1-#3 (xe bus) vì kẹt xe và giờ xe là yếu tố ngoài tầm kiểm soát, coi như rủi ro phải chấp nhận; loại #6-#7 vì tần suất thấp hơn. | 3 card của tôi vào bảng candidate của nhóm ở vị trí #7, #8, #9, góp phần vào tổng 15 candidate để nhóm cluster và shortlist. |
| Pitch Problem Card | Pitch Card #1 — mất quyền tải slide làm quy trình ghi chép bằng AI đắt lên gấp 6 lần (5 phút → 30 phút/buổi, 5 buổi/tuần ≈ mất thêm 2h/tuần). Điểm tôi nhấn khi pitch: chỗ nghẽn **không nằm ở AI** mà ở quyền truy cập nội dung slide, nên Quick gut của tôi là No AI / process fix chứ không phải chọn AI. | Nhóm ghi nhận đúng theo hướng tôi pitch: "Pain rõ nhưng chưa phải AI problem… nên ưu tiên process fix" (bảng 3.1, #7). |
| Challenge bài của bạn khác | Challenge bài #14 của Trần Long Khánh (xác định root cause khi project AI gặp lỗi) ở điểm scope: bài đang trải rộng từ code, library, CUDA/driver đến hardware nên khó xác định ranh giới làm được trong một pilot. | Câu trả lời của bạn ấy đủ thuyết phục nên tôi không yêu cầu sửa gì thêm. Dù vậy, mối lo về scope vẫn được ghi lại trong nhận xét của nhóm cho #14: "scope hiện rộng, nên thu hẹp vào Jetson/CUDA/TensorRT hoặc một environment cụ thể". |
| Gom trùng / cluster | Tham gia bước gom cluster, xếp cả 3 problem của mình (#7 slide/ghi chép, #8 thông báo nhiều kênh, #9 lên lịch hằng ngày) vào cluster A. | Cluster A được nhóm đặt tên "Họp, thông báo và quản lý việc" với pattern chung là "thông tin nằm rải rác hoặc phải đọc, tóm tắt và chuyển thành task/lịch thủ công", và được ghi chú rằng nhiều bài trong cụm này nên process fix trước khi nghĩ tới AI. |
| Chọn candidate problem | Không có ý kiến phản đối khi nhóm chốt #6 (ID switch), vì #6 có actor và workflow cụ thể hơn, impact đo được bằng metric tracking, và nhóm có dataset thật để làm pilot — trong khi 3 card của tôi chỉ ảnh hưởng đúng 1 người và khó mở rộng thành bài nộp nhóm. | Nhóm chốt #6 với tổng điểm 34/35 ở bảng score 3.4, cao nhất trong shortlist. |
| Validation / research | Không phải người đi tìm nguồn (phần này do Ngô Gia Quốc và Nguyễn Hải Đăng phụ trách). Việc tôi làm là đọc lại các link trong mục 4.2 và kiểm tra mức độ uy tín của nguồn — xem đây có phải repo/tài liệu chính thức hay không, thay vì nhận số liệu mà không verify. | Ba nguồn được giữ lại đều là nguồn chính thức kiểm được: repo TrackEval, tài liệu CVAT và tài liệu Ultralytics. Điều này giúp nhóm giữ đúng nguyên tắc của worksheet là không dùng số liệu AI đưa nếu không verify được link chính thức. |
| Workflow nhóm | Đề xuất phiên bản đầu tiên của workflow cho bài ID switch, trước khi nhóm chỉnh sửa và bổ sung thành bản 7 bước như trong mục 5.1 hiện tại. | Bản đầu của tôi là điểm khởi đầu để nhóm bàn tiếp; bản cuối giữ mạch "chạy tracker → xem tuần tự → đối chiếu → xác nhận frame switch → sửa → lưu" và bổ sung thời gian từng bước cùng bước QA cuối.|
| Problem Statement | Chủ yếu đọc và rà lại bản draft, không phải người chấp bút. Tôi đồng ý với hướng thu hẹp ở v1: hệ thống chỉ flag/xếp hạng đoạn nghi vấn, còn con người xác nhận và sửa. | Không có thay đổi nào do tôi đề xuất ở phần này. |
| Rule / Workflow / Agent | Đọc và đồng ý với mức Workflow (Rule + AI scoring + human review) mà nhóm chọn, không phải người đưa ra lập luận. Lý do tôi thấy thuyết phục: các bước đi theo thứ tự cố định và người luôn là gate trước khi dữ liệu bị sửa, nên không cần đến năng lực tự lập kế hoạch của Agent. | Không có thay đổi nào do tôi đề xuất ở phần này. |
| Decision | Đọc và đồng ý với quyết định "Not Yet", không tranh luận. Tôi thấy lý do hợp lý vì bằng chứng pain hiện mới là self-report của một thành viên, chưa có interview/survey độc lập và chưa có ground truth để đo recall/precision. | Không có thay đổi nào do tôi đề xuất ở phần này. |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Dấu tay rõ nhất là phiên bản đầu tiên của workflow bài ID switch do tôi đề xuất — bản 7 bước ở mục
5.1 được phát triển lên từ đó. Ngoài ra, ba card của tôi (#7, #8, #9) không được chọn làm bài chính
nhưng lại được nhóm dùng làm bằng chứng cho việc nhóm không cố dùng AI cho mọi vấn đề: bảng tổng
kết Phase 3 ghi rõ #7 và #9 là ví dụ tốt cho thấy nhóm biết khi nào nên process fix thay vì AI, và
điều đó đến từ chính cách tôi viết card — tôi tự tick Quick gut là "No AI / process fix" cho cả ba
card thay vì mặc định chọn AI.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Nhờ Claude gợi ý các đầu việc hằng tuần của sinh viên năm 3 để làm điểm xuất phát, sau đó tự kể từng tình huống thật và nhờ AI hỏi ngược để làm rõ. | Tách "đi xe bus 3h/ngày" thành 3 problem riêng (chờ xe / chuyển trạm / kẹt xe) thay vì nhồi vào một dòng. Liên tục đòi số cụ thể nên mỗi dòng đều có tần suất hoặc thời lượng, không có dòng chung chung. | Gợi ý một loạt đầu việc không phải của tôi: thực tập/part-time, báo cáo tiến độ cho công ty, viết README dự án cá nhân — đúng kiểu mẫu "sinh viên nói chung" chứ không phải sinh hoạt thật của tôi. | Bỏ hết các đầu việc tôi không thực sự làm, chỉ giữ 3 việc thật (đi học, làm nhóm, quản lý lịch trình). Toàn bộ con số trong bảng scan là tôi tự cung cấp từ trải nghiệm, AI không tự đặt được số nào. |
| Problem Card | Dùng AI dựng bản nháp 3 Problem Card (workflow, bottleneck, metric, non-AI alternative) trước khi tự chỉnh sửa chi tiết và nhờ AI chỉ ra điểm yếu của card; AI cũng hỗ trợ dựng khung phần pitch và gợi ý câu hỏi challenge ở mục 2.3. | Chỉ ra 5 điểm yếu của Card #1, trong đó có 2 điểm tôi chưa nghĩ tới: (1) chỉ cần đi xin file slide là vấn đề tự hết, nên phải trả lời được vì sao vẫn đáng làm; (2) đo bằng thời gian có thể sai bản chất, vì 30 phút tự duyệt slide có khi giúp học tốt hơn 5 phút đọc bản AI tóm tắt. | Tự chia thời lượng từng bước (5'/10'/8'/2'/5') cho khớp tổng 30 phút chứ không dựa trên dữ liệu thật. Giả định "chụp hết slide rồi để AI lọc sẽ nhanh hơn tự lọc" mà không có bằng chứng. Số "15-20 phút/ngày quét tin" ở Card #2 là suy ra từ phép nhân, không phải tôi bấm giờ. | Tự chọn top 3 theo tiêu chí của mình (mức khó chịu + khả năng kiểm soát được), không theo thứ tự AI đề xuất. Ghi rõ trong card rằng các con số là tự ước lượng và cần bấm giờ để xác nhận. Tự tick Quick gut là "No AI / process fix" cho cả 3 card thay vì mặc định chọn AI. Phần pitch/challenge ở mục 2.3 tôi đọc lại và viết lại thành lời của mình. |
| Workflow | Với 3 card cá nhân: dùng AI vẽ lại sơ đồ current state / future state dạng ASCII. Với workflow nhóm: `Không dùng` — phiên bản đầu tiên tôi tự đề xuất rồi nhóm bàn tiếp. | Sơ đồ trước/sau giúp nhìn ra ngay bước nào phình lên: workflow cũ 3 bước/5 phút so với workflow hiện tại 5 bước/30 phút. | Thời gian từng bước trong sơ đồ vẫn là con số AI tự chia, nên sơ đồ trông chặt hơn thực tế. | Tự xác định bottleneck nằm ở bước tự lọc và chụp slide, và tự đặt human boundary ở bước người kiểm lại bản tóm tắt. Bản workflow nhóm là ý của tôi, không qua AI. |
| Research | `Không dùng` để tìm nguồn — phần này do Ngô Gia Quốc và Nguyễn Hải Đăng phụ trách. Tôi tự mở từng link và tự đánh giá độ uy tín. | — | — | Worksheet yêu cầu không dùng số liệu nếu không verify được link chính thức, nên tôi tự kiểm bằng mắt thay vì để AI xác nhận hộ. Kết quả: 3 nguồn giữ lại đều là repo/tài liệu chính thức (TrackEval, CVAT, Ultralytics). |
| Problem Statement | `Không dùng` — bản PS v0/v1 do nhóm chấp bút, tôi đọc và rà lại. | — | — | Tôi tự đối chiếu xem boundary có khớp với workflow không, và đồng ý với hướng thu hẹp ở v1: hệ thống chỉ flag/xếp hạng, người xác nhận và sửa. |
| Rule / Workflow / Agent | Với 3 card cá nhân: dùng AI phản biện xem nên chọn mức nào. Với bài nhóm: `Không dùng` — nhóm tự lập luận, tôi đọc và đồng ý. | Với card cá nhân, AI chỉ ra rằng AI không phải chỗ đang nghẽn: Claude vẫn tóm tắt tốt cả PDF lẫn ảnh, chỗ nghẽn là quyền truy cập slide. Đây là lý do tôi hạ xuống No AI / process fix. | Ở Card #3, AI ban đầu nói có thể xếp lịch hộ, nhưng thực tế tôi chưa từng log thời gian nên AI không có dữ liệu nào để ước lượng — tức là đề xuất nghe được nhưng không chạy được với đầu vào hiện tại. | Tự kết luận Card #3 là ca "chưa đến lúc dùng AI": phải ghi lịch ra và log thời gian thật trước, có dữ liệu rồi mới bàn tới AI. Với bài nhóm, tôi tự kiểm lại lập luận vì sao Workflow đủ và Agent là quá mức trước khi đồng ý. |
| Decision | `Không dùng` — nhóm tự chốt Not Yet. | — | — | Tôi tự soát lại bằng chứng trước khi đồng ý: pain mới là self-report của một thành viên, chưa có interview/survey độc lập, chưa có ground truth để đo recall/precision. Thấy Not Yet là trung thực hơn Go nên tôi không phản đối. |

> Nếu phase nào không dùng AI, ghi `Không dùng` và vì sao tự làm.

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):
- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Điều khó nhất khi viết Problem Statement là gì, metric hay boundary?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Điều tôi học rõ nhất khi nghe top 3 của các bạn khác là khoảng cách về độ rộng của actor. Ba
problem của tôi đều xoay quanh chính tôi — không tải được slide, thông báo rải trên 4 kênh, tự lên
lịch hằng ngày — nên dù có số đo thật thì vẫn chỉ ảnh hưởng đúng một người. Trong khi đó bài ID
switch của Quốc hay bài prompt regression của Đăng có actor là cả một nhóm người làm cùng công
việc, nên impact nhân lên theo số người và số dataset. Đó là lý do tôi không phản đối khi nhóm
chọn #6 thay vì card của mình, dù card của tôi cũng có số rõ.

Nhóm tôi không bị solution-first, và tôi nghĩ đó là điểm tốt nhất của bản nộp. Ở Phase 6, bài toán
rơi vào ô "mơ hồ cao – phức tạp cao" nên hoàn toàn có lý để đòi làm Agent, nhưng nhóm vẫn chốt
Workflow vì các bước đi theo thứ tự cố định và người phải là gate trước khi dữ liệu bị sửa. Ba
card của tôi cũng đi theo hướng đó: cả ba tôi đều tự tick "No AI / process fix" chứ không mặc định
chọn AI, và cuối cùng hai trong ba card được nhóm dùng làm ví dụ chứng minh nhóm không cố dùng AI
cho mọi vấn đề.

Điều khó nhất khi viết Problem Statement với tôi là metric, không phải boundary. Boundary tương đối
dễ vì chỉ cần nói rõ AI được làm gì và không được làm gì. Còn metric thì nhóm viết ra được những
con số nghe rất chặt — recall ≥90%, precision ≥70%, giảm thời gian QA ≥70% — nhưng khi soát lại
thì baseline 50 phút chỉ là một thành viên tự nhớ lại, và để đo được recall thì cần ground truth
mà nhóm chưa có. Tôi học được rằng một metric chỉ có giá trị khi nói được luôn cách đo và dữ liệu
lấy từ đâu, không thì nó chỉ là con số cho đẹp bài.

Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở Phase 4. Bảng validation hiện ghi 0 interview và 0
survey, toàn bộ pain dựa trên self-report của một thành viên; nhóm có ghi trung thực chỗ này nhưng
lẽ ra tôi nên lên tiếng sớm hơn để nhóm dành 15 phút phỏng vấn 2 người, vì đó là thứ duy nhất có
thể đổi quyết định từ Not Yet sang Go. Tôi cũng phải thừa nhận mình dùng AI khá nhiều ở phần cá
nhân: AI dựng khung 3 Problem Card và chỉ ra điểm yếu mà tôi chưa nghĩ tới, nhưng nó cũng tự chia
thời lượng từng bước cho khớp tổng 30 phút và gợi ý những đầu việc không phải của tôi. Phần tôi
thực sự tự làm là chọn vấn đề nào là pain thật, cung cấp toàn bộ con số từ trải nghiệm, và tự quyết
định hạ cả ba card xuống mức process fix.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards — 8 problems, đủ 4 lăng kính, 3 card đủ field
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1) — pitch Card #1, challenge scope bài #14
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài — 15 candidates → 4 cluster → shortlist 3 → score → chọn #6
- [x] [15đ] Nhóm có workflow trước/sau — mục 5.1 (7 bước, ~50 phút) và 5.2 (future + fallback)
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ — mục 5.3 và 6.2, boundary có làm/không làm
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent — mục 6.1, chọn Workflow và giải thích vì sao không Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ — Not Yet, kèm danh sách cần validate trước
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI

