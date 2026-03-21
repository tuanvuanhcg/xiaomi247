# HƯỚNG DẪN SETUP & TRIỂN KHAI FACEBOOK ADS + GOOGLE ADS — XIAOMI247.COM

> **Tổng budget quảng cáo:** 24.5M VNĐ/tháng (14M Facebook + 10.5M Google)
> **Mục tiêu:** ROAS ≥ 3x, CPA ≤ 150K VNĐ
> **Website:** xiaomi247.com
> **Cập nhật:** Tháng 3/2026

---

## MỤC LỤC

**PHẦN 1 — FACEBOOK/INSTAGRAM ADS (14M VNĐ/tháng)**
1. [Business Manager Setup](#1-business-manager-setup)
2. [Facebook Pixel](#2-facebook-pixel--capi)
3. [Custom Audiences](#3-custom-audiences)
4. [Lookalike Audiences](#4-lookalike-audiences)
5. [Campaign Setup theo Funnel](#5-campaign-setup-theo-funnel)
6. [Ad Creative Specs](#6-ad-creative-specs)
7. [A/B Testing Plan](#7-ab-testing-plan)

**PHẦN 2 — GOOGLE ADS (10.5M VNĐ/tháng)**
8. [Google Ads Account Setup](#8-google-ads-account-setup)
9. [Search Campaigns](#9-search-campaigns---6-campaigns)
10. [Google Shopping](#10-google-shopping)
11. [Display / Remarketing](#11-display--remarketing)
12. [Negative Keywords](#12-negative-keywords)
13. [Budget Breakdown](#13-budget-breakdown-tổng-hợp)

---

# PHẦN 1 — FACEBOOK/INSTAGRAM ADS

> **Budget:** 14M VNĐ/tháng (40% tổng digital marketing)
> **Objective:** Traffic + Conversion, ROAS ≥ 3x

---

## 1. BUSINESS MANAGER SETUP

### 1.1. Tạo Business Manager

| Bước | Thao tác | Ghi chú |
|------|---------|---------|
| 1 | Truy cập [business.facebook.com](https://business.facebook.com) | Dùng tài khoản Facebook cá nhân của admin |
| 2 | Click **"Tạo tài khoản"** | Đặt tên: **Xiaomi247 Vietnam** |
| 3 | Nhập email business: `ads@xiaomi247.com` | Email nhận thông báo billing, policy |
| 4 | Xác nhận email | Check inbox + spam folder |

### 1.2. Tạo Ad Account

| Bước | Thao tác | Cài đặt |
|------|---------|---------|
| 1 | BM → Business Settings → Ad Accounts → **Add** | Chọn "Create a new ad account" |
| 2 | Đặt tên: **Xiaomi247 - Main** | |
| 3 | Timezone: **(GMT+7) Ho Chi Minh** | ⚠️ Không đổi được sau khi tạo |
| 4 | Currency: **VND** | ⚠️ Không đổi được sau khi tạo |
| 5 | Payment method: Thẻ Visa/Mastercard hoặc chuyển khoản | Nạp tối thiểu 1M VNĐ để bắt đầu |

### 1.3. Facebook Page Setup

| Mục | Cài đặt |
|-----|---------|
| **Tên Page** | Xiaomi247 - Xiaomi Chính Hãng |
| **Category** | Electronics Store / Home Goods Store |
| **Username** | @xiaomi247 |
| **Profile Picture** | Logo Xiaomi247 (180x180px) |
| **Cover Photo** | Banner thương hiệu (820x312px) |
| **CTA Button** | "Shop Now" → xiaomi247.com |
| **About** | Đại lý ủy quyền Xiaomi chính hãng. Tivi, Robot hút bụi, Gia dụng thông minh. Freeship toàn quốc. |
| **Website** | https://xiaomi247.com |
| **Whatsapp/Phone** | Số hotline chính |

### 1.4. Instagram Business Account

1. Tạo Instagram account: **@xiaomi247.vn**
2. Chuyển sang **Professional Account** → Business
3. Liên kết với Facebook Page **Xiaomi247**
4. BM → Business Settings → Instagram Accounts → **Add** → Connect

### 1.5. Verify Domain

1. BM → Brand Safety → **Domains** → Add domain: `xiaomi247.com`
2. Chọn phương thức verify — **Meta-tag verification** (khuyên dùng):
   ```html
   <meta name="facebook-domain-verification" content="[MÃ XÁC MINH]" />
   ```
3. Thêm meta tag vào `<head>` website qua **GTM** hoặc plugin **Insert Headers & Footers**
4. Quay lại BM → Click **Verify**
5. ✅ Domain verified → Cho phép dùng Aggregated Event Measurement

### 1.6. Phân quyền trong BM

| Vai trò | Quyền | Ai |
|---------|-------|-----|
| **Admin** | Full access BM, Ad Account, Page | Chủ doanh nghiệp |
| **Advertiser** | Tạo/chỉnh sửa ads, xem reports | Marketing Manager |
| **Analyst** | Chỉ xem reports | Team member |

---

## 2. FACEBOOK PIXEL + CAPI

### 2.1. Tạo Facebook Pixel

1. BM → Events Manager → **Connect Data Sources** → Web → Facebook Pixel
2. Đặt tên Pixel: **Xiaomi247 Pixel**
3. Lưu lại **Pixel ID** (dạng `123456789012345`)

### 2.2. Cài Pixel qua Google Tag Manager (GTM)

> 📎 Tham chiếu chi tiết: [Tracking & Analytics](../website-dev/07-tracking-analytics.md)

**Bước 1 — Tạo Tag Facebook Pixel Base Code:**

| Cài đặt GTM | Giá trị |
|-------------|---------|
| Tag Type | Custom HTML |
| Tag Name | FB Pixel - Base Code |
| Trigger | All Pages |

```html
<!-- Facebook Pixel Code -->
<script>
!function(f,b,e,v,n,t,s)
{if(f.fbq)return;n=f.fbq=function(){n.callMethod?
n.callMethod.apply(n,arguments):n.queue.push(arguments)};
if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
n.queue=[];t=b.createElement(e);t.async=!0;
t.src=v;s=b.getElementsByTagName(e)[0];
s.parentNode.insertBefore(t,s)}(window, document,'script',
'https://connect.facebook.net/en_US/fbevents.js');
fbq('init', '[PIXEL_ID]');
fbq('track', 'PageView');
</script>
<noscript><img height="1" width="1" style="display:none"
src="https://www.facebook.com/tr?id=[PIXEL_ID]&ev=PageView&noscript=1"/></noscript>
<!-- End Facebook Pixel Code -->
```

**Bước 2 — Tạo Tags cho E-commerce Events:**

| Event | GTM Trigger | Pixel Event | Parameters |
|-------|------------|-------------|------------|
| Xem sản phẩm | Custom Event: `view_item` | `ViewContent` | `content_ids`, `content_type: product`, `value`, `currency: VND` |
| Thêm giỏ hàng | Custom Event: `add_to_cart` | `AddToCart` | `content_ids`, `content_type: product`, `value`, `currency: VND` |
| Bắt đầu thanh toán | Custom Event: `begin_checkout` | `InitiateCheckout` | `value`, `currency: VND`, `num_items` |
| Mua hàng | Custom Event: `purchase` | `Purchase` | `content_ids`, `value`, `currency: VND`, `order_id` |
| Tìm kiếm | Custom Event: `search` | `Search` | `search_string` |

### 2.3. Test Events với Facebook Pixel Helper

1. Cài Chrome extension: **Facebook Pixel Helper**
2. Truy cập xiaomi247.com → Kiểm tra Pixel Helper hiện ✅ xanh
3. Test từng event:

| Hành động trên website | Event cần hiện | Status |
|----------------------|---------------|--------|
| Truy cập trang chủ | `PageView` | ☐ |
| Click vào 1 sản phẩm | `ViewContent` | ☐ |
| Click "Thêm vào giỏ hàng" | `AddToCart` | ☐ |
| Vào trang thanh toán | `InitiateCheckout` | ☐ |
| Hoàn tất thanh toán (test order) | `Purchase` | ☐ |

4. Events Manager → **Test Events** → Nhập URL xiaomi247.com → Test trực tiếp
5. Kiểm tra **Diagnostics** tab — xử lý tất cả warnings

### 2.4. Conversions API (CAPI) — Nâng cao

> CAPI giúp tracking chính xác hơn khi iOS 14+ block cookies

1. Events Manager → Settings → **Conversions API** → Set up manually
2. Dùng plugin **PixelYourSite Pro** (khuyên dùng cho WooCommerce):
   - Settings → Facebook → Nhập Pixel ID + Access Token
   - Bật **Server-side events** cho: Purchase, AddToCart, ViewContent
3. Hoặc setup qua **GTM Server-Side Container** (nâng cao hơn)

---

## 3. CUSTOM AUDIENCES

### 3.1. Tạo 4 Custom Audiences cần thiết

> BM → Audiences → **Create Audience** → Custom Audience

| # | Tên Audience | Source | Điều kiện | Window | Mục đích |
|---|-------------|--------|----------|--------|----------|
| 1 | **Website Visitors 7D** | Website (Pixel) | All website visitors | 7 ngày | Retargeting nóng |
| 2 | **Website Visitors 30D** | Website (Pixel) | All website visitors | 30 ngày | Retargeting rộng |
| 3 | **Cart Abandoners** | Website (Pixel) | Event = AddToCart BUT NOT Purchase | 14 ngày | Cart recovery |
| 4 | **Purchasers** | Website (Pixel) | Event = Purchase | 180 ngày | Exclusion + Cross-sell |

### 3.2. Audiences bổ sung (tạo khi có data)

| Tên | Source | Điều kiện | Window |
|-----|--------|----------|--------|
| **Email Subscribers** | Customer List | Upload CSV email list | — |
| **FB/IG Engagers** | Facebook Page | People who engaged with Page | 90 ngày |
| **Video Viewers 50%+** | Video | People who watched 50%+ | 30 ngày |
| **Product Viewers** | Website (Pixel) | Event = ViewContent | 14 ngày |

### 3.3. Hướng dẫn Upload Email List

1. Chuẩn bị file CSV: cột `email`, `phone` (optional), `fn` (first name), `ln` (last name)
2. Audiences → Create → Custom Audience → **Customer list**
3. Upload CSV → Map fields → Create Audience
4. Chờ match (thường 24-48h), match rate kỳ vọng: 40-60%

---

## 4. LOOKALIKE AUDIENCES

### 4.1. Tạo Lookalike Audiences

> Audiences → Create Audience → **Lookalike Audience**

| # | Source Audience | LAL Size | Mục đích | Ưu tiên |
|---|---------------|----------|----------|---------|
| 1 | **Purchasers** | 1% | Conversion campaign — chất lượng cao nhất | ⭐⭐⭐ |
| 2 | **Add to Cart** | 1% | Traffic campaign — high intent | ⭐⭐⭐ |
| 3 | **Website Visitors 30D** | 2% | Awareness campaign — reach rộng | ⭐⭐ |
| 4 | **Email Subscribers** | 1% | Traffic campaign — data 1st party | ⭐⭐ |

### 4.2. Lưu ý khi tạo LAL

- **Country:** Việt Nam
- **Source cần tối thiểu 100 người** (khuyến nghị 1,000+)
- LAL 1% ≈ 700K người tại VN → đủ lớn cho hầu hết campaigns
- LAL sẽ **tự động cập nhật** khi source audience thay đổi
- **Tuần 1-2:** Chưa có data → dùng Interest targeting trước
- **Tuần 3+:** Khi Pixel có data → tạo LAL và chuyển dần sang LAL

---

## 5. CAMPAIGN SETUP THEO FUNNEL

### 5.1. Tổng quan 4 Campaigns

```
┌─────────────────────────────────────────────────────────────────────┐
│                    FACEBOOK ADS FUNNEL — 14M VNĐ                    │
├──────────────┬──────────┬───────────┬───────────────────────────────┤
│  AWARENESS   │ TRAFFIC  │CONVERSION │         RETENTION             │
│   10% (1.4M) │30% (4.2M)│45% (6.3M) │         15% (2.1M)           │
├──────────────┼──────────┼───────────┼───────────────────────────────┤
│ Video Views  │Link Clicks│ Purchase  │ Conversions (Cross-sell)      │
│              │          │           │                               │
│ Interest:    │Interest: │Retarget:  │ Custom:                       │
│ • Tech 22-35 │• Xiaomi  │• Viewers  │ • Past Customers 30-90D      │
│ • SmartHome  │  Users   │  7D       │ • Email Subscribers           │
│   28-45      │• Home    │• Cart     │                               │
│ • Urban      │  Applian.│  Abandon  │ Creative:                     │
│   22-45      │          │  14D      │ • SP mới, accessories         │
│              │LAL:      │           │ • Mã giảm giá riêng           │
│              │• 1% ATC  │LAL:       │                               │
│              │• 1% Email│• 1% Purch.│                               │
└──────────────┴──────────┴───────────┴───────────────────────────────┘
```

### 5.2. Campaign 1: AWARENESS — 1.4M VNĐ/tháng (10%)

| Cài đặt | Giá trị |
|---------|---------|
| **Campaign Objective** | Awareness → Video Views |
| **Budget** | 47K VNĐ/ngày |
| **Schedule** | Liên tục, review mỗi 7 ngày |
| **Optimization** | ThruPlay (xem ≥ 15s) |

**Ad Sets:**

| Ad Set | Targeting | Age | Gender | Placement |
|--------|----------|-----|--------|-----------|
| Interest - Tech Enthusiasts | Xiaomi, Smartphone, Technology, Gadgets | 22-35 | 60% Nam | FB + IG Feed, Reels |
| Interest - Smart Home | Smart Home, IoT, Home Automation, Interior Design | 28-45 | Cả 2 | FB + IG Feed, Reels |
| Broad - Urban | Vị trí: HN, HCM, ĐN + Online shopping | 22-45 | Cả 2 | Automatic |

**Ad Creative:**
- Format: **Video 15-30s** (1080x1080 Feed + 1080x1920 Reels)
- Nội dung: Unboxing sản phẩm, giới thiệu Xiaomi247, lifestyle
- 3 giây đầu: Hook mạnh (sản phẩm + giá sốc)
- Text overlay cho người xem tắt tiếng
- CTA cuối: "Khám phá tại Xiaomi247.com"

### 5.3. Campaign 2: TRAFFIC — 4.2M VNĐ/tháng (30%)

| Cài đặt | Giá trị |
|---------|---------|
| **Campaign Objective** | Traffic → Link Clicks |
| **Budget** | 140K VNĐ/ngày |
| **Optimization** | Landing Page Views |
| **Destination** | xiaomi247.com (category pages) |

**Ad Sets:**

| Ad Set | Targeting | Budget/ngày | Landing Page |
|--------|----------|-------------|-------------|
| Interest - Xiaomi Users | Interest: Xiaomi, Mi fans | 40K | /tivi-xiaomi/, /robot-hut-bui/ |
| Interest - Home Appliances | Interest: Home appliances, kitchen | 30K | /gia-dung-xiaomi/ |
| LAL 1% - Website Visitors | Lookalike 1% từ WV 30D | 35K | Trang chủ |
| LAL 1% - Add to Cart | Lookalike 1% từ ATC | 35K | Best sellers |

**Ad Creative:**
- Format: **Carousel (3-5 cards)** — 1080x1080/card
- Card 1: Hero product (best seller)
- Card 2-4: Features/benefits/giá
- Card cuối: CTA "Xem tất cả →"
- Headline: Giá + "Chính hãng Xiaomi"

### 5.4. Campaign 3: CONVERSION — 6.3M VNĐ/tháng (45%)

| Cài đặt | Giá trị |
|---------|---------|
| **Campaign Objective** | Sales → Purchase |
| **Budget** | 210K VNĐ/ngày |
| **Optimization** | Purchase (hoặc Add to Cart nếu chưa đủ data) |
| **Attribution** | 7-day click, 1-day view |

> ⚠️ **Learning Phase:** Cần tối thiểu 50 conversions/tuần. Nếu chưa đủ → optimize cho Add to Cart trước, chuyển sang Purchase khi có data.

**Ad Sets:**

| Ad Set | Targeting | Budget/ngày | Strategy |
|--------|----------|-------------|---------|
| Retarget - Product Viewers 7D | Custom: ViewContent 7D | 70K | Dynamic Product Ads |
| Retarget - Cart Abandoners 14D | Custom: ATC NOT Purchase 14D | 70K | DPA + Mã giảm giá 5% |
| LAL 1% - Purchasers | Lookalike 1% Purchasers | 50K | Collection Ads |
| Interest - High Intent | Interest: Online shopping + Engaged shoppers | 20K | Collection Ads |

**Ad Creative:**
- **Retargeting:** Dynamic Product Ads (DPA) — tự động hiển thị SP đã xem
- **Cart Recovery:** DPA + badge "Giảm thêm 5% — Mã: QUAYLAI5"
- **LAL/Interest:** Collection Ad (cover image/video + product catalog)

### 5.5. Campaign 4: RETENTION — 2.1M VNĐ/tháng (15%)

| Cài đặt | Giá trị |
|---------|---------|
| **Campaign Objective** | Sales → Conversions |
| **Budget** | 70K VNĐ/ngày |
| **Optimization** | Purchase |
| **Frequency Cap** | Tối đa 3 lần/tuần |

**Ad Sets:**

| Ad Set | Targeting | Budget/ngày | Message |
|--------|----------|-------------|---------|
| Past Customers 30-90D | Custom: Purchase 30-90D | 45K | SP mới + Phụ kiện liên quan |
| Email Subscribers | Custom: Email list | 25K | Ưu đãi VIP + Sản phẩm mới |

**Ad Creative:**
- Format: **Single Image + Offer** — 1080x1080
- Nội dung: Cross-sell (mua tivi → soundbar), new arrivals, loyalty offers
- CTA rõ ràng: "Mua ngay" + giá đặc biệt

---

## 6. AD CREATIVE SPECS

### 6.1. Kích thước hình ảnh/video

| Format | Kích thước | Tỷ lệ | Sử dụng cho |
|--------|-----------|--------|-------------|
| **Feed Square** | 1080 × 1080 px | 1:1 | FB/IG Feed — Mọi campaign |
| **Stories/Reels** | 1080 × 1920 px | 9:16 | IG Stories, FB Stories, Reels |
| **Landscape** | 1200 × 628 px | 1.91:1 | FB Feed, Right Column, Audience Network |
| **Carousel Card** | 1080 × 1080 px | 1:1 | Carousel Ads (3-10 cards) |
| **Collection Cover** | 1200 × 628 px | 1.91:1 | Collection Ads cover |
| **Video Feed** | 1080 × 1080 px | 1:1 | Video Ads — Feed |
| **Video Reels** | 1080 × 1920 px | 9:16 | Video Ads — Reels/Stories |

### 6.2. Video Specs

| Yếu tố | Yêu cầu |
|---------|---------|
| **Độ dài** | 15-30 giây (tối đa 60s) |
| **File size** | Tối đa 4GB |
| **Format** | MP4, MOV |
| **Resolution** | Tối thiểu 1080p |
| **Captions** | Bắt buộc — 85% người xem tắt tiếng |
| **3 giây đầu** | PHẢI có hook: sản phẩm + giá/ưu đãi |
| **CTA** | Cuối video: logo + "Mua ngay tại Xiaomi247.com" |

### 6.3. Copy Guidelines

| Yếu tố | Quy tắc | Ví dụ |
|---------|---------|-------|
| **Primary Text** | 125 ký tự (tối ưu), max 3 dòng trước "Xem thêm" | 🔥 Tivi Xiaomi 55 inch 4K — Chỉ 7.990K! Freeship + Trả góp 0% |
| **Headline** | 40 ký tự, có giá hoặc offer | Tivi Xiaomi A Pro 55" — 7.990K |
| **Description** | 30 ký tự | Chính hãng • Freeship • Trả góp 0% |
| **CTA Button** | Chọn phù hợp | "Shop Now" (Conversion), "Learn More" (Traffic) |
| **Emoji** | 2-3 emoji/post, đầu dòng | ✅ 🔥 🎁 🚚 ⏰ 💰 |
| **Hashtags** | 3-5 hashtags cuối post | #Xiaomi247 #XiaomiChinhHang #TiviXiaomi |

### 6.4. Creative Do's & Don'ts

| ✅ DO | ❌ DON'T |
|-------|---------|
| Nền trắng/sáng cho ảnh sản phẩm | Text chiếm >20% diện tích ảnh |
| Badge "Chính hãng" trên mọi ad | Ảnh mờ, chất lượng thấp |
| Giá rõ ràng trên ảnh/video | Claim quá mức ("Rẻ nhất VN") |
| Logo Xiaomi247 góc dưới | Copy dài >3 đoạn |
| CTA nổi bật, màu cam #FF6900 | Quá nhiều sản phẩm trong 1 ảnh |

---

## 7. A/B TESTING PLAN

### 7.1. Framework Test 4 Tuần Đầu

```
TUẦN 1 ──────────────────────────────────────────────────
│ Test: AD FORMAT
│ Variant A: Carousel (3 sản phẩm)
│ Variant B: Video 15s (unboxing)
│ Metric: CTR + CPC
│ Budget: 100K/variant/ngày × 7 ngày = 1.4M
│
TUẦN 2 ──────────────────────────────────────────────────
│ Test: AD COPY
│ Variant A: Giá + "Chính hãng" (price-led)
│ Variant B: Feature + benefit (feature-led)
│ Metric: CTR + Conversion Rate
│ Budget: 100K/variant/ngày × 7 ngày = 1.4M
│
TUẦN 3 ──────────────────────────────────────────────────
│ Test: AUDIENCE
│ Variant A: Interest-based (Tech + Home)
│ Variant B: Lookalike 1% (Website Visitors)
│ Metric: CPA + ROAS
│ Budget: 150K/variant/ngày × 7 ngày = 2.1M
│
TUẦN 4 ──────────────────────────────────────────────────
│ Test: PLACEMENT
│ Variant A: FB + IG Feed only
│ Variant B: Automatic Placements (incl. Reels, Stories)
│ Metric: CPA + Reach
│ Budget: 150K/variant/ngày × 7 ngày = 2.1M
```

### 7.2. Bảng theo dõi A/B Test

| Tuần | Yếu tố test | Variant A | Variant B | Metric chính | Budget | Kết quả |
|------|------------|----------|----------|-------------|--------|---------|
| 1 | Ad Format | Carousel | Video 15s | CTR, CPC | 1.4M | ☐ Pending |
| 2 | Ad Copy | Price-led | Feature-led | CTR, CVR | 1.4M | ☐ Pending |
| 3 | Audience | Interest | LAL 1% | CPA, ROAS | 2.1M | ☐ Pending |
| 4 | Placement | Feed only | Automatic | CPA, Reach | 2.1M | ☐ Pending |

### 7.3. Quy tắc A/B Test

| Quy tắc | Chi tiết |
|---------|---------|
| **Budget tối thiểu** | 50K VNĐ/variant/ngày |
| **Thời gian chạy** | Tối thiểu 5 ngày hoặc 1,000 impressions/variant |
| **Winning criteria** | Statistically significant (95% confidence) |
| **Sau khi có kết quả** | Tắt loser → Scale winner → Tạo iteration mới |
| **Chỉ test 1 yếu tố** | Không đổi 2+ yếu tố cùng lúc |

---

# PHẦN 2 — GOOGLE ADS

> **Budget:** 10.5M VNĐ/tháng (30% tổng digital marketing)
> **Objective:** Bắt purchase intent, CPA ≤ 150K, ROAS ≥ 4x

---

## 8. GOOGLE ADS ACCOUNT SETUP

### 8.1. Tạo Google Ads Account

| Bước | Thao tác | Ghi chú |
|------|---------|---------|
| 1 | Truy cập [ads.google.com](https://ads.google.com) | Dùng Google Account business |
| 2 | Click **"Start Now"** | Chọn "Switch to Expert Mode" ngay lập tức |
| 3 | Skip campaign creation | "Create an account without a campaign" |
| 4 | Billing country: **Việt Nam** | |
| 5 | Currency: **VND** | ⚠️ Không đổi được |
| 6 | Timezone: **(GMT+7) Ho Chi Minh** | ⚠️ Không đổi được |
| 7 | Payment: Thẻ Visa/Mastercard | Nạp tối thiểu 1M VNĐ |

### 8.2. Liên kết Google Analytics 4 (GA4)

1. Google Ads → Tools & Settings → **Linked accounts** → Google Analytics (GA4)
2. Tìm property **xiaomi247.com** → Click **Link**
3. Bật **Import site metrics** (sessions, bounce rate)
4. Bật **Import conversions** (purchase, add_to_cart)

### 8.3. Liên kết Google Search Console (GSC)

1. Tools & Settings → Linked accounts → **Search Console**
2. Chọn property `xiaomi247.com`
3. Verify ownership (nếu chưa) → Link

### 8.4. Setup Conversion Tracking

1. Tools & Settings → **Conversions** → New conversion action
2. Tạo các conversion actions:

| Conversion Action | Category | Value | Count | Attribution |
|------------------|----------|-------|-------|------------|
| **Purchase** | Purchase | Dynamic (từ GA4) | Every | Data-driven |
| **Add to Cart** | Add to cart | Dynamic | Every | Data-driven |
| **Begin Checkout** | Begin checkout | Dynamic | Every | Data-driven |
| **Lead (Form)** | Submit lead form | 50,000đ (fixed) | One | Data-driven |

3. Import từ GA4: Conversions → Import → Google Analytics 4 → Chọn events

### 8.5. Liên kết Google Merchant Center

1. Truy cập [merchants.google.com](https://merchants.google.com)
2. Tạo account: **Xiaomi247 Vietnam**
3. Verify & claim domain `xiaomi247.com`
4. Google Ads → Tools & Settings → Linked accounts → **Merchant Center** → Link

---

## 9. SEARCH CAMPAIGNS — 6 CAMPAIGNS

### 9.1. Tổng quan Campaign Structure

```
┌─────────────────────────────────────────────────────────────────────┐
│                  GOOGLE SEARCH ADS — 10.5M VNĐ                     │
├──────────────────┬──────────┬───────────────────────────────────────┤
│   Campaign       │Budget/ngày│ Bid Strategy                        │
├──────────────────┼──────────┼───────────────────────────────────────┤
│ 1. Branded       │   50K    │ Manual CPC                           │
│ 2. Tivi ⭐       │   80K    │ Target CPA → 120K                    │
│ 3. Robot hút bụi │   60K    │ Target CPA → 150K                    │
│ 4. Gia dụng      │   50K    │ Target CPA → 150K                    │
│ 5. Tủ lạnh ⭐    │   40K    │ Maximize Clicks → Target CPA         │
│ 6. Máy lọc KK    │   30K    │ Maximize Clicks → Target CPA         │
│   + Hút ẩm       │          │                                      │
├──────────────────┼──────────┼───────────────────────────────────────┤
│ TỔNG             │  310K    │ ≈ 9.3M/tháng (Search)                │
└──────────────────┴──────────┴───────────────────────────────────────┘
+ Google Shopping: 50K/ngày (1.5M/tháng)
+ Display Remarketing: 33K/ngày (1M/tháng)
```

### 9.2. Campaign 1: Branded Search — 50K/ngày

| Cài đặt | Giá trị |
|---------|---------|
| **Objective** | Brand protection |
| **Bid Strategy** | Manual CPC |
| **Network** | Search only |
| **Location** | Việt Nam |
| **Language** | Tiếng Việt |

**Keywords:**

| Keyword | Match Type | Max CPC |
|---------|-----------|---------|
| xiaomi247 | Exact | 2,000đ |
| xiaomi247.com | Exact | 2,000đ |
| xiaomi 247 | Phrase | 1,500đ |
| xiaomi247 chính hãng | Phrase | 2,000đ |

**Ad Copy mẫu:**
```
Headline 1: Xiaomi247.com — Đại Lý Xiaomi Chính Hãng
Headline 2: Freeship Toàn Quốc | Trả Góp 0%
Headline 3: Bảo Hành Chính Hãng 12-24 Tháng
Description 1: Tivi, Robot hút bụi, Gia dụng Xiaomi giá tốt nhất. Cam kết chính hãng 100%. Đổi trả 7 ngày.
Description 2: Hotline: [SĐT]. Giao hàng nhanh 2-4h tại HN/HCM. Thanh toán COD, chuyển khoản, trả góp.
```

### 9.3. Campaign 2: Tivi Xiaomi — 80K/ngày ⭐ TOP PRIORITY

| Keyword | Match Type | Max CPC | Landing Page |
|---------|-----------|---------|-------------|
| mua tivi xiaomi | Exact | 5,000đ | /tivi-xiaomi/ |
| tivi xiaomi 55 inch | Exact | 4,500đ | /tivi-xiaomi/55-inch/ |
| tivi xiaomi 43 inch giá rẻ | Phrase | 4,000đ | /tivi-xiaomi/43-inch/ |
| tivi xiaomi a pro 55 | Exact | 4,500đ | /tivi-xiaomi/a-pro-55/ |
| tivi xiaomi chính hãng giá tốt | Phrase | 4,000đ | /tivi-xiaomi/ |
| mua tivi xiaomi ở đâu uy tín | Phrase | 3,500đ | /gioi-thieu/ |
| tivi xiaomi 65 inch | Exact | 4,000đ | /tivi-xiaomi/65-inch/ |

**Ad Extensions:**
- **Sitelinks:** Tivi 43 inch, Tivi 55 inch, Tivi 65 inch, So sánh tivi
- **Callout:** Chính hãng 100%, Freeship, Trả góp 0%, Bảo hành 24 tháng
- **Price:** Hiển thị giá từng model
- **Structured Snippet:** Thương hiệu: Xiaomi | Kích thước: 43", 55", 65"

### 9.4. Campaign 3: Robot Hút Bụi — 60K/ngày

| Keyword | Match Type | Max CPC | Landing Page |
|---------|-----------|---------|-------------|
| robot hút bụi lau nhà xiaomi | Exact | 5,000đ | /robot-hut-bui-xiaomi/ |
| robot hút bụi xiaomi giá rẻ | Phrase | 4,000đ | /robot-hut-bui-xiaomi/?sort=price |
| robot hút bụi xiaomi x10+ | Exact | 4,500đ | /robot-hut-bui-xiaomi/x10-plus/ |
| robot hút bụi xiaomi chính hãng | Phrase | 4,500đ | /robot-hut-bui-xiaomi/ |
| mua robot hút bụi xiaomi | Exact | 4,500đ | /robot-hut-bui-xiaomi/ |

### 9.5. Campaign 4: Gia Dụng — 50K/ngày

| Keyword | Match Type | Max CPC | Landing Page |
|---------|-----------|---------|-------------|
| gia dụng xiaomi chính hãng | Phrase | 3,000đ | /gia-dung-xiaomi/ |
| đồ gia dụng xiaomi | Phrase | 3,000đ | /gia-dung-xiaomi/ |
| xiaomi smart home | Exact | 3,500đ | /gia-dung-xiaomi/ |
| máy hút bụi cầm tay xiaomi | Exact | 3,500đ | /gia-dung-xiaomi/may-hut-bui/ |

### 9.6. Campaign 5: Tủ Lạnh — 40K/ngày ⭐ LOW COMPETITION

| Keyword | Match Type | Max CPC | Landing Page |
|---------|-----------|---------|-------------|
| mua tủ lạnh xiaomi | Exact | 3,500đ | /tu-lanh-xiaomi/ |
| tủ lạnh xiaomi 4 cánh | Exact | 3,000đ | /tu-lanh-xiaomi/4-canh/ |
| tủ lạnh xiaomi chính hãng | Phrase | 3,000đ | /tu-lanh-xiaomi/ |
| tủ lạnh xiaomi side by side | Exact | 3,000đ | /tu-lanh-xiaomi/side-by-side/ |

> ⭐ **Quick Win:** Competition thấp → CPC rẻ → bắt đầu với Maximize Clicks, chuyển sang Target CPA khi có 15+ conversions.

### 9.7. Campaign 6: Máy Lọc Không Khí + Hút Ẩm — 30K/ngày

| Keyword | Match Type | Max CPC | Landing Page |
|---------|-----------|---------|-------------|
| mua máy lọc không khí xiaomi | Exact | 4,000đ | /may-loc-khong-khi-xiaomi/ |
| máy lọc không khí xiaomi 4 pro | Exact | 3,500đ | /may-loc-khong-khi-xiaomi/4-pro/ |
| mua máy hút ẩm xiaomi | Exact | 3,000đ | /may-hut-am-xiaomi/ |
| máy hút ẩm xiaomi chính hãng | Phrase | 3,000đ | /may-hut-am-xiaomi/ |

---

## 10. GOOGLE SHOPPING

### 10.1. Merchant Center Setup

| Bước | Thao tác | Chi tiết |
|------|---------|---------|
| 1 | Tạo Merchant Center account | [merchants.google.com](https://merchants.google.com) |
| 2 | Verify & claim domain | Dùng HTML tag hoặc GA4 verification |
| 3 | Cấu hình shipping | Free ship đơn >500K, phí ship theo vùng |
| 4 | Cấu hình return policy | Đổi trả 7 ngày |
| 5 | Link Google Ads account | Settings → Linked accounts |

### 10.2. Product Feed từ WooCommerce

**Plugin khuyên dùng:** [Product Feed PRO for WooCommerce](https://wordpress.org/plugins/woo-product-feed-pro/) (miễn phí)

1. WordPress → Plugins → Cài **Product Feed PRO**
2. Tạo feed mới → Channel: **Google Shopping**
3. Map fields:

| Google Field | WooCommerce Field | Ví dụ |
|-------------|-------------------|-------|
| `id` | Product ID | `SKU-TV55APRO` |
| `title` | Product Title (tối ưu) | Xiaomi Tivi A Pro 55 inch 4K Google TV |
| `description` | Short Description | Tivi Xiaomi 55 inch, 4K UHD, Google TV... |
| `link` | Product URL | https://xiaomi247.com/tivi-xiaomi/a-pro-55/ |
| `image_link` | Main Image URL | Ảnh nền trắng, min 800x800px |
| `price` | Regular Price | `7990000 VND` |
| `sale_price` | Sale Price | `6990000 VND` |
| `availability` | Stock Status | `in_stock` / `out_of_stock` |
| `brand` | Xiaomi (fixed) | Xiaomi |
| `condition` | new (fixed) | new |
| `google_product_category` | Category mapping | Electronics > Television |

4. **Title format chuẩn:** `[Brand] + [Product Name] + [Key Feature] + [Size/Model]`
   - VD: "Xiaomi Tivi A Pro 55 inch 4K Google TV"
5. Cấu hình auto-update: Mỗi 6 giờ (cập nhật giá, tồn kho)
6. Submit feed URL lên Merchant Center

### 10.3. Shopping Campaign Structure

| Campaign | Products | Bid Strategy | Priority | Budget |
|----------|---------|-------------|----------|--------|
| **High Priority — Best Sellers** | Top 10 SP bán chạy | Manual CPC (bid cao hơn) | High | 25K/ngày |
| **Medium Priority — Category** | Tất cả SP theo danh mục | Target ROAS | Medium | 15K/ngày |
| **Low Priority — Catch All** | Tất cả SP còn lại | Maximize Clicks | Low | 10K/ngày |

### 10.4. Lộ trình Bidding

| Giai đoạn | Thời gian | Strategy | Điều kiện chuyển |
|-----------|----------|----------|-----------------|
| **Phase 1** | Tháng 1 | Manual CPC | Kiểm soát chi phí, học data |
| **Phase 2** | Tháng 2 | Target ROAS | Khi có 30+ conversions |
| **Phase 3** | Tháng 3 | Performance Max | Đủ data → tự động tối ưu cross-channel |

---

## 11. DISPLAY / REMARKETING

### 11.1. Remarketing Audiences Setup

> Google Ads → Tools & Settings → Audience Manager → Create

| Audience | Window | Message | Frequency Cap |
|----------|--------|---------|--------------|
| **All Visitors (chưa mua)** | 30 ngày | "Quay lại Xiaomi247 — Ưu đãi đang chờ bạn" | 5 lần/tuần |
| **Product Viewers** | 14 ngày | Dynamic — hiển thị SP đã xem | 7 lần/tuần |
| **Cart Abandoners** | 7 ngày | "Hoàn tất đơn hàng — Giảm thêm 5%" | 10 lần/tuần |
| **Past Customers** | 60 ngày | Cross-sell phụ kiện, SP mới | 3 lần/tuần |

### 11.2. Responsive Display Ads

**Assets cần chuẩn bị:**

| Asset | Số lượng | Kích thước | Yêu cầu |
|-------|---------|-----------|---------|
| **Landscape image** | 3-5 | 1200 × 628 px | Sản phẩm rõ ràng, nền sáng |
| **Square image** | 3-5 | 1200 × 1200 px | Logo nhỏ góc dưới |
| **Logo (landscape)** | 1 | 512 × 128 px | Logo Xiaomi247 |
| **Logo (square)** | 1 | 128 × 128 px | Icon Xiaomi247 |
| **Short headline** | 5 | Max 30 ký tự | "Tivi Xiaomi từ 4.5 triệu" |
| **Long headline** | 1 | Max 90 ký tự | "Xiaomi Chính Hãng — Freeship Toàn Quốc, Trả Góp 0%" |
| **Description** | 5 | Max 90 ký tự | "Mua tivi, robot hút bụi, gia dụng Xiaomi giá tốt nhất" |
| **Business name** | 1 | Max 25 ký tự | Xiaomi247 |
| **CTA** | 1 | Auto hoặc "Shop Now" | |

### 11.3. Banner Sizes (nếu dùng static ads)

| Size | Tên | Vị trí hiển thị |
|------|-----|-----------------|
| 300 × 250 | Medium Rectangle | In-article, sidebar |
| 728 × 90 | Leaderboard | Header, between content |
| 320 × 50 | Mobile Leaderboard | Mobile websites |
| 160 × 600 | Wide Skyscraper | Sidebar |
| 300 × 600 | Half Page | Sidebar premium |

### 11.4. Display Creative Guidelines

- Logo Xiaomi247 ở góc (nhất quán với brand)
- Hình sản phẩm rõ ràng, nền trắng hoặc sáng
- Giá hiển thị rõ + badge **"Chính hãng"**
- CTA button nổi bật: màu cam **#FF6900**
- Palette: #FF6900 (cam Xiaomi) + #FFFFFF + #333333

---

## 12. NEGATIVE KEYWORDS

### 12.1. Account-Level Negatives (áp dụng tất cả campaigns)

| Nhóm | Keywords |
|------|---------|
| **Miễn phí/Free** | miễn phí, free, crack, download |
| **Cũ/Secondhand** | cũ, secondhand, thanh lý, đã qua sử dụng, refurbished |
| **Sửa chữa** | sửa chữa, repair, fix, thay thế linh kiện, trung tâm bảo hành |
| **Tuyển dụng** | tuyển dụng, việc làm, job, career, nhân viên |
| **Ngoài phạm vi** | xiaomi điện thoại, xiaomi phone, redmi, poco, mi band, xiaomi watch |
| **Hàng giả** | fake, nhái, hàng giả, hàng nhái, replica, copy |
| **ROM/Firmware** | hướng dẫn root, rom, firmware, flash, unlock |
| **Marketplace** | lazada, shopee, tiki, sendo, amazon |

### 12.2. Campaign-Level Negatives

| Campaign | Negative Keywords |
|----------|-----------------|
| **Tivi** | -điện thoại -phone -laptop -tablet -máy tính |
| **Robot hút bụi** | -roomba -ecovacs -dreame (chỉ nếu CPC quá cao) |
| **Tủ lạnh** | -samsung -lg -hitachi -panasonic (evaluate trước khi add) |
| **Máy lọc KK** | -sharp -panasonic -daikin (evaluate trước) |
| **Tất cả Non-Branded** | -[branded terms] (tránh chồng chéo với Branded campaign) |

### 12.3. Quy trình Review Negative Keywords

1. **Hàng tuần:** Vào Google Ads → Keywords → **Search terms** report
2. Tìm các search terms không liên quan → Add negative
3. Check CPC cao bất thường → Evaluate negative
4. Maintain shared negative keyword list cho toàn account

---

## 13. BUDGET BREAKDOWN TỔNG HỢP

### 13.1. Tổng Budget Digital Ads — 24.5M VNĐ/tháng

| Kênh | Budget/tháng | % Tổng | Budget/ngày |
|------|-------------|--------|-------------|
| **Facebook/Instagram Ads** | 14,000,000đ | 57.1% | 467,000đ |
| **Google Ads** | 10,500,000đ | 42.9% | 350,000đ |
| **TỔNG** | **24,500,000đ** | **100%** | **817,000đ** |

### 13.2. Chi tiết Facebook Ads — 14M VNĐ

| Campaign | Budget/tháng | Budget/ngày | % FB Budget | Objective |
|----------|-------------|-------------|-------------|-----------|
| Awareness - Video Views | 1,400,000đ | 47,000đ | 10% | Video Views |
| Traffic - Interest | 2,100,000đ | 70,000đ | 15% | Link Clicks |
| Traffic - Lookalike | 2,100,000đ | 70,000đ | 15% | Link Clicks |
| Conversion - Retarget | 4,200,000đ | 140,000đ | 30% | Purchase |
| Conversion - LAL Purchasers | 2,100,000đ | 70,000đ | 15% | Purchase |
| Retention - Cross-sell | 2,100,000đ | 70,000đ | 15% | Conversions |
| **TỔNG** | **14,000,000đ** | **467,000đ** | **100%** | |

### 13.3. Chi tiết Google Ads — 10.5M VNĐ

| Campaign | Budget/tháng | Budget/ngày | % Google Budget | Bid Strategy |
|----------|-------------|-------------|----------------|-------------|
| Branded Search | 1,500,000đ | 50,000đ | 14.3% | Manual CPC |
| Search: Tivi ⭐ | 2,400,000đ | 80,000đ | 22.9% | Target CPA |
| Search: Robot hút bụi | 1,800,000đ | 60,000đ | 17.1% | Target CPA |
| Search: Gia dụng | 1,500,000đ | 50,000đ | 14.3% | Target CPA |
| Search: Tủ lạnh ⭐ | 1,200,000đ | 40,000đ | 11.4% | Max Clicks → CPA |
| Search: Máy lọc KK + Hút ẩm | 900,000đ | 30,000đ | 8.6% | Max Clicks → CPA |
| Google Shopping | 1,500,000đ | 50,000đ | 14.3% | Manual CPC → ROAS |
| Display Remarketing | 1,000,000đ | 33,000đ | 9.5% | Target CPA |
| **TỔNG** | **11,800,000đ** | — | — | |

> ⚠️ **Ghi chú:** Tổng Google chi tiết = 11.8M > 10.5M budget. Trong thực tế, các campaign sẽ không chi hết daily budget mỗi ngày. Monitor và điều chỉnh hàng tuần để giữ tổng ≤ 10.5M/tháng.

### 13.4. KPI Targets

| Metric | Facebook Ads | Google Ads | Tổng |
|--------|-------------|-----------|------|
| **Budget** | 14M | 10.5M | 24.5M |
| **Clicks (dự kiến)** | 7K–10K | 5K–8K | 12K–18K |
| **Conversions** | 20–35 đơn | 15–30 đơn | 35–65 đơn |
| **CPA target** | ≤ 180K | ≤ 150K | ≤ 165K |
| **ROAS target** | ≥ 3x | ≥ 4x | ≥ 3.5x |
| **CTR target** | ≥ 1.5% | ≥ 2% | — |

### 13.5. Quy tắc Tối ưu Budget

| Tình huống | Hành động |
|-----------|----------|
| ✅ ROAS > 3x liên tục 5+ ngày | Tăng budget 20% cho campaign đó |
| ✅ CPA < target 7 ngày liên tiếp | Tăng budget 20% |
| 🔴 ROAS < 2x sau 7 ngày | Giảm 30% budget hoặc tắt campaign |
| 🔴 CPA > 2× target | Pause → review creative + targeting |
| 🔴 CTR < 0.5% | Creative không hiệu quả → thay mới |
| 🔄 Hàng tuần (Thứ 2) | Review budget allocation, chuyển từ kênh CPA cao → thấp |
| 💡 Luôn giữ | Ít nhất 5% budget cho test creative/audience mới |

---

*📢 Hướng dẫn Setup Ads — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Review: Hàng tuần*
*Tham chiếu: [Facebook Ads Plan](../marketing/05-digital-marketing/facebook-ads-plan.md) | [Google Ads Plan](../marketing/05-digital-marketing/google-ads-plan.md) | [Ads Budget](../marketing/05-digital-marketing/ads-budget-proposal.md) | [Tracking & Analytics](../website-dev/07-tracking-analytics.md)*

