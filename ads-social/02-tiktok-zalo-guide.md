# HƯỚNG DẪN SETUP & TRIỂN KHAI TIKTOK ADS + ZALO OA — XIAOMI247.COM

> **Tổng budget:** 8.75M VNĐ/tháng (TikTok 7M + Zalo OA 1.75M)
> **Mục tiêu:** Brand awareness Gen Z/Millennials (TikTok) + Chăm sóc khách hàng (Zalo OA)
> **Tham chiếu:** [TikTok Strategy](../marketing/05-digital-marketing/tiktok-strategy.md) | [Digital Marketing](../marketing/05-digital-marketing/digital-marketing-strategy.md) | [Ads Budget](../marketing/05-digital-marketing/ads-budget-proposal.md)
> **Cập nhật:** Tháng 3/2026

---

# PHẦN 1 — TIKTOK (7M VNĐ/THÁNG)

---

## 1. TIKTOK BUSINESS ACCOUNT — ĐĂNG KÝ & SETUP

### 1.1. Đăng ký tài khoản

1. Truy cập [TikTok for Business](https://www.tiktok.com/business/vi)
2. Chọn **"Bắt đầu"** → Đăng ký bằng email doanh nghiệp (vd: `marketing@xiaomi247.com`)
3. Chọn loại tài khoản: **Business Account**
4. Điền thông tin doanh nghiệp:
   - Tên doanh nghiệp: **Xiaomi247 — Phân phối Xiaomi chính hãng**
   - Ngành: **Retail / E-commerce**
   - Quốc gia: **Việt Nam**
   - Số điện thoại liên hệ

### 1.2. Setup Profile

| Mục | Nội dung |
|-----|---------|
| **Tên hiển thị** | Xiaomi247.com |
| **Username** | @xiaomi247 |
| **Avatar** | Logo Xiaomi247 (vuông, nền trắng, 200x200px) |
| **Bio** | 🏠 Phân phối Xiaomi chính hãng toàn quốc · Tivi · Robot hút bụi · Gia dụng thông minh · 🛒 Mua ngay 👇 |
| **Link website** | https://xiaomi247.com?utm_source=tiktok&utm_medium=bio |
| **Email liên hệ** | info@xiaomi247.com |
| **Danh mục** | Electronics / Technology |

### 1.3. Xác minh tài khoản (Verify)

1. Vào **Settings → Manage Account → Verification**
2. Chuẩn bị giấy tờ:
   - Giấy phép kinh doanh (bản scan rõ nét)
   - CMND/CCCD người đại diện
   - Hóa đơn tiện ích hoặc giấy tờ xác nhận địa chỉ
3. Upload và chờ duyệt (3-5 ngày làm việc)
4. Sau khi verify → nhận **tick xanh** (Blue Checkmark)

> ⚠️ **Lưu ý:** Tài khoản Business được ưu tiên duyệt nhanh hơn. Đảm bảo tên tài khoản khớp với tên trên giấy phép kinh doanh.

---

## 2. TIKTOK PIXEL — CÀI ĐẶT QUA GTM

### 2.1. Tạo TikTok Pixel

1. Đăng nhập [TikTok Ads Manager](https://ads.tiktok.com)
2. Vào **Assets → Events → Web Events**
3. Chọn **"Create Pixel"**
4. Đặt tên: `Xiaomi247_TikTok_Pixel`
5. Chọn phương thức: **Manually Install Pixel Code** (để dùng GTM)
6. Copy **Pixel ID** (dạng: `CXXXXXXXXXXXXXXXXX`)

### 2.2. Cài đặt qua Google Tag Manager (GTM)

**Bước 1 — Tạo Tag TikTok Base Pixel:**
1. Mở GTM → **Tags → New**
2. Tag type: **Custom HTML**
3. Dán code TikTok Pixel base:

```html
<script>
!function (w, d, t) {
  w.TiktokAnalyticsObject=t;var ttq=w[t]=w[t]||[];
  ttq.methods=["page","track","identify","instances","debug","on","off","once","ready","alias","group","enableCookie","disableCookie"];
  ttq.setAndDefer=function(t,e){t[e]=function(){t.push([e].concat(Array.prototype.slice.call(arguments,0)))}};
  for(var i=0;i<ttq.methods.length;i++)ttq.setAndDefer(ttq,ttq.methods[i]);
  ttq.instance=function(t){for(var e=ttq._i[t]||[],n=0;n<ttq.methods.length;n++)ttq.setAndDefer(e,ttq.methods[n]);return e};
  ttq.load=function(e,n){var i="https://analytics.tiktok.com/i18n/pixel/events.js";
  ttq._i=ttq._i||{};ttq._i[e]=[];ttq._i[e]._u=i;ttq._t=ttq._t||{};ttq._t[e+""]=+new Date;
  ttq._o=ttq._o||{};ttq._o[e+""]=n||{};
  var o=document.createElement("script");o.type="text/javascript";o.async=!0;o.src=i+"?sdkid="+e+"&lib="+t;
  var a=document.getElementsByTagName("script")[0];a.parentNode.insertBefore(o,a)};
  ttq.load('YOUR_PIXEL_ID');
  ttq.page();
}(window, document, 'ttq');
</script>
```

4. Thay `YOUR_PIXEL_ID` bằng Pixel ID thực tế
5. Trigger: **All Pages**
6. Lưu và publish

**Bước 2 — Event Mapping:**

| Event TikTok | Trigger GTM | Mô tả |
|--------------|-------------|-------|
| `ViewContent` | Product page view | Khách xem trang sản phẩm |
| `AddToCart` | Add to cart button click | Khách thêm SP vào giỏ |
| `InitiateCheckout` | Checkout page load | Khách bắt đầu thanh toán |
| `CompletePayment` | Thank you page / Purchase event | Khách mua hàng thành công |
| `ClickButton` | CTA button clicks | Khách click nút CTA |

**Bước 3 — Tạo Event Tags trong GTM:**

Ví dụ tag `AddToCart`:
```html
<script>
  ttq.track('AddToCart', {
    content_id: '{{Product ID}}',
    content_name: '{{Product Name}}',
    content_type: 'product',
    quantity: 1,
    price: {{Product Price}},
    currency: 'VND'
  });
</script>
```

### 2.3. Kiểm tra Pixel

1. Cài extension **TikTok Pixel Helper** trên Chrome
2. Truy cập xiaomi247.com → kiểm tra pixel fire đúng
3. Trong TikTok Ads Manager → **Events → Diagnostics** → xác nhận events nhận được
4. Test từng event: xem SP, thêm giỏ, thanh toán

> ✅ **Checklist Pixel:**
> - [ ] Base pixel fire trên tất cả trang
> - [ ] ViewContent fire trên trang sản phẩm
> - [ ] AddToCart fire khi click "Thêm vào giỏ"
> - [ ] CompletePayment fire trên trang cảm ơn
> - [ ] Pixel Helper không báo lỗi

---

## 3. ORGANIC CONTENT PLAN — 4 VIDEOS/TUẦN

### 3.1. Năm trụ cột nội dung (5 Content Pillars)

| # | Pillar | Tỷ lệ | Videos/tháng | Mô tả |
|---|--------|--------|-------------|-------|
| 1 | 📦 **Unboxing & First Impressions** | 25% | 4 | POV unboxing, ASMR mở hộp, reaction đầu tiên |
| 2 | ⚡ **Review nhanh & Highlights** | 25% | 4 | Quick review 60s, "3 lý do nên mua", highlight tính năng |
| 3 | 💡 **Tips sử dụng & Mẹo hay** | 20% | 3-4 | Tutorial ngắn, tips ẩn, life hacks sản phẩm Xiaomi |
| 4 | 🔄 **So sánh & Đối đầu** | 20% | 3-4 | Side-by-side comparison, "A hay B?", challenge |
| 5 | 🎬 **Behind-the-scenes & Engagement** | 10% | 1-2 | Hậu trường, đóng gói đơn, team Xiaomi247, Q&A |

### 3.2. Ý tưởng content theo pillar

**📦 Unboxing & First Impressions (25%)**
- Unboxing Robot hút bụi Xiaomi X10+ — tự đổ rác luôn!
- Mở hộp Tivi Xiaomi A Pro 55" — Giá 8 triệu có gì?
- ASMR mở hộp máy lọc không khí Xiaomi 4 Pro
- Hook mẫu: *"Mở hộp [sản phẩm] giá [X] triệu — Có đáng tiền?"*

**⚡ Review nhanh & Highlights (25%)**
- Tivi Xiaomi A Pro 55 inch — 1 phút review nhanh
- 3 lý do nên mua Robot hút bụi Xiaomi NGAY
- Máy lọc không khí Xiaomi — Dùng 1 tuần, đây là kết quả
- Hook mẫu: *"3 lý do nên mua [sản phẩm] NGAY"*

**💡 Tips sử dụng & Mẹo hay (20%)**
- 5 mẹo dùng robot hút bụi hiệu quả gấp đôi
- Tính năng ẩn trên Tivi Xiaomi ít người biết
- Cách setup smart home Xiaomi cho người mới
- Hook mẫu: *"Mẹo ít người biết khi dùng [sản phẩm]"*

**🔄 So sánh & Đối đầu (20%)**
- Máy lọc KK Xiaomi 4 Pro vs 4 Lite — Chênh 1 triệu, khác gì?
- Robot hút bụi Xiaomi vs Ecovacs — Cái nào đáng tiền?
- Tivi Xiaomi 55" vs Samsung 55" cùng tầm giá
- Hook mẫu: *"[SP A] vs [SP B] — Cái nào đáng tiền hơn?"*

**🎬 Behind-the-scenes & Engagement (10%)**
- Một ngày tại kho Xiaomi247
- Pack 20 đơn hàng trong 1 tiếng — ASMR đóng gói
- Q&A: Trả lời câu hỏi từ followers
- Hook mẫu: *"Một ngày tại kho Xiaomi247"*

---

## 4. VIDEO PRODUCTION GUIDELINES

### 4.1. Cấu trúc video chuẩn

```
┌─────────────────────────────────────────┐
│  HOOK (0-3 giây)                        │
│  → Câu hỏi gây tò mò / Visual bắt mắt │
├─────────────────────────────────────────┤
│  NỘI DUNG CHÍNH (3-50 giây)            │
│  → Thông tin giá trị, demo sản phẩm    │
├─────────────────────────────────────────┤
│  CTA (3-5 giây cuối)                   │
│  → Kêu gọi hành động rõ ràng          │
└─────────────────────────────────────────┘
```

### 4.2. Thông số kỹ thuật

| Thông số | Yêu cầu |
|----------|---------|
| **Tỷ lệ khung hình** | 9:16 (dọc, full screen) |
| **Thời lượng** | 30-60 giây (tối ưu: 45s) |
| **Độ phân giải** | 1080x1920 (Full HD) |
| **FPS** | 30fps |
| **Định dạng** | MP4, MOV |
| **Dung lượng** | Tối đa 500MB |
| **Phụ đề** | BẮT BUỘC — 80% người xem tắt tiếng |

### 4.3. Hook — 3 giây đầu tiên (QUAN TRỌNG NHẤT)

> 🎯 **Quy tắc:** Nếu 3 giây đầu không hấp dẫn → người xem lướt qua. Hook quyết định 80% hiệu quả video.

**Công thức hook hiệu quả:**

| Loại hook | Ví dụ | Khi nào dùng |
|-----------|-------|-------------|
| **Câu hỏi** | "Bạn có biết tivi này giá chỉ 8 triệu?" | Review, so sánh |
| **Số liệu** | "3 lý do nên mua robot hút bụi Xiaomi" | Tips, review |
| **Thách thức** | "Thử dùng robot hút bụi dọn nhà trong 30 phút" | Challenge, BTS |
| **Bí mật** | "Tính năng ẩn trên Tivi Xiaomi ít ai biết" | Tips, mẹo |
| **So sánh** | "Xiaomi vs Samsung — Cái nào đáng tiền hơn?" | So sánh |
| **Visual** | Cận cảnh mở hộp / sản phẩm hoạt động | Unboxing |

### 4.4. CTA (Call-to-Action)

- **Mua hàng:** "Link mua trong bio nhé!" / "Comment 'MUA' để nhận link"
- **Tương tác:** "Follow để xem thêm review!" / "Save lại để không quên!"
- **Chia sẻ:** "Tag bạn đang tìm [sản phẩm]!" / "Share cho ai cần!"

### 4.5. Trending Sounds & Music

- Ưu tiên **nhạc trending** trên TikTok VN (kiểm tra tab Discover hàng ngày)
- Dùng **original sound** cho review/tips (giọng nói tự nhiên)
- **ASMR sounds** cho unboxing (tiếng xé hộp, bóc nilon)
- Tránh nhạc có bản quyền → dùng TikTok Commercial Music Library

### 4.6. Editing Tips

- **Text overlay:** Thêm chữ lớn, dễ đọc (font: bold, có viền/shadow)
- **Transitions:** Dùng cut nhanh, zoom in/out, swipe
- **Pace:** Nhanh, không kéo dài — mỗi shot 2-4 giây
- **Captions:** Tự động bằng CapCut hoặc thêm thủ công
- **App chỉnh sửa:** CapCut (miễn phí, nhiều template TikTok)

### 4.7. Equipment cơ bản

| Thiết bị | Gợi ý | Chi phí ước tính |
|----------|-------|-----------------|
| **Điện thoại** | Xiaomi 14 / iPhone 13+ (camera tốt) | Có sẵn |
| **Tripod** | Tripod điện thoại có remote bluetooth | 150K-300K |
| **Ring light** | Đèn LED ring 26cm | 200K-400K |
| **Micro** | Micro cài áo wireless (nếu cần) | 300K-500K |
| **Phông nền** | Góc trưng bày sản phẩm gọn gàng | 0đ (tận dụng) |

> 💡 **Tổng chi phí equipment:** ~700K-1.2M VNĐ (đầu tư 1 lần)


---

## 5. TIKTOK ADS SETUP — CHIẾN DỊCH QUẢNG CÁO

### 5.1. Cấu trúc tài khoản quảng cáo

```
TikTok Ads Manager
├── Campaign 1: Spark Ads (60% = 4.2M/tháng)
│   ├── Ad Group: Broad Targeting (25-45, VN)
│   └── Ad Group: Interest Targeting (Tech, Home)
├── Campaign 2: In-feed Ads (30% = 2.1M/tháng)
│   ├── Ad Group: Traffic - Interest
│   └── Ad Group: Traffic - Lookalike
└── Campaign 3: Retargeting (10% = 700K/tháng)
    ├── Ad Group: Website Visitors (7 ngày)
    └── Ad Group: Video Viewers (50%+)
```

### 5.2. Spark Ads — Boost Organic (Ưu tiên — 60% budget)

**Concept:** Boost các video organic đã có performance tốt → tăng reach với chi phí thấp.

**Cách setup:**
1. Vào TikTok Ads Manager → **Create Campaign**
2. Objective: **Traffic** hoặc **Video Views**
3. Ad Group:
   - Placement: TikTok
   - Targeting: Broad (25-45 tuổi, Việt Nam) hoặc Interest (Technology, Home & Garden)
   - Budget: 100-200K/ngày cho mỗi Spark Ad
   - Schedule: 5-7 ngày/video
4. Ad: Chọn **Spark Ads** → Authorize organic post
5. Tiêu chí chọn video để boost:
   - ✅ Video organic đạt >5,000 views
   - ✅ Engagement rate >5%
   - ✅ Watch time trung bình >50%
   - ✅ Comment/share tích cực

### 5.3. In-feed Ads — Traffic (30% budget)

**Cách setup:**
1. Campaign objective: **Traffic** hoặc **Conversion**
2. Ad Group:
   - Format: Video 9:16, 15-30 giây, native-looking
   - Targeting:
     - **Interest:** Technology, Smart Home, Home Appliances, Xiaomi
     - **Behavior:** Video viewers, Engaged with tech content
     - **Demographics:** 22-45 tuổi, Urban (HN, HCM, ĐN, HP, CT)
   - Budget: 200-300K/ngày
   - Bidding: Lowest cost (ban đầu) → Cost cap (khi có data)
3. Ad creative:
   - Video giống organic (không quá "quảng cáo")
   - CTA: "Mua ngay" / "Tìm hiểu thêm"
   - Landing page: Trang sản phẩm tương ứng trên xiaomi247.com

### 5.4. Phân bổ budget TikTok Ads chi tiết

| Campaign | Budget/tháng | Budget/ngày | Objective |
|----------|-------------|-------------|-----------|
| Spark Ads (boost organic) | 3M | 100K | Video Views + Traffic |
| In-feed Ads (traffic) | 2.5M | 83K | Traffic |
| Retargeting | 1.5M | 50K | Conversions |
| **Tổng** | **7M** | **233K** | — |

---

## 6. TIKTOK SHOP — ĐĂNG KÝ & LIÊN KẾT SẢN PHẨM

### 6.1. Điều kiện đăng ký TikTok Shop

- ✅ Có giấy phép kinh doanh hợp lệ
- ✅ Tài khoản TikTok Business đã verify
- ✅ Có kho hàng và khả năng vận chuyển
- ✅ Sản phẩm không thuộc danh mục cấm

### 6.2. Quy trình đăng ký

1. Truy cập [TikTok Shop Seller Center](https://seller-vn.tiktok.com)
2. Đăng nhập bằng tài khoản TikTok Business
3. Upload giấy tờ:
   - Giấy phép kinh doanh
   - CMND/CCCD người đại diện
   - Thông tin ngân hàng (tài khoản doanh nghiệp)
4. Chờ duyệt (5-7 ngày làm việc)
5. Sau khi duyệt → setup shop:
   - Tên shop: **Xiaomi247 Official**
   - Logo, banner, mô tả shop
   - Chính sách đổi trả, vận chuyển

### 6.3. Upload sản phẩm ưu tiên

| Nhóm SP | Ví dụ | Lý do ưu tiên |
|---------|-------|---------------|
| **Phụ kiện** (giá thấp) | Dây sạc, ốp lưng, tai nghe | Dễ impulse buy, AOV thấp |
| **Gia dụng nhỏ** (<1M) | Quạt, máy sấy tóc, đèn bàn | Giá hợp lý cho TikTok |
| **Robot hút bụi entry** | Xiaomi Robot Vacuum E10 | SP hero, viral potential |

### 6.4. Liên kết sản phẩm trong video

- Gắn **product link** trực tiếp vào video TikTok
- Sử dụng **Product Showcase** (tab sản phẩm trên profile)
- Trong video: thêm **giỏ hàng màu vàng** (shopping bag icon)
- Live Shopping: hiển thị SP đang giới thiệu real-time

### 6.5. Lộ trình TikTok Shop

| Giai đoạn | Thời gian | Hoạt động |
|-----------|----------|----------|
| **Setup** | T1 tuần 1-2 | Đăng ký, upload 20-30 SP chủ lực |
| **Optimize** | T1 tuần 3-4 | Tối ưu listing, thêm video cho SP |
| **Launch** | T2 | Flash Sale, Collection Ads |
| **Scale** | T3 | Affiliate program, Live Shopping 2 lần/tuần |

---

## 7. POSTING SCHEDULE — LỊCH ĐĂNG BÀI TUẦN

### 7.1. Bảng lịch đăng tuần

| Ngày | Giờ đăng | Content Pillar | Format | Ghi chú |
|------|---------|---------------|--------|---------|
| **Thứ 2** | 12:00 | ⚡ Review nhanh | Quick review 60s | Đầu tuần, người xem tìm SP mới |
| **Thứ 4** | 19:00 | 📦 Unboxing / 🔄 So sánh | Unboxing hoặc comparison | Giữa tuần, engagement cao buổi tối |
| **Thứ 6** | 18:00 | 💡 Tips / Mẹo hay | Tutorial ngắn | Cuối tuần, content giáo dục |
| **Chủ nhật** | 10:00 | 🎬 BTS / Engagement | Behind-the-scenes, trend | Weekend, casual content |

### 7.2. Golden Hours TikTok Việt Nam

| Khung giờ | Đặc điểm | Phù hợp cho |
|-----------|----------|-------------|
| **7:00 - 9:00** | Sáng sớm, lướt trước khi đi làm | Tips ngắn, mẹo hay |
| **12:00 - 13:00** | Giờ nghỉ trưa | Review nhanh, so sánh |
| **19:00 - 22:00** | Tối, engagement cao nhất | Unboxing, content dài hơn |

### 7.3. Quy tắc đăng bài

- **Tối thiểu:** 4 videos/tuần (16 videos/tháng)
- **Tăng lên 5 videos/tuần** khi có đủ content backlog (từ tháng 2)
- **Đăng lại content tốt** sau 2-3 tuần với góc quay/hook khác
- **Không đăng 2 video cùng pillar** liên tiếp
- **Chuẩn bị content trước 1 tuần** — quay batch vào cuối tuần

---

## 8. HASHTAG STRATEGY

### 8.1. Hashtag Mix (mỗi video: 5-8 hashtags)

| Loại | Số lượng | Ví dụ |
|------|---------|-------|
| **Branded** (bắt buộc) | 1-2 | #xiaomi247 #xiaomi247review |
| **Product** | 1-2 | #tivixiaomi #robothutbui #tulanhxiaomi |
| **Category** | 1-2 | #smarthome #giadungthongminh #congnghe |
| **Trending** | 1-2 | #fyp #xuhuong #tiktokvietnam #viral |
| **Niche** | 1 | #reviewcongnghe #nenmuagi #meohay |

### 8.2. Branded Hashtags cần xây dựng

| Hashtag | Mục đích | Dùng khi |
|---------|---------|---------|
| `#xiaomi247` | Hashtag chính thương hiệu | Mọi video |
| `#xiaomi247review` | Series review sản phẩm | Video review, so sánh |
| `#xiaomi247unboxing` | Series unboxing | Video mở hộp |
| `#hoinhadepxiaomi` | UGC campaign | Khuyến khích khách chia sẻ |

### 8.3. Hashtag theo pillar

| Pillar | Hashtags gợi ý |
|--------|---------------|
| 📦 Unboxing | #unboxing #moihop #xiaomi #review #fyp |
| ⚡ Review | #review #danhgia #nenmuagi #xiaomi247 #congnghe |
| 💡 Tips | #tips #meohay #huongdan #smarthome #tinhnanganh |
| 🔄 So sánh | #sosánh #battle #nenmuacainao #techreview |
| 🎬 BTS | #behindthescenes #hautrường #xiaomi247 #donhang |

### 8.4. Quy tắc sử dụng hashtag

- **Luôn đặt branded hashtag đầu tiên** (#xiaomi247)
- **Không spam hashtag** — tối đa 8 hashtags/video
- **Kiểm tra trending hashtags** hàng ngày trên tab Discover
- **Tạo hashtag riêng cho campaign** (vd: #xiaomi247sale, #xiaomi247tet)
- **Theo dõi performance** từng hashtag qua TikTok Analytics

---
---

# PHẦN 2 — ZALO OA (1.75M VNĐ/THÁNG)

---

## 9. ZALO OA SETUP — ĐĂNG KÝ & CẤU HÌNH

### 9.1. Đăng ký Zalo Official Account

1. Truy cập [Zalo OA Admin](https://oa.zalo.me)
2. Đăng nhập bằng tài khoản Zalo cá nhân (của người quản lý)
3. Chọn **"Tạo Official Account"**
4. Chọn loại: **OA Doanh nghiệp** (Enterprise)
5. Điền thông tin:
   - Tên OA: **Xiaomi247 — Phân phối Xiaomi chính hãng**
   - Danh mục: **Cửa hàng / Điện tử - Công nghệ**
   - Mô tả: Phân phối sản phẩm Xiaomi chính hãng toàn quốc. Tivi, Robot hút bụi, Máy lọc không khí, Gia dụng thông minh.
   - Địa chỉ, SĐT, email, website

### 9.2. Xác minh OA (Verify)

**Giấy tờ cần chuẩn bị:**
- Giấy phép kinh doanh (bản scan rõ nét)
- CMND/CCCD người đại diện pháp luật
- Ảnh chụp mặt tiền cửa hàng/văn phòng (nếu có)

**Quy trình:**
1. Vào **Quản lý → Xác minh OA**
2. Upload giấy tờ
3. Chờ Zalo duyệt (3-7 ngày làm việc)
4. Sau khi verify → nhận **tick xanh** + mở khóa tính năng nâng cao

### 9.3. Setup Profile OA

| Mục | Nội dung |
|-----|---------|
| **Ảnh đại diện** | Logo Xiaomi247 (vuông, 500x500px) |
| **Ảnh bìa** | Banner sản phẩm chủ lực + slogan (1080x360px) |
| **Mô tả** | 🏠 Phân phối Xiaomi chính hãng · Tivi · Robot hút bụi · Gia dụng · Giao toàn quốc · Bảo hành chính hãng |
| **Địa chỉ** | Địa chỉ cửa hàng/kho |
| **Website** | https://xiaomi247.com?utm_source=zalo&utm_medium=oa |
| **Giờ làm việc** | 8:00 - 21:00 (T2-CN) |

---

## 10. MENU CONFIGURATION — CẤU HÌNH MENU OA

### 10.1. Cấu trúc menu (tối đa 4 mục chính)

```
📱 Menu Zalo OA — Xiaomi247
├── 🛒 Sản phẩm
│   ├── Tivi Xiaomi
│   ├── Robot hút bụi
│   ├── Máy lọc không khí
│   └── Gia dụng thông minh
├── 🔥 Khuyến mãi
│   ├── Flash Sale hôm nay
│   ├── Combo tiết kiệm
│   └── Mã giảm giá
├── 📋 Chính sách
│   ├── Bảo hành
│   ├── Đổi trả
│   ├── Vận chuyển
│   └── Thanh toán
└── 📞 Liên hệ & Hỗ trợ
    ├── Chat với tư vấn viên
    ├── Tra cứu đơn hàng
    ├── Hotline: 0xxx.xxx.xxx
    └── Địa chỉ cửa hàng
```

### 10.2. Cách cấu hình

1. Vào **Zalo OA Admin → Quản lý → Menu**
2. Thêm từng mục menu:
   - **Type:** URL (link đến trang web) hoặc Message (gửi tin nhắn)
   - **Sản phẩm:** Link đến danh mục trên xiaomi247.com
   - **Khuyến mãi:** Link đến trang khuyến mãi
   - **Chính sách:** Link đến trang chính sách
   - **Liên hệ:** Trigger message → chuyển đến chatbot/nhân viên
3. **Lưu** và kiểm tra trên điện thoại

---

## 11. AUTO-REPLY & WELCOME MESSAGE

### 11.1. Tin nhắn chào mừng (Welcome Message)

Khi người dùng **quan tâm (follow) OA** lần đầu:

```
Xin chào! 👋 Cảm ơn bạn đã quan tâm Xiaomi247!

🏠 Chúng tôi phân phối sản phẩm Xiaomi chính hãng toàn quốc:
📺 Tivi Xiaomi
🤖 Robot hút bụi
🌬️ Máy lọc không khí
🏡 Gia dụng thông minh

🔥 Nhận ngay mã giảm 5% cho đơn hàng đầu tiên!
👉 Mã: WELCOME5

Bạn cần tư vấn sản phẩm nào? Chọn bên dưới hoặc nhắn tin trực tiếp nhé! 😊
```

### 11.2. Auto-reply ngoài giờ làm việc

Khi nhận tin nhắn **ngoài giờ 8:00-21:00:**

```
Cảm ơn bạn đã nhắn tin cho Xiaomi247! 🙏

⏰ Hiện tại ngoài giờ làm việc (8:00 - 21:00).
Chúng tôi sẽ phản hồi ngay khi online!

Trong khi chờ, bạn có thể:
🛒 Xem sản phẩm: xiaomi247.com
📋 Tra cứu đơn hàng: [link]
❓ Xem FAQ: [link]

Chúc bạn một ngày tốt lành! 😊
```

### 11.3. FAQ Auto-responses

| Câu hỏi thường gặp | Auto-reply |
|-------------------|-----------|
| "Giá bao nhiêu?" | "Bạn quan tâm sản phẩm nào ạ? Xem giá tại: xiaomi247.com 🛒" |
| "Có bảo hành không?" | "Tất cả SP đều bảo hành chính hãng 12-24 tháng ✅ Chi tiết: [link]" |
| "Ship bao lâu?" | "Giao hàng 2-5 ngày toàn quốc 🚚 Nội thành HN/HCM: 1-2 ngày" |
| "Có COD không?" | "Có ạ! Hỗ trợ COD toàn quốc 💰 Hoặc chuyển khoản giảm thêm 2%" |
| "Đổi trả thế nào?" | "Đổi trả trong 7 ngày nếu lỗi từ nhà sản xuất 🔄 Chi tiết: [link]" |

---

## 12. ZALO ADS — QUẢNG CÁO TRÊN ZALO

### 12.1. Loại quảng cáo Zalo

| Loại | Mô tả | Chi phí | Phù hợp khi |
|------|-------|---------|-------------|
| **Message Ads** | Gửi tin nhắn trực tiếp đến người dùng Zalo | ~500-1,500đ/tin | Khuyến mãi, sản phẩm mới, remarketing |
| **Article Ads** | Bài viết quảng cáo hiển thị trên Zalo feed | ~300-800đ/click | Brand awareness, content marketing |
| **Display Ads** | Banner quảng cáo trên Zalo | CPM ~30-60K | Reach rộng, brand awareness |

### 12.2. Message Ads — Gửi tin nhắn (Ưu tiên)

**Cách setup:**
1. Vào [Zalo Ads](https://ads.zalo.me) → **Tạo chiến dịch**
2. Chọn mục tiêu: **Tin nhắn**
3. Targeting:
   - **Vị trí:** Toàn quốc hoặc tỉnh/thành cụ thể
   - **Giới tính:** Tất cả
   - **Độ tuổi:** 25-50
   - **Sở thích:** Công nghệ, Gia dụng, Mua sắm online
4. Nội dung tin nhắn:
   - Tiêu đề hấp dẫn (max 50 ký tự)
   - Hình ảnh sản phẩm (tỷ lệ 1:1 hoặc 16:9)
   - Nội dung ngắn gọn + CTA rõ ràng
   - Button: "Mua ngay" / "Xem chi tiết" / "Nhắn tin"
5. Budget: 50-80K/ngày

### 12.3. Article Ads — Bài viết quảng cáo

**Cách setup:**
1. Tạo bài viết trên Zalo OA (dạng article)
2. Vào Zalo Ads → **Tạo chiến dịch → Bài viết**
3. Chọn bài viết cần quảng cáo
4. Targeting tương tự Message Ads
5. Budget: 30-50K/ngày

### 12.4. Phân bổ budget Zalo Ads

| Loại | Budget/tháng | Budget/ngày | Mục tiêu |
|------|-------------|-------------|-----------|
| Message Ads | 1M | 33K | Push promotions, remarketing |
| Article Ads | 500K | 17K | Content, brand awareness |
| Dự phòng | 250K | — | Test, tăng budget winning |
| **Tổng** | **1.75M** | **~58K** | — |

---

## 13. PUSH NOTIFICATION STRATEGY

### 13.1. Tần suất & Lịch gửi

| Ngày | Giờ gửi | Nội dung | Loại |
|------|---------|---------|------|
| **Thứ 3** | 10:00 | Sản phẩm mới / Highlight tuần | Product |
| **Thứ 5** | 14:00 | Khuyến mãi / Flash sale | Promotion |
| **Thứ 7** | 9:00 | Tips sử dụng / Mẹo hay | Content |

> ⚠️ **Quy tắc:** Tối đa 2-3 lần/tuần. Gửi quá nhiều → người dùng bỏ quan tâm OA.

### 13.2. Template nội dung push notification

**🆕 Sản phẩm mới:**
```
📺 MỚI: Tivi Xiaomi A Pro 65" — Màn hình 4K, giá chỉ 12.990.000đ!

✅ 4K HDR, 60Hz
✅ Google TV tích hợp
✅ Loa Dolby Audio

👉 Xem ngay: [link]
🔥 Giảm thêm 500K khi đặt trước!
```

**🔥 Khuyến mãi:**
```
⚡ FLASH SALE 24H — Giảm đến 30%!

🤖 Robot hút bụi Xiaomi E10: 3.990.000đ → 2.790.000đ (-30%)
🌬️ Máy lọc KK Xiaomi 4: 2.990.000đ → 2.390.000đ (-20%)

⏰ Chỉ hôm nay!
👉 Mua ngay: [link]
```

**💡 Tips & Mẹo:**
```
💡 5 mẹo dùng robot hút bụi hiệu quả gấp đôi!

1️⃣ Dọn vật cản trước khi chạy
2️⃣ Lên lịch hút tự động
3️⃣ Vệ sinh chổi quét hàng tuần
...

👉 Đọc đầy đủ: [link blog]
```

### 13.3. Quy tắc push notification

- **Không gửi trước 8:00 sáng** và **sau 21:00 tối**
- **Luôn có CTA** rõ ràng (link, button)
- **Cá nhân hóa** khi có thể (tên khách hàng, SP đã xem)
- **A/B test** tiêu đề để tối ưu open rate
- **Theo dõi metrics:** Open rate (target ≥40%), CTR (target ≥5%)

---

## 14. CHATBOT SETUP — TƯ VẤN TỰ ĐỘNG

### 14.1. Flow chatbot cơ bản

```
Khách nhắn tin
    │
    ▼
🤖 Chào mừng + Hỏi nhu cầu
    │
    ├── "Xem sản phẩm" ──→ Chọn danh mục
    │       │
    │       ├── Tivi ──→ Gợi ý 3 SP hot + link
    │       ├── Robot hút bụi ──→ Gợi ý 3 SP hot + link
    │       ├── Máy lọc KK ──→ Gợi ý 3 SP hot + link
    │       └── Gia dụng khác ──→ Gợi ý 3 SP hot + link
    │
    ├── "Khuyến mãi" ──→ Hiển thị deal đang chạy + mã giảm giá
    │
    ├── "Tra cứu đơn" ──→ Hỏi mã đơn hàng → Tra cứu
    │
    ├── "Tư vấn" ──→ Hỏi ngân sách + nhu cầu → Gợi ý SP
    │       │
    │       └── Nếu cần chi tiết ──→ 👤 Chuyển nhân viên
    │
    └── "Gặp nhân viên" ──→ 👤 Chuyển nhân viên trực tiếp
```

### 14.2. Cách setup trên Zalo OA

1. Vào **Zalo OA Admin → Chatbot**
2. Tạo **kịch bản tự động** (Scenario):
   - **Trigger:** Tin nhắn đầu tiên / Keyword cụ thể
   - **Response:** Text + Button (chọn nhanh)
   - **Action:** Gửi tin nhắn tiếp theo / Chuyển nhân viên
3. Tạo **Quick Reply buttons:**
   - "🛒 Xem sản phẩm"
   - "🔥 Khuyến mãi"
   - "📦 Tra cứu đơn"
   - "💬 Tư vấn"
   - "👤 Gặp nhân viên"
4. Setup **chuyển nhân viên** khi:
   - Khách chọn "Gặp nhân viên"
   - Chatbot không hiểu câu hỏi (sau 2 lần)
   - Khách hỏi về giá/tư vấn chi tiết

### 14.3. Lưu ý chatbot

- **Giữ đơn giản** — tối đa 3 cấp menu
- **Luôn có option "Gặp nhân viên"** — không ép khách ở trong bot
- **Cập nhật SP/khuyến mãi** trong chatbot hàng tuần
- **Theo dõi:** Tỷ lệ hoàn thành flow, điểm chuyển nhân viên

---

## 15. ZALO MINI APP — KẾ HOẠCH TƯƠNG LAI

### 15.1. Zalo Mini App là gì?

Zalo Mini App là ứng dụng nhỏ chạy bên trong Zalo, không cần cài đặt riêng. Cho phép tạo trải nghiệm mua sắm trực tiếp trên Zalo.

### 15.2. Khả năng ứng dụng cho Xiaomi247

| Tính năng | Mô tả | Ưu tiên |
|-----------|-------|---------|
| **Product Catalog** | Xem danh mục SP, giá, hình ảnh | ⭐⭐⭐ |
| **Đặt hàng** | Đặt hàng trực tiếp trên Zalo | ⭐⭐⭐ |
| **Tra cứu đơn** | Kiểm tra trạng thái đơn hàng | ⭐⭐ |
| **Loyalty Program** | Tích điểm, đổi quà | ⭐ |
| **Flash Sale** | Chương trình giảm giá exclusive | ⭐⭐ |

### 15.3. Lộ trình triển khai (Dự kiến)

| Giai đoạn | Thời gian | Nội dung |
|-----------|----------|---------|
| **Nghiên cứu** | T3-T4 | Tìm hiểu Zalo Mini App SDK, chi phí phát triển |
| **MVP** | T5-T6 | Product catalog + đặt hàng cơ bản |
| **Launch** | T7 | Ra mắt Mini App, quảng bá qua OA |
| **Optimize** | T8+ | Thêm loyalty, flash sale, tra cứu đơn |

> 💡 **Chi phí ước tính:** 15-30M VNĐ cho phát triển MVP (thuê developer hoặc dùng nền tảng no-code).

---
---

# TỔNG KẾT BUDGET

| Kênh | Budget/tháng | Tỷ trọng |
|------|-------------|----------|
| **TikTok Ads** | 7,000,000 VNĐ | 80% |
| **Zalo OA Ads** | 1,750,000 VNĐ | 20% |
| **Tổng** | **8,750,000 VNĐ** | **100%** |

### Phân bổ chi tiết

| Hạng mục | Budget |
|----------|--------|
| TikTok — Spark Ads | 3,000,000 |
| TikTok — In-feed Ads | 2,500,000 |
| TikTok — Retargeting | 1,500,000 |
| Zalo — Message Ads | 1,000,000 |
| Zalo — Article Ads | 500,000 |
| Zalo — Dự phòng | 250,000 |
| **Tổng** | **8,750,000** |

---

*📱 Hướng dẫn TikTok & Zalo OA — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Review: Hàng tháng*
*Tham chiếu: [TikTok Strategy](../marketing/05-digital-marketing/tiktok-strategy.md) | [Digital Marketing](../marketing/05-digital-marketing/digital-marketing-strategy.md) | [Ads Budget](../marketing/05-digital-marketing/ads-budget-proposal.md)*