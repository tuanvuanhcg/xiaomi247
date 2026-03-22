# 🏠 Xiaomi247.com — Project Hub

> Trung tâm điều phối dự án xiaomi247.com — website e-commerce bán lẻ sản phẩm Xiaomi & Smart Home tại Việt Nam.

## 📌 Giới thiệu

Repository này chứa toàn bộ tài liệu chiến lược, kế hoạch triển khai và nội dung marketing cho **xiaomi247.com**. Mục tiêu là xây dựng thương hiệu, tối ưu website, và tăng trưởng doanh thu thông qua các kênh digital.

## 🏢 Thông tin Brand

|  |  |
| --- | --- |
| Website | xiaomi247.com |
| Ngành | E-commerce — Điện tử tiêu dùng & Smart Home |
| Platform | WordPress + WooCommerce + Elementor + Motta Theme |
| Chủ sở hữu | Karomind |
| Catalog | 200+ SKU (Tivi Xiaomi, Robot hút bụi, Máy lọc KK, Tủ lạnh, Máy hút ẩm, Điều hòa, Máy giặt, Máy rửa bát, Gia dụng thông minh, Loa, Máy chiếu, Laptop) |
| USP | Giao hàng toàn quốc 64 tỉnh · COD + chuyển khoản · Bảo hành đổi trả · Hỗ trợ 24/7 |
| Thị trường | Toàn quốc Việt Nam |

## 📊 Hiện trạng

### ✅ Điểm mạnh

- Giao diện modern (Motta theme)
- Hỗ trợ đa kênh (Zalo / Messenger / SMS / Call)
- Catalog đa dạng (~200+ SKU)
- Giao hàng toàn quốc 64 tỉnh
- Domain dễ nhớ

### ⚠️ Điểm yếu cần cải thiện

- Trang Blog & Contact → lỗi 404
- Menu còn demo text (Home v1-v10, Shop v1-v4...)
- Search placeholder chưa Việt hóa
- Thiếu social proof (review, video)
- Brand awareness thấp

## 📂 Cấu trúc thư mục

### Tổng quan Marketing

Tổng quan và spec cho toàn bộ marketing operations. Đọc file spec.md để hiểu scope, tiến độ dự án, và phân công công việc giữa các giai đoạn.

| File | Mô tả |
| --- | --- |
| [spec.md](marketing/spec.md) | Marketing Operations Spec — scope, timeline, deliverables tổng thể |
| [README.md](marketing/README.md) | Tổng quan thư mục marketing — mục lục và hướng dẫn đọc |

### 01 — Technical Audit

Báo cáo kiểm tra toàn diện website hiện tại. Xác định 15+ lỗi cần fix, đánh giá performance, UX, và bảo mật. **Đọc đầu tiên** khi bắt đầu dự án.

| File | Mô tả |
| --- | --- |
| [website-audit-report.md](marketing/01-technical-audit/website-audit-report.md) | Báo cáo audit website — điểm mạnh, điểm yếu, đánh giá 8 mục |
| [bug-fix-checklist.md](marketing/01-technical-audit/bug-fix-checklist.md) | 15 bugs cần fix + hướng dẫn khắc phục từng bug |
| [technical-recommendations.md](marketing/01-technical-audit/technical-recommendations.md) | Khuyến nghị kỹ thuật: caching, CDN, bảo mật, monitoring |

### 02 — SEO

Chiến lược SEO tổng thể 3-6-12 tháng, keyword research 65+ từ khóa chia 4 clusters. Nền tảng cho toàn bộ SEO Implementation ở phần sau.

| File | Mô tả |
| --- | --- |
| [seo-strategy.md](marketing/02-seo/seo-strategy.md) | Chiến lược SEO 3-6-12 tháng — mục tiêu, phân bổ nguồn lực |
| [keyword-map.md](marketing/02-seo/keyword-map.md) | 65+ keywords chia 4 clusters — transactional, informational, brand, local |
| [onpage-optimization-guide.md](marketing/02-seo/onpage-optimization-guide.md) | Hướng dẫn tối ưu on-page — title, meta, heading, internal links |
| [technical-seo-checklist.md](marketing/02-seo/technical-seo-checklist.md) | Checklist technical SEO — sitemap, robots.txt, page speed, mobile |

### 03 — Content Marketing

Chiến lược content và 8 bài blog SEO sẵn sàng publish (1,500–2,500 từ/bài). Bao gồm lịch đăng bài tháng 1 với timeline cụ thể.

| File | Mô tả |
| --- | --- |
| [content-strategy.md](marketing/03-content-marketing/content-strategy.md) | Chiến lược content — tone of voice, content pillars, quy trình sản xuất |
| [content-calendar-month1.md](marketing/03-content-marketing/content-calendar-month1.md) | Lịch content tháng 1 — schedule 8 bài blog theo tuần |

#### 📝 Blog Articles (8 bài)

| File | Mô tả |
| --- | --- |
| [01-top-5-tivi-xiaomi-dang-mua-2026.md](marketing/03-content-marketing/blog-articles/01-top-5-tivi-xiaomi-dang-mua-2026.md) | Top 5 Tivi Xiaomi đáng mua 2026 — so sánh specs, giá, đánh giá |
| [02-so-sanh-roborock-vs-ecovacs-vs-dreame.md](marketing/03-content-marketing/blog-articles/02-so-sanh-roborock-vs-ecovacs-vs-dreame.md) | So sánh 3 hãng robot hút bụi hàng đầu — Roborock vs Ecovacs vs Dreame |
| [03-review-tu-lanh-xiaomi-mijia-430l.md](marketing/03-content-marketing/blog-articles/03-review-tu-lanh-xiaomi-mijia-430l.md) | Review chi tiết tủ lạnh Xiaomi Mijia 430L — thiết kế, tính năng, giá |
| [04-huong-dan-chon-may-loc-khong-khi.md](marketing/03-content-marketing/blog-articles/04-huong-dan-chon-may-loc-khong-khi.md) | Hướng dẫn chọn máy lọc không khí — tiêu chí, so sánh models, budget |
| [05-robot-hut-bui-nha-co-thu-cung.md](marketing/03-content-marketing/blog-articles/05-robot-hut-bui-nha-co-thu-cung.md) | Robot hút bụi cho nhà có thú cưng — chống rối lông, lực hút mạnh |
| [06-tivi-xiaomi-a-pro-vs-s-pro-mini-led.md](marketing/03-content-marketing/blog-articles/06-tivi-xiaomi-a-pro-vs-s-pro-mini-led.md) | So sánh Tivi Xiaomi A Pro vs S Pro Mini LED — panel, HDR, gaming |
| [07-top-may-hut-am-duoi-5-trieu.md](marketing/03-content-marketing/blog-articles/07-top-may-hut-am-duoi-5-trieu.md) | Top máy hút ẩm dưới 5 triệu — công suất, diện tích phòng, tiết kiệm điện |
| [08-huong-dan-ket-noi-xiaomi-smart-home.md](marketing/03-content-marketing/blog-articles/08-huong-dan-ket-noi-xiaomi-smart-home.md) | Hướng dẫn kết nối hệ sinh thái Xiaomi Smart Home — app, gateway, automation |

### 04 — Trust Building

Tài liệu xây dựng niềm tin khách hàng: trang Về chúng tôi, 3 chính sách (bảo hành, đổi trả, vận chuyển), hướng dẫn CRO và thu thập review. Triển khai song song với website development.

| File | Mô tả |
| --- | --- |
| [trust-strategy.md](marketing/04-trust-building/trust-strategy.md) | Chiến lược xây dựng trust — trust signals, social proof, brand story |
| [about-us-page-content.md](marketing/04-trust-building/about-us-page-content.md) | Nội dung trang Về chúng tôi — sẵn sàng copy lên website |
| [conversion-optimization.md](marketing/04-trust-building/conversion-optimization.md) | Hướng dẫn CRO — tối ưu tỉ lệ chuyển đổi trên từng trang |
| [review-collection-guide.md](marketing/04-trust-building/review-collection-guide.md) | Quy trình thu thập review khách hàng — email, SMS, incentive |

#### 📄 Policy Pages

| File | Mô tả |
| --- | --- |
| [bao-hanh.md](marketing/04-trust-building/policy-pages/bao-hanh.md) | Chính sách bảo hành — điều kiện, quy trình, liên hệ |
| [doi-tra.md](marketing/04-trust-building/policy-pages/doi-tra.md) | Chính sách đổi trả — thời hạn, điều kiện, hoàn tiền |
| [van-chuyen.md](marketing/04-trust-building/policy-pages/van-chuyen.md) | Chính sách vận chuyển — phí ship, thời gian, khu vực giao hàng |

### 05 — Digital Marketing

Kế hoạch quảng cáo đa kênh: Facebook/IG (40%), Google (30%), TikTok (20%), Zalo (10%). Budget 35M VNĐ/tháng. Bao gồm social media calendar tháng 1 và templates sẵn dùng.

| File | Mô tả |
| --- | --- |
| [digital-marketing-strategy.md](marketing/05-digital-marketing/digital-marketing-strategy.md) | Chiến lược digital tổng thể — phân bổ kênh, budget, timeline |
| [facebook-ads-plan.md](marketing/05-digital-marketing/facebook-ads-plan.md) | Kế hoạch Facebook/IG Ads — audience, ad sets, creative brief |
| [google-ads-plan.md](marketing/05-digital-marketing/google-ads-plan.md) | Kế hoạch Google Ads — Search, Shopping, remarketing campaigns |
| [tiktok-strategy.md](marketing/05-digital-marketing/tiktok-strategy.md) | Chiến lược TikTok — content format, hashtags, KOL collaboration |
| [social-media-calendar-month1.md](marketing/05-digital-marketing/social-media-calendar-month1.md) | Social media calendar tháng 1 — 12 posts với nội dung chi tiết |
| [social-media-templates.md](marketing/05-digital-marketing/social-media-templates.md) | 4 template post — sản phẩm, tips, review, khuyến mãi |
| [ads-budget-proposal.md](marketing/05-digital-marketing/ads-budget-proposal.md) | Đề xuất budget 35M VNĐ/tháng — phân bổ theo kênh, ROI dự kiến |

### 06 — Measurement

Framework đo lường hiệu quả: KPIs, OKRs Q1, hướng dẫn setup tracking, template báo cáo tuần. **Đọc để thiết lập metrics trước khi chạy campaigns.**

| File | Mô tả |
| --- | --- |
| [kpis-dashboard.md](marketing/06-measurement/kpis-dashboard.md) | KPIs theo kênh — traffic, conversion, revenue, engagement targets |
| [tracking-setup-guide.md](marketing/06-measurement/tracking-setup-guide.md) | Hướng dẫn setup GA4, GTM, Facebook Pixel, TikTok Pixel |
| [okrs-q1.md](marketing/06-measurement/okrs-q1.md) | OKRs quý 1 — 4 objectives, 12 key results, milestones |
| [weekly-report-template.md](marketing/06-measurement/weekly-report-template.md) | Template báo cáo tuần — metrics, insights, action items |

### 🌐 Website Development

7 hướng dẫn kỹ thuật step-by-step để triển khai thay đổi trên website WordPress. Từ fix bug → plugin → performance → bảo mật → mobile → tracking. **Thực hiện theo thứ tự file 01 → 07.**

| File | Mô tả |
| --- | --- |
| [01-critical-fixes.md](website-dev/01-critical-fixes.md) | Hướng dẫn fix 6 lỗi critical |
| [02-localization-content.md](website-dev/02-localization-content.md) | Việt hóa & tạo trang nội dung |
| [03-plugin-setup.md](website-dev/03-plugin-setup.md) | Cài đặt & cấu hình 10 plugin |
| [04-performance-cdn.md](website-dev/04-performance-cdn.md) | Tối ưu performance & Cloudflare CDN |
| [05-security.md](website-dev/05-security.md) | Bảo mật WordPress toàn diện |
| [06-mobile-ux.md](website-dev/06-mobile-ux.md) | Mobile responsive & UX enhancement |
| [07-tracking-analytics.md](website-dev/07-tracking-analytics.md) | GTM, GA4, Facebook/TikTok Pixel |

### 📄 Migration Analysis

Phân tích chi tiết chuyển đổi từ WordPress sang Next.js 16. So sánh 3 phương án (A/B/C) về chi phí, thời gian, rủi ro. **Đọc khi cân nhắc thay đổi platform** (khuyến nghị khi traffic >10K/ngày).

| File | Mô tả |
| --- | --- |
| [nextjs-migration-analysis.md](migration-analysis/nextjs-migration-analysis.md) | Phân tích chuyển đổi WordPress → Next.js 16 (3 phương án) |

### 🔍 SEO Implementation

6 hướng dẫn triển khai SEO thực tế dựa trên chiến lược ở mục 02-SEO. Từ technical SEO → schema → on-page → content clusters → backlinks → monitoring. **Thực hiện sau khi fix website xong.**

| File | Mô tả |
| --- | --- |
| [01-technical-seo-setup.md](seo-impl/01-technical-seo-setup.md) | Sitemap, robots.txt, GSC, redirects, canonical URLs |
| [02-schema-markup.md](seo-impl/02-schema-markup.md) | Schema.org JSON-LD (Product, Organization, FAQ, Article) |
| [03-onpage-seo-templates.md](seo-impl/03-onpage-seo-templates.md) | Title/meta templates, 23 sản phẩm mẫu, checklist |
| [04-content-clusters.md](seo-impl/04-content-clusters.md) | 4 pillar pages, 24 supporting articles, content map |
| [05-backlink-strategy.md](seo-impl/05-backlink-strategy.md) | 30+ target sites, outreach templates, KOL list |
| [06-seo-monitoring.md](seo-impl/06-seo-monitoring.md) | Weekly/monthly checklists, report template, competitor tracking |

### 📝 Content Publishing

Quy trình publish blog lên WordPress với 52-item checklist, và content calendar tháng 2 (8 bài mới). **Đọc trước khi đăng bài lên website.**

| File | Mô tả |
| --- | --- |
| [01-blog-publishing-guide.md](content-publishing/01-blog-publishing-guide.md) | Quy trình publish blog, 52 checklist items, cấu hình 8 bài |
| [02-content-calendar-month2.md](content-publishing/02-content-calendar-month2.md) | Content calendar tháng 2 (8 bài mới, focus tủ lạnh & máy hút ẩm) |

### 📢 Ads & Social Media

4 hướng dẫn setup & vận hành quảng cáo đa kênh. Từ setup platform → social media ops → optimization. Tổng budget 35M VNĐ/tháng. **Đọc khi sẵn sàng chạy quảng cáo.**

| File | Mô tả |
| --- | --- |
| [01-ads-setup-guide.md](ads-social/01-ads-setup-guide.md) | Facebook & Google Ads setup, campaigns, budget 24.5M VNĐ |
| [02-tiktok-zalo-guide.md](ads-social/02-tiktok-zalo-guide.md) | TikTok Ads + Zalo OA setup, video production, chatbot |
| [03-social-media-operations.md](ads-social/03-social-media-operations.md) | Daily ops, calendar tháng 2, community & crisis management |
| [04-ads-optimization.md](ads-social/04-ads-optimization.md) | KPI tracking, report templates, optimization playbook, ROI calculator |

### 📋 Data Collection

Template thu thập số liệu thực tế từ website, e-commerce, SEO, social media và business. Team điền trực tiếp vào file rồi commit lên repo để phân tích và điều chỉnh chiến lược.

| File | Mô tả |
| --- | --- |
| [data-collection-template.md](data-collection/data-collection-template.md) | Template thu thập dữ liệu 6 mục: GA4 Analytics, WooCommerce, GSC SEO, Social Media, Business Data, Technical — có hướng dẫn lấy dữ liệu và bảng để điền |

### 📊 Marketing Analysis

Phân tích đánh giá toàn diện chiến lược marketing online. Bao gồm chấm điểm 8 tiêu chí, SWOT, ROI dự kiến, so sánh vs best practices, và khuyến nghị điều chỉnh. **Đọc sau khi đã hiểu tổng quan dự án.**

| File | Mô tả |
| --- | --- |
| [marketing-strategy-evaluation.md](marketing-analysis/marketing-strategy-evaluation.md) | Phân tích & đánh giá chiến lược marketing — điểm mạnh, điểm yếu, SWOT, ROI projection, ma trận quyết định, khuyến nghị |

## 🚀 Bước tiếp theo — Triển khai thực tế

> Tất cả tài liệu hướng dẫn đã sẵn sàng. Dưới đây là thứ tự triển khai khuyến nghị.

### Giai đoạn 1: Fix Website & Setup cơ bản (Tuần 1-2)

| # | Hành động | Tài liệu hướng dẫn | Ưu tiên |
|---|---|---|---|
| 1 | Fix 6 lỗi critical (404, demo text, menu) | [01-critical-fixes.md](website-dev/01-critical-fixes.md) | 🔴 Cao |
| 2 | Việt hóa website + tạo 4 trang nội dung | [02-localization-content.md](website-dev/02-localization-content.md) | 🔴 Cao |
| 3 | Cài đặt & cấu hình 10 plugin | [03-plugin-setup.md](website-dev/03-plugin-setup.md) | 🔴 Cao |
| 4 | Bảo mật WordPress (SSL, Wordfence, backup) | [05-security.md](website-dev/05-security.md) | 🔴 Cao |

### Giai đoạn 2: SEO & Performance (Tuần 2-3)

| # | Hành động | Tài liệu hướng dẫn | Ưu tiên |
|---|---|---|---|
| 5 | Setup technical SEO (sitemap, robots.txt, GSC) | [01-technical-seo-setup.md](seo-impl/01-technical-seo-setup.md) | 🟠 Cao |
| 6 | Triển khai Schema Markup (Product, Organization) | [02-schema-markup.md](seo-impl/02-schema-markup.md) | 🟠 Cao |
| 7 | Tối ưu performance & setup Cloudflare CDN | [04-performance-cdn.md](website-dev/04-performance-cdn.md) | 🟠 Cao |
| 8 | Tối ưu mobile & UX | [06-mobile-ux.md](website-dev/06-mobile-ux.md) | 🟡 TB |

### Giai đoạn 3: Content & Tracking (Tuần 3-4)

| # | Hành động | Tài liệu hướng dẫn | Ưu tiên |
|---|---|---|---|
| 9 | Setup tracking (GA4, GTM, Facebook/TikTok Pixel) | [07-tracking-analytics.md](website-dev/07-tracking-analytics.md) | 🟠 Cao |
| 10 | Publish 8 bài blog tháng 1 | [01-blog-publishing-guide.md](content-publishing/01-blog-publishing-guide.md) | 🟠 Cao |
| 11 | Áp dụng on-page SEO cho tất cả trang | [03-onpage-seo-templates.md](seo-impl/03-onpage-seo-templates.md) | 🟡 TB |
| 12 | Bắt đầu xây dựng content clusters | [04-content-clusters.md](seo-impl/04-content-clusters.md) | 🟡 TB |

### Giai đoạn 4: Ads & Social Media (Tháng 2)

| # | Hành động | Tài liệu hướng dẫn | Ưu tiên |
|---|---|---|---|
| 13 | Setup & launch Facebook + Google Ads | [01-ads-setup-guide.md](ads-social/01-ads-setup-guide.md) | 🟠 Cao |
| 14 | Setup TikTok + Zalo OA | [02-tiktok-zalo-guide.md](ads-social/02-tiktok-zalo-guide.md) | 🟡 TB |
| 15 | Vận hành social media hàng ngày | [03-social-media-operations.md](ads-social/03-social-media-operations.md) | 🟡 TB |
| 16 | Publish 8 bài blog tháng 2 | [02-content-calendar-month2.md](content-publishing/02-content-calendar-month2.md) | 🟡 TB |

### Giai đoạn 5: Tối ưu & Mở rộng (Tháng 3+)

| # | Hành động | Tài liệu hướng dẫn | Ưu tiên |
|---|---|---|---|
| 17 | Triển khai backlink strategy | [05-backlink-strategy.md](seo-impl/05-backlink-strategy.md) | 🟡 TB |
| 18 | A/B test & tối ưu quảng cáo | [04-ads-optimization.md](ads-social/04-ads-optimization.md) | 🟡 TB |
| 19 | SEO monitoring & reporting hàng tuần/tháng | [06-seo-monitoring.md](seo-impl/06-seo-monitoring.md) | 🟢 Ongoing |
| 20 | Đánh giá chuyển đổi sang Next.js (khi traffic >10K/ngày) | [nextjs-migration-analysis.md](migration-analysis/nextjs-migration-analysis.md) | 🟢 Dài hạn |

## 📚 Reference — Tra cứu nhanh

> Bảng tra cứu theo chủ đề — tìm nhanh tài liệu cần đọc.

### Theo chủ đề

| Chủ đề | Tài liệu chính | Tài liệu bổ sung |
|---|---|---|
| **Fix lỗi website** | [01-critical-fixes.md](website-dev/01-critical-fixes.md) | [bug-fix-checklist.md](marketing/01-technical-audit/bug-fix-checklist.md), [website-audit-report.md](marketing/01-technical-audit/website-audit-report.md) |
| **Việt hóa & Nội dung** | [02-localization-content.md](website-dev/02-localization-content.md) | [about-us-page-content.md](marketing/04-trust-building/about-us-page-content.md), [policy-pages/](marketing/04-trust-building/policy-pages/) |
| **Plugin & Cấu hình** | [03-plugin-setup.md](website-dev/03-plugin-setup.md) | [technical-recommendations.md](marketing/01-technical-audit/technical-recommendations.md) |
| **Performance & CDN** | [04-performance-cdn.md](website-dev/04-performance-cdn.md) | [technical-recommendations.md](marketing/01-technical-audit/technical-recommendations.md) |
| **Bảo mật** | [05-security.md](website-dev/05-security.md) | [03-plugin-setup.md](website-dev/03-plugin-setup.md) (Wordfence section) |
| **Mobile & UX** | [06-mobile-ux.md](website-dev/06-mobile-ux.md) | [conversion-optimization.md](marketing/04-trust-building/conversion-optimization.md) |
| **Tracking & Analytics** | [07-tracking-analytics.md](website-dev/07-tracking-analytics.md) | [tracking-setup-guide.md](marketing/06-measurement/tracking-setup-guide.md), [kpis-dashboard.md](marketing/06-measurement/kpis-dashboard.md) |
| **SEO tổng thể** | [seo-strategy.md](marketing/02-seo/seo-strategy.md) | [keyword-map.md](marketing/02-seo/keyword-map.md), [technical-seo-checklist.md](marketing/02-seo/technical-seo-checklist.md) |
| **SEO triển khai** | [01-technical-seo-setup.md](seo-impl/01-technical-seo-setup.md) | [02-schema-markup.md](seo-impl/02-schema-markup.md), [03-onpage-seo-templates.md](seo-impl/03-onpage-seo-templates.md) |
| **Content & Blog** | [01-blog-publishing-guide.md](content-publishing/01-blog-publishing-guide.md) | [content-strategy.md](marketing/03-content-marketing/content-strategy.md), [content-calendar-month1.md](marketing/03-content-marketing/content-calendar-month1.md) |
| **Content Clusters** | [04-content-clusters.md](seo-impl/04-content-clusters.md) | [keyword-map.md](marketing/02-seo/keyword-map.md) |
| **Backlinks** | [05-backlink-strategy.md](seo-impl/05-backlink-strategy.md) | [seo-strategy.md](marketing/02-seo/seo-strategy.md) |
| **Facebook & Google Ads** | [01-ads-setup-guide.md](ads-social/01-ads-setup-guide.md) | [facebook-ads-plan.md](marketing/05-digital-marketing/facebook-ads-plan.md), [google-ads-plan.md](marketing/05-digital-marketing/google-ads-plan.md) |
| **TikTok & Zalo** | [02-tiktok-zalo-guide.md](ads-social/02-tiktok-zalo-guide.md) | [tiktok-strategy.md](marketing/05-digital-marketing/tiktok-strategy.md) |
| **Social Media** | [03-social-media-operations.md](ads-social/03-social-media-operations.md) | [social-media-calendar-month1.md](marketing/05-digital-marketing/social-media-calendar-month1.md), [social-media-templates.md](marketing/05-digital-marketing/social-media-templates.md) |
| **Tối ưu quảng cáo** | [04-ads-optimization.md](ads-social/04-ads-optimization.md) | [ads-budget-proposal.md](marketing/05-digital-marketing/ads-budget-proposal.md) |
| **Báo cáo & KPIs** | [06-seo-monitoring.md](seo-impl/06-seo-monitoring.md) | [kpis-dashboard.md](marketing/06-measurement/kpis-dashboard.md), [weekly-report-template.md](marketing/06-measurement/weekly-report-template.md), [okrs-q1.md](marketing/06-measurement/okrs-q1.md) |
| **Thu thập dữ liệu** | [data-collection-template.md](data-collection/data-collection-template.md) | — |
| **Đánh giá chiến lược** | [marketing-strategy-evaluation.md](marketing-analysis/marketing-strategy-evaluation.md) | [kpis-dashboard.md](marketing/06-measurement/kpis-dashboard.md), [okrs-q1.md](marketing/06-measurement/okrs-q1.md) |
| **Migration Next.js** | [nextjs-migration-analysis.md](migration-analysis/nextjs-migration-analysis.md) | — |

### Theo vai trò

| Vai trò | Đọc trước | Đọc khi cần |
|---|---|---|
| **Project Manager** | README, [Lộ trình](#-lộ-trình), [KPIs](marketing/06-measurement/kpis-dashboard.md), [OKRs](marketing/06-measurement/okrs-q1.md) | [Weekly Report](marketing/06-measurement/weekly-report-template.md), [Ads Budget](marketing/05-digital-marketing/ads-budget-proposal.md) |
| **WordPress Developer** | [01-critical-fixes.md](website-dev/01-critical-fixes.md), [03-plugin-setup.md](website-dev/03-plugin-setup.md), [05-security.md](website-dev/05-security.md) | [04-performance-cdn.md](website-dev/04-performance-cdn.md), [06-mobile-ux.md](website-dev/06-mobile-ux.md), [07-tracking-analytics.md](website-dev/07-tracking-analytics.md) |
| **SEO Specialist** | [01-technical-seo-setup.md](seo-impl/01-technical-seo-setup.md), [03-onpage-seo-templates.md](seo-impl/03-onpage-seo-templates.md), [keyword-map.md](marketing/02-seo/keyword-map.md) | [02-schema-markup.md](seo-impl/02-schema-markup.md), [04-content-clusters.md](seo-impl/04-content-clusters.md), [05-backlink-strategy.md](seo-impl/05-backlink-strategy.md) |
| **Content Writer** | [01-blog-publishing-guide.md](content-publishing/01-blog-publishing-guide.md), [content-strategy.md](marketing/03-content-marketing/content-strategy.md) | [Blog Articles](marketing/03-content-marketing/blog-articles/), [02-content-calendar-month2.md](content-publishing/02-content-calendar-month2.md) |
| **Marketing Manager** | [digital-marketing-strategy.md](marketing/05-digital-marketing/digital-marketing-strategy.md), [01-ads-setup-guide.md](ads-social/01-ads-setup-guide.md) | [04-ads-optimization.md](ads-social/04-ads-optimization.md), [03-social-media-operations.md](ads-social/03-social-media-operations.md) |

## 🗺️ Lộ trình

| Tháng | Focus | Deliverables |
| --- | --- | --- |
| Tháng 1 | Fix website + SEO setup + Content đầu tiên | 8 blog posts, tracking setup, policy pages |
| Tháng 2 | Scale content + Launch ads | 8 blog posts thêm, Facebook + Google Ads live, social media active |
| Tháng 3 | Optimize + Expand | A/B test ads, TikTok launch, review collection, performance review |

## 📞 Liên hệ

- **Website:** [xiaomi247.com](https://xiaomi247.com)
- **Chủ sở hữu:** Karomind
- **Kênh hỗ trợ:** Zalo · Messenger · SMS · Điện thoại · Google Maps

> Dự án được quản lý bởi Karomind. Tài liệu trong repository này phục vụ mục đích nội bộ.