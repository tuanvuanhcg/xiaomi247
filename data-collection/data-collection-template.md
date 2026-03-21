# 📋 Template Thu Thập Số Liệu Thực Tế — xiaomi247.com

> **Mục đích:** Thu thập số liệu thực tế từ các nền tảng (GA4, WooCommerce, GSC, Social Media) để đánh giá hiện trạng và điều chỉnh chiến lược marketing cho xiaomi247.com.

## 📝 Hướng dẫn sử dụng

1. **Điền giá trị** vào các cột trống (`___`) trong từng bảng
2. **Chụp screenshot** theo hướng dẫn ở cuối mỗi phần và attach vào thư mục `data-collection/screenshots/`
3. **Đánh dấu hoàn thành** ở checklist cuối file
4. **Commit lên repo** khi điền xong và thông báo cho team phân tích

### Mức ưu tiên
- 🔴 **Bắt buộc** — Phải có để phân tích được
- 🟠 **Quan trọng** — Cần thiết cho chiến lược đầy đủ
- 🟡 **Nếu có** — Bổ sung thêm nếu team có thời gian

---

| | |
|---|---|
| **Ngày thu thập** | ___ |
| **Người thu thập** | ___ |
| **Khoảng thời gian dữ liệu** | ___ đến ___ |

---

## 1. 🌐 Website Analytics (GA4) — 🔴 Bắt buộc

**Cách truy cập:** [analytics.google.com](https://analytics.google.com) → chọn property **xiaomi247**

### 1.1 Traffic Overview (30 ngày gần nhất)

> **Hướng dẫn lấy dữ liệu:**
> 1. Mở GA4 → **Reports** → **Acquisition** → **Overview**
> 2. Đặt date range: **Last 30 days**
> 3. Đọc các metric từ dashboard và điền vào bảng bên dưới

| Metric | Giá trị | Ghi chú |
|---|---|---|
| Total Users | ___ | |
| New Users | ___ | |
| Sessions | ___ | |
| Pageviews | ___ | |
| Avg Session Duration | ___ phút ___ giây | |
| Bounce Rate | ___% | |
| Pages per Session | ___ | |

### 1.2 Traffic Sources

> **Hướng dẫn lấy dữ liệu:**
> 1. GA4 → **Reports** → **Acquisition** → **Traffic acquisition**
> 2. Đặt date range: **Last 30 days**
> 3. Xem bảng "Session default channel group"

| Nguồn | Sessions | % tổng | Users |
|---|---|---|---|
| Organic Search | ___ | ___% | ___ |
| Direct | ___ | ___% | ___ |
| Social | ___ | ___% | ___ |
| Referral | ___ | ___% | ___ |
| Paid Search | ___ | ___% | ___ |
| Paid Social | ___ | ___% | ___ |
| Email | ___ | ___% | ___ |
| Khác | ___ | ___% | ___ |

### 1.3 Top 20 Trang Được Xem Nhiều Nhất

> **Hướng dẫn lấy dữ liệu:**
> 1. GA4 → **Reports** → **Engagement** → **Pages and screens**
> 2. Sort by **Views** (giảm dần)
> 3. Ghi lại 20 trang đầu tiên

| # | URL trang | Pageviews | Avg Time |
|---|---|---|---|
| 1 | ___ | ___ | ___ |
| 2 | ___ | ___ | ___ |
| 3 | ___ | ___ | ___ |
| 4 | ___ | ___ | ___ |
| 5 | ___ | ___ | ___ |
| 6 | ___ | ___ | ___ |
| 7 | ___ | ___ | ___ |
| 8 | ___ | ___ | ___ |
| 9 | ___ | ___ | ___ |
| 10 | ___ | ___ | ___ |
| 11 | ___ | ___ | ___ |
| 12 | ___ | ___ | ___ |
| 13 | ___ | ___ | ___ |
| 14 | ___ | ___ | ___ |
| 15 | ___ | ___ | ___ |
| 16 | ___ | ___ | ___ |
| 17 | ___ | ___ | ___ |
| 18 | ___ | ___ | ___ |
| 19 | ___ | ___ | ___ |
| 20 | ___ | ___ | ___ |

### 1.4 Thiết Bị

> **Hướng dẫn lấy dữ liệu:**
> 1. GA4 → **Reports** → **Tech** → **Overview**
> 2. Xem biểu đồ "Users by platform / device category"

| Thiết bị | Sessions | % |
|---|---|---|
| Mobile | ___ | ___% |
| Desktop | ___ | ___% |
| Tablet | ___ | ___% |

### 1.5 Địa Lý — Top 10 Tỉnh/Thành

> **Hướng dẫn lấy dữ liệu:**
> 1. GA4 → **Reports** → **Demographics** → **Demographic details**
> 2. Chọn dimension: **City**
> 3. Sort by **Users** (giảm dần)

| # | Tỉnh/Thành | Users | % |
|---|---|---|---|
| 1 | ___ | ___ | ___% |
| 2 | ___ | ___ | ___% |
| 3 | ___ | ___ | ___% |
| 4 | ___ | ___ | ___% |
| 5 | ___ | ___ | ___% |
| 6 | ___ | ___ | ___% |
| 7 | ___ | ___ | ___% |
| 8 | ___ | ___ | ___% |
| 9 | ___ | ___ | ___% |
| 10 | ___ | ___ | ___% |

📸 **Screenshot cần chụp:**
- [ ] GA4 Acquisition Overview dashboard
- [ ] Traffic Sources chart (biểu đồ tròn/cột)
- [ ] Demographics → City map

---

## 2. 🛒 E-commerce Data (WooCommerce) — 🔴 Bắt buộc

**Cách truy cập:** WP Admin → **WooCommerce** → **Analytics**

### 2.1 Doanh Thu & Đơn Hàng (30 ngày gần nhất)

> **Hướng dẫn lấy dữ liệu:**
> 1. Đăng nhập WP Admin → **WooCommerce** → **Analytics** → **Revenue**
> 2. Đặt date range: **Last 30 days** (hoặc Custom)
> 3. Đọc các metric từ dashboard

| Metric | Giá trị | Ghi chú |
|---|---|---|
| Tổng doanh thu (VNĐ) | ___ | |
| Số đơn hàng | ___ | |
| Giá trị đơn TB (AOV) | ___ VNĐ | Doanh thu ÷ số đơn |
| Số sản phẩm bán ra | ___ | |
| Tỉ lệ hoàn/hủy đơn | ___% | |
| Đơn COD vs Chuyển khoản | ___% / ___% | |

### 2.2 Top 10 Sản Phẩm Bán Chạy

> **Hướng dẫn lấy dữ liệu:**
> 1. WP Admin → **WooCommerce** → **Analytics** → **Products**
> 2. Sort by **Items Sold** (giảm dần)
> 3. Ghi lại 10 sản phẩm đầu tiên

| # | Tên sản phẩm | Số lượng bán | Doanh thu (VNĐ) | Giá bán |
|---|---|---|---|---|
| 1 | ___ | ___ | ___ | ___ |
| 2 | ___ | ___ | ___ | ___ |
| 3 | ___ | ___ | ___ | ___ |
| 4 | ___ | ___ | ___ | ___ |
| 5 | ___ | ___ | ___ | ___ |
| 6 | ___ | ___ | ___ | ___ |
| 7 | ___ | ___ | ___ | ___ |
| 8 | ___ | ___ | ___ | ___ |
| 9 | ___ | ___ | ___ | ___ |
| 10 | ___ | ___ | ___ | ___ |

### 2.3 Top 5 Danh Mục Bán Chạy

> **Hướng dẫn lấy dữ liệu:**
> 1. WP Admin → **WooCommerce** → **Analytics** → **Categories**
> 2. Sort by **Items Sold** (giảm dần)

| # | Danh mục | Số SP bán | Doanh thu (VNĐ) | % tổng DT |
|---|---|---|---|---|
| 1 | ___ | ___ | ___ | ___% |
| 2 | ___ | ___ | ___ | ___% |
| 3 | ___ | ___ | ___ | ___% |
| 4 | ___ | ___ | ___ | ___% |
| 5 | ___ | ___ | ___ | ___% |

### 2.4 Catalog

> **Hướng dẫn lấy dữ liệu:**
> 1. WP Admin → **Products** → **All Products** → xem tổng số
> 2. Filter by **Stock status: Out of stock** để đếm SP hết hàng
> 3. Kiểm tra thủ công ảnh và mô tả sản phẩm

| Metric | Giá trị |
|---|---|
| Tổng số SKU active | ___ |
| Số SP hết hàng | ___ |
| Số SP có ảnh đầy đủ (≥3 ảnh) | ___ |
| Số SP có mô tả đầy đủ (>200 từ) | ___ |
| Khoảng giá: thấp nhất — cao nhất | ___ — ___ VNĐ |

📸 **Screenshot cần chụp:**
- [ ] WooCommerce Revenue chart (30 ngày)
- [ ] Products report (top 10)
- [ ] All Products list (tổng số SKU)

---

## 3. 🔍 SEO Data (Google Search Console) — 🟠 Quan trọng

**Cách truy cập:** [search.google.com/search-console](https://search.google.com/search-console) → chọn property **xiaomi247.com**

### 3.1 Performance Overview (3 tháng gần nhất)

> **Hướng dẫn lấy dữ liệu:**
> 1. GSC → **Performance** → **Search results**
> 2. Đặt Date range: **Last 3 months**
> 3. Bật tất cả 4 metrics: Clicks, Impressions, CTR, Position

| Metric | Giá trị |
|---|---|
| Total Clicks | ___ |
| Total Impressions | ___ |
| Average CTR | ___% |
| Average Position | ___ |

### 3.2 Top 20 Keywords Đang Rank

> **Hướng dẫn lấy dữ liệu:**
> 1. GSC → **Performance** → tab **Queries**
> 2. Sort by **Impressions** (giảm dần)
> 3. Ghi lại 20 keywords đầu tiên

| # | Keyword | Clicks | Impressions | CTR | Position |
|---|---|---|---|---|---|
| 1 | ___ | ___ | ___ | ___% | ___ |
| 2 | ___ | ___ | ___ | ___% | ___ |
| 3 | ___ | ___ | ___ | ___% | ___ |
| 4 | ___ | ___ | ___ | ___% | ___ |
| 5 | ___ | ___ | ___ | ___% | ___ |
| 6 | ___ | ___ | ___ | ___% | ___ |
| 7 | ___ | ___ | ___ | ___% | ___ |
| 8 | ___ | ___ | ___ | ___% | ___ |
| 9 | ___ | ___ | ___ | ___% | ___ |
| 10 | ___ | ___ | ___ | ___% | ___ |
| 11 | ___ | ___ | ___ | ___% | ___ |
| 12 | ___ | ___ | ___ | ___% | ___ |
| 13 | ___ | ___ | ___ | ___% | ___ |
| 14 | ___ | ___ | ___ | ___% | ___ |
| 15 | ___ | ___ | ___ | ___% | ___ |
| 16 | ___ | ___ | ___ | ___% | ___ |
| 17 | ___ | ___ | ___ | ___% | ___ |
| 18 | ___ | ___ | ___ | ___% | ___ |
| 19 | ___ | ___ | ___ | ___% | ___ |

### 3.3 Top 20 Pages Organic

> **Hướng dẫn lấy dữ liệu:**
> 1. GSC → **Performance** → tab **Pages**
> 2. Sort by **Clicks** (giảm dần)
> 3. Ghi lại 20 trang đầu tiên

| # | URL | Clicks | Impressions | CTR | Position |
|---|---|---|---|---|---|
| 1 | ___ | ___ | ___ | ___% | ___ |
| 2 | ___ | ___ | ___ | ___% | ___ |
| 3 | ___ | ___ | ___ | ___% | ___ |
| 4 | ___ | ___ | ___ | ___% | ___ |
| 5 | ___ | ___ | ___ | ___% | ___ |
| 6 | ___ | ___ | ___ | ___% | ___ |
| 7 | ___ | ___ | ___ | ___% | ___ |
| 8 | ___ | ___ | ___ | ___% | ___ |
| 9 | ___ | ___ | ___ | ___% | ___ |
| 10 | ___ | ___ | ___ | ___% | ___ |
| 11 | ___ | ___ | ___ | ___% | ___ |
| 12 | ___ | ___ | ___ | ___% | ___ |
| 13 | ___ | ___ | ___ | ___% | ___ |
| 14 | ___ | ___ | ___ | ___% | ___ |
| 15 | ___ | ___ | ___ | ___% | ___ |
| 16 | ___ | ___ | ___ | ___% | ___ |
| 17 | ___ | ___ | ___ | ___% | ___ |
| 18 | ___ | ___ | ___ | ___% | ___ |
| 19 | ___ | ___ | ___ | ___% | ___ |
| 20 | ___ | ___ | ___ | ___% | ___ |

### 3.4 Indexing Status

> **Hướng dẫn lấy dữ liệu:**
> 1. GSC → **Indexing** → **Pages**
> 2. Xem tổng số trang indexed vs not indexed

| Metric | Giá trị |
|---|---|
| Trang đã index | ___ |
| Trang không index (lỗi) | ___ |
| Trang không index (excluded) | ___ |
| Sitemap submitted? | Có / Chưa |

### 3.5 Core Web Vitals

> **Hướng dẫn lấy dữ liệu:**
> 1. GSC → **Experience** → **Core Web Vitals**
> 2. Xem cả Mobile và Desktop reports

| Metric | Mobile | Desktop |
|---|---|---|
| LCP (Largest Contentful Paint) | ___ s | ___ s |
| FID/INP (Interaction to Next Paint) | ___ ms | ___ ms |
| CLS (Cumulative Layout Shift) | ___ | ___ |
| Trạng thái (Good/Needs Improvement/Poor) | ___ | ___ |

📸 **Screenshot cần chụp:**
- [ ] GSC Performance chart (3 tháng)
- [ ] Indexing status overview
- [ ] Core Web Vitals report (Mobile + Desktop)

---

## 4. 📱 Social Media — 🟠 Quan trọng

### 4.1 Facebook Page

> **Hướng dẫn lấy dữ liệu:**
> 1. Vào Facebook Page → **Professional Dashboard** hoặc **Meta Business Suite**
> 2. Xem **Insights** → **Overview**

| Metric | Giá trị |
|---|---|
| Page name / URL | ___ |
| Followers | ___ |
| Page Likes | ___ |
| Reach (tuần gần nhất) | ___ |
| Engagement rate | ___% |
| Đang chạy ads? | Có / Không |
| Budget ads/tháng | ___ VNĐ |

### 4.2 Instagram

> **Hướng dẫn lấy dữ liệu:**
> 1. Instagram → Profile → **Professional Dashboard** → **Insights**

| Metric | Giá trị |
|---|---|
| Username / URL | ___ |
| Followers | ___ |
| Reach (tuần gần nhất) | ___ |
| Engagement rate | ___% |

### 4.3 TikTok (nếu có)

> **Hướng dẫn:** TikTok → Profile → **Creator tools** → **Analytics**

| Metric | Giá trị |
|---|---|
| Username / URL | ___ |
| Followers | ___ |
| Views (tuần gần nhất) | ___ |
| Số videos đã đăng | ___ |

### 4.4 Zalo OA (nếu có)

> **Hướng dẫn:** Đăng nhập [oa.zalo.me](https://oa.zalo.me) → **Dashboard**

| Metric | Giá trị |
|---|---|
| OA ID / tên | ___ |
| Followers | ___ |
| Tin nhắn/tuần | ___ |

📸 **Screenshot cần chụp:**
- [ ] Facebook Page Insights overview
- [ ] Instagram Insights (nếu có)

---

## 5. 💰 Business Data — 🔴 Bắt buộc

### 5.1 Tài Chính

> **Hướng dẫn:** Thông tin từ kế toán/owner — không cần tool cụ thể

| Metric | Giá trị | Ghi chú |
|---|---|---|
| Budget marketing sẵn sàng/tháng | ___ VNĐ | Tổng tất cả kênh |
| Margin trung bình trên mỗi đơn | ___% | Sau chi phí hàng + vận chuyển |
| CPA break-even (chi phí tối đa để có 1 đơn) | ___ VNĐ | AOV × margin% |
| Mục tiêu doanh thu tháng | ___ VNĐ | |
| Mục tiêu doanh thu quý | ___ VNĐ | |
| Mục tiêu số đơn/tháng | ___ đơn | |

### 5.2 Nguồn Hàng & Vận Hành

| Câu hỏi | Trả lời |
|---|---|
| Nguồn hàng chính? (chính hãng Xiaomi VN / nhập khẩu / mixed) | ___ |
| Có giấy tờ ủy quyền phân phối? | Có / Không |
| Có showroom/kho offline? (nếu có, ở đâu?) | ___ |
| Đối tác vận chuyển? (GHTK, GHN, Viettel Post, khác?) | ___ |
| Thời gian giao hàng trung bình? | ___ ngày |
| Khu vực giao hàng chính? (HN, HCM, toàn quốc?) | ___ |
| Có hỗ trợ lắp đặt sản phẩm lớn? (tivi, tủ lạnh) | Có / Không |

### 5.3 Team

| Vai trò | Số người | Kỹ năng chính | Full-time/Part-time |
|---|---|---|---|
| Quản lý/Owner | ___ | ___ | ___ |
| Marketing | ___ | ___ | ___ |
| Content Writer | ___ | ___ | ___ |
| CSKH | ___ | ___ | ___ |
| Kỹ thuật/IT | ___ | ___ | ___ |
| Kho/Logistics | ___ | ___ | ___ |
| Khác: ___ | ___ | ___ | ___ |

### 5.4 Cạnh Tranh

| Câu hỏi | Trả lời |
|---|---|
| Đối thủ đang lo ngại nhất? | ___ |
| Điểm mạnh đối thủ mà mình chưa có? | ___ |
| Lợi thế cạnh tranh chính của xiaomi247? | ___ |
| Có nhận biết được nguồn khách hàng chính từ đâu? | ___ |

---

## 6. ⚙️ Technical — 🟡 Nếu có

### 6.1 Hosting & Infrastructure

> **Hướng dẫn lấy dữ liệu:**
> 1. Hỏi admin/IT hoặc kiểm tra WP Admin → **Tools** → **Site Health** → **Info**
> 2. WP Admin → **Dashboard** → **Updates** để xem version WordPress
> 3. WP Admin → **WooCommerce** → **Status** → **System status** để xem WooCommerce version, PHP version

| Metric | Giá trị |
|---|---|
| Hosting provider | ___ (VD: Tinohost, AZDIGI, HostingViet, Vultr...) |
| Hosting plan | ___ (shared / VPS / dedicated) |
| Chi phí hosting/tháng | ___ VNĐ |
| PHP version | ___ |
| WordPress version | ___ |
| WooCommerce version | ___ |
| Motta theme version | ___ |
| Có CDN? (Cloudflare, etc.) | Có / Không — ___ |
| SSL certificate | Có / Không — ___ |

### 6.2 PageSpeed Insights

> **Hướng dẫn lấy dữ liệu:**
> 1. Truy cập [pagespeed.web.dev](https://pagespeed.web.dev)
> 2. Nhập URL: `https://xiaomi247.com`
> 3. Chạy test cho cả **Mobile** và **Desktop**

| Metric | Mobile | Desktop |
|---|---|---|
| Performance Score | ___/100 | ___/100 |
| LCP | ___ s | ___ s |
| TBT | ___ ms | ___ ms |
| CLS | ___ | ___ |

### 6.3 Plugins Đang Cài

> **Hướng dẫn lấy dữ liệu:**
> 1. WP Admin → **Plugins** → **Installed Plugins**
> 2. Liệt kê tất cả plugins có trạng thái **Active**

Liệt kê tất cả plugins đang active:

| # | Tên Plugin | Version | Mục đích |
|---|---|---|---|
| 1 | ___ | ___ | ___ |
| 2 | ___ | ___ | ___ |
| 3 | ___ | ___ | ___ |
| 4 | ___ | ___ | ___ |
| 5 | ___ | ___ | ___ |
| 6 | ___ | ___ | ___ |
| 7 | ___ | ___ | ___ |
| 8 | ___ | ___ | ___ |
| 9 | ___ | ___ | ___ |
| 10 | ___ | ___ | ___ |
| ... | ___ | ___ | ___ |

📸 **Screenshot cần chụp:**
- [ ] PageSpeed Insights results — Mobile
- [ ] PageSpeed Insights results — Desktop
- [ ] WP Admin → Plugins list (full page)

---

## ✅ Checklist Hoàn Thành

| # | Phần | Ưu tiên | Trạng thái | Người thực hiện | Ngày |
|---|---|---|---|---|---|
| 1 | 🌐 Website Analytics (GA4) | 🔴 Bắt buộc | ☐ | ___ | ___ |
| 2 | 🛒 E-commerce Data (WooCommerce) | 🔴 Bắt buộc | ☐ | ___ | ___ |
| 3 | 🔍 SEO Data (GSC) | 🟠 Quan trọng | ☐ | ___ | ___ |
| 4 | 📱 Social Media | 🟠 Quan trọng | ☐ | ___ | ___ |
| 5 | 💰 Business Data | 🔴 Bắt buộc | ☐ | ___ | ___ |
| 6 | ⚙️ Technical | 🟡 Nếu có | ☐ | ___ | ___ |

---

## 📎 Tổng hợp Screenshot cần chụp

| # | Screenshot | Phần | Đã chụp? |
|---|---|---|---|
| 1 | GA4 Acquisition Overview dashboard | 1. Website Analytics | ☐ |
| 2 | GA4 Traffic Sources chart | 1. Website Analytics | ☐ |
| 3 | GA4 Demographics → City map | 1. Website Analytics | ☐ |
| 4 | WooCommerce Revenue chart (30 ngày) | 2. E-commerce | ☐ |
| 5 | WooCommerce Products report (top 10) | 2. E-commerce | ☐ |
| 6 | WooCommerce All Products list | 2. E-commerce | ☐ |
| 7 | GSC Performance chart (3 tháng) | 3. SEO | ☐ |
| 8 | GSC Indexing status overview | 3. SEO | ☐ |
| 9 | GSC Core Web Vitals report | 3. SEO | ☐ |
| 10 | Facebook Page Insights overview | 4. Social Media | ☐ |
| 11 | Instagram Insights (nếu có) | 4. Social Media | ☐ |
| 12 | PageSpeed Insights — Mobile | 6. Technical | ☐ |
| 13 | PageSpeed Insights — Desktop | 6. Technical | ☐ |
| 14 | WP Admin → Plugins list | 6. Technical | ☐ |

> **Lưu screenshots vào:** `data-collection/screenshots/` — đặt tên file theo format: `{số}-{mô-tả}.png`
> VD: `01-ga4-acquisition-overview.png`, `04-woo-revenue-chart.png`

---

**Sau khi điền xong:**
1. ✅ Kiểm tra lại tất cả các phần đã điền đầy đủ
2. 📸 Đảm bảo đã chụp và attach tất cả screenshot
3. 💾 Commit file này lên repo: `git add . && git commit -m "data: Thu thập số liệu thực tế"`
4. 📢 Thông báo cho team phân tích để điều chỉnh chiến lược