# SEO MONITORING & REPORTING — XIAOMI247.COM

> **Domain:** xiaomi247.com
> **Cập nhật:** Tháng 3/2026
> **Tham chiếu:** [SEO Strategy](../marketing/02-seo/seo-strategy.md) | [KPIs Dashboard](../marketing/06-measurement/kpis-dashboard.md)

---

## 1. CÔNG CỤ MONITORING

### Bảng so sánh công cụ

| Công cụ | Chi phí | Chức năng chính | Mức độ cần thiết | Ghi chú |
|---------|---------|-----------------|-------------------|---------|
| **Google Search Console** | Free | Indexing, errors, queries, CTR, impressions | ⭐ BẮT BUỘC | Dữ liệu trực tiếp từ Google |
| **Google Analytics 4** | Free | Traffic, conversions, user behavior | ⭐ BẮT BUỘC | Cần setup Enhanced Ecommerce |
| **Screaming Frog** | Free (500 URLs) / $259/năm | Technical audit, crawl errors, broken links | ⭐ BẮT BUỘC (bản free đủ giai đoạn đầu) | Upgrade khi site >500 trang |
| **Ahrefs** | $99–399/tháng | Backlinks, keyword ranking, competitor analysis | 🔶 RẤT NÊN CÓ | Gói Lite $99 đủ dùng cho xiaomi247 |
| **SEMrush** | $130–500/tháng | Keyword research, site audit, position tracking | 🔶 THAY THẾ Ahrefs | Chọn 1 trong 2: Ahrefs HOẶC SEMrush |
| **Ubersuggest** | Free (giới hạn) / $29/tháng | Keyword ideas, content ideas, site audit cơ bản | ⚪ OPTIONAL | Dùng free khi chưa có budget cho Ahrefs |
| **UptimeRobot** | Free (50 monitors) | Uptime monitoring, response time | ⭐ BẮT BUỘC | Setup alert qua email + Telegram |
| **PageSpeed Insights** | Free | Core Web Vitals, performance score | ⭐ BẮT BUỘC | Chạy thủ công hàng tháng |

### Khuyến nghị theo giai đoạn

**Tháng 1–3 (Budget thấp):**
- GSC + GA4 + Screaming Frog Free + UptimeRobot Free + Ubersuggest Free
- **Chi phí: 0đ**

**Tháng 4–6 (Bắt đầu đầu tư):**
- Thêm Ahrefs Lite ($99/tháng) — theo dõi keyword ranking + backlinks + competitor
- **Chi phí: ~2.5M VNĐ/tháng**

**Tháng 7–12 (Scale up):**
- Upgrade Screaming Frog nếu site >500 trang
- Giữ Ahrefs Lite hoặc upgrade Standard nếu cần
- **Chi phí: ~3–5M VNĐ/tháng**

---

## 2. WEEKLY SEO CHECK — 15 Phút/Tuần (Mỗi thứ 2)

### Checklist nhanh

| # | Hạng mục | Công cụ | Thời gian | Check gì |
|---|----------|---------|-----------|----------|
| 1 | **GSC Errors** | Google Search Console → Pages | 3 phút | Errors mới, Not indexed tăng? Valid pages giảm? |
| 2 | **Indexing Status** | GSC → Pages → xem trend | 2 phút | Số trang indexed có tăng theo content mới? |
| 3 | **Top Queries Changes** | GSC → Performance → Queries | 3 phút | Top 20 queries: position tăng/giảm bất thường? CTR thay đổi? |
| 4 | **404 Errors mới** | GSC → Pages → Not found (404) | 2 phút | URLs mới bị 404? Fix redirect nếu có |
| 5 | **Uptime Check** | UptimeRobot dashboard | 1 phút | Downtime tuần qua? Response time bình thường? |
| 6 | **Security Issues** | GSC → Security & Manual Actions | 1 phút | Có manual action hoặc security issue mới? |
| 7 | **Quick Traffic Glance** | GA4 → Acquisition → Organic | 3 phút | Organic traffic tuần này vs tuần trước? Anomaly? |

### Quy trình thực hiện

```
Mỗi thứ 2 sáng (9:00 - 9:15):
1. Mở GSC → kiểm tra errors + indexing (5 phút)
2. GSC Performance → scan top queries changes (3 phút)
3. UptimeRobot → check uptime (1 phút)
4. GA4 → quick organic traffic check (3 phút)
5. Ghi note nếu có anomaly → tạo action item
```

### Khi nào cần escalate

| Tín hiệu | Mức độ | Action |
|-----------|--------|--------|
| Traffic giảm >20% so tuần trước | 🔴 Urgent | Investigate ngay: Google update? Server issue? De-index? |
| 404 errors tăng >10 URLs mới | 🟡 Warning | Check + setup redirects trong ngày |
| GSC Manual Action | 🔴 Critical | Stop mọi thứ, fix ngay lập tức |
| Uptime <99% | 🟡 Warning | Liên hệ hosting provider |
| Keyword chính rớt >5 positions | 🟡 Warning | Analyze nguyên nhân trong 48h |

---

## 3. MONTHLY SEO AUDIT — 2 Giờ/Tháng (Ngày 1 hàng tháng)

### Checklist chi tiết

#### A. Technical Audit — Screaming Frog Full Crawl (45 phút)

| # | Check | Cách làm | Target |
|---|-------|----------|--------|
| 1 | **Crawl toàn site** | Screaming Frog → nhập xiaomi247.com → Start | Crawl xong không lỗi |
| 2 | **Broken links (4xx)** | Tab: Response Codes → Client Error 4xx | 0 broken links |
| 3 | **Server errors (5xx)** | Tab: Response Codes → Server Error 5xx | 0 server errors |
| 4 | **Missing titles** | Tab: Page Titles → filter Missing/Duplicate | Mọi trang có title unique |
| 5 | **Missing meta descriptions** | Tab: Meta Description → filter Missing | Mọi trang có meta description |
| 6 | **Missing H1** | Tab: H1 → filter Missing/Duplicate | Mỗi trang 1 H1 unique |
| 7 | **Missing alt text** | Tab: Images → filter Missing Alt Text | >90% images có alt text |
| 8 | **Redirect chains** | Tab: Response Codes → Redirects 3xx | Không có redirect chain >2 hops |
| 9 | **Canonical issues** | Tab: Canonicals → filter issues | Mọi trang có canonical đúng |
| 10 | **Duplicate content** | Tab: URL → filter Near Duplicates | 0 near duplicates |



#### B. GSC Coverage Review (20 phút)

| # | Check | Nơi xem | Ghi chú |
|---|-------|---------|---------|
| 1 | **Valid pages trend** | GSC → Pages → Valid | Phải tăng khi publish content mới |
| 2 | **Excluded pages** | GSC → Pages → Not indexed | Review lý do: Crawled not indexed? Noindex? Duplicate? |
| 3 | **Crawl stats** | GSC → Settings → Crawl stats | Crawl rate ổn định? Response time <500ms? |
| 4 | **Sitemaps** | GSC → Sitemaps | Submitted = Indexed? Errors? |
| 5 | **Mobile usability** | GSC → Mobile Usability | 0 errors |

#### C. Core Web Vitals Check (15 phút)

| Metric | Target | Công cụ | Cách đo |
|--------|--------|---------|---------|
| **LCP** (Largest Contentful Paint) | ≤ 2.5s | PageSpeed Insights + GSC | Test trang chủ + 3 trang sản phẩm + 1 blog |
| **INP** (Interaction to Next Paint) | ≤ 200ms | PageSpeed Insights | Test trên mobile + desktop |
| **CLS** (Cumulative Layout Shift) | ≤ 0.1 | PageSpeed Insights | Chú ý images không có width/height |

**Trang cần test hàng tháng:**
- Trang chủ: `xiaomi247.com`
- Danh mục chính: `/tivi-xiaomi/`, `/robot-hut-bui-xiaomi/`, `/tu-lanh-xiaomi/`
- Trang sản phẩm bán chạy nhất (top 3)
- Blog post mới nhất

#### D. Keyword Ranking Update (20 phút)

| # | Việc cần làm | Công cụ | Output |
|---|-------------|---------|--------|
| 1 | Export keyword rankings | Ahrefs/GSC | Bảng top keywords + positions |
| 2 | So sánh với tháng trước | Excel/Sheets | Columns: Keyword, Position trước, Position nay, Change |
| 3 | Phân loại keywords | Manual | Top 3 / Top 10 / Top 20 / Top 50 / Chưa rank |
| 4 | Identify top movers | Sort by change | Top 5 tăng + Top 5 giảm |
| 5 | Update KPI tracking | KPI Dashboard | Cập nhật bảng tracking tháng |

#### E. Backlink Profile Review (10 phút)

| # | Check | Công cụ | Action |
|---|-------|---------|--------|
| 1 | **New backlinks** | Ahrefs → New referring domains | Ghi nhận domains mới |
| 2 | **Lost backlinks** | Ahrefs → Lost referring domains | Outreach lại nếu link quan trọng |
| 3 | **Toxic backlinks** | Ahrefs → filter low DR spam | Disavow nếu cần (thận trọng) |
| 4 | **Referring domains count** | Ahrefs → Overview | So sánh với target KPI |
| 5 | **DR/DA update** | Ahrefs → Overview | Track xu hướng tăng |

#### F. Content Performance (10 phút)

| # | Check | Công cụ | Output |
|---|-------|---------|--------|
| 1 | **Top 10 blog posts by organic traffic** | GA4 → Explore → Blog pages | Bài nào mang traffic nhiều nhất |
| 2 | **Content decay** | GSC → filter blog → compare periods | Bài nào traffic giảm → cần update |
| 3 | **Conversion from organic** | GA4 → Conversions → filter Organic | Organic mang lại bao nhiêu conversions |
| 4 | **Content gap** | GSC → Queries low CTR + high impressions | Keywords có impressions cao nhưng CTR thấp → optimize title/meta |

---

## 4. QUARTERLY SEO REVIEW — Nửa Ngày/Quý

### Agenda (4 tiếng)

| Thời gian | Hạng mục | Chi tiết |
|-----------|----------|----------|
| **9:00 – 9:45** | Strategy Review | KPI vs Target theo bảng SEO Strategy Phần 6. Đạt/không đạt từng metric. Root cause cho metrics off-track |
| **9:45 – 10:30** | Competitor Analysis Update | Crawl lại competitors (mivietnam.vn, mihanoi.vn, xiaomimall.vn). Cập nhật bảng so sánh. Keywords mới đối thủ đang rank |
| **10:30 – 10:45** | Break | |
| **10:45 – 11:30** | Content Gap Reassessment | Keyword research mới. Content nào cần tạo Q tới? Pillar pages nào cần update? |
| **11:30 – 12:15** | Technical SEO Deep Dive | Site architecture review. Internal linking audit. Schema markup coverage. Mobile performance |
| **12:15 – 13:00** | Plan Q+1 | Set targets mới. Phân bổ resources. Content calendar Q tới. Link building plan Q tới |

### Quarterly KPI Review Template

| KPI | Target Q này | Actual | % Đạt | Status | Root Cause (nếu off-track) | Action Q tới |
|-----|-------------|--------|-------|--------|---------------------------|-------------|
| Keywords Top 10 | | | | 🟢/🟡/🔴 | | |
| Keywords Top 3 | | | | 🟢/🟡/🔴 | | |
| Organic Sessions | | | | 🟢/🟡/🔴 | | |
| Organic Conversions | | | | 🟢/🟡/🔴 | | |
| Referring Domains | | | | 🟢/🟡/🔴 | | |
| Domain Authority | | | | 🟢/🟡/🔴 | | |
| Số bài blog | | | | 🟢/🟡/🔴 | | |
| Core Web Vitals Pass | | | | 🟢/🟡/🔴 | | |

### Quarterly Output Deliverables

1. **Quarterly SEO Report** (dùng template Phần 6 bên dưới, mở rộng)
2. **Updated Competitor Matrix** (cập nhật bảng Phần 8)
3. **Content Plan Q+1** (danh sách bài viết + keywords target)
4. **Link Building Targets Q+1** (số lượng + nguồn cụ thể)
5. **Technical SEO Backlog** (issues cần fix, priority order)

---

## 5. KPI TRACKING DASHBOARD

### Bảng theo dõi KPIs — Mục tiêu theo tháng

> Nguồn target: [SEO Strategy Phần 6](../marketing/02-seo/seo-strategy.md) + [KPIs Dashboard](../marketing/06-measurement/kpis-dashboard.md)

| # | KPI | T1 | T2 | T3 | T4 | T5 | T6 | T7 | T8 | T9 | T10 | T11 | T12 |
|---|-----|----|----|----|----|----|----|----|----|----|----|-----|-----|
| 1 | Keywords Top 10 | 3 | 6 | **10** | 14 | 18 | **25** | 30 | 35 | 40 | 43 | 47 | **50+** |
| 2 | Keywords Top 3 | 0 | 1 | **3** | 5 | 7 | **10** | 12 | 14 | 16 | 17 | 19 | **20+** |
| 3 | Organic Sessions | 1.000 | 3.000 | **5.000** | 8.000 | 14.000 | **20.000** | 25.000 | 30.000 | 35.000 | 40.000 | 45.000 | **50.000** |
| 4 | Organic Conversions | 10 | 25 | **50** | 80 | 130 | **200** | 250 | 300 | 350 | 400 | 450 | **500+** |
| 5 | Referring Domains | 3 | 6 | **10** | 15 | 22 | **30** | 35 | 38 | 42 | 45 | 48 | **50+** |
| 6 | Domain Authority | 0 | 2 | **5** | 8 | 12 | **15** | 17 | 19 | 21 | 22 | 24 | **25+** |
| 7 | Số bài blog (tích lũy) | 4 | 8 | **12** | 16 | 22 | **30** | 36 | 42 | 48 | 52 | 56 | **60+** |
| 8 | Indexed Pages | 20 | 35 | **50** | 70 | 100 | **150** | 180 | 210 | 240 | 260 | 280 | **300** |
| 9 | Avg. CTR (GSC) | 1% | 1.5% | **2%** | 2.3% | 2.7% | **3%** | 3.2% | 3.4% | 3.6% | 3.7% | 3.9% | **4%** |
| 10 | Core Web Vitals | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

> **Cách đọc:** Số **in đậm** = milestone target chính (Tháng 3/6/12). Số thường = target nội suy hàng tháng.
>
> **Color coding:** 🟢 Đạt ≥90% target | 🟡 Đạt 70–89% | 🔴 Dưới 70%

### Bảng tracking thực tế (Cập nhật cuối mỗi tháng)

| # | KPI | T1 Actual | T2 Actual | T3 Actual | T4 Actual | T5 Actual | T6 Actual | Status |
|---|-----|-----------|-----------|-----------|-----------|-----------|-----------|--------|
| 1 | Keywords Top 10 | ___ | ___ | ___ | ___ | ___ | ___ | 🟢/🟡/🔴 |
| 2 | Keywords Top 3 | ___ | ___ | ___ | ___ | ___ | ___ | 🟢/🟡/🔴 |
| 3 | Organic Sessions | ___ | ___ | ___ | ___ | ___ | ___ | 🟢/🟡/🔴 |
| 4 | Organic Conversions | ___ | ___ | ___ | ___ | ___ | ___ | 🟢/🟡/🔴 |
| 5 | Referring Domains | ___ | ___ | ___ | ___ | ___ | ___ | 🟢/🟡/🔴 |
| 6 | Domain Authority | ___ | ___ | ___ | ___ | ___ | ___ | 🟢/🟡/🔴 |
| 7 | Số bài blog | ___ | ___ | ___ | ___ | ___ | ___ | 🟢/🟡/🔴 |
| 8 | Indexed Pages | ___ | ___ | ___ | ___ | ___ | ___ | 🟢/🟡/🔴 |

---

## 6. SEO REPORT TEMPLATE (MONTHLY)

> **Tần suất:** Cuối mỗi tháng (ngày 28–30)
> **Thời gian hoàn thành:** 1–2 giờ
> **Gửi cho:** Marketing Manager, CEO/Founder
> **Format:** Google Docs hoặc Google Slides

---

### 📋 TEMPLATE BÁO CÁO SEO THÁNG [MM/YYYY]

#### A. EXECUTIVE SUMMARY

**Tóm tắt tháng (3-5 dòng):**

> Tháng [X], organic traffic đạt [___] sessions ([↑/↓ ___%] so tháng trước). [X] keywords mới vào Top 10. Backlinks tăng [X] referring domains. Core Web Vitals [Pass/Fail]. Conversion rate organic ở mức [___%].
>
> **Highlight:** [Thành tựu nổi bật nhất tháng]
> **Concern:** [Vấn đề cần chú ý nhất]

| Metric | Tháng này | Tháng trước | % Change | Target | % vs Target | Status |
|--------|-----------|-------------|----------|--------|-------------|--------|
| Organic Sessions | | | | | | 🟢/🟡/🔴 |
| Keywords Top 10 | | | | | | 🟢/🟡/🔴 |
| Keywords Top 3 | | | | | | 🟢/🟡/🔴 |
| Organic Conversions | | | | | | 🟢/🟡/🔴 |
| Referring Domains | | | | | | 🟢/🟡/🔴 |
| Domain Authority | | | | | | 🟢/🟡/🔴 |

#### B. TRAFFIC OVERVIEW

| Metric | Tuần 1 | Tuần 2 | Tuần 3 | Tuần 4 | Tổng tháng | vs Tháng trước |
|--------|--------|--------|--------|--------|------------|----------------|
| Organic Sessions | | | | | | |
| Impressions (GSC) | | | | | | |
| Clicks (GSC) | | | | | | |
| Avg. CTR | | | | | | |
| Avg. Position | | | | | | |

**Top 10 Landing Pages by Organic Traffic:**

| # | URL | Sessions | Bouncing Rate | Avg. Time | Conversions | vs Tháng trước |
|---|-----|----------|---------------|-----------|-------------|----------------|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |
| 6 | | | | | | |
| 7 | | | | | | |
| 8 | | | | | | |
| 9 | | | | | | |
| 10 | | | | | | |

**📊 Recommendation:** [Ví dụ: "Trang /tu-lanh-xiaomi/ có bounce rate cao (75%). Cần cải thiện content above-the-fold và thêm internal links đến sản phẩm cụ thể."]

#### C. KEYWORD RANKINGS

**Top 10 Keywords tăng ranking (Top Movers):**

| # | Keyword | Position trước | Position nay | Change | Search Volume | URL ranking |
|---|---------|---------------|-------------|--------|---------------|-------------|
| 1 | | | | ↑ ___ | | |
| 2 | | | | ↑ ___ | | |
| 3 | | | | ↑ ___ | | |
| 4 | | | | ↑ ___ | | |
| 5 | | | | ↑ ___ | | |

**Top 5 Keywords giảm ranking (Top Losers):**

| # | Keyword | Position trước | Position nay | Change | Nguyên nhân dự đoán | Action |
|---|---------|---------------|-------------|--------|---------------------|--------|
| 1 | | | | ↓ ___ | | |
| 2 | | | | ↓ ___ | | |
| 3 | | | | ↓ ___ | | |

**Keyword Distribution:**

| Nhóm | Số lượng | vs Tháng trước | Target tháng |
|------|---------|----------------|-------------|
| Top 3 (Position 1–3) | | | |
| Top 10 (Position 4–10) | | | |
| Top 20 (Position 11–20) | | | |
| Top 50 (Position 21–50) | | | |
| Ngoài Top 50 | | | |

**📊 Recommendation:** [Ví dụ: "3 keywords đang ở position 11-15 có cơ hội lên Top 10 nếu bổ sung internal links và update content: 'tủ lạnh xiaomi 4 cánh', 'robot hút bụi xiaomi giá rẻ', 'máy lọc không khí xiaomi có tốt không'."]

#### D. CONTENT PERFORMANCE

**Bài viết mới tháng này:**

| # | Tiêu đề | Ngày publish | Target keyword | Position hiện tại | Organic clicks |
|---|---------|-------------|----------------|-------------------|----------------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |

**Content cần update (Traffic giảm >20%):**

| # | URL | Traffic trước | Traffic nay | % Giảm | Action đề xuất |
|---|-----|--------------|------------|--------|----------------|
| 1 | | | | | Update content + thêm data mới |
| 2 | | | | | Cải thiện title tag + meta |

**📊 Recommendation:** [Ví dụ: "Tháng tới nên ưu tiên viết 2 bài về 'máy hút ẩm xiaomi' — keyword gap lớn, đối thủ chưa có content mạnh."]

#### E. BACKLINK PROFILE

| Metric | Tháng này | Tháng trước | Change | Target |
|--------|-----------|-------------|--------|--------|
| Total Referring Domains | | | | |
| New Referring Domains | | | +___ | |
| Lost Referring Domains | | | -___ | |
| Domain Rating (DR) | | | | |
| Total Backlinks | | | | |

**Top 5 Backlinks mới chất lượng nhất:**

| # | Referring Domain | DR | Anchor Text | Target URL | Type (dofollow/nofollow) |
|---|-----------------|-----|------------|------------|--------------------------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**📊 Recommendation:** [Ví dụ: "Cần tăng cường outreach đến các trang tech (tinhte, genk). Target: 5 guest posts tháng tới. Focus anchor text vào 'tủ lạnh xiaomi' và 'robot hút bụi xiaomi'."]

#### F. TECHNICAL HEALTH

| Check | Status | Chi tiết |
|-------|--------|----------|
| Crawl Errors (GSC) | ✅/⚠️/❌ | ___ errors (tháng trước: ___) |
| 404 Pages | ✅/⚠️/❌ | ___ pages (đã redirect: ___) |
| Server Errors (5xx) | ✅/⚠️/❌ | ___ occurrences |
| Mobile Usability | ✅/⚠️/❌ | ___ issues |
| Core Web Vitals (LCP) | ✅/⚠️/❌ | ___s (target: ≤2.5s) |
| Core Web Vitals (INP) | ✅/⚠️/❌ | ___ms (target: ≤200ms) |
| Core Web Vitals (CLS) | ✅/⚠️/❌ | ___ (target: ≤0.1) |
| Sitemap Status | ✅/⚠️/❌ | Submitted: ___ / Indexed: ___ |
| Robots.txt | ✅/⚠️/❌ | Không có lỗi blocking |
| HTTPS | ✅/⚠️/❌ | Toàn site HTTPS |
| Schema Markup | ✅/⚠️/❌ | ___% trang sản phẩm có Product schema |

**📊 Recommendation:** [Ví dụ: "15 trang sản phẩm mới chưa có Product schema. Cần triển khai trong tuần đầu tháng tới."]

#### G. ACTION ITEMS THÁNG TỚI

| Priority | Action | Owner | Deadline | KPI Impact |
|----------|--------|-------|----------|------------|
| 🔴 P1 | | | | |
| 🔴 P1 | | | | |
| 🟡 P2 | | | | |
| 🟡 P2 | | | | |
| 🟢 P3 | | | | |
| 🟢 P3 | | | | |

> **Quy tắc:** Mỗi action item phải có recommendation cụ thể (không chỉ "cải thiện SEO" mà là "Viết 2 bài review tủ lạnh Xiaomi 600L targeting keyword 'tủ lạnh xiaomi 4 cánh giá bao nhiêu'")

---

## 7. ALERT SETUP

### Cấu hình cảnh báo tự động

#### A. Google Search Console — Email Notifications

| Alert | Cách bật | Tần suất |
|-------|---------|----------|
| **Coverage issues** | GSC → Settings → Email preferences → ✅ "Coverage issues" | Khi phát hiện |
| **Manual actions** | GSC → Settings → Email preferences → ✅ "Manual actions" | Khi phát hiện |
| **Security issues** | GSC → Settings → Email preferences → ✅ "Security issues" | Khi phát hiện |
| **Enhancement issues** | GSC → Settings → Email preferences → ✅ "Enhancements" | Khi phát hiện |

> ⚠️ **Bật TẤT CẢ email notifications trong GSC.** Đây là nguồn cảnh báo quan trọng nhất và miễn phí.

#### B. Google Analytics 4 — Custom Alerts

**Alert 1: Organic Traffic Drop >20%**
```
GA4 → Admin → Custom Definitions → Custom Alerts
- Tên: "Organic Traffic Drop Alert"
- Condition: Sessions from Organic Search < [80% of weekly average]
- Period: Tuần
- Notify: Email marketing team
```

**Alert 2: Conversion Rate Drop**
```
GA4 → Admin → Custom Alerts
- Tên: "Conversion Rate Drop Alert"
- Condition: Ecommerce conversion rate < 50% of previous period
- Period: Tuần
- Notify: Email marketing + dev team
```

**Alert 3: Spike in 404 Pageviews**
```
GA4 → Admin → Custom Alerts
- Tên: "404 Spike Alert"
- Condition: Pageviews on /404 page > [2x weekly average]
- Period: Ngày
- Notify: Email dev team
```

#### C. Ahrefs Alerts (Khi có subscription)

| Alert | Cách setup | Tần suất |
|-------|-----------|----------|
| **New backlinks** | Ahrefs → Alerts → New backlinks → Add xiaomi247.com | Tuần |
| **Lost backlinks** | Ahrefs → Alerts → Lost backlinks → Add xiaomi247.com | Tuần |
| **New keywords** | Ahrefs → Alerts → New keywords → Add xiaomi247.com | Tuần |
| **Competitor new backlinks** | Ahrefs → Alerts → Add mivietnam.vn, mihanoi.vn, xiaomimall.vn | 2 tuần |
| **Keyword ranking changes** | Ahrefs → Rank Tracker → Set alert thresholds | Tuần |

#### D. UptimeRobot — Uptime Monitoring

**Setup (Free plan — 50 monitors):**

| Monitor | URL | Check Interval | Alert |
|---------|-----|----------------|-------|
| Homepage | `https://xiaomi247.com` | 5 phút | Email + Telegram |
| Product page | `https://xiaomi247.com/tivi-xiaomi/` | 5 phút | Email + Telegram |
| Blog | `https://xiaomi247.com/blog/` | 5 phút | Email |
| Sitemap | `https://xiaomi247.com/sitemap.xml` | 30 phút | Email |
| Robots.txt | `https://xiaomi247.com/robots.txt` | 30 phút | Email |

**Cấu hình alert contacts:**
1. Email marketing team
2. Email dev/hosting team
3. Telegram bot (optional — setup qua @UptimeRobot_bot)

**Target uptime:** ≥99.5% hàng tháng

#### E. Tổng hợp Alert Matrix

| Loại alert | Công cụ | Mức độ | Response time | Ai xử lý |
|-----------|---------|--------|---------------|-----------|
| Site down | UptimeRobot | 🔴 Critical | <15 phút | Dev team |
| Manual action (Google) | GSC Email | 🔴 Critical | <2 giờ | SEO + Dev |
| Security issue | GSC Email | 🔴 Critical | <1 giờ | Dev team |
| Organic traffic drop >20% | GA4 Alert | 🟡 High | <24 giờ | Marketing |
| 404 spike | GA4 Alert | 🟡 High | <24 giờ | Dev team |
| Lost backlinks (DR >30) | Ahrefs Alert | 🟡 Medium | <48 giờ | Marketing |
| New competitor content | Ahrefs Alert | ⚪ Low | <1 tuần | Content team |
| Keyword ranking drop >5 pos | Ahrefs Alert | 🟡 Medium | <48 giờ | SEO team |

---

## 8. COMPETITOR TRACKING

### Đối thủ cần theo dõi

| # | Domain | Lý do theo dõi | Mức độ đe dọa | Điểm mạnh |
|---|--------|---------------|----------------|-----------|
| 1 | **mivietnam.vn** | Đối thủ lớn nhất, DA cao, content nhiều | 🔴 Cao | DA 25-35, 1.000+ trang, blog 50+ bài |
| 2 | **mihanoi.vn** | Đối thủ trung bình, CWV tốt | 🟡 Trung bình | Core Web Vitals tốt, 500+ trang |
| 3 | **xiaomimall.vn** | Đối thủ mạnh, DA tốt, có schema | 🔴 Cao | DA 20-30, 800+ trang, Product schema |

### Framework theo dõi hàng tháng

#### A. Keyword Overlap Analysis

| Keyword | xiaomi247 Position | mivietnam Position | mihanoi Position | xiaomimall Position | Gap | Action |
|---------|-------------------|-------------------|-----------------|--------------------|----|--------|
| tivi xiaomi | | | | | | |
| robot hút bụi xiaomi | | | | | | |
| tủ lạnh xiaomi | | | | | | |
| máy lọc không khí xiaomi | | | | | | |
| máy hút ẩm xiaomi | | | | | | |
| robot hút bụi lau nhà xiaomi | | | | | | |
| tivi xiaomi 55 inch | | | | | | |
| tủ lạnh xiaomi 4 cánh | | | | | | |
| xiaomi chính hãng | | | | | | |
| gia dụng xiaomi | | | | | | |

> **Cách dùng:** Ahrefs → Content Gap → nhập 3 competitors → xem keywords họ rank mà mình chưa rank

#### B. Content Monitoring — Nội dung mới của đối thủ

| Tháng | mivietnam.vn | mihanoi.vn | xiaomimall.vn |
|-------|-------------|------------|---------------|
| **Số bài mới** | | | |
| **Chủ đề nổi bật** | | | |
| **Bài nào rank cao** | | | |
| **Cơ hội cho xiaomi247** | | | |

**Cách theo dõi:**
1. Ahrefs → Site Explorer → [competitor domain] → Top Pages → filter "New" (30 ngày)
2. Google: `site:mivietnam.vn` → filter "Past month"
3. Subscribe RSS feed nếu có

#### C. Backlink Monitoring — Links mới của đối thủ

| Tháng | Metric | mivietnam.vn | mihanoi.vn | xiaomimall.vn | xiaomi247.com |
|-------|--------|-------------|------------|---------------|---------------|
| | Total Referring Domains | | | | |
| | New RDs (30 ngày) | | | | |
| | DR/DA | | | | |
| | Top new backlink source | | | | |

**Cách theo dõi:**
- Ahrefs → Alerts → setup "New backlinks" cho từng competitor
- Hàng tháng: Ahrefs → Site Explorer → [competitor] → Referring domains → filter "New"

#### D. Ranking Changes Tracker

| Keyword nhóm | xiaomi247 Trend | mivietnam Trend | mihanoi Trend | xiaomimall Trend | Nhận xét |
|-------------|----------------|----------------|--------------|-----------------|----------|
| Tivi Xiaomi | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | |
| Robot hút bụi | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | |
| Tủ lạnh Xiaomi | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | |
| Gia dụng Xiaomi | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | |
| So sánh sản phẩm | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | ↑/↓/→ | |

### Competitor Tracking — Tổng hợp Quarterly

| Tiêu chí | xiaomi247.com | mivietnam.vn | mihanoi.vn | xiaomimall.vn |
|-----------|--------------|--------------|------------|---------------|
| Domain Age | Mới | 3+ năm | 2+ năm | 2+ năm |
| DA/DR | ___ | ___ | ___ | ___ |
| Số trang indexed | ___ | ___ | ___ | ___ |
| Keywords Top 10 | ___ | ___ | ___ | ___ |
| Referring Domains | ___ | ___ | ___ | ___ |
| Blog posts (tổng) | ___ | ___ | ___ | ___ |
| Schema coverage | ___ | ___ | ___ | ___ |
| Core Web Vitals | ___ | ___ | ___ | ___ |
| Organic traffic (ước tính) | ___ | ___ | ___ | ___ |

> Cập nhật bảng này mỗi quý trong Quarterly SEO Review (Phần 4)

---

## 📎 PHỤ LỤC

### Lịch SEO Monitoring

| Tần suất | Công việc | Thời gian | Ngày thực hiện |
|----------|----------|-----------|----------------|
| **Hàng tuần** | Weekly SEO Check | 15 phút | Thứ 2 sáng |
| **Hàng tháng** | Monthly SEO Audit | 2 giờ | Ngày 1 hàng tháng |
| **Hàng tháng** | Monthly SEO Report | 1–2 giờ | Ngày 28–30 hàng tháng |
| **Hàng quý** | Quarterly SEO Review | 4 giờ (nửa ngày) | Tuần đầu quý mới |
| **Liên tục** | Alert Monitoring | Tự động | 24/7 (email/Telegram) |

### Tham chiếu

- [SEO Strategy — Phần 6: KPI & Đo lường](../marketing/02-seo/seo-strategy.md)
- [KPIs Dashboard](../marketing/06-measurement/kpis-dashboard.md)
- [Weekly Report Template](../marketing/06-measurement/weekly-report-template.md)

---

*📊 SEO Monitoring & Reporting — Xiaomi247.com*
*Phiên bản: v1.0 | Ngày tạo: 21/03/2026*
*Review: Hàng tháng | Người phụ trách: Marketing Manager / SEO Specialist*