# 📊 TRACKING & ANALYTICS — XIAOMI247.COM

*Phiên bản: v1.0 | Ngày tạo: 21/03/2026*
*Platform: WordPress + WooCommerce | Domain: xiaomi247.com*
*GA Tracking ID: G-JM11GNEF22*

---

## Mục lục

1. [Google Tag Manager (GTM)](#1-google-tag-manager-gtm)
2. [GA4 Enhanced E-commerce](#2-ga4-enhanced-e-commerce)
3. [Facebook Pixel](#3-facebook-pixel)
4. [TikTok Pixel](#4-tiktok-pixel)
5. [Google Search Console](#5-google-search-console)
6. [Bing Webmaster Tools](#6-bing-webmaster-tools)
7. [Conversion Goals & Funnel](#7-conversion-goals--funnel)
8. [UptimeRobot Monitoring](#8-uptimerobot-monitoring)
9. [Testing & Debugging](#9-testing--debugging)

---

## 1. Google Tag Manager (GTM)

### 1.1 Tạo Account & Container

1. Truy cập [tagmanager.google.com](https://tagmanager.google.com)
2. Tạo **Account mới:**
   - **Account Name:** Xiaomi247
   - **Country:** Việt Nam
3. Tạo **Container:**
   - **Container name:** xiaomi247.com
   - **Target platform:** Web
4. Lưu lại **GTM ID** (dạng `GTM-XXXXXXX`)

### 1.2 Cài GTM Container trên WordPress

**Cách 1 — Plugin GTM4WP (Khuyên dùng):**

1. WordPress Admin → Plugins → Add New → Tìm **"GTM4WP"**
2. Cài đặt & Kích hoạt plugin
3. Settings → Google Tag Manager:
   - **Container ID:** `GTM-XXXXXXX`
   - **Container code placement:** Codeless injection (recommended)
4. Tab **Integration** → Bật **WooCommerce** integration
5. Lưu Settings

**Cách 2 — Chèn thủ công:**

Thêm vào `<head>` (qua theme header hoặc plugin Insert Headers & Footers):

```html
<!-- Google Tag Manager -->
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-XXXXXXX');</script>
<!-- End Google Tag Manager -->
```

Thêm ngay sau `<body>`:

```html
<!-- Google Tag Manager (noscript) -->
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-XXXXXXX"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<!-- End Google Tag Manager (noscript) -->
```

### 1.3 Cấu hình Built-in Variables

GTM → Variables → Configure Built-In Variables → Bật:

| Nhóm | Variables cần bật |
| --- | --- |
| Pages | Page URL, Page Path, Page Hostname, Page Title, Referrer |
| Clicks | Click Element, Click Classes, Click ID, Click URL, Click Text |
| Forms | Form Element, Form Classes, Form ID, Form URL, Form Text |
| Utilities | Event, Container ID, Container Version, Debug Mode |

### 1.4 Tạo User-Defined Variables (Data Layer)

GTM → Variables → User-Defined Variables → New:

| Variable Name | Type | Data Layer Variable Name | Dùng cho |
| --- | --- | --- | --- |
| dlv - ecommerce.items | Data Layer Variable | ecommerce.items | GA4 Ecommerce items |
| dlv - ecommerce.value | Data Layer Variable | ecommerce.value | Transaction value |
| dlv - ecommerce.transaction_id | Data Layer Variable | ecommerce.transaction_id | Order ID |
| dlv - ecommerce.currency | Data Layer Variable | ecommerce.currency | Luôn = VND |
| dlv - ecommerce.shipping | Data Layer Variable | ecommerce.shipping | Phí ship |
| dlv - ecommerce.tax | Data Layer Variable | ecommerce.tax | Thuế |
| dlv - ecommerce.item_list_name | Data Layer Variable | ecommerce.item_list_name | Tên danh mục |
| dlv - ecommerce.payment_type | Data Layer Variable | ecommerce.payment_type | Phương thức TT |
| dlv - ecommerce.shipping_tier | Data Layer Variable | ecommerce.shipping_tier | Hình thức ship |

### 1.5 Cấu hình Triggers

| # | Trigger Name | Type | Điều kiện | Dùng cho |
| --- | --- | --- | --- | --- |
| 1 | All Pages | Page View | Tất cả trang | GA4 Config, FB/TikTok Base |
| 2 | CE - view_item | Custom Event | Event = view_item | Xem sản phẩm |
| 3 | CE - view_item_list | Custom Event | Event = view_item_list | Xem danh mục |
| 4 | CE - select_item | Custom Event | Event = select_item | Click sản phẩm |
| 5 | CE - add_to_cart | Custom Event | Event = add_to_cart | Thêm giỏ hàng |
| 6 | CE - remove_from_cart | Custom Event | Event = remove_from_cart | Xóa khỏi giỏ |
| 7 | CE - view_cart | Custom Event | Event = view_cart | Xem giỏ hàng |
| 8 | CE - begin_checkout | Custom Event | Event = begin_checkout | Bắt đầu checkout |
| 9 | CE - add_shipping_info | Custom Event | Event = add_shipping_info | Nhập shipping |
| 10 | CE - add_payment_info | Custom Event | Event = add_payment_info | Chọn thanh toán |
| 11 | CE - purchase | Custom Event | Event = purchase | Mua hàng thành công |
| 12 | CE - refund | Custom Event | Event = refund | Hoàn tiền |
| 13 | Click - Phone | Click - Just Links | Click URL contains "tel:" | Click SĐT |
| 14 | Click - Zalo | Click - All Elements | Click URL contains "zalo.me" | Click Zalo |
| 15 | Form Submission | Form Submission | Tất cả forms | Gửi form |

### 1.6 Cấu hình Tags

| # | Tag Name | Tag Type | Trigger | Cấu hình |
| --- | --- | --- | --- | --- |
| 1 | GA4 - Configuration | Google Tag | All Pages | Measurement ID: `G-JM11GNEF22` |
| 2 | GA4 - view_item | GA4 Event | CE - view_item | Event: view_item, Ecommerce: true |
| 3 | GA4 - view_item_list | GA4 Event | CE - view_item_list | Event: view_item_list, Ecommerce: true |
| 4 | GA4 - select_item | GA4 Event | CE - select_item | Event: select_item, Ecommerce: true |
| 5 | GA4 - add_to_cart | GA4 Event | CE - add_to_cart | Event: add_to_cart, Ecommerce: true |
| 6 | GA4 - remove_from_cart | GA4 Event | CE - remove_from_cart | Event: remove_from_cart, Ecommerce: true |
| 7 | GA4 - view_cart | GA4 Event | CE - view_cart | Event: view_cart, Ecommerce: true |
| 8 | GA4 - begin_checkout | GA4 Event | CE - begin_checkout | Event: begin_checkout, Ecommerce: true |
| 9 | GA4 - add_shipping_info | GA4 Event | CE - add_shipping_info | Event: add_shipping_info, Ecommerce: true |
| 10 | GA4 - add_payment_info | GA4 Event | CE - add_payment_info | Event: add_payment_info, Ecommerce: true |
| 11 | GA4 - purchase | GA4 Event | CE - purchase | Event: purchase, Ecommerce: true |
| 12 | GA4 - refund | GA4 Event | CE - refund | Event: refund, Ecommerce: true |
| 13 | GA4 - phone_click | GA4 Event | Click - Phone | Event: phone_click |
| 14 | GA4 - zalo_click | GA4 Event | Click - Zalo | Event: zalo_click |

## 2. GA4 Enhanced E-commerce

### 2.1 Plugin Setup — GTM4WP

1. WordPress Admin → Settings → Google Tag Manager
2. Tab **Integration** → Bật **WooCommerce**
3. Tick tất cả tracking options:
   - ✅ Track enhanced ecommerce
   - ✅ Product impressions on product listing pages
   - ✅ Product clicks on product listing pages
   - ✅ Product detail views
   - ✅ Add to cart events
   - ✅ Remove from cart events
   - ✅ Checkout steps
   - ✅ Purchases

### 2.2 Event Mapping Chi Tiết

#### 📦 `view_item` — Xem trang sản phẩm

- **Trigger:** User mở trang chi tiết sản phẩm
- **GTM Trigger:** Custom Event = `view_item`
- **Parameters:**

| Parameter | Giá trị | Ví dụ |
| --- | --- | --- |
| currency | VND | VND |
| value | Giá sản phẩm | 6990000 |
| items[].item_id | SKU sản phẩm | `RN14P-8-256-BLK` |
| items[].item_name | Tên sản phẩm | `Redmi Note 14 Pro` |
| items[].price | Giá | 6990000 |
| items[].item_category | Danh mục | `Điện thoại` |
| items[].item_category2 | Danh mục con | `Redmi` |
| items[].item_brand | Thương hiệu | `Xiaomi` |

**Data Layer format:**

```javascript
dataLayer.push({
  event: "view_item",
  ecommerce: {
    currency: "VND",
    value: 6990000,
    items: [{
      item_id: "RN14P-8-256-BLK",
      item_name: "Redmi Note 14 Pro",
      price: 6990000,
      item_category: "Điện thoại",
      item_category2: "Redmi",
      item_brand: "Xiaomi",
      quantity: 1
    }]
  }
});
```

#### 📋 `view_item_list` — Xem danh mục sản phẩm

- **Trigger:** User mở trang danh mục (category page) hoặc trang tìm kiếm
- **GTM Trigger:** Custom Event = `view_item_list`
- **Parameters:**

| Parameter | Giá trị | Ví dụ |
| --- | --- | --- |
| item_list_id | ID danh mục | `dien-thoai` |
| item_list_name | Tên danh mục | `Điện thoại` |
| items[] | Mảng sản phẩm hiển thị | (tối đa 10-20 items) |

**Data Layer format:**

```javascript
dataLayer.push({
  event: "view_item_list",
  ecommerce: {
    item_list_id: "dien-thoai",
    item_list_name: "Điện thoại",
    items: [
      { item_id: "RN14P", item_name: "Redmi Note 14 Pro", price: 6990000, index: 0 },
      { item_id: "RN14", item_name: "Redmi Note 14", price: 4990000, index: 1 }
    ]
  }
});
```

#### 👆 `select_item` — Click chọn sản phẩm từ danh sách

- **Trigger:** User click vào 1 sản phẩm trong danh mục/search results
- **GTM Trigger:** Custom Event = `select_item`
- **Parameters:**

| Parameter | Giá trị |
| --- | --- |
| item_list_id | ID danh mục nguồn |
| item_list_name | Tên danh mục nguồn |
| items[] | Sản phẩm được click (1 item) |

**Data Layer format:**

```javascript
dataLayer.push({
  event: "select_item",
  ecommerce: {
    item_list_id: "dien-thoai",
    item_list_name: "Điện thoại",
    items: [{ item_id: "RN14P", item_name: "Redmi Note 14 Pro", price: 6990000, index: 0 }]
  }
});
```

#### 🛒 `add_to_cart` — Thêm vào giỏ hàng

- **Trigger:** User click nút "Thêm vào giỏ" hoặc "Mua ngay"
- **GTM Trigger:** Custom Event = `add_to_cart`
- **Parameters:**

| Parameter | Giá trị | Ví dụ |
| --- | --- | --- |
| currency | VND | VND |
| value | Giá × Số lượng | 6990000 |
| items[].item_id | SKU | `RN14P-8-256-BLK` |
| items[].item_name | Tên SP | `Redmi Note 14 Pro` |
| items[].price | Giá đơn vị | 6990000 |
| items[].quantity | Số lượng thêm | 1 |

**Data Layer format:**

```javascript
dataLayer.push({
  event: "add_to_cart",
  ecommerce: {
    currency: "VND",
    value: 6990000,
    items: [{
      item_id: "RN14P-8-256-BLK",
      item_name: "Redmi Note 14 Pro",
      price: 6990000,
      item_brand: "Xiaomi",
      item_category: "Điện thoại",
      quantity: 1
    }]
  }
});
```

#### ❌ `remove_from_cart` — Xóa khỏi giỏ hàng

- **Trigger:** User click nút xóa sản phẩm trong giỏ hàng
- **GTM Trigger:** Custom Event = `remove_from_cart`
- **Data Layer format:** Tương tự `add_to_cart` nhưng event = `remove_from_cart`

#### 👁️ `view_cart` — Xem giỏ hàng

- **Trigger:** User mở trang giỏ hàng `/gio-hang/`
- **GTM Trigger:** Custom Event = `view_cart`
- **Parameters:** currency, value, items[] (tất cả SP trong giỏ)

**Data Layer format:**

```javascript
dataLayer.push({
  event: "view_cart",
  ecommerce: {
    currency: "VND",
    value: 13980000,
    items: [
      { item_id: "RN14P", item_name: "Redmi Note 14 Pro", price: 6990000, quantity: 2 }
    ]
  }
});
```

#### 🏁 `begin_checkout` — Bắt đầu thanh toán

- **Trigger:** User chuyển sang trang checkout `/thanh-toan/`
- **GTM Trigger:** Custom Event = `begin_checkout`
- **Parameters:** currency, value, items[], coupon (nếu có)

**Data Layer format:**

```javascript
dataLayer.push({
  event: "begin_checkout",
  ecommerce: {
    currency: "VND",
    value: 13980000,
    coupon: "GIAM10",
    items: [
      { item_id: "RN14P", item_name: "Redmi Note 14 Pro", price: 6990000, quantity: 2 }
    ]
  }
});
```

#### 🚚 `add_shipping_info` — Nhập thông tin giao hàng

- **Trigger:** User hoàn tất nhập địa chỉ giao hàng
- **GTM Trigger:** Custom Event = `add_shipping_info`
- **Parameters:**

| Parameter | Giá trị | Ví dụ |
| --- | --- | --- |
| currency | VND | VND |
| value | Tổng giá trị | 13980000 |
| shipping_tier | Hình thức ship | `Giao hàng nhanh` |
| items[] | Danh sách SP | (tất cả SP) |

**Data Layer format:**

```javascript
dataLayer.push({
  event: "add_shipping_info",
  ecommerce: {
    currency: "VND",
    value: 13980000,
    shipping_tier: "Giao hàng nhanh",
    items: [{ item_id: "RN14P", item_name: "Redmi Note 14 Pro", price: 6990000, quantity: 2 }]
  }
});
```

#### 💳 `add_payment_info` — Chọn phương thức thanh toán

- **Trigger:** User chọn phương thức thanh toán (COD, chuyển khoản, v.v.)
- **GTM Trigger:** Custom Event = `add_payment_info`
- **Parameters:**

| Parameter | Giá trị | Ví dụ |
| --- | --- | --- |
| currency | VND | VND |
| value | Tổng giá trị | 13980000 |
| payment_type | Phương thức TT | `COD` / `Bank Transfer` / `Momo` |
| items[] | Danh sách SP | (tất cả SP) |

**Data Layer format:**

```javascript
dataLayer.push({
  event: "add_payment_info",
  ecommerce: {
    currency: "VND",
    value: 13980000,
    payment_type: "COD",
    items: [{ item_id: "RN14P", item_name: "Redmi Note 14 Pro", price: 6990000, quantity: 2 }]
  }
});
```

#### ✅ `purchase` — Hoàn tất đơn hàng

- **Trigger:** User đặt hàng thành công, chuyển đến trang "Thank you" / Order Received
- **GTM Trigger:** Custom Event = `purchase`
- **Parameters:**

| Parameter | Giá trị | Ví dụ |
| --- | --- | --- |
| transaction_id | Mã đơn hàng | `ORD-20260321-001` |
| value | Tổng giá trị | 13980000 |
| tax | Thuế | 0 |
| shipping | Phí ship | 30000 |
| currency | VND | VND |
| coupon | Mã giảm giá | `GIAM10` |
| items[] | Danh sách SP | (tất cả SP đã mua) |

**Data Layer format:**

```javascript
dataLayer.push({
  event: "purchase",
  ecommerce: {
    transaction_id: "ORD-20260321-001",
    value: 13980000,
    tax: 0,
    shipping: 30000,
    currency: "VND",
    coupon: "GIAM10",
    items: [{
      item_id: "RN14P-8-256-BLK",
      item_name: "Redmi Note 14 Pro",
      price: 6990000,
      item_brand: "Xiaomi",
      item_category: "Điện thoại",
      quantity: 2
    }]
  }
});
```

#### 🔄 `refund` — Hoàn tiền

- **Trigger:** Admin xử lý hoàn tiền trong WooCommerce
- **GTM Trigger:** Custom Event = `refund`
- **Parameters:**

| Parameter | Giá trị | Ví dụ |
| --- | --- | --- |
| transaction_id | Mã đơn hàng gốc | `ORD-20260321-001` |
| value | Số tiền hoàn | 6990000 |
| currency | VND | VND |
| items[] | SP bị hoàn (partial refund) | (optional) |

**Data Layer format:**

```javascript
dataLayer.push({
  event: "refund",
  ecommerce: {
    transaction_id: "ORD-20260321-001",
    value: 6990000,
    currency: "VND"
  }
});
```

### 2.3 Custom Events bổ sung

| Event | Mô tả | Trigger | Parameters |
| --- | --- | --- | --- |
| `phone_click` | Click số điện thoại | Click link `tel:` | link_url |
| `zalo_click` | Click chat Zalo | Click nút Zalo | link_url |
| `form_submit` | Gửi form liên hệ | Form submission | form_id, form_name |
| `promotion_click` | Click banner KM | Click banner promo | promotion_id, promotion_name |
| `search` | Tìm kiếm SP | Dùng search box | search_term |

### 2.4 Đánh dấu Conversions trong GA4

GA4 → Admin → Events → Mark as conversion:

- ✅ `purchase` — Mua hàng thành công
- ✅ `add_to_cart` — Thêm giỏ hàng
- ✅ `begin_checkout` — Bắt đầu checkout
- ✅ `phone_click` — Click số điện thoại
- ✅ `zalo_click` — Click chat Zalo
- ✅ `form_submit` — Gửi form liên hệ

---

## 3. Facebook Pixel

### 3.1 Tạo Pixel

1. Truy cập [Meta Events Manager](https://business.facebook.com/events_manager)
2. Chọn **Connect Data Sources** → **Web** → **Facebook Pixel**
3. Đặt tên: **Xiaomi247 Pixel**
4. Nhập URL: `https://xiaomi247.com`
5. Lưu lại **Pixel ID** (16 chữ số)

### 3.2 Cài Facebook Pixel qua GTM

**Tạo Tag trong GTM:**

Tag Name: `FB Pixel - Base Code`
Tag Type: Custom HTML
Trigger: All Pages

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
fbq('init', 'YOUR_PIXEL_ID');
fbq('track', 'PageView');
</script>
<noscript><img height="1" width="1" style="display:none"
src="https://www.facebook.com/tr?id=YOUR_PIXEL_ID&ev=PageView&noscript=1"/></noscript>
<!-- End Facebook Pixel Code -->
```

> ⚠️ Thay `YOUR_PIXEL_ID` bằng Pixel ID thực tế (16 chữ số)

### 3.3 Event Tracking qua GTM

Tạo thêm các Tags cho từng event:

#### Tag: `FB Pixel - ViewContent`
- **Trigger:** CE - view_item
- **Code:**

```html
<script>
fbq('track', 'ViewContent', {
  content_ids: [{{dlv - ecommerce.items}}.map(i => i.item_id)],
  content_name: {{dlv - ecommerce.items}}[0].item_name,
  content_type: 'product',
  value: {{dlv - ecommerce.value}},
  currency: 'VND'
});
</script>
```

#### Tag: `FB Pixel - AddToCart`
- **Trigger:** CE - add_to_cart
- **Code:**

```html
<script>
fbq('track', 'AddToCart', {
  content_ids: [{{dlv - ecommerce.items}}.map(i => i.item_id)],
  content_name: {{dlv - ecommerce.items}}[0].item_name,
  content_type: 'product',
  value: {{dlv - ecommerce.value}},
  currency: 'VND'
});
</script>
```

#### Tag: `FB Pixel - InitiateCheckout`
- **Trigger:** CE - begin_checkout
- **Code:**

```html
<script>
fbq('track', 'InitiateCheckout', {
  content_ids: {{dlv - ecommerce.items}}.map(i => i.item_id),
  num_items: {{dlv - ecommerce.items}}.length,
  value: {{dlv - ecommerce.value}},
  currency: 'VND'
});
</script>
```

#### Tag: `FB Pixel - Purchase`
- **Trigger:** CE - purchase
- **Code:**

```html
<script>
fbq('track', 'Purchase', {
  content_ids: {{dlv - ecommerce.items}}.map(i => i.item_id),
  content_type: 'product',
  value: {{dlv - ecommerce.value}},
  currency: 'VND',
  order_id: {{dlv - ecommerce.transaction_id}}
});
</script>
```

### 3.4 Custom Audiences

Tạo trong Meta Events Manager → Custom Audiences:

| Tên Audience | Điều kiện | Retention | Dùng cho |
| --- | --- | --- | --- |
| Website Visitors 30d | Tất cả PageView | 30 ngày | Retargeting chung |
| Product Viewers 14d | ViewContent event | 14 ngày | Retargeting sản phẩm |
| Add to Cart 7d | AddToCart event | 7 ngày | Retargeting giỏ hàng bỏ dở |
| Purchasers 180d | Purchase event | 180 ngày | Lookalike + Upsell |
| Checkout Abandoned 7d | InitiateCheckout NOT Purchase | 7 ngày | Recovery campaign |

### 3.5 Conversions API (CAPI)

- Cài đặt CAPI qua plugin **PixelYourSite Pro** hoặc **Facebook for WooCommerce**
- Mục đích: Gửi server-side events để tăng accuracy (do iOS 14+ block cookies)
- Events cần gửi qua CAPI: Purchase, AddToCart, InitiateCheckout
- Cấu hình **Event Deduplication** để tránh đếm trùng browser + server events

---

## 4. TikTok Pixel

### 4.1 Tạo Pixel

1. Truy cập [TikTok Ads Manager](https://ads.tiktok.com)
2. **Assets** → **Events** → **Web Events** → **Create Pixel**
3. Đặt tên: **Xiaomi247 Pixel**
4. Chọn **Manually Install Pixel Code**
5. Lưu lại **Pixel ID**

### 4.2 Cài TikTok Pixel qua GTM

**Tạo Tag trong GTM:**

Tag Name: `TikTok Pixel - Base Code`
Tag Type: Custom HTML
Trigger: All Pages

```html
<!-- TikTok Pixel Code -->
<script>
!function (w, d, t) {
  w.TiktokAnalyticsObject=t;var ttq=w[t]=w[t]||[];ttq.methods=["page","track","identify","instances","debug","on","off","once","ready","alias","group","enableCookie","disableCookie"],ttq.setAndDefer=function(t,e){t[e]=function(){t.push([e].concat(Array.prototype.slice.call(arguments,0)))}};for(var i=0;i<ttq.methods.length;i++)ttq.setAndDefer(ttq,ttq.methods[i]);ttq.instance=function(t){for(var e=ttq._i[t]||[],n=0;n<ttq.methods.length;n++)ttq.setAndDefer(e,ttq.methods[n]);return e};ttq.load=function(e,n){var i="https://analytics.tiktok.com/i18n/pixel/events.js";ttq._i=ttq._i||{},ttq._i[e]=[],ttq._i[e]._u=i,ttq._t=ttq._t||{},ttq._t[e]=+new Date,ttq._o=ttq._o||{},ttq._o[e]=n||{};var o=document.createElement("script");o.type="text/javascript",o.async=!0,o.src=i+"?sdkid="+e+"&lib="+t;var a=document.getElementsByTagName("script")[0];a.parentNode.insertBefore(o,a)};
  ttq.load('YOUR_TIKTOK_PIXEL_ID');
  ttq.page();
}(window, document, 'ttq');
</script>
<!-- End TikTok Pixel Code -->
```

> ⚠️ Thay `YOUR_TIKTOK_PIXEL_ID` bằng Pixel ID thực tế

### 4.3 Event Tracking qua GTM

| Event TikTok | Trigger GTM | Parameters | Tương đương FB |
| --- | --- | --- | --- |
| `ViewContent` | CE - view_item | content_id, content_name, content_type, price, currency | ViewContent |
| `AddToCart` | CE - add_to_cart | content_id, content_name, price, quantity, currency | AddToCart |
| `PlaceAnOrder` | CE - begin_checkout | content_id, content_name, price, quantity, currency | InitiateCheckout |
| `CompletePayment` | CE - purchase | content_id, value, currency | Purchase |
| `Search` | Search event | query | Search |

**Ví dụ Tag — TikTok ViewContent:**

```html
<script>
ttq.track('ViewContent', {
  content_id: {{dlv - ecommerce.items}}[0].item_id,
  content_name: {{dlv - ecommerce.items}}[0].item_name,
  content_type: 'product',
  price: {{dlv - ecommerce.value}},
  currency: 'VND'
});
</script>
```

**Ví dụ Tag — TikTok CompletePayment:**

```html
<script>
ttq.track('CompletePayment', {
  content_id: {{dlv - ecommerce.items}}.map(i => i.item_id).join(','),
  value: {{dlv - ecommerce.value}},
  currency: 'VND'
});
</script>
```

---

## 5. Google Search Console

### 5.1 Đăng ký & Xác minh

1. Truy cập [search.google.com/search-console](https://search.google.com/search-console)
2. Click **Add Property**
3. Chọn **URL prefix** → Nhập: `https://xiaomi247.com`
4. **Xác minh quyền sở hữu** (chọn 1 trong các cách):

| Phương pháp | Cách thực hiện | Khuyên dùng |
| --- | --- | --- |
| HTML tag | Thêm meta tag qua Yoast SEO → Webmaster Tools | ✅ Dễ nhất |
| Google Analytics | Tự động nếu GA4 đã cài trên site | ✅ Nhanh |
| Google Tag Manager | Tự động nếu GTM đã cài trên site | ✅ Nhanh |
| DNS record | Thêm TXT record tại nhà cung cấp domain | Phức tạp hơn |
| HTML file | Upload file xác minh lên root website | OK |

5. Thêm cả phiên bản `https://www.xiaomi247.com` (nếu có redirect)

### 5.2 Submit Sitemap

1. Google Search Console → **Sitemaps** (menu trái)
2. Nhập URL sitemap và Submit:

| Sitemap URL | Nội dung |
| --- | --- |
| `https://xiaomi247.com/sitemap_index.xml` | Sitemap tổng (Yoast SEO tự tạo) |
| `https://xiaomi247.com/product-sitemap.xml` | Tất cả sản phẩm WooCommerce |
| `https://xiaomi247.com/category-sitemap.xml` | Tất cả danh mục |
| `https://xiaomi247.com/post-sitemap.xml` | Bài viết blog/tin tức |
| `https://xiaomi247.com/page-sitemap.xml` | Các trang tĩnh |

### 5.3 Monitor Indexing

Theo dõi thường xuyên (hàng tuần):

| Mục | Đường dẫn | Theo dõi gì |
| --- | --- | --- |
| **Performance** | Search Console → Performance | Clicks, Impressions, CTR, Position theo keyword |
| **Pages** | Search Console → Pages | Trang nào đã index, lỗi crawl, warnings |
| **Core Web Vitals** | Search Console → Core Web Vitals | LCP, FID/INP, CLS trên mobile & desktop |
| **Mobile Usability** | Search Console → Mobile Usability | Lỗi hiển thị trên mobile |
| **Links** | Search Console → Links | Backlinks, internal links |
| **Manual Actions** | Search Console → Security & Manual Actions | Có bị Google phạt không |

---

## 6. Bing Webmaster Tools

### 6.1 Đăng ký

1. Truy cập [bing.com/webmasters](https://www.bing.com/webmasters)
2. Đăng nhập bằng tài khoản Microsoft

### 6.2 Import từ Google Search Console

1. Chọn **Import from Google Search Console** (cách nhanh nhất)
2. Đăng nhập Google → Cho phép Bing truy cập
3. Chọn property `https://xiaomi247.com`
4. Bing sẽ tự động:
   - ✅ Xác minh domain
   - ✅ Import sitemaps
   - ✅ Bắt đầu crawl

### 6.3 Cấu hình thêm

- Submit sitemap thủ công nếu cần: `https://xiaomi247.com/sitemap_index.xml`
- Kiểm tra **URL Inspection** cho các trang quan trọng
- Theo dõi **Search Performance** trên Bing
- Thiết lập **Email Alerts** cho lỗi crawl

> 💡 Bing chiếm ~5-8% thị phần search tại VN. Cài đặt đơn giản, không tốn thời gian, nhưng có thêm traffic miễn phí.

---

## 7. Conversion Goals & Funnel

### 7.1 Conversion Goals trong GA4

GA4 → Admin → Events → Đánh dấu events sau là **Key Events (Conversions):**

| Event | Loại | Giá trị |
| --- | --- | --- |
| `purchase` | E-commerce | Dynamic (= transaction value) |
| `add_to_cart` | E-commerce | Dynamic (= item value) |
| `begin_checkout` | Engagement | Dynamic |
| `phone_click` | Lead | Ước tính 100.000đ |
| `zalo_click` | Lead | Ước tính 80.000đ |
| `form_submit` | Lead | Ước tính 50.000đ |

### 7.2 Funnel Visualization trong GA4

Tạo **Funnel Exploration** trong GA4 → Explore → Funnel Exploration:

**E-commerce Purchase Funnel:**

```
Step 1: view_item          → "Xem sản phẩm"
    ↓ (target: ≥ 30% chuyển sang step 2)
Step 2: add_to_cart        → "Thêm giỏ hàng"
    ↓ (target: ≥ 60% chuyển sang step 3)
Step 3: begin_checkout     → "Bắt đầu checkout"
    ↓ (target: ≥ 70% chuyển sang step 4)
Step 4: add_shipping_info  → "Nhập địa chỉ giao hàng"
    ↓ (target: ≥ 85% chuyển sang step 5)
Step 5: add_payment_info   → "Chọn phương thức thanh toán"
    ↓ (target: ≥ 90% chuyển sang step 6)
Step 6: purchase           → "Hoàn tất đơn hàng"
```

**Cấu hình:**
1. GA4 → Explore → Create new exploration → **Funnel exploration**
2. Tab Settings:
   - **Technique:** Funnel exploration
   - **Make open funnel:** ✅ (cho phép user vào từ bất kỳ step nào)
3. Tab Steps: Thêm 6 steps như trên
4. **Breakdown:** Thêm dimension `Device category` để so sánh mobile vs desktop
5. **Segments:** So sánh giữa các nguồn traffic (Organic, Paid, Social)

### 7.3 UTM Parameters — Quy ước chuẩn

| Parameter | Quy ước | Ví dụ |
| --- | --- | --- |
| `utm_source` | Tên platform (lowercase) | facebook, google, tiktok, zalo |
| `utm_medium` | Loại traffic | cpc, social, email, referral, organic |
| `utm_campaign` | Tên chiến dịch (slug) | redmi-note-14-launch, sale-thang4 |
| `utm_content` | Nội dung/ad cụ thể | banner-hero, post-review, video-unbox |
| `utm_term` | Từ khóa (cho search ads) | mua-xiaomi-chinh-hang |

**Ví dụ URL hoàn chỉnh:**

```
https://xiaomi247.com/san-pham/redmi-note-14-pro?utm_source=facebook&utm_medium=cpc&utm_campaign=redmi-note-14-launch&utm_content=carousel-ad-1
```

---

## 8. UptimeRobot Monitoring

### 8.1 Đăng ký & Setup

1. Truy cập [uptimerobot.com](https://uptimerobot.com)
2. Đăng ký tài khoản miễn phí (Free plan: 50 monitors, check mỗi 5 phút)
3. Click **Add New Monitor**

### 8.2 Cấu hình Monitors

| # | Monitor Name | Type | URL / Host | Interval | Alert |
| --- | --- | --- | --- | --- | --- |
| 1 | Xiaomi247 - Homepage | HTTP(s) | `https://xiaomi247.com` | 5 phút | Email + Telegram |
| 2 | Xiaomi247 - Shop Page | HTTP(s) | `https://xiaomi247.com/cua-hang/` | 5 phút | Email |
| 3 | Xiaomi247 - Checkout | HTTP(s) | `https://xiaomi247.com/thanh-toan/` | 5 phút | Email + Telegram |
| 4 | Xiaomi247 - SSL | HTTP(s) | `https://xiaomi247.com` | 5 phút | Email |
| 5 | Xiaomi247 - Keyword | Keyword | `https://xiaomi247.com` → "Xiaomi" | 5 phút | Email |

### 8.3 Alert Contacts

Cấu hình thông báo khi website down:

| Kênh | Cấu hình | Khi nào dùng |
| --- | --- | --- |
| **Email** | Email admin + dev team | Luôn bật |
| **Telegram Bot** | Tạo bot → Webhook URL | Thông báo realtime |
| **Slack** | Webhook integration | Nếu team dùng Slack |

### 8.4 Status Page (Optional)

- Tạo Public Status Page: `status.xiaomi247.com`
- Hiển thị uptime history cho khách hàng
- Tăng độ tin cậy cho website

---

## 9. Testing & Debugging

### 9.1 GA4 DebugView

**Cách bật:**

1. Cài extension [Google Analytics Debugger](https://chrome.google.com/webstore/detail/google-analytics-debugger) trên Chrome
2. Bật extension → Icon chuyển thành "ON"
3. Truy cập website xiaomi247.com
4. GA4 → Admin → DebugView

**Kiểm tra:**

| Bước test | Hành động | Event mong đợi | Parameters kiểm tra |
| --- | --- | --- | --- |
| 1 | Mở trang chủ | `page_view` | page_title, page_location |
| 2 | Mở danh mục Điện thoại | `view_item_list` | item_list_name, items[] |
| 3 | Click vào 1 sản phẩm | `select_item` → `view_item` | item_id, item_name, price |
| 4 | Click "Thêm vào giỏ" | `add_to_cart` | item_id, quantity, value |
| 5 | Mở giỏ hàng | `view_cart` | items[], value |
| 6 | Click "Thanh toán" | `begin_checkout` | items[], value |
| 7 | Nhập địa chỉ | `add_shipping_info` | shipping_tier |
| 8 | Chọn COD | `add_payment_info` | payment_type = "COD" |
| 9 | Đặt hàng | `purchase` | transaction_id, value, items[] |

### 9.2 Facebook Pixel Helper

**Cách dùng:**

1. Cài extension [Meta Pixel Helper](https://chrome.google.com/webstore/detail/meta-pixel-helper) trên Chrome
2. Truy cập xiaomi247.com
3. Click icon Pixel Helper → Kiểm tra:

| Kiểm tra | Kết quả mong đợi |
| --- | --- |
| Trang chủ | ✅ PageView event fired |
| Trang sản phẩm | ✅ PageView + ViewContent |
| Click "Thêm giỏ hàng" | ✅ AddToCart với content_ids + value |
| Trang checkout | ✅ InitiateCheckout với num_items + value |
| Đặt hàng thành công | ✅ Purchase với value + order_id |

**Lỗi thường gặp:**
- ❌ "Pixel did not load" → Kiểm tra GTM tag có fire không
- ❌ "No PageView event" → Base pixel code chưa cài đúng
- ❌ "Duplicate pixels" → Kiểm tra không cài pixel cả qua GTM lẫn plugin

### 9.3 GTM Preview Mode

**Cách dùng:**

1. GTM → Click **Preview** (góc trên phải)
2. Nhập URL: `https://xiaomi247.com` → Connect
3. Tag Assistant sẽ mở trong tab mới
4. Duyệt website bình thường → Kiểm tra:

| Mục kiểm tra | Cách kiểm tra |
| --- | --- |
| Tags Fired | Click vào event → Xem tags nào đã fire |
| Tags Not Fired | Kiểm tra trigger conditions |
| Data Layer | Tab "Data Layer" → Xem giá trị variables |
| Variables | Tab "Variables" → Kiểm tra giá trị đúng/sai |
| Errors | Tab "Errors" → Fix lỗi JavaScript |

**Workflow test trong GTM Preview:**

1. Mở Preview → Truy cập trang sản phẩm
2. Kiểm tra: `view_item` event xuất hiện → GA4 tag + FB ViewContent tag fired
3. Click "Thêm vào giỏ"
4. Kiểm tra: `add_to_cart` event → GA4 + FB AddToCart + TikTok AddToCart fired
5. Tiến hành checkout → purchase
6. Kiểm tra tất cả tags fire đúng thứ tự

### 9.4 TikTok Pixel Helper

**Cách dùng:**

1. Cài extension [TikTok Pixel Helper](https://chrome.google.com/webstore/detail/tiktok-pixel-helper) trên Chrome
2. Truy cập website → Kiểm tra tương tự Facebook Pixel Helper
3. Đảm bảo các event fire đúng:
   - `PageView` trên mọi trang
   - `ViewContent` trên trang sản phẩm
   - `AddToCart` khi thêm giỏ
   - `PlaceAnOrder` khi checkout
   - `CompletePayment` khi mua thành công

### 9.5 Checklist Kiểm Tra Tổng Hợp

| # | Hạng mục | Công cụ kiểm tra | Status |
| --- | --- | --- | --- |
| 1 | GTM container load đúng | GTM Preview Mode | ⬜ |
| 2 | GA4 page_view fire trên mọi trang | GA4 DebugView | ⬜ |
| 3 | GA4 E-commerce events đầy đủ | GA4 DebugView | ⬜ |
| 4 | GA4 Conversions được đánh dấu | GA4 Admin → Events | ⬜ |
| 5 | Facebook PageView fire | Meta Pixel Helper | ⬜ |
| 6 | Facebook E-commerce events | Meta Pixel Helper | ⬜ |
| 7 | Facebook CAPI gửi events | Events Manager → Test Events | ⬜ |
| 8 | TikTok PageView fire | TikTok Pixel Helper | ⬜ |
| 9 | TikTok E-commerce events | TikTok Pixel Helper | ⬜ |
| 10 | Google Search Console verified | Search Console | ⬜ |
| 11 | Sitemaps submitted | Search Console → Sitemaps | ⬜ |
| 12 | Bing Webmaster Tools imported | Bing Webmaster | ⬜ |
| 13 | UptimeRobot monitors active | UptimeRobot Dashboard | ⬜ |
| 14 | Funnel exploration tạo xong | GA4 → Explore | ⬜ |
| 15 | Không có duplicate pixels | Pixel Helper + DebugView | ⬜ |
| 16 | Events không fire 2 lần (dedup) | DebugView + Pixel Helper | ⬜ |

---

## 📋 Tham chiếu

| Tài liệu | Link |
| --- | --- |
| Tracking Setup Guide (chi tiết) | [marketing/06-measurement/tracking-setup-guide.md](../marketing/06-measurement/tracking-setup-guide.md) |
| KPIs Dashboard | [marketing/06-measurement/kpis-dashboard.md](../marketing/06-measurement/kpis-dashboard.md) |
| Technical Recommendations | [marketing/01-technical-audit/technical-recommendations.md](../marketing/01-technical-audit/technical-recommendations.md) |
| GA4 Documentation | [developers.google.com/analytics](https://developers.google.com/analytics) |
| GTM Documentation | [developers.google.com/tag-platform](https://developers.google.com/tag-platform) |
| Meta Pixel Docs | [developers.facebook.com/docs/meta-pixel](https://developers.facebook.com/docs/meta-pixel) |
| TikTok Pixel Docs | [ads.tiktok.com/help](https://ads.tiktok.com/help) |

---

*📊 Tracking & Analytics Guide — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | GA Tracking ID: G-JM11GNEF22*
*Người thực hiện: Digital Marketing & Dev Team*

