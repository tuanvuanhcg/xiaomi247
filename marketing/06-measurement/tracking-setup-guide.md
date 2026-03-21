# 🔧 TRACKING SETUP GUIDE — XIAOMI247.COM

*Phiên bản: v1.0 | Ngày tạo: 21/03/2026*
*Platform: WordPress + WooCommerce | Domain: xiaomi247.com*

---

## 1. GOOGLE ANALYTICS 4 (GA4)

### 1.1 Setup Property

1. Truy cập [analytics.google.com](https://analytics.google.com)
2. Tạo Property mới: **Xiaomi247.com**
3. Cấu hình:
   - **Property name:** Xiaomi247.com
   - **Reporting time zone:** (GMT+07:00) Hà Nội
   - **Currency:** VND (₫)
   - **Industry:** Shopping
   - **Business size:** Small

### 1.2 Data Streams

1. Tạo **Web** data stream:
   - **Website URL:** https://xiaomi247.com
   - **Stream name:** Xiaomi247 Web
2. Lưu **Measurement ID** (G-XXXXXXXXXX)
3. Bật **Enhanced Measurement:**
   - ✅ Page views
   - ✅ Scrolls
   - ✅ Outbound clicks
   - ✅ Site search
   - ✅ File downloads

### 1.3 Ecommerce Events (WooCommerce)

Cài plugin **GTM4WP** hoặc **GA4 for WooCommerce** để tự động track:

| Event | Trigger | Parameters |
| --- | --- | --- |
| `view_item` | Xem trang sản phẩm | item_id, item_name, price, item_category |
| `view_item_list` | Xem danh mục sản phẩm | item_list_name, items[] |
| `add_to_cart` | Thêm vào giỏ hàng | item_id, item_name, price, quantity |
| `remove_from_cart` | Xóa khỏi giỏ hàng | item_id, item_name, price, quantity |
| `begin_checkout` | Bắt đầu thanh toán | items[], value, currency |
| `add_shipping_info` | Nhập thông tin giao hàng | shipping_tier, items[] |
| `add_payment_info` | Chọn phương thức thanh toán | payment_type, items[] |
| `purchase` | Hoàn tất đơn hàng | transaction_id, value, tax, shipping, items[] |

### 1.4 Custom Events bổ sung

| Event | Mô tả | Trigger |
| --- | --- | --- |
| `phone_click` | Click số điện thoại | Click vào link tel: |
| `zalo_click` | Click chat Zalo | Click nút Zalo |
| `form_submit` | Gửi form liên hệ | Submit form |
| `promotion_click` | Click banner khuyến mãi | Click vào banner promo |
| `search` | Tìm kiếm sản phẩm | Sử dụng search box |

### 1.5 Conversions cần đánh dấu

Vào GA4 → Admin → Conversions → Mark as conversion:
- ✅ `purchase`
- ✅ `add_to_cart`
- ✅ `begin_checkout`
- ✅ `phone_click`
- ✅ `zalo_click`
- ✅ `form_submit`

---

## 2. GOOGLE TAG MANAGER (GTM)

### 2.1 Container Setup

1. Truy cập [tagmanager.google.com](https://tagmanager.google.com)
2. Tạo Account: **Xiaomi247**
3. Tạo Container: **xiaomi247.com** (Web)
4. Lấy mã GTM (GTM-XXXXXXX)
5. Cài GTM vào WordPress:
   - Plugin: **GTM4WP** (khuyên dùng)
   - Hoặc chèn thủ công vào `<head>` và `<body>`

### 2.2 Tags cần thiết

| # | Tag | Type | Trigger | Ghi chú |
| --- | --- | --- | --- | --- |
| 1 | GA4 Configuration | Google Analytics: GA4 Configuration | All Pages | Measurement ID: G-XXXXXXXXXX |
| 2 | GA4 Ecommerce Events | Google Analytics: GA4 Event | Ecommerce events | Sử dụng Data Layer từ GTM4WP |
| 3 | Facebook Pixel - Base | Custom HTML | All Pages | Pixel ID cơ bản |
| 4 | Facebook Pixel - Events | Custom HTML | Ecommerce events | ViewContent, AddToCart, Purchase |
| 5 | TikTok Pixel - Base | Custom HTML | All Pages | Pixel ID cơ bản |
| 6 | TikTok Pixel - Events | Custom HTML | Ecommerce events | ViewContent, AddToCart, PlaceAnOrder |
| 7 | Google Ads Conversion | Google Ads Conversion Tracking | Purchase | Conversion ID + Label |
| 8 | Google Ads Remarketing | Google Ads Remarketing | All Pages | Remarketing audiences |
| 9 | Hotjar/Clarity | Custom HTML | All Pages | Heatmaps + Session recordings |

### 2.3 Data Layer Variables

Cấu hình trong GTM → Variables → User-Defined Variables:

| Variable Name | Data Layer Variable | Dùng cho |
| --- | --- | --- |
| dlv - ecommerce.items | ecommerce.items | GA4 Ecommerce |
| dlv - ecommerce.value | ecommerce.value | Transaction value |
| dlv - ecommerce.transaction_id | ecommerce.transaction_id | Order ID |
| dlv - ecommerce.currency | ecommerce.currency | VND |

---

## 3. FACEBOOK PIXEL

### 3.1 Setup

1. Truy cập [Meta Events Manager](https://business.facebook.com/events_manager)
2. Tạo Pixel mới: **Xiaomi247 Pixel**
3. Lấy **Pixel ID** (16 chữ số)
4. Cài qua GTM (khuyên dùng) hoặc plugin **PixelYourSite**

### 3.2 Standard Events

| Event | Trigger | Parameters |
| --- | --- | --- |
| `PageView` | Tất cả trang | Tự động |
| `ViewContent` | Xem sản phẩm | content_ids, content_name, content_type, value, currency |
| `AddToCart` | Thêm giỏ hàng | content_ids, content_name, value, currency |
| `InitiateCheckout` | Bắt đầu checkout | content_ids, num_items, value, currency |
| `Purchase` | Hoàn tất mua hàng | content_ids, content_type, value, currency, order_id |
| `Search` | Tìm kiếm | search_string, content_category |
| `Lead` | Gửi form liên hệ | content_name, value |

### 3.3 Custom Conversions

Tạo trong Events Manager → Custom Conversions:

| Tên | Rule | Category | Giá trị |
| --- | --- | --- | --- |
| Mua hàng thành công | URL contains `/order-received/` | Purchase | Dynamic |
| Xem danh mục Điện thoại | URL contains `/dien-thoai/` | ViewContent | — |
| Xem danh mục Phụ kiện | URL contains `/phu-kien/` | ViewContent | — |
| Liên hệ tư vấn | URL contains `/lien-he/` + Event = Lead | Lead | 50.000đ |

### 3.4 Conversions API (CAPI)

- Cài đặt CAPI qua plugin **PixelYourSite Pro** hoặc **Facebook for WooCommerce**
- Mục đích: Gửi server-side events để tăng accuracy (do iOS 14+ block cookies)
- Events cần gửi qua CAPI: Purchase, AddToCart, InitiateCheckout

---

## 4. TIKTOK PIXEL

### 4.1 Setup

1. Truy cập [TikTok Ads Manager](https://ads.tiktok.com)
2. Assets → Events → Web Events → Create Pixel
3. Chọn **Manual Setup** hoặc **Partner Integration**
4. Lấy **Pixel ID**
5. Cài qua GTM

### 4.2 Events

| Event | Trigger | Parameters |
| --- | --- | --- |
| `PageView` | Tất cả trang | Tự động |
| `ViewContent` | Xem sản phẩm | content_id, content_name, content_type, price, currency |
| `AddToCart` | Thêm giỏ hàng | content_id, content_name, price, quantity, currency |
| `PlaceAnOrder` | Đặt hàng | content_id, content_name, price, quantity, currency |
| `CompletePayment` | Thanh toán thành công | content_id, value, currency |
| `Search` | Tìm kiếm | query |

---

## 5. GOOGLE SEARCH CONSOLE

### 5.1 Setup

1. Truy cập [search.google.com/search-console](https://search.google.com/search-console)
2. Thêm Property: **https://xiaomi247.com** (URL prefix)
3. Xác minh quyền sở hữu:
   - ✅ Ưu tiên: HTML tag (qua GTM hoặc plugin Yoast SEO)
   - Hoặc: DNS record, HTML file upload
4. Thêm cả phiên bản: **https://www.xiaomi247.com** (nếu có)

### 5.2 Submit Sitemap

1. Vào Search Console → Sitemaps
2. Submit các sitemap:
   - `https://xiaomi247.com/sitemap_index.xml` (Yoast SEO)
   - `https://xiaomi247.com/product-sitemap.xml`
   - `https://xiaomi247.com/category-sitemap.xml`
   - `https://xiaomi247.com/post-sitemap.xml`

### 5.3 Theo dõi

- **Performance:** Clicks, Impressions, CTR, Position theo keyword
- **Coverage:** Lỗi index, warnings
- **Core Web Vitals:** LCP, FID, CLS
- **Mobile Usability:** Lỗi trên mobile

---

## 6. HOTJAR / MICROSOFT CLARITY (Optional)

### 6.1 Microsoft Clarity (Miễn phí — Khuyên dùng)

1. Truy cập [clarity.microsoft.com](https://clarity.microsoft.com)
2. Tạo Project: **Xiaomi247**
3. Lấy mã Clarity → Cài qua GTM
4. Tính năng:
   - **Heatmaps:** Click maps, scroll maps, area maps
   - **Session Recordings:** Xem lại hành vi người dùng
   - **Insights:** Dead clicks, rage clicks, quick backs

### 6.2 Hotjar (Bản Free hoặc Plus)

1. Truy cập [hotjar.com](https://hotjar.com)
2. Tạo Site: **xiaomi247.com**
3. Cài tracking code qua GTM
4. Tính năng sử dụng:
   - **Heatmaps:** Trang chủ, trang sản phẩm top, trang checkout
   - **Recordings:** Filter theo trang checkout để xem drop-off
   - **Surveys:** Hỏi "Bạn tìm thấy sản phẩm cần mua chưa?" trên trang danh mục

---

## 7. ENHANCED ECOMMERCE TRACKING (WooCommerce)

### 7.1 Plugin Setup

**Plugin khuyên dùng:** GTM4WP (Google Tag Manager for WordPress)

Cấu hình GTM4WP:
1. Settings → Google Tag Manager → Container ID: GTM-XXXXXXX
2. Tab **Integration** → Bật WooCommerce
3. Chọn tracking options:
   - ✅ Track enhanced ecommerce
   - ✅ Product impressions on product listing pages
   - ✅ Product clicks on product listing pages
   - ✅ Product detail views
   - ✅ Add to cart events
   - ✅ Remove from cart events
   - ✅ Checkout steps
   - ✅ Purchases

### 7.2 Funnel Tracking trong GA4

Tạo Funnel Exploration trong GA4 → Explore:

```
Step 1: view_item (Xem sản phẩm)
    ↓
Step 2: add_to_cart (Thêm giỏ hàng)
    ↓
Step 3: begin_checkout (Bắt đầu checkout)
    ↓
Step 4: add_shipping_info (Nhập địa chỉ)
    ↓
Step 5: add_payment_info (Chọn thanh toán)
    ↓
Step 6: purchase (Hoàn tất)
```

### 7.3 UTM Parameters

Quy ước UTM cho tất cả campaigns:

| Parameter | Quy ước | Ví dụ |
| --- | --- | --- |
| `utm_source` | Tên platform | facebook, google, tiktok, zalo |
| `utm_medium` | Loại traffic | cpc, social, email, referral |
| `utm_campaign` | Tên chiến dịch | redmi-note-14-launch, sale-thang4 |
| `utm_content` | Nội dung cụ thể | banner-hero, post-review, video-unbox |
| `utm_term` | Từ khóa (cho search ads) | mua-xiaomi-chinh-hang |

**Ví dụ URL hoàn chỉnh:**
```
https://xiaomi247.com/san-pham/redmi-note-14-pro?utm_source=facebook&utm_medium=cpc&utm_campaign=redmi-note-14-launch&utm_content=carousel-ad-1
```

---

## ✅ CHECKLIST SETUP

| # | Hạng mục | Ưu tiên | Status |
| --- | --- | --- | --- |
| 1 | Cài GTM lên website | P0 | ⬜ |
| 2 | Cấu hình GA4 Property + Data Stream | P0 | ⬜ |
| 3 | Cài GTM4WP + cấu hình WooCommerce tracking | P0 | ⬜ |
| 4 | Setup GA4 Ecommerce events qua GTM | P0 | ⬜ |
| 5 | Đánh dấu Conversions trong GA4 | P0 | ⬜ |
| 6 | Cài Facebook Pixel qua GTM | P1 | ⬜ |
| 7 | Setup FB Standard Events + CAPI | P1 | ⬜ |
| 8 | Tạo Custom Conversions trên Meta | P1 | ⬜ |
| 9 | Cài TikTok Pixel qua GTM | P1 | ⬜ |
| 10 | Xác minh Google Search Console | P0 | ⬜ |
| 11 | Submit Sitemaps | P0 | ⬜ |
| 12 | Cài Microsoft Clarity | P2 | ⬜ |
| 13 | Tạo Funnel Exploration trong GA4 | P1 | ⬜ |
| 14 | Test tất cả events bằng GA4 DebugView | P0 | ⬜ |
| 15 | Test FB Pixel bằng Meta Pixel Helper | P1 | ⬜ |
| 16 | Setup UTM quy ước cho team | P1 | ⬜ |

---

*🔧 Tracking Setup Guide — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Người thực hiện: Digital Marketing Team*
*Tham chiếu: [KPIs Dashboard](kpis-dashboard.md) | [OKRs Q1](okrs-q1.md)*

