# second-brain-file-ai

**Bộ khung dựng Bộ Não Thứ 2** — dành cho thành viên Creator CEO / Creator Việt Nam.

Ném thư mục này vào một công cụ AI bậc 2, nhắn *"bắt đầu"*, trả lời phỏng vấn — bạn có một bộ não thứ 2 chạy được thật trong 5–10 tiếng.

> **Phiên bản:** `v3.2` · 2026-09-07 — xem [CHANGELOG.md](CHANGELOG.md)

---

## Cài đặt

### Cách 1 — `git clone` *(khuyên dùng)*

Bộ khung này còn tiến hoá. Clone thì sau này gõ một lệnh là có bản mới nhất.

```bash
git clone https://github.com/creator-ceo/second-brain-file-ai.git
cd second-brain-file-ai
```

Cập nhật về sau:

```bash
git pull
```

### Cách 2 — tải file zip

Chưa quen `git` thì tải bản `.zip`, giải nén là dùng được ngay. Đổi lại: có bản mới thì phải tải lại thủ công, và bạn sẽ không biết lúc nào có bản mới.

---

## Bắt đầu

1. Mở công cụ AI **bậc 2** — Claude Cowork, Claude Code, Codex CLI, hoặc AntiGravity.
   *(Chatbot thường như ChatGPT web không dùng được: nó không ghi file ra máy bạn, mà bộ não thứ 2 chính là các file trên máy bạn.)*
2. **Mở công cụ NGAY TRONG thư mục này** — xem mục dưới, đây là chỗ hay sai nhất.
3. Nhắn: **`bắt đầu`**

AI tự tạo `SecondBrain/` rồi phỏng vấn bạn từng câu.

### ⚠️ Chỗ hay sai nhất — phải mở đúng thư mục

`CLAUDE.md` và 3 lệnh `/onboard` `/nap-kho` `/kiem-chung` **chỉ được nạp khi thư mục này là gốc của phiên làm việc**. Clone về rồi vẫn ngồi ở thư mục cũ thì AI không thấy gì cả.

**Dấu hiệu bạn đang sai chỗ:** nhắn *"bắt đầu"* mà AI trả lời như một AI bình thường — không hỏi ngược, không tạo thư mục `SecondBrain/`, gõ `/` không thấy 3 lệnh trên. Bộ khung không hỏng, chỉ là chưa được nạp.

**Claude Code:**
```bash
git clone https://github.com/creator-ceo/second-brain-file-ai.git
cd second-brain-file-ai
claude
```
Ba dòng, theo đúng thứ tự. Dòng `cd` là dòng quan trọng nhất — thiếu nó thì hai dòng kia vô nghĩa.

*(Nếu bạn nhờ AI clone hộ: clone xong phải **thoát ra, `cd` vào thư mục vừa tạo, mở lại** ở đó. Clone trong cùng một phiên rồi nhắn tiếp thì phiên đó vẫn chưa nạp `CLAUDE.md`.)*

**Claude Cowork / AntiGravity:** kéo cả thư mục `second-brain-file-ai` vào cửa sổ, hoặc chọn nó làm workspace — không chọn thư mục cha chứa nó.

**🪟 Máy Windows:** ba dòng lệnh y hệt, gõ trong **PowerShell**. Claude Code có bản chạy thẳng trên Windows, **không cần WSL** — cài bằng `irm https://claude.ai/install.ps1 | iex`. Bốn chỗ hay vấp (lệnh `claude` không nhận, chưa có git, đường dẫn có dấu cách, thư mục ẩn `.claude`) đã ghi ở [`reference/huong-dan-cai-dat.md`](reference/huong-dan-cai-dat.md).

**Codex CLI:**
```bash
git clone https://github.com/creator-ceo/second-brain-file-ai.git
cd second-brain-file-ai
codex
```
Codex đọc [`AGENTS.md`](AGENTS.md) thay vì `CLAUDE.md` — file đó có sẵn trong bộ này và trỏ ngược về `CLAUDE.md`, nên nội dung y hệt.

Khác biệt duy nhất: **Codex không có lệnh gạch chéo** cho 3 skill, vì nó tìm skill ở `.codex/skills/` còn bộ này để ở `.claude/skills/`. Thay vào đó bạn gọi **bằng lời**: *"dựng bộ não cho tôi"*, *"lưu cái này vào não"*, *"kiểm chứng bộ não"*. `AGENTS.md` đã dặn sẵn AI mở đúng file khi nghe những câu đó. *(Muốn có lệnh `/` thì xem mục cuối `AGENTS.md`.)*

**Kiểm nhanh trước khi bắt đầu:**
- Claude Code / Cowork: gõ `/` và tìm `/onboard`. Thấy là đúng chỗ.
- Codex: hỏi *"bạn đang đọc luật từ file nào?"* — trả lời có `AGENTS.md` hoặc `CLAUDE.md` là đúng chỗ.

Không thấy gì thì bạn đang ở sai thư mục — đừng nhắn tiếp, thoát ra `cd` vào rồi mở lại.

📍 **Toàn bộ lộ trình 8 việc:** [BAT-DAU-TU-DAY.md](BAT-DAU-TU-DAY.md) — tick từng ô, vừa là bản đồ vừa là bằng chứng.

---

## Bộ não của bạn trông như thế nào

AI sẽ tạo ra một thư mục `SecondBrain/` ngay cạnh các file này:

```
SecondBrain/
  raw/          nguồn gốc — bài viết cũ, transcript, ghi chép bạn thả vào
                ⛔ AI KHÔNG BAO GIỜ được sửa thư mục này
  wiki/         10 trang AI viết ra, nối nhau bằng [[liên kết]]
                  chân dung:  about-me · values-and-principles · contrarian-beliefs
                              decision-style · network
                  dùng chung: target-customer · offer-ladder · goals
                              ai-operating-preferences · systems-and-stack
  index.md      bản đồ — liệt kê cả trang CHƯA có, kèm cột "ai lấp"
  log.md        nhật ký — mỗi lần nạp một dòng, chỉ thêm không xoá
```

Rồi ba thư mục nữa **mọc lên khi bạn nạp**, không tạo rỗng chờ sẵn — `/nap-kho` dựng chúng lúc ghi file đầu tiên:

```
  wiki/people/     mỗi người một trang — NHẬT KÝ QUAN HỆ, không phải danh bạ.
                   Nối thêm mỗi lần gặp lại, không viết đè.
  wiki/projects/   mỗi dự án một trang — SỔ QUYẾT ĐỊNH: chốt gì, ngày nào, vì sao.
  wiki/learnings/  thứ bạn hấp thụ từ ngoài, gom theo CHỦ ĐỀ chứ không theo nguồn.
```

⚡ **Đúng 10 trang, và thư mục `wiki/` sạch trơn ngoài chúng.** Không có file rỗng nào chờ sẵn.

Cài thêm một vai — Content chẳng hạn — thì **vai đó** dựng kho của nó: `voice-profile`, `hook-library`, `models/`… Vai nào chưa cài thì trang của nó chưa tồn tại, và `index.md` nói rõ ai là chủ của nó.

> **Vì sao không tạo sẵn file rỗng cho gọn:** một file rỗng còn chủ và một file rỗng đã mất chủ **trông y hệt nhau**. Đã mắc thật: `nut-that.md` được dựng sẵn kèm dòng *"trang này sinh ra từ việc X"*, rồi việc X chuyển sang vai khác — để lại một file trỏ vào lệnh không có trong máy, mà không có gì báo. Một dòng trong `index.md` thì luôn nói được chủ của nó là ai.

Đây là mẫu **LLM Wiki** của Andrej Karpathy (thành viên sáng lập OpenAI). Khác biệt nằm ở một chỗ:

> Chatbot thông thường **suy luận lại từ đầu** mỗi lần bạn hỏi — dùng 100 lần vẫn y như lần đầu.
> Bộ não thứ 2 thì **biên tập** những gì bạn đưa vào thành các trang dày, liên kết chéo. Mỗi lần dùng là một lần nó dày thêm.
>
> **Ngừng suy luận lại từ đầu, bắt đầu tích luỹ.**

Khung này đã được thiết kế sẵn — bạn **không cần tự nghĩ ra cấu trúc**, chỉ cần trả lời câu hỏi. Và vì nó là file markdown thuần trên máy bạn, nó là **của bạn**: đổi công cụ AI, đổi máy, hay ngừng trả phí đều không mất.

---

## Trong này có gì

```
CLAUDE.md                    luật vận hành — Claude Code/Cowork tự đọc mỗi phiên
AGENTS.md                    bản cho Codex CLI — trỏ về CLAUDE.md, không lặp nội dung
BAT-DAU-TU-DAY.md            checklist 7 việc
START-HERE.txt               hướng dẫn 1 phút

.claude/skills/
  onboard/                   dựng bộ não lần đầu
  nap-kho/                   đường ghi DUY NHẤT vào wiki
  kiem-chung/                Việc 6 — bài test bộ não đã lưu thật chưa

templates/                   khung 10 trang nền + index + log
  khung-lap-lai/             khung cho people · projects · learnings

reference/
  huong-dan-cai-dat.md       Việc 1 + Việc 5 + bảng tra lỗi
  luat-du-lieu-nhay-cam.md   ĐỌC TRƯỚC khi nạp dữ liệu khách hàng
  Persona-Extraction-Protocol.md   bộ 48 câu hỏi sâu
  Notion-Build-Kit-advanced.md     nếu bạn muốn dùng Notion thay vì file
```

---

## Ba lệnh — và đó là toàn bộ bộ khung này

| Lệnh | Làm gì | Bao lâu một lần |
|---|---|---|
| `/onboard` | **dựng** bộ não lần đầu, hoặc dựng lại từ đầu nếu cần | một lần |
| `/nap-kho` | **ghi** vào bộ não — chuyện mới, insight mới, tài liệu mới. **Đường ghi duy nhất**, đừng sửa tay file `.md` | mỗi lần có gì đáng nạp |
| `/kiem-chung` | **kiểm** bộ não — Việc 6, chạy sau khi dựng xong và sau mỗi lần nạp khối lớn | sau mỗi khối lớn |

📌 **Ba lệnh này cố ý ít.** Bộ khung chỉ làm đúng một việc: **xây và giữ cái bộ não**. Còn *dùng* bộ não để viết bài, thiết kế, bán hàng, chốt việc của tháng — đó là các **vai nhân sự A.I**, cài rời ở kho riêng. Xem mục ngay dưới.

⚠️ **`/banh-xe-cuoc-doi` đã rời khỏi bộ khung từ v3.0.** Nó là bài lập kế hoạch, không phải việc xây bộ não — nay thuộc vai Điều phối, chưa phát. Có sẵn một bản kế hoạch (bánh xe, OKR, kế hoạch 90 ngày) thì cứ đưa cho AI ở Việc 3, `/onboard` dùng thẳng làm `goals.md`. Chưa có cũng chạy được hết lộ trình.

---

## ⚠️ Hai điều đọc trước khi bắt đầu

**1. Bộ não của bạn KHÔNG nằm trong repo này.**
AI sẽ tạo thư mục `SecondBrain/` — thư mục đó đã được `.gitignore` chặn sẵn. Nghĩa là dữ liệu khách hàng, doanh thu, chuyện riêng của bạn **không bao giờ bị đẩy lên** khi bạn `git push`.

Đừng gỡ dòng `SecondBrain/` khỏi `.gitignore`. Một lần push nhầm là đủ, và xoá file sau đó không cứu được — lịch sử git vẫn giữ.

**2. Đọc `reference/luat-du-lieu-nhay-cam.md` trước khi nạp khách hàng.**
Mất 3 phút. Bộ não này sắp chứa tên người thật và chuyện của người khác.

---

## Cập nhật bộ khung mà không mất bộ não

Bộ khung này còn tiến hoá — xem [CHANGELOG.md](CHANGELOG.md) để biết bản mới đổi gì.

Điểm mấu chốt: **`SecondBrain/` hoàn toàn tách rời khỏi file khung.** Nên cập nhật = thay cái khung, bê bộ não sang. Không bao giờ phải trộn hai thứ.

### Nếu bạn cài bằng `git clone`

```bash
cd second-brain-file-ai
git pull
```

`.gitignore` chặn `SecondBrain/`, nên `git pull` **không đụng được** vào dữ liệu của bạn dù có muốn. Nếu bạn từng sửa file khung và `git pull` báo xung đột: giữ bản của bạn hay lấy bản mới đều được — bộ não không bị ảnh hưởng.

### Nếu bạn cài bằng file zip

1. Tải bản mới → giải nén → được thư mục `second-brain-file-ai` **mới**
2. Mở thư mục **cũ**, kéo nguyên thư mục **`SecondBrain`** sang thư mục **mới**
3. Xoá thư mục cũ, mở công cụ AI trong thư mục mới

Kéo một lần là xong. Bộ não của bạn là một thư mục khép kín — không có file nào của nó nằm lẫn ngoài.

### ⛔ Đừng nhờ AI "tự đọc bản mới rồi bổ sung phần còn thiếu"

Nghe tiện, nhưng câu đó mơ hồ giữa hai thứ khác hẳn nhau: thiếu **file khung**, hay thiếu **nội dung trong bộ não của bạn**. AI rất dễ hiểu sang nghĩa thứ hai, rồi tự tạo và tự điền các trang trong `wiki/` — phá Luật sắt số 2, và nếu không có dữ liệu thật thì nó **bịa để lấp chỗ trống**.

Thay khung bằng hai cách trên thì chắc chắn và kiểm được. AI chỉ nên dùng để **xác nhận sau khi thay**, không dùng để thay.

### Kiểm sau khi cập nhật — 2 câu

1. *"Phiên bản khung đang là bao nhiêu?"* → phải khớp số ở đầu `CLAUDE.md`
2. Chạy `/kiem-chung` → bộ não vẫn trả lời đúng như trước là dữ liệu còn nguyên

---

## Đóng góp ngược

Dùng thấy chỗ nào tắc, câu hỏi nào thừa, khung trang nào thiếu — báo lại trong nhóm. Bộ khung này lớn lên bằng đúng cách đó: người dùng thật gặp chỗ vướng thật.

---

## Ai làm bộ khung này

**Tô Hải Đoàn** — người làm nội dung và xây thương hiệu cá nhân tại Việt Nam. Bộ khung này là cách tôi tổ chức bộ não thứ 2 của chính mình, đóng gói lại để bạn dựng bản của bạn.

**Kẹt ở bước nào, hoặc muốn được hướng dẫn** thì nhắn tôi: **[facebook.com/tohaidoan](https://www.facebook.com/tohaidoan/)**

---

## Cài thêm vai nhân sự A.I

Bộ khung này là **cái nền** — dữ liệu và sáu lệnh ở trên. Các vai làm việc (viết content, thiết kế, bán hàng, chăm sóc) nằm ở **kho riêng, cài rời**, vì phần lớn người ta chỉ cần một vai chứ không cần cả đội.

Cài xong nền rồi thì thêm vai bằng hai lệnh:

```bash
claude plugin marketplace add creator-ceo/nhan-su-content
claude plugin install content
```

| Vai | Kho | Trạng thái |
|---|---|---|
| ✍️ **Content** — viết bài, hook, ý tưởng, kịch bản video, mindmap | `creator-ceo/nhan-su-content` | ✅ cài được |
| 🎛️ Điều phối · 🎨 Thiết kế · 💰 Bán hàng · 🤝 Chăm sóc · 🔍 Nghiên cứu | — | ⬜ đang đóng gói |

⚠️ **Vai cần nền chạy trước.** Vai Content đọc `wiki/voice-profile.md`, `wiki/experiences-library.md`… — những trang do `/onboard` và `/nap-kho` dựng ra. Cài vai lên một thư mục trống thì nó chạy được nhưng viết bằng trí nhớ chung chung, không phải bằng chất liệu của bạn.
