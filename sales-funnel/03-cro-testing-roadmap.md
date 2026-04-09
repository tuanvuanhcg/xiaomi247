# KẾ HOẠCH A/B TESTING & TỐI ƯU CONVERSION RATE (CRO) — XIAOMI247.COM

> **Ngày tạo:** 09/04/2026
> **Phiên bản:** 1.0
> **Áp dụng cho:** WordPress + WooCommerce
> **Tham chiếu:**
> - [Conversion Optimization](../marketing/04-trust-building/conversion-optimization.md)
> - [Mobile UX](../website-dev/06-mobile-ux.md)
> - [Sales Funnel Strategy](./01-sales-funnel-strategy.md)

---

## Mục lục

1. [Tổng quan CRO](#1-tổng-quan-cro)
2. [CRO Audit Framework](#2-cro-audit-framework)
3. [Quick Wins — Triển khai ngay](#3-quick-wins--triển-khai-ngay)
4. [12-Week Testing Roadmap](#4-12-week-testing-roadmap)
5. [Testing Methodology](#5-testing-methodology)
6. [Heatmap & Session Recording](#6-heatmap--session-recording)
7. [Page-specific CRO Guides](#7-page-specific-cro-guides)
8. [Tools & Setup](#8-tools--setup)
9. [Conversion Rate Targets](#9-conversion-rate-targets)
10. [Reporting Template](#10-reporting-template)
11. [Checklist triển khai CRO Program](#11-checklist-triển-khai-cro-program)

---

## 1. TỔNG QUAN CRO

### 1.1. Conversion Rate là gì?

**Conversion Rate (CR)** = Số lượng chuyển đổi / Tổng số visitors × 100%

Ví dụ: Website có 10.000 sessions/tháng, 200 đơn hàng → CR = 200 / 10.000 = **2%**

Conversion không chỉ là "mua hàng" — bất kỳ hành động mong muốn nào cũng là conversion:
- **Macro conversion:** Đặt hàng thành công, thanh toán
- **Micro conversion:** Add to cart, đăng ký email, click Zalo tư vấn, xem video sản phẩm

### 1.2. Benchmark E-commerce Việt Nam

| Chỉ số | Thấp | Trung bình | Tốt | Xuất sắc |
|--------|------|-----------|-----|----------|
| **Overall CR** | < 0.5% | 1-2% | 2-3% | > 3% |
| **Add to Cart Rate** | < 3% | 5-8% | 8-12% | > 12% |
| **Cart → Checkout** | < 30% | 40-50% | 50-60% | > 60% |
| **Checkout → Purchase** | < 40% | 50-60% | 60-70% | > 70% |
| **Mobile CR** | < 0.5% | 0.8-1.5% | 1.5-2.5% | > 2.5% |
| **Desktop CR** | < 1% | 1.5-2.5% | 2.5-4% | > 4% |

> 📊 **Ngành điện tử VN:** Trung bình 1-2%. Mục tiêu Xiaomi247: **3-5%** sau 3 tháng tối ưu.

### 1.3. ROI của CRO so với Quảng cáo

| Phương pháp | Chi phí | Hiệu quả | Thời gian | Bền vững |
|------------|---------|----------|----------|----------|
| **Tăng traffic (Ads)** | Cao — tăng liên tục | Tuyến tính: gấp đôi chi phí = gấp đôi traffic | Ngay lập tức | ❌ Dừng ads = hết traffic |
| **CRO (tối ưu CR)** | Thấp — chi phí 1 lần | Cộng hưởng: CR tăng 1% = doanh thu tăng 50%+ | 1-3 tháng | ✅ Hiệu quả lâu dài |

**Ví dụ cụ thể cho Xiaomi247:**

```
Hiện tại:  10,000 sessions × 1.5% CR × 3,000,000đ AOV = 450,000,000đ/tháng
Sau CRO:   10,000 sessions × 3.0% CR × 3,000,000đ AOV = 900,000,000đ/tháng
                                                         ↑ +450,000,000đ (+100%)

→ Tăng CR từ 1.5% lên 3% = GẤPÔI doanh thu mà KHÔNG cần tăng traffic!
```

**Chi phí CRO ước tính:**
- Công cụ A/B testing: 0đ (dùng giải pháp miễn phí)
- Heatmap (Microsoft Clarity): 0đ
- Nhân lực: 2-3 giờ/tuần cho 1 người
- **ROI kỳ vọng: 500-1000%**

### 1.4. Nguyên tắc CRO cốt lõi

1. **Data-driven:** Mọi thay đổi dựa trên dữ liệu, không phải cảm tính
2. **One change at a time:** Chỉ test 1 yếu tố mỗi lần để biết rõ nguyên nhân
3. **Statistical significance:** Đủ sample size, đủ thời gian, tin cậy 95%
4. **Continuous improvement:** CRO là quá trình liên tục, không phải dự án 1 lần
5. **Customer-centric:** Tối ưu cho trải nghiệm khách hàng, không phải tricks ngắn hạn

---

## 2. CRO AUDIT FRAMEWORK

### 2.1. Heuristic Analysis — 5 Yếu tố đánh giá

Mô hình đánh giá nhanh mỗi trang dựa trên 5 yếu tố (thang điểm 1-5):

| Yếu tố | Câu hỏi đánh giá | Điểm lý tưởng |
|---------|-------------------|---------------|
| **Relevancy (Phù hợp)** | Nội dung trang có khớp với kỳ vọng của khách khi click vào? | 5/5 |
| **Clarity (Rõ ràng)** | Thông tin có dễ hiểu? CTA có rõ ràng? Layout có logic? | 5/5 |
| **Value (Giá trị)** | Khách có thấy rõ giá trị/lợi ích? USP có nổi bật? | 5/5 |
| **Friction (Ma sát)** | Có rào cản nào khiến khách khó thực hiện hành động? | 1/5 (càng thấp càng tốt) |
| **Distraction (Phân tâm)** | Có yếu tố nào làm khách mất tập trung khỏi mục tiêu? | 1/5 (càng thấp càng tốt) |

### 2.2. Checklist đánh giá từng trang

#### Trang sản phẩm (Product Page)

| # | Yếu tố | Hạng mục kiểm tra | ✅/❌ |
|---|--------|-------------------|------|
| 1 | Relevancy | Title/H1 chứa tên sản phẩm chính xác | |
| 2 | Relevancy | Ảnh khớp với sản phẩm thực tế | |
| 3 | Relevancy | Giá hiển thị rõ ràng, đúng | |
| 4 | Clarity | CTA ("Thêm vào giỏ") nổi bật, dễ tìm | |
| 5 | Clarity | Thông số kỹ thuật dễ đọc (bảng, bullet points) | |
| 6 | Clarity | Breadcrumb navigation rõ ràng | |
| 7 | Value | Trust badges hiển thị (chính hãng, bảo hành, đổi trả) | |
| 8 | Value | Social proof (rating, số đánh giá, số đã bán) | |
| 9 | Value | USP/lợi ích nổi bật (freeship, BH 18T) | |
| 10 | Friction | Không yêu cầu đăng nhập để mua | |
| 11 | Friction | Ít bước để thêm vào giỏ (< 2 clicks) | |
| 12 | Friction | Tốc độ tải trang < 3 giây | |
| 13 | Distraction | Không có popup quá nhiều | |
| 14 | Distraction | Không có banner/ads không liên quan | |
| 15 | Distraction | Navigation không quá phức tạp | |


#### Homepage

| # | Yếu tố | Hạng mục kiểm tra | ✅/❌ |
|---|--------|-------------------|------|
| 1 | Relevancy | Hero banner phản ánh đúng value proposition | |
| 2 | Relevancy | Danh mục sản phẩm phù hợp với nhu cầu khách | |
| 3 | Clarity | CTA trên banner rõ ràng, dễ click | |
| 4 | Clarity | Categories dễ tìm, có icon/hình minh họa | |
| 5 | Value | Flash sale/khuyến mãi nổi bật | |
| 6 | Value | Trust badges section hiển thị | |
| 7 | Value | Social proof (đánh giá khách hàng) | |
| 8 | Friction | Tốc độ tải < 3 giây (bao gồm slider) | |
| 9 | Friction | Search bar dễ tìm, hoạt động tốt | |
| 10 | Distraction | Không quá nhiều slider (max 3-5 slides) | |

#### Checkout Page

| # | Yếu tố | Hạng mục kiểm tra | ✅/❌ |
|---|--------|-------------------|------|
| 1 | Relevancy | Tóm tắt đơn hàng hiển thị rõ (ảnh, tên, giá) | |
| 2 | Clarity | Form fields có label rõ ràng bằng tiếng Việt | |
| 3 | Clarity | Error messages cụ thể, hữu ích | |
| 4 | Clarity | Progress bar hiển thị bước hiện tại | |
| 5 | Value | Trust badges (SSL, đổi trả, chính hãng) | |
| 6 | Value | Free shipping threshold rõ ràng | |
| 7 | Friction | Guest checkout (không bắt đăng ký) | |
| 8 | Friction | Số fields tối thiểu (< 7 required fields) | |
| 9 | Friction | Auto-fill hoạt động (autocomplete attributes) | |
| 10 | Distraction | Ẩn navigation/menu phức tạp khi checkout | |

#### Category Page

| # | Yếu tố | Hạng mục kiểm tra | ✅/❌ |
|---|--------|-------------------|------|
| 1 | Relevancy | Tiêu đề trang khớp với danh mục | |
| 2 | Clarity | Filter/Sort dễ sử dụng | |
| 3 | Clarity | Product cards hiển thị đủ thông tin (ảnh, tên, giá, rating) | |
| 4 | Value | Badge sale/hot/new trên sản phẩm | |
| 5 | Friction | Pagination hoặc infinite scroll hoạt động tốt | |
| 6 | Distraction | Sidebar không chiếm quá nhiều không gian | |

### 2.3. Cách thực hiện CRO Audit

**Bước 1:** Chụp screenshot mỗi trang quan trọng (desktop + mobile)
**Bước 2:** Đánh giá 5 yếu tố cho mỗi trang (điểm 1-5)
**Bước 3:** Ghi chú cụ thể vấn đề + đề xuất cải thiện
**Bước 4:** Sắp xếp theo impact (cao → thấp) và effort (thấp → cao)
**Bước 5:** Ưu tiên triển khai: Quick wins trước, A/B test cho thay đổi lớn

```
Scoring Matrix:
┌──────────────────────────────────────────┐
│           IMPACT (Tác động)              │
│       Thấp          Cao                  │
│  ┌─────────────┬─────────────┐           │
│  │ BỎ QUA      │ ĐƯA VÀO    │  EFFORT   │
│  │             │ BACKLOG     │  Cao      │
│  ├─────────────┼─────────────┤           │
│  │ ĐỂ SAU     │ ★ QUICK WIN │  EFFORT   │
│  │             │ LÀM NGAY!  │  Thấp     │
│  └─────────────┴─────────────┘           │
└──────────────────────────────────────────┘
```

---

## 3. QUICK WINS — TRIỂN KHAI NGAY

> Những thay đổi có thể implement ngay, không cần A/B test vì đã được chứng minh hiệu quả rộng rãi trong e-commerce.

### 3.1. Trust & Social Proof (Ưu tiên cao)

| # | Quick Win | Mô tả | Impact | Effort |
|---|-----------|-------|--------|--------|
| 1 | **Trust badges** | Thêm icons: 🛡️ Chính hãng, 🚚 Freeship, 🔧 BH 18T, 🔄 Đổi trả 7 ngày — đặt dưới giá SP và cạnh CTA | ★★★★★ | ★☆☆☆☆ |
| 2 | **Ratings & Reviews** | Bật WooCommerce Reviews, hiển thị rating sao + số lượng đánh giá ngay dưới tên SP | ★★★★★ | ★★☆☆☆ |
| 3 | **Số lượng đã bán** | Hiển thị "📦 Đã bán 456 sản phẩm" trên product page | ★★★★☆ | ★☆☆☆☆ |
| 4 | **Số người đang xem** | "👥 23 người đang xem sản phẩm này" (real-time hoặc estimated) | ★★★☆☆ | ★★☆☆☆ |
| 5 | **Đánh giá kèm ảnh** | Cho phép khách upload ảnh khi review sản phẩm | ★★★★☆ | ★★☆☆☆ |

### 3.2. CTA & Conversion Elements

| # | Quick Win | Mô tả | Impact | Effort |
|---|-----------|-------|--------|--------|
| 6 | **Tối ưu CTA text** | Đổi "Add to cart" → "🛒 THÊM VÀO GIỎ HÀNG" (tiếng Việt, có icon, in hoa) | ★★★★★ | ★☆☆☆☆ |
| 7 | **Sticky add-to-cart bar** | Thanh CTA cố định ở bottom khi scroll trên mobile: giá + nút "THÊM GIỎ" | ★★★★★ | ★★☆☆☆ |
| 8 | **Sticky hotline/Zalo** | Nút gọi điện + Zalo chat cố định góc phải dưới màn hình | ★★★★☆ | ★☆☆☆☆ |
| 9 | **CTA button color** | Nút chính màu cam (#FF6D00), đủ lớn (min 52px height), full-width trên mobile | ★★★★☆ | ★☆☆☆☆ |
| 10 | **"Mua ngay" button** | Thêm nút "⚡ MUA NGAY" cho phép skip cart → checkout trực tiếp | ★★★★☆ | ★★★☆☆ |

### 3.3. UX & Performance

| # | Quick Win | Mô tả | Impact | Effort |
|---|-----------|-------|--------|--------|
| 11 | **Giảm bước checkout** | Chuyển sang 2-step checkout: Thông tin giao hàng → Thanh toán & Xác nhận | ★★★★★ | ★★★☆☆ |
| 12 | **Guest checkout** | Cho phép mua không cần đăng ký tài khoản | ★★★★★ | ★★☆☆☆ |
| 13 | **Lazy load images** | Chỉ load ảnh khi scroll đến — giảm thời gian tải trang 40-60% | ★★★★☆ | ★☆☆☆☆ |
| 14 | **Breadcrumb navigation** | Thêm breadcrumb trên mọi trang: Trang chủ > Danh mục > Sản phẩm | ★★★☆☆ | ★☆☆☆☆ |
| 15 | **Free shipping threshold** | Progress bar trên cart: "Thêm 120.000đ để được FREE SHIP 🚚" | ★★★★☆ | ★★☆☆☆ |

### 3.4. Pricing & Urgency

| # | Quick Win | Mô tả | Impact | Effort |
|---|-----------|-------|--------|--------|
| 16 | **Anchor pricing** | Hiển thị giá gốc gạch ngang + giá sale + % giảm + "Tiết kiệm X đồng" | ★★★★★ | ★☆☆☆☆ |
| 17 | **Countdown timer** | Cho sản phẩm flash sale: "⏰ Giá ưu đãi còn 2 ngày 15:30:22" | ★★★★☆ | ★★☆☆☆ |
| 18 | **"Giao trong ngày"** | Badge "⏰ Đặt trước 15h — Giao trong ngày (nội thành)" | ★★★☆☆ | ★☆☆☆☆ |

### 3.5. Thứ tự triển khai Quick Wins

```
Tuần 1 (Ngay lập tức):
  ✅ Trust badges trên product page (#1)
  ✅ Tối ưu CTA text tiếng Việt (#6)
  ✅ CTA button color cam (#9)
  ✅ Sticky hotline/Zalo (#8)
  ✅ Breadcrumb navigation (#14)
  ✅ Anchor pricing (#16)

Tuần 2:
  ✅ Bật Reviews & Ratings (#2)
  ✅ Sticky add-to-cart bar mobile (#7)
  ✅ Guest checkout (#12)
  ✅ Lazy load images (#13)
  ✅ Số lượng đã bán (#3)

Tuần 3:
  ✅ Giảm bước checkout (#11)
  ✅ Free shipping threshold bar (#15)
  ✅ "Mua ngay" button (#10)
  ✅ Countdown timer (#17)
  ✅ Người đang xem (#4)
  ✅ Đánh giá kèm ảnh (#5)
  ✅ Badge giao trong ngày (#18)

---

## 4. 12-WEEK TESTING ROADMAP

> **Nguyên tắc:** 1 test/tuần, chạy tối thiểu 7 ngày, đạt 95% statistical significance trước khi kết luận.
> **Thứ tự:** Product Page (tuần 1-4) → Homepage (tuần 5-8) → Checkout (tuần 9-12)

### 4.1. TUẦN 1-4: PRODUCT PAGE TESTS

#### Tuần 1 — CTA Button Optimization

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu thay đổi màu nút CTA từ xám/xanh sang cam (#FF6D00) và tăng kích thước lên 52px height trên product page, thì add-to-cart rate sẽ tăng 15-20% vì nút nổi bật hơn và dễ nhấn hơn trên mobile |
| **Control (A)** | Nút CTA hiện tại (màu mặc định theme, kích thước nhỏ) |
| **Variant (B)** | Nút cam #FF6D00, min-height 52px, full-width mobile, text "🛒 THÊM VÀO GIỎ HÀNG" |
| **Metric chính** | Add to Cart Rate (add_to_cart / view_item) |
| **Metric phụ** | Click-through rate trên CTA, Checkout rate |
| **Duration** | 7 ngày |
| **Sample size** | 1,000+ product page views per variant (2,000+ total) |

#### Tuần 2 — Image Layout: Gallery vs Slider

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu chuyển từ image slider sang gallery grid (hiển thị 4 ảnh cùng lúc + thumbnails) trên product page, thì engagement tăng 10% vì khách xem được nhiều góc ảnh nhanh hơn |
| **Control (A)** | Slider ảnh (swipe 1 ảnh/lần, dots indicator) |
| **Variant (B)** | Gallery grid: 1 ảnh lớn + 4 thumbnails dưới, click để zoom |
| **Metric chính** | Product page engagement time |
| **Metric phụ** | Add to Cart Rate, Image interaction rate |
| **Duration** | 7 ngày |
| **Sample size** | 1,000+ product page views per variant |

#### Tuần 3 — Price Display Optimization

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu hiển thị giá gốc gạch ngang + giá sale lớn + badge "Tiết kiệm X đồng" thay vì chỉ hiển thị giá bán, thì add-to-cart rate tăng 20% vì khách cảm nhận giá trị tốt hơn (anchor pricing effect) |
| **Control (A)** | Chỉ hiển thị giá bán: "4.990.000đ" |
| **Variant (B)** | Giá gốc gạch ngang + giá sale + % giảm: "~~5.990.000đ~~ **4.990.000đ** -17% 💰 Tiết kiệm 1.000.000đ" |
| **Metric chính** | Add to Cart Rate |
| **Metric phụ** | Revenue per visitor, Average Order Value |
| **Duration** | 7 ngày |
| **Sample size** | 1,000+ product page views per variant |

#### Tuần 4 — Trust Badges Placement

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu đặt trust badges (chính hãng, freeship, BH, đổi trả) ngay dưới nút CTA thay vì ở cuối trang, thì add-to-cart rate tăng 12% vì khách thấy đảm bảo ngay trước khi quyết định |
| **Control (A)** | Trust badges ở cuối product page (dưới description) |
| **Variant (B)** | Trust badges ngay dưới nút CTA: 🛡️ Chính hãng · 🚚 Freeship · 🔧 BH 18T · 🔄 Đổi trả 7N |
| **Metric chính** | Add to Cart Rate |
| **Metric phụ** | Checkout initiation rate, Bounce rate |
| **Duration** | 7 ngày |
| **Sample size** | 1,000+ product page views per variant |

### 4.2. TUẦN 5-8: HOMEPAGE TESTS

#### Tuần 5 — Hero Banner: Static vs Slider

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu thay slider 5 banner bằng 1 static hero image với CTA rõ ràng, thì click-through rate từ homepage tăng 25% vì khách tập trung vào 1 thông điệp thay vì bị phân tâm bởi nhiều slides |
| **Control (A)** | Slider 5 banners, auto-rotate mỗi 5 giây |
| **Variant (B)** | 1 static hero banner: ảnh chất lượng cao + headline + 1 CTA nổi bật |
| **Metric chính** | Banner CTR (click trên banner / homepage sessions) |
| **Metric phụ** | Homepage bounce rate, Pages per session |
| **Duration** | 7 ngày |
| **Sample size** | 2,000+ homepage sessions per variant |

#### Tuần 6 — CTA Placement on Homepage

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu thêm CTA "Xem khuyến mãi" ngay above the fold (dưới category icons) thay vì chỉ trong banner, thì category page traffic tăng 15% vì CTA dễ thấy hơn trên mobile |
| **Control (A)** | CTA chỉ trong banner slider |
| **Variant (B)** | CTA rõ ràng dưới category icons: "🔥 XEM KHUYẾN MÃI HÔM NAY" (nút cam, full-width) |
| **Metric chính** | Homepage → Category/Product page rate |
| **Metric phụ** | Scroll depth, Click distribution |
| **Duration** | 7 ngày |
| **Sample size** | 2,000+ homepage sessions per variant |

#### Tuần 7 — Category Grid Layout: 2x3 vs 3x4

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu hiển thị category grid 3 cột (hiện nhiều danh mục hơn above the fold) thay vì 2 cột trên mobile, thì category exploration rate tăng 10% vì khách thấy nhiều lựa chọn hơn |
| **Control (A)** | Category grid 2 cột: icon lớn 64x64px + tên dưới |
| **Variant (B)** | Category grid 3 cột: icon nhỏ hơn 48x48px + tên dưới, horizontal scroll |
| **Metric chính** | Category click rate (clicks trên category / homepage views) |
| **Metric phụ** | Homepage scroll depth, Category page sessions |
| **Duration** | 7 ngày |
| **Sample size** | 2,000+ homepage sessions per variant |

#### Tuần 8 — Social Proof Section + Featured Products

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu thêm section "⭐ Khách hàng nói gì" (3 review carousel) trước section "Sản phẩm nổi bật", thì product page visits từ homepage tăng 12% vì social proof tăng niềm tin trước khi xem sản phẩm |
| **Control (A)** | Không có review section trên homepage |
| **Variant (B)** | Carousel 3 reviews (tên + sao + nội dung ngắn + ảnh) trước featured products |
| **Metric chính** | Homepage → Product page rate |
| **Metric phụ** | Time on homepage, Featured products CTR |
| **Duration** | 7 ngày |
| **Sample size** | 2,000+ homepage sessions per variant |

### 4.3. TUẦN 9-12: CHECKOUT TESTS

#### Tuần 9 — Form Fields: Fewer vs More

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu giảm số required fields trong checkout form từ 8 xuống 5 (bỏ email, phường/xã, ghi chú bắt buộc), thì checkout completion rate tăng 15% vì giảm friction |
| **Control (A)** | 8 fields: Họ tên, Email, SĐT, Tỉnh/TP, Quận/Huyện, Phường/Xã, Địa chỉ, Ghi chú |
| **Variant (B)** | 5 fields: Họ tên, SĐT, Tỉnh/TP, Quận/Huyện, Địa chỉ (email + ghi chú = optional, phường/xã bỏ) |
| **Metric chính** | Checkout Completion Rate (purchase / begin_checkout) |
| **Metric phụ** | Form abandonment rate, Time to complete checkout |
| **Duration** | 7 ngày |
| **Sample size** | 200+ checkout initiations per variant |

#### Tuần 10 — Payment Options Order

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu hiển thị COD là mặc định + chuyển khoản QR Code lên vị trí thứ 2 (thay vì VNPAY), thì checkout rate tăng 8% vì COD chiếm 65% đơn hàng VN và QR code ngày càng phổ biến |
| **Control (A)** | Thứ tự: COD → VNPAY → MoMo → Chuyển khoản → Visa |
| **Variant (B)** | Thứ tự: COD (mặc định) → Chuyển khoản (QR Code) → MoMo → VNPAY → Visa |
| **Metric chính** | Checkout Completion Rate |
| **Metric phụ** | Payment method distribution, Payment failure rate |
| **Duration** | 7 ngày |
| **Sample size** | 200+ checkout initiations per variant |

#### Tuần 11 — Shipping Display + Upsell in Checkout

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu hiển thị "🚚 MIỄN PHÍ vận chuyển!" (cho đơn > 500K) thay vì "Phí vận chuyển: 0đ" + thêm upsell 1 sản phẩm phụ kiện ngay trong checkout, thì AOV tăng 10% |
| **Control (A)** | "Phí vận chuyển: 0đ" (plain text), không có upsell |
| **Variant (B)** | "🚚 MIỄN PHÍ vận chuyển!" (badge xanh lá) + "Thêm [Phụ kiện] chỉ 99K?" (1 sản phẩm gợi ý) |
| **Metric chính** | Average Order Value (AOV) |
| **Metric phụ** | Upsell acceptance rate, Checkout completion rate |
| **Duration** | 7 ngày |
| **Sample size** | 200+ checkout initiations per variant |

#### Tuần 12 — Guest Checkout vs Login Prompt

| Hạng mục | Chi tiết |
|----------|---------|
| **Hypothesis** | Nếu mặc định guest checkout (không hiển thị form đăng nhập/đăng ký) thay vì hiển thị options đăng nhập trước, thì checkout completion rate tăng 20% vì giảm friction cho first-time buyers |
| **Control (A)** | Hiển thị "Đăng nhập" + "Đăng ký" + "Mua không cần tài khoản" |
| **Variant (B)** | Mặc định guest checkout, nhỏ gọn link "Đã có tài khoản? Đăng nhập" ở góc |
| **Metric chính** | Checkout Completion Rate |
| **Metric phụ** | Account creation rate, Repeat purchase rate (30 ngày) |
| **Duration** | 7 ngày |
| **Sample size** | 200+ checkout initiations per variant |

### 4.4. Bảng tổng hợp 12-Week Roadmap

| Tuần | Trang | Test | Metric chính | Expected Lift |
|------|-------|------|-------------|--------------|
| 1 | Product | CTA button (color + size + text) | Add to Cart Rate | +15-20% |
| 2 | Product | Image layout (gallery vs slider) | Engagement time | +10% |
| 3 | Product | Price display (anchor pricing) | Add to Cart Rate | +20% |
| 4 | Product | Trust badges placement | Add to Cart Rate | +12% |
| 5 | Homepage | Hero banner (static vs slider) | Banner CTR | +25% |
| 6 | Homepage | CTA placement (above fold) | HP → Category rate | +15% |
| 7 | Homepage | Category grid (2x3 vs 3x4) | Category click rate | +10% |
| 8 | Homepage | Social proof section | HP → Product rate | +12% |
| 9 | Checkout | Form fields (fewer vs more) | Checkout completion | +15% |
| 10 | Checkout | Payment options order | Checkout completion | +8% |
| 11 | Checkout | Shipping display + upsell | AOV | +10% |
| 12 | Checkout | Guest checkout vs login | Checkout completion | +20% |

---

## 5. TESTING METHODOLOGY

### 5.1. Hypothesis Template

Mỗi A/B test **bắt buộc** phải có hypothesis rõ ràng trước khi bắt đầu:

```
"Nếu [thay đổi X] trên [trang Y]
 thì [metric Z] sẽ tăng/giảm [N%]
 vì [lý do/insight]"
```

**Ví dụ:**
- "Nếu **thay đổi màu nút CTA sang cam** trên **trang sản phẩm**, thì **add-to-cart rate** sẽ **tăng 15%** vì **cam là màu có contrast cao nhất trên nền trắng và tạo urgency**"
- "Nếu **bỏ bước đăng ký bắt buộc** trên **checkout**, thì **checkout completion rate** sẽ **tăng 20%** vì **65% khách VN mua 1 lần không muốn tạo tài khoản**"

### 5.2. Statistical Significance (Ý nghĩa thống kê)

- **Confidence level:** 95% (p-value < 0.05)
- Nghĩa là: Có 95% chắc chắn rằng kết quả không phải do ngẫu nhiên
- **Không dừng test sớm** khi thấy kết quả "tốt" — chờ đủ sample size

### 5.3. Sample Size Calculator

**Công thức đơn giản:**

```
Sample Size per Variant = (Zα + Zβ)² × p(1-p) × 2 / (MDE)²

Trong đó:
- Zα = 1.96 (95% confidence)
- Zβ = 0.84 (80% power)
- p = baseline conversion rate
- MDE = Minimum Detectable Effect (mức thay đổi tối thiểu muốn phát hiện)
```

**Bảng tra nhanh Sample Size (per variant):**

| Baseline CR | MDE 10% | MDE 15% | MDE 20% | MDE 25% | MDE 30% |
|------------|---------|---------|---------|---------|---------|
| **1%** | 78,400 | 34,800 | 19,600 | 12,500 | 8,700 |
| **2%** | 38,400 | 17,100 | 9,600 | 6,200 | 4,300 |
| **3%** | 25,000 | 11,100 | 6,300 | 4,000 | 2,800 |
| **5%** | 14,600 | 6,500 | 3,700 | 2,300 | 1,600 |
| **8%** | 8,800 | 3,900 | 2,200 | 1,400 | 1,000 |
| **10%** | 6,900 | 3,100 | 1,700 | 1,100 | 800 |
| **15%** | 4,400 | 1,900 | 1,100 | 700 | 500 |
| **20%** | 3,100 | 1,400 | 800 | 500 | 400 |

> **Cách đọc:** Nếu baseline CR = 3% và muốn phát hiện tăng 20% (từ 3% → 3.6%), cần 6,300 visitors mỗi variant = 12,600 total.

### 5.4. Minimum Detectable Effect (MDE)

MDE là mức thay đổi nhỏ nhất mà test có thể phát hiện được với sample size hiện có.

**Khuyến nghị MDE cho Xiaomi247:**

| Trang | Traffic/tuần ước tính | MDE khả thi | Ghi chú |
|-------|----------------------|-------------|---------|
| Product Page | 2,000-5,000 views | 15-25% | Đủ traffic cho test |
| Homepage | 3,000-8,000 sessions | 10-20% | Traffic cao nhất |
| Checkout | 200-500 initiations | 20-30% | Traffic thấp, cần MDE cao |
| Cart Page | 500-1,500 views | 15-25% | Traffic trung bình |

### 5.5. Quy tắc chạy test

1. **Thời gian tối thiểu:** 7 ngày (bao gồm cả ngày trong tuần và cuối tuần)
2. **Minimum conversions:** 100+ conversions per variant cho metric chính
3. **Không thay đổi giữa chừng:** Không chỉnh sửa variant khi test đang chạy
4. **Một test một lúc:** Không chạy 2 test cùng trang cùng lúc (confounding)
5. **Ghi chép:** Document mọi thứ — hypothesis, setup, kết quả, learnings
6. **External factors:** Ghi chú nếu có sự kiện bất thường (sale, lỗi server, ngày lễ)

---

## 6. HEATMAP & SESSION RECORDING

### 6.1. Microsoft Clarity Setup (Miễn phí, khuyến nghị)

**Tại sao chọn Clarity:**
- ✅ Hoàn toàn miễn phí, không giới hạn traffic
- ✅ GDPR compliant (không thu thập dữ liệu cá nhân)
- ✅ Tích hợp sẵn với Google Analytics 4
- ✅ Heatmaps + Session recordings + Insights tự động
- ✅ Không ảnh hưởng tốc độ tải trang (async loading)

**Cài đặt:**

1. Đăng ký tại [clarity.microsoft.com](https://clarity.microsoft.com)
2. Tạo project mới cho xiaomi247.com
3. Copy tracking code vào `<head>` qua:
   - **Cách 1:** WPCode plugin → Header Scripts
   - **Cách 2:** Theme Customizer → Additional Scripts
   - **Cách 3:** Google Tag Manager → Custom HTML tag
4. Verify cài đặt: chờ 1-2 giờ, kiểm tra Dashboard
5. Kết nối GA4: Settings → Integrations → Google Analytics

### 6.2. Heatmap Analysis

#### Click Maps (Bản đồ click)

**Cách đọc:**
- Màu **đỏ/cam** = vùng nhiều click nhất (hot zone)
- Màu **xanh dương** = ít click
- Màu **trắng/không màu** = không ai click

**Insights cần tìm:**
- Khách click vào đâu nhiều nhất? Có phải CTA không?
- Có "rage clicks" (click nhiều lần vào 1 chỗ)? → Element bị lỗi hoặc không clickable
- Khách click vào elements không phải link? → Cần biến thành link hoặc làm rõ
- CTA chính có nhận được nhiều click không? → Nếu không, cần tối ưu vị trí/design

#### Scroll Maps (Bản đồ cuộn trang)

**Cách đọc:**
- % visitors đạt đến mỗi vị trí trên trang
- "Fold line" = điểm mà content bắt đầu bị ẩn khi mới load
- "Drop-off points" = nơi đa số khách ngừng scroll

**Insights cần tìm:**
- Bao nhiêu % khách scroll qua CTA chính?
- Content nào nằm dưới fold mà ít ai thấy?
- Có nên đưa trust badges / reviews lên cao hơn?
- Trang quá dài? Khách bỏ cuộc ở đâu?

#### Attention Maps (Bản đồ chú ý)

**Cách đọc:**
- Kết hợp click + scroll + hover time
- Vùng khách dành nhiều thời gian nhất

**Insights cần tìm:**
- Khách đọc mô tả sản phẩm hay chỉ xem ảnh?
- Reviews section có được chú ý không?
- Phần nào của trang bị bỏ qua hoàn toàn?

### 6.3. Session Recording

#### Filters quan trọng trong Clarity:

| Filter | Mục đích | Hành động |
|--------|---------|----------|
| **Rage clicks** | Khách click liên tục vào 1 chỗ → frustration | Fix bug, làm rõ clickability |
| **Dead clicks** | Click vào elements không có action | Thêm link hoặc remove misleading design |
| **Excessive scrolling** | Cuộn lên xuống nhiều lần → tìm kiếm thứ gì đó | Cải thiện navigation, search |
| **Quick backs** | Vào trang rồi quay lại ngay | Content không khớp kỳ vọng, fix messaging |
| **Error clicks** | Click gây ra JS error | Fix technical bugs |

#### Cách xem Session Recordings hiệu quả:

1. **Xem sessions có conversion** — Hiểu behavior path thành công
2. **Xem sessions có cart abandonment** — Tìm friction points
3. **Xem sessions từ mobile** — Kiểm tra UX mobile thực tế
4. **Xem sessions dài (>5 phút)** — Khách đang cân nhắc, có gì cản trở?
5. **Xem sessions ngắn (<30 giây)** — Tại sao khách rời đi nhanh?

### 6.4. Insights → Action: Quy trình từ heatmap đến A/B test

```
Bước 1: Thu thập data (2-4 tuần)
  └── Cài Clarity, chờ đủ data (1,000+ sessions)

Bước 2: Phân tích heatmap
  └── Xem click map, scroll map cho mỗi trang quan trọng
  └── Ghi chú: vùng hot, vùng dead, drop-off points

Bước 3: Xem session recordings (20-30 sessions)
  └── Filter: rage clicks, cart abandoners, mobile users
  └── Ghi chú patterns: friction, confusion, errors

Bước 4: Hình thành hypothesis
  └── "Heatmap cho thấy 60% khách không scroll đến trust badges
       → Di chuyển trust badges lên trên CTA
       → Hypothesis: Add-to-cart rate tăng 12%"

Bước 5: A/B test
  └── Setup test, chạy 7+ ngày, đo kết quả

Bước 6: Implement winner & lặp lại
```

### 6.5. Cách đọc Heatmap cho từng trang

#### Product Page
- **Ảnh sản phẩm:** Khách có swipe/zoom không? → Nếu ít, ảnh đầu tiên chưa đủ hấp dẫn
- **Giá:** Có click vào khu vực giá không? → Nếu nhiều, khách quan tâm giá, cần hiển thị rõ hơn
- **CTA:** % click trên CTA so với tổng clicks? → Nên > 30%
- **Tabs (Mô tả/Đánh giá):** Tab nào được click nhiều nhất? → Ưu tiên content đó
- **Scroll depth:** Bao nhiêu % đến reviews? → Nếu < 20%, đưa reviews lên cao

#### Homepage
- **Banner:** Click rate trên banner? → Nếu thấp, thay đổi design/CTA
- **Categories:** Danh mục nào được click nhiều? → Ưu tiên hiển thị
- **Below fold:** % scroll đến featured products? → Nếu < 50%, content above fold chưa hấp dẫn
- **Footer:** Ai scroll đến footer? → Nếu nhiều, khách tìm thông tin → thêm links

#### Checkout
- **Form fields:** Field nào khách dừng lâu? → Có thể gây confusion
- **Error indicators:** Vùng đỏ quanh field nào? → Fix validation/label
- **Payment options:** Method nào được hover/click? → Sắp xếp theo popularity
- **CTA "Đặt hàng":** Heatmap warm hay cold? → Nếu cold, trust chưa đủ

---

## 7. PAGE-SPECIFIC CRO GUIDES

### 7.1. Product Page — 10 Elements to Optimize

| # | Element | Mục tiêu tối ưu | Best Practice | Metric đo |
|---|---------|-----------------|--------------|----------|
| 1 | **Ảnh sản phẩm** | Tăng engagement, giảm return rate | 5-8 ảnh + 1-2 video, zoom, ảnh thực tế, background trắng, alt text tiếng Việt | Image interaction rate |
| 2 | **Giá hiển thị** | Tăng perceived value | Giá gốc gạch + giá sale (lớn, đỏ) + % giảm + "Tiết kiệm X đồng" | Add to cart rate |
| 3 | **Mô tả sản phẩm** | Giảm uncertainty, tăng trust | USP bullet points đầu tiên, specs bảng rõ ràng, ảnh minh họa trong mô tả | Time on page |
| 4 | **CTA buttons** | Tăng add-to-cart rate | Nút cam #FF6D00, full-width mobile, text tiếng Việt có icon, min 52px | Add to cart rate |
| 5 | **Reviews & Ratings** | Tăng trust, social proof | Rating sao ngay dưới tên SP, cho upload ảnh, hiển thị filter theo sao | Review engagement |
| 6 | **Trust badges** | Giảm lo ngại mua hàng | 4 badges cạnh CTA: chính hãng, freeship, BH, đổi trả. Background nhẹ nổi bật | Bounce rate |
| 7 | **Related products** | Tăng page views, cross-sell | "Thường mua cùng" + "Sản phẩm tương tự", horizontal scroll, max 6 SP | Cross-sell rate |
| 8 | **Urgency elements** | Tạo FOMO, thúc đẩy mua | Countdown (sale), stock count (<10), người đang xem. CHỈ hiển thị thông tin thật | Conversion rate |
| 9 | **Share buttons** | Tăng reach organic | Zalo, Facebook, Copy link. Nhỏ gọn, không chiếm diện tích CTA | Share rate |
| 10 | **Breadcrumb** | Giảm bounce, tăng navigation | Trang chủ > Danh mục > Sản phẩm. Schema markup cho SEO | Pages per session |

### 7.2. Homepage — 8 Elements to Optimize

| # | Element | Best Practice | Metric đo |
|---|---------|--------------|----------|
| 1 | **Hero banner** | 1 static image tốt hơn slider 5 banners. CTA rõ ràng, text đọc được trên mobile | Banner CTR |
| 2 | **Categories** | Icons + tên, horizontal scroll trên mobile, max 8-10 danh mục | Category click rate |
| 3 | **Bestsellers** | Grid 2 cột mobile, badge "Bán chạy", giá + giá gốc + rating | Product page visits |
| 4 | **Trust section** | 4 badges grid 2x2: chính hãng, freeship, BH, đổi trả. Background nhẹ (#FFF3E0) | Bounce rate |
| 5 | **Blog/Tin tức** | 2-3 bài mới nhất, ảnh thumbnail, title hấp dẫn. Link "Xem tất cả" | Blog CTR |
| 6 | **Popup** | Exit-intent only, 1 lần/session, delay 30s, offer giảm 100K đơn đầu | Opt-in rate |
| 7 | **Search bar** | Nổi bật trên header, auto-suggest, trending keywords, recent searches | Search usage rate |
| 8 | **CTA cuối trang** | Form đăng ký email/SĐT: "Nhận tin khuyến mãi sớm nhất" | Email opt-in rate |

### 7.3. Cart Page — 6 Elements to Optimize

| # | Element | Best Practice | Metric đo |
|---|---------|--------------|----------|
| 1 | **Upsell suggestions** | "Thường mua cùng" 2-3 phụ kiện dưới cart items, nút "Thêm" nhanh | Upsell rate |
| 2 | **Free shipping bar** | Progress bar: "Thêm 120.000đ để FREE SHIP 🚚" + gợi ý SP nhỏ | AOV increase |
| 3 | **Trust badges** | "🔄 Đổi trả 7 ngày" + "🔒 Thanh toán an toàn" ngay trên CTA checkout | Cart → Checkout rate |
| 4 | **CTA checkout** | "TIẾN HÀNH THANH TOÁN" — cam, full-width, sticky bottom trên mobile | Cart → Checkout rate |
| 5 | **Saved items** | "Lưu cho lần sau" cho items bị xóa khỏi giỏ → recovery later | Return visit rate |
| 6 | **Countdown timer** | Cho items đang flash sale: "⏰ Giá ưu đãi hết sau 2:15:30" | Cart → Checkout rate |

### 7.4. Checkout Page — 8 Elements to Optimize

| # | Element | Best Practice | Metric đo |
|---|---------|--------------|----------|
| 1 | **Progress bar** | 2-3 bước, step hiện tại highlight, completed steps có checkmark ✅ | Checkout completion |
| 2 | **Form fields** | Min required fields, label trên input, autocomplete attributes, keyboard phù hợp | Form completion time |
| 3 | **Payment options** | COD mặc định, icons/logos cho mỗi option, radio button lớn (48px touch) | Payment selection rate |
| 4 | **Shipping info** | "Nội thành: 1-2 ngày, Tỉnh: 3-5 ngày", hiển thị logo đơn vị vận chuyển | Trust perception |
| 5 | **Coupon input** | Collapsed mặc định ("Có mã giảm giá?"), nút "Áp dụng" rõ ràng | Coupon usage rate |
| 6 | **Trust signals** | 🔒 SSL + 🛡️ Chính hãng + 🔄 Đổi trả ngay trên nút "Đặt hàng" | Checkout completion |
| 7 | **CTA "Đặt hàng"** | Cam #FF6D00, full-width, sticky bottom, min 52px, text "🛒 ĐẶT HÀNG" | Checkout completion |
| 8 | **Error handling** | Real-time validation, error messages tiếng Việt, auto-scroll đến field lỗi | Error recovery rate |

### 7.5. Category Page — 6 Elements to Optimize

| # | Element | Best Practice | Metric đo |
|---|---------|--------------|----------|
| 1 | **Filters** | Giá, thương hiệu, tính năng. Mobile: bottom sheet/modal, không sidebar | Filter usage rate |
| 2 | **Sort options** | Mặc định: "Bán chạy nhất", options: Giá thấp→cao, Giá cao→thấp, Mới nhất, Rating | Sort usage rate |
| 3 | **Product cards** | Ảnh + tên + giá + giá gốc + % giảm + rating. Badge "HOT"/"MỚI" | Product page CTR |
| 4 | **Pagination** | Infinite scroll hoặc "Xem thêm" button (không phân trang số) trên mobile | Pages per session |
| 5 | **Quick add-to-cart** | Nút "Thêm giỏ" trên card (desktop hover, mobile tap) | Add to cart rate |
| 6 | **Breadcrumb** | Trang chủ > Danh mục chính > Danh mục phụ. Clickable, schema markup | Navigation efficiency |

---

## 8. TOOLS & SETUP

### 8.1. A/B Testing Tools

> Google Optimize đã ngừng hoạt động (09/2023). Dưới đây là các lựa chọn thay thế.

| Tool | Giá | Ưu điểm | Nhược điểm | Phù hợp |
|------|-----|---------|-----------|---------|
| **VWO (Visual Website Optimizer)** | Từ $199/tháng | Visual editor, heatmaps tích hợp, split URL testing | Giá cao cho startup | Khi có budget CRO |
| **Optimizely** | Liên hệ | Enterprise-grade, feature flags, personalization | Giá rất cao | Khi scale lớn |
| **Custom CSS/JS (Khuyến nghị ban đầu)** | 0đ | Miễn phí, linh hoạt, kiểm soát hoàn toàn | Cần developer, không có visual editor | Giai đoạn đầu |
| **Google Tag Manager** | 0đ | Miễn phí, A/B test đơn giản qua custom JS | Không có reporting tích hợp | Kết hợp với GA4 |
| **Nelio A/B Testing (WordPress)** | Từ $49/tháng | Plugin WordPress native, dễ dùng | Chỉ dành cho WordPress | WordPress sites |

**Khuyến nghị cho Xiaomi247 (giai đoạn đầu):**
1. Dùng **Custom CSS/JS qua Google Tag Manager** cho A/B tests đơn giản
2. Tracking bằng **GA4 custom events** (gtag('event', 'experiment_variant', {variant: 'B'}))
3. Phân tích bằng **GA4 Explorations** (funnel, comparison)
4. Nâng cấp lên **VWO hoặc Nelio** khi có budget và chạy nhiều tests đồng thời

### 8.2. Heatmap & Recording Tools

| Tool | Giá | Tính năng | Khuyến nghị |
|------|-----|----------|------------|
| **Microsoft Clarity** | 🆓 Miễn phí | Heatmaps, session recordings, insights AI, GA4 integration | ⭐ Khuyến nghị #1 |
| **Hotjar** | Từ $32/tháng | Heatmaps, recordings, surveys, feedback | Khi cần surveys |
| **Lucky Orange** | Từ $32/tháng | Heatmaps, recordings, live chat, form analytics | Alternative |

### 8.3. Analytics & Funnel Analysis

| Tool | Giá | Sử dụng |
|------|-----|---------|
| **Google Analytics 4 (GA4)** | 🆓 | Funnel Explorations, path analysis, cohort analysis, ecommerce tracking |
| **Google Search Console** | 🆓 | SEO performance, click-through rates từ search |
| **WooCommerce Analytics** | 🆓 (built-in) | Revenue, orders, products, categories, coupons reports |

### 8.4. Survey & Feedback Tools

| Tool | Giá | Sử dụng |
|------|-----|---------|
| **Hotjar Feedback** | Từ $32/tháng | Widget feedback "Trang này hữu ích không?" + surveys |
| **Google Forms** | 🆓 | Post-purchase survey, NPS survey |
| **Custom popup survey** | 0đ (plugin) | "Bạn tìm thấy sản phẩm mong muốn chưa?" — hiển thị trên category page |

### 8.5. Setup Priority

```
Tuần 0 (Ngay):
  1. ✅ Cài Microsoft Clarity → Bắt đầu thu data heatmap
  2. ✅ Setup GA4 Enhanced Ecommerce → Track đầy đủ funnel events
  3. ✅ Setup Google Tag Manager → Sẵn sàng cho A/B tests

Tuần 2:
  4. ✅ Cấu hình GA4 Explorations → Tạo funnel reports
  5. ✅ Review Clarity data → Phân tích heatmap đầu tiên

Tuần 4:
  6. ✅ Chạy A/B test đầu tiên qua GTM + Custom JS
  7. ✅ Setup post-purchase survey (Google Forms)
```

---

## 9. CONVERSION RATE TARGETS

### 9.1. Bảng Targets theo trang và giai đoạn

| Funnel Step | Metric | Tháng 1 (Baseline) | Tháng 3 (Target) | Tháng 6 (Stretch) | Cách đo |
|-------------|--------|-------------------|-------------------|-------------------|---------|
| **Homepage → Product** | HP → PDP rate | 20-25% | 30% | 35% | GA4: Product page views / Homepage sessions |
| **Product → Add to Cart** | ATC rate | 3-5% | 8-10% | 10-12% | GA4: add_to_cart / view_item |
| **Add to Cart → Checkout** | Cart → Checkout | 30-35% | 40-50% | 50-60% | GA4: begin_checkout / add_to_cart |
| **Checkout → Purchase** | Checkout completion | 40-50% | 60-65% | 65-70% | GA4: purchase / begin_checkout |
| **Overall CR** | Conversion rate | 0.5-1% | 1.5-2.5% | 2.5-3.5% | GA4: purchase / total sessions |
| **Mobile CR** | Mobile conversion | 0.3-0.8% | 1-2% | 2-3% | GA4: segment by device |
| **Desktop CR** | Desktop conversion | 1-2% | 2.5-3.5% | 3.5-5% | GA4: segment by device |

### 9.2. Revenue Impact Calculator

```
Baseline:
  Sessions/tháng: 10,000
  CR: 1.5%
  AOV: 3,000,000đ
  Revenue: 10,000 × 1.5% × 3,000,000 = 450,000,000đ/tháng

Sau 3 tháng CRO:
  Sessions/tháng: 10,000 (giữ nguyên)
  CR: 3% (+100%)
  AOV: 3,500,000đ (+17% nhờ upsell)
  Revenue: 10,000 × 3% × 3,500,000 = 1,050,000,000đ/tháng

  → TĂNG: +600,000,000đ/tháng (+133%)
  → CHI PHÍ CRO: ~5,000,000đ/tháng (tools + nhân lực)
  → ROI: 12,000% (120x)
```

### 9.3. KPIs phụ cần theo dõi

| KPI | Mục tiêu | Tần suất đo |
|-----|---------|-------------|
| Bounce Rate (homepage) | < 55% | Hàng tuần |
| Bounce Rate (product page) | < 45% | Hàng tuần |
| Avg. Session Duration | > 2 phút | Hàng tuần |
| Pages per Session | > 3 | Hàng tuần |
| Cart Abandonment Rate | < 70% | Hàng tuần |
| Mobile vs Desktop ratio | Track trend | Hàng tháng |
| New vs Returning visitors | Target 30%+ returning | Hàng tháng |
| Revenue per Session | > 50,000đ | Hàng tuần |

---

## 10. REPORTING TEMPLATE

### 10.1. Monthly CRO Report Structure

```
═══════════════════════════════════════════════════════
  BÁO CÁO CRO THÁNG [X] — XIAOMI247.COM
═══════════════════════════════════════════════════════

1. EXECUTIVE SUMMARY
   - CR tháng này: X% (vs tháng trước: Y%, vs mục tiêu: Z%)
   - Doanh thu ảnh hưởng: +/- X đồng
   - Số tests chạy: X tests
   - Tests thắng: X / Thua: Y / Không kết luận: Z

2. FUNNEL PERFORMANCE
   ┌──────────────────────────────────────────────┐
   │ Homepage Sessions:     X,XXX (±X% vs LM)    │
   │ → Product Page Views:  X,XXX (XX% of HP)     │
   │ → Add to Cart:         XXX   (X% of PDP)     │
   │ → Begin Checkout:      XXX   (XX% of ATC)    │
   │ → Purchase:            XX    (XX% of BC)      │
   │                                               │
   │ Overall CR: X.XX%  |  AOV: X,XXX,XXXđ       │
   │ Revenue: XXX,XXX,XXXđ                        │
   └──────────────────────────────────────────────┘

3. A/B TESTS RUN THIS MONTH
   ┌─────────────────────────────────────────────┐
   │ Test 1: [Tên test]                          │
   │ Status: Winner / Loser / Inconclusive       │
   │ Metric: X% → Y% (±Z%)                      │
   │ Confidence: XX%                              │
   │ Revenue Impact: +/- X,XXX,XXXđ/tháng       │
   │ Action: Implemented / Rolled back            │
   └─────────────────────────────────────────────┘
   (Lặp lại cho mỗi test)

4. HEATMAP & SESSION RECORDING INSIGHTS
   - Top 3 findings từ Clarity
   - Key friction points phát hiện
   - Hypotheses mới cho tháng sau

5. QUICK WINS IMPLEMENTED
   - Danh sách thay đổi đã triển khai
   - Impact ước tính

6. NEXT MONTH PLAN
   - Tests dự kiến: [Test A], [Test B], [Test C], [Test D]
   - Quick wins còn lại
   - Tools/setup cần thêm

7. KEY LEARNINGS
   - Bài học từ tests tháng này
   - Patterns phát hiện
   - Điều cần tránh
```

### 10.2. Test Result Log (Google Sheets)

Tạo Google Sheet với các cột sau:

| Cột | Nội dung |
|-----|---------|
| Test ID | T001, T002, ... |
| Tên test | VD: "CTA Button Color" |
| Trang | Product / Homepage / Checkout |
| Hypothesis | Full hypothesis statement |
| Control (A) | Mô tả variant A |
| Variant (B) | Mô tả variant B |
| Metric chính | VD: Add to Cart Rate |
| Baseline | VD: 3.5% |
| Target | VD: 4.2% (+20%) |
| Ngày bắt đầu | DD/MM/YYYY |
| Ngày kết thúc | DD/MM/YYYY |
| Sample Size A | Số visitors variant A |
| Sample Size B | Số visitors variant B |
| Result A | VD: 3.5% |
| Result B | VD: 4.1% |
| Confidence | VD: 96% |
| Kết luận | Winner B / No winner / Inconclusive |
| Revenue Impact | VD: +50,000,000đ/tháng |
| Action | Implemented / Rolled back |
| Learnings | Ghi chú bài học |

---

## 11. CHECKLIST TRIỂN KHAI CRO PROGRAM

### 11.1. Phase 0: Chuẩn bị (Tuần 0)

- [ ] Cài đặt Microsoft Clarity (heatmaps + recordings)
- [ ] Verify GA4 Enhanced Ecommerce tracking hoạt động đúng
- [ ] Cài đặt Google Tag Manager (nếu chưa có)
- [ ] Tạo GA4 Explorations: Funnel report (view_item → add_to_cart → begin_checkout → purchase)
- [ ] Chụp baseline screenshots tất cả trang quan trọng (desktop + mobile)
- [ ] Ghi nhận baseline metrics cho mỗi funnel step
- [ ] Tạo Google Sheet "CRO Test Log" theo template mục 10.2
- [ ] Đọc và hiểu toàn bộ tài liệu CRO này

### 11.2. Phase 1: Quick Wins (Tuần 1-3)

- [ ] Triển khai 18 quick wins theo thứ tự ưu tiên (mục 3.5)
- [ ] Tuần 1: Trust badges, CTA text, button color, Zalo widget, breadcrumb, anchor pricing
- [ ] Tuần 2: Reviews, sticky CTA, guest checkout, lazy load, số đã bán
- [ ] Tuần 3: Giảm bước checkout, free shipping bar, mua ngay, countdown, live viewers
- [ ] Đo metrics trước và sau quick wins → Ghi nhận impact

### 11.3. Phase 2: Heatmap Analysis (Tuần 2-4)

- [ ] Thu thập đủ 1,000+ sessions trong Clarity
- [ ] Phân tích click maps cho: Product page, Homepage, Checkout
- [ ] Phân tích scroll maps: xác định fold line và drop-off points
- [ ] Xem 20-30 session recordings (filter: rage clicks, cart abandoners)
- [ ] Ghi chép findings: friction points, confusion areas, dead zones
- [ ] Hình thành 5-10 hypotheses từ heatmap data

### 11.4. Phase 3: A/B Testing (Tuần 4-15)

- [ ] Tuần 4: Setup A/B testing framework (GTM + Custom JS hoặc VWO)
- [ ] Tuần 4-7: Chạy 4 tests Product Page theo roadmap
- [ ] Tuần 8-11: Chạy 4 tests Homepage theo roadmap
- [ ] Tuần 12-15: Chạy 4 tests Checkout theo roadmap
- [ ] Mỗi test: document hypothesis, variants, results, learnings
- [ ] Implement winning variants ngay sau khi test kết thúc

### 11.5. Phase 4: Reporting & Iteration (Liên tục)

- [ ] Tạo Monthly CRO Report theo template mục 10.1
- [ ] Review heatmap data hàng tháng (new insights)
- [ ] Cập nhật test backlog dựa trên findings mới
- [ ] Quarterly review: so sánh metrics vs targets
- [ ] Chia sẻ learnings với team
- [ ] Lập roadmap testing cho quarter tiếp theo

### 11.6. Ownership & Responsibility

| Vai trò | Trách nhiệm | Thời gian/tuần |
|---------|-------------|---------------|
| **CRO Lead** | Lên kế hoạch tests, phân tích data, ra quyết định | 3-4 giờ |
| **Developer** | Implement variants, tracking code, quick wins | 2-3 giờ |
| **Designer** | Thiết kế variants cho A/B tests | 1-2 giờ |
| **Content** | Viết CTA text, trust badges copy, email templates | 1 giờ |

> 💡 **Ghi nhớ:** CRO là marathon, không phải sprint. Kiên trì test, học từ data, và cải thiện liên tục. Mỗi test thất bại cũng là 1 bài học quý giá.

---

*Kế hoạch A/B Testing & Tối ưu Conversion Rate — Xiaomi247.com*
*Ngày tạo: 09/04/2026 | Phiên bản: 1.0*
*Tham chiếu: [Conversion Optimization](../marketing/04-trust-building/conversion-optimization.md) | [Mobile UX](../website-dev/06-mobile-ux.md) | [Sales Funnel](./01-sales-funnel-strategy.md)*
```