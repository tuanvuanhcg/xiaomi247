# ⚡ Tối ưu Performance & CDN — Xiaomi247.com

> **Ngày tạo:** 21/03/2026
> **Phiên bản:** 1.0
> **Áp dụng cho:** WordPress + WooCommerce + Motta Theme
> **Tham chiếu:** [Technical Recommendations](../marketing/01-technical-audit/technical-recommendations.md)

---

## Mục lục

1. [Cloudflare CDN Setup](#1-cloudflare-cdn-setup)
2. [Image Optimization](#2-image-optimization)
3. [CSS/JS Optimization](#3-cssjs-optimization)
4. [Browser Caching](#4-browser-caching)
5. [Web Vitals Targets](#5-web-vitals-targets)
6. [Đo lường Performance](#6-đo-lường-performance)
7. [Checklist tối ưu định kỳ](#7-checklist-tối-ưu-định-kỳ)

---

## 1. Cloudflare CDN Setup

### 1.1 Đăng ký & Trỏ DNS

**Bước 1 — Tạo tài khoản Cloudflare:**
1. Truy cập [dash.cloudflare.com](https://dash.cloudflare.com) → Đăng ký tài khoản miễn phí
2. Click **"Add a Site"** → Nhập `xiaomi247.com`
3. Chọn plan **Free** (đủ dùng cho giai đoạn đầu)

**Bước 2 — Trỏ DNS:**
1. Cloudflare sẽ scan DNS records hiện tại → Kiểm tra đầy đủ các record
2. Đảm bảo các record quan trọng:

| Type | Name | Value | Proxy |
| --- | --- | --- | --- |
| A | `@` | IP hosting | ☁️ Proxied |
| CNAME | `www` | `xiaomi247.com` | ☁️ Proxied |
| MX | `@` | Mail server | ❌ DNS only |
| TXT | `@` | SPF/DKIM records | ❌ DNS only |

3. Cập nhật nameservers tại nhà đăng ký domain:
   - Thay nameservers cũ bằng nameservers Cloudflare (vd: `xxx.ns.cloudflare.com`)
   - Chờ 24-48h để DNS propagate (thường nhanh hơn)

**Bước 3 — Xác nhận hoạt động:**
- Kiểm tra tại [dnschecker.org](https://dnschecker.org) → NS records đã trỏ về Cloudflare
- Truy cập website → Kiểm tra response header có `cf-ray` = Cloudflare đang hoạt động

### 1.2 Cấu hình SSL

| Cài đặt | Giá trị | Lý do |
| --- | --- | --- |
| **SSL/TLS Mode** | Full (Strict) | Mã hóa end-to-end, yêu cầu SSL cert hợp lệ trên hosting |
| **Always Use HTTPS** | ON | Redirect tất cả HTTP → HTTPS |
| **Automatic HTTPS Rewrites** | ON | Fix mixed content tự động |
| **HSTS** | ON (max-age: 6 tháng) | Bảo mật, SEO boost |
| **Minimum TLS Version** | TLS 1.2 | Bảo mật, loại bỏ TLS cũ |

> ⚠️ **Lưu ý:** Đảm bảo hosting đã cài SSL certificate (Let's Encrypt miễn phí) trước khi bật Full (Strict).

### 1.3 Tối ưu Performance trên Cloudflare

**Speed → Optimization:**

| Cài đặt | Giá trị | Ghi chú |
| --- | --- | --- |
| **Auto Minify** | ✅ CSS, JS, HTML | Giảm dung lượng file |
| **Brotli** | ✅ ON | Nén tốt hơn Gzip 15-20% |
| **Early Hints** | ✅ ON | Preload resources sớm hơn |
| **Rocket Loader** | ❌ OFF | Có thể conflict với WooCommerce JS |
| **Mirage** | ❌ OFF (Free plan không có) | Image lazy loading (Pro plan) |

> ⚠️ **Quan trọng:** KHÔNG bật Rocket Loader — thường gây lỗi JS trên WooCommerce (add to cart, checkout không hoạt động).

### 1.4 Page Rules (3 rules miễn phí)

Cấu hình theo thứ tự ưu tiên:

**Rule 1 — Bypass cache cho WooCommerce dynamic pages:**
```
URL: xiaomi247.com/cart/*
     xiaomi247.com/checkout/*
     xiaomi247.com/my-account/*
Settings:
  - Cache Level: Bypass
  - Disable Performance (tắt minify cho các trang này)
```

**Rule 2 — Cache everything cho static content:**
```
URL: xiaomi247.com/wp-content/*
Settings:
  - Cache Level: Cache Everything
  - Edge Cache TTL: 1 month
  - Browser Cache TTL: 1 year
```

**Rule 3 — Cache trang chủ & danh mục:**
```
URL: xiaomi247.com/*
Settings:
  - Cache Level: Standard
  - Browser Cache TTL: 4 hours
```

> 💡 **Mẹo:** Với Free plan chỉ có 3 Page Rules. Nếu cần thêm, nâng lên Pro ($20/tháng) hoặc dùng **Transform Rules** (miễn phí, không giới hạn).

### 1.5 Cấu hình bổ sung

**Caching → Configuration:**
- **Caching Level:** Standard
- **Browser Cache TTL:** Respect Existing Headers
- **Always Online:** ON (hiển thị cached version khi server down)

**Firewall (Security):**
- **Security Level:** Medium
- **Bot Fight Mode:** ON
- **Challenge Passage:** 30 minutes

---

## 2. Image Optimization

### 2.1 Plugin & Workflow

**Plugin đề xuất:** ShortPixel Image Optimizer (hoặc Imagify)

| Tính năng | ShortPixel | Imagify | Smush Pro |
| --- | --- | --- | --- |
| Free quota | 100 ảnh/tháng | 20MB/tháng | Unlimited (lossy only) |
| WebP conversion | ✅ | ✅ | ✅ (Pro) |
| Bulk optimize | ✅ | ✅ | ✅ |
| Backup originals | ✅ | ✅ | ✅ |
| Giá Pro | ~$4.99/tháng | ~$9.99/tháng | ~$7/tháng |

### 2.2 Bulk Optimize Workflow

**Bước 1 — Backup trước khi optimize:**
```
- Backup toàn bộ thư mục wp-content/uploads/
- Hoặc dùng UpdraftPlus backup full site
```

**Bước 2 — Cài đặt ShortPixel:**
1. WordPress Admin → Plugins → Add New → Tìm "ShortPixel"
2. Cài đặt & Kích hoạt → Nhập API key (đăng ký tại shortpixel.com)
3. Cấu hình:
   - **Compression type:** Lossy (khuyến nghị cho e-commerce)
   - **Compression level:** 80-85% quality
   - **Create WebP:** ✅ ON
   - **Backup originals:** ✅ ON

**Bước 3 — Bulk Optimize:**
1. Media → ShortPixel Bulk → Start Optimizing
2. Chờ quá trình hoàn tất (có thể mất vài giờ nếu nhiều ảnh)
3. Kiểm tra kết quả: xem % dung lượng đã giảm

### 2.3 WebP Conversion

WebP giảm 25-35% dung lượng so với JPEG với chất lượng tương đương.

**Cấu hình tự động:**
- ShortPixel: Settings → Create WebP → ON
- Plugin sẽ tự tạo file `.webp` song song với file gốc
- Serve WebP cho browser hỗ trợ (Chrome, Firefox, Edge) qua `<picture>` tag hoặc `.htaccess` rewrite

**Kiểm tra WebP đang hoạt động:**
- Mở DevTools (F12) → Network → Filter: Img
- Kiểm tra cột "Type" → Phải hiển thị `webp` thay vì `jpeg/png`

### 2.4 Lazy Loading

```html
<!-- WordPress 5.5+ tự động thêm lazy loading -->
<img src="product.webp" loading="lazy" alt="Xiaomi 14 Ultra chính hãng" />

<!-- Hình ảnh above-the-fold: KHÔNG lazy load (ảnh hưởng LCP) -->
<img src="hero-banner.webp" loading="eager" fetchpriority="high" alt="Banner khuyến mãi" />
```

**Quy tắc:**
- ✅ Lazy load: Tất cả ảnh dưới fold (sản phẩm trong grid, footer, sidebar)
- ❌ KHÔNG lazy load: Hero banner, logo, ảnh sản phẩm đầu tiên trên trang chi tiết
- Plugin hỗ trợ: WP Rocket hoặc LiteSpeed Cache đều có tính năng lazy loading

### 2.5 Responsive Images (srcset)

```html
<img
  srcset="
    xiaomi-14-ultra-300w.webp 300w,
    xiaomi-14-ultra-600w.webp 600w,
    xiaomi-14-ultra-1200w.webp 1200w
  "
  sizes="(max-width: 768px) 300px, (max-width: 1024px) 600px, 1200px"
  src="xiaomi-14-ultra-600w.webp"
  alt="Xiaomi 14 Ultra chính hãng giá tốt"
  loading="lazy"
/>
```

**Kích thước ảnh chuẩn cho WooCommerce:**

| Loại | Kích thước | Sử dụng |
| --- | --- | --- |
| Thumbnail | 300 × 300px | Grid sản phẩm, related products |
| Product | 600 × 600px | Trang chi tiết sản phẩm |
| Full | 1200 × 1200px | Zoom, lightbox |

> WordPress + WooCommerce tự động tạo srcset nếu upload ảnh đủ lớn (≥ 1200px).

### 2.6 Naming Convention & Alt Text

**Quy tắc đặt tên file ảnh (SEO-friendly):**

| ❌ Sai | ✅ Đúng |
| --- | --- |
| `IMG_20260321.jpg` | `xiaomi-14-ultra-chinh-hang.webp` |
| `product-1.png` | `dong-ho-xiaomi-watch-s4-den.webp` |
| `screenshot.jpeg` | `may-hut-bui-xiaomi-g11-trang.webp` |

**Format:** `{ten-san-pham}-{mau-sac/variant}.webp`

**Alt text tiếng Việt — Quy tắc:**
- Mô tả chính xác nội dung ảnh
- Bao gồm tên sản phẩm + từ khóa chính
- Độ dài: 50-125 ký tự
- Không nhồi keyword

| Ảnh | Alt text |
| --- | --- |
| Ảnh chính sản phẩm | `Xiaomi 14 Ultra chính hãng - Mặt trước` |
| Ảnh góc khác | `Xiaomi 14 Ultra - Camera Leica 50MP mặt sau` |
| Ảnh phụ kiện | `Ốp lưng Xiaomi 14 Ultra silicon trong suốt` |
| Banner KM | `Khuyến mãi Xiaomi tháng 3 - Giảm đến 30%` |

---

## 3. CSS/JS Optimization

### 3.1 Minify & Combine

**Plugin đề xuất:** WP Rocket hoặc LiteSpeed Cache

| Cài đặt | WP Rocket | LiteSpeed Cache |
| --- | --- | --- |
| Minify CSS | ✅ File Optimization → Minify CSS | ✅ Page Optimization → CSS Minify |
| Minify JS | ✅ File Optimization → Minify JS | ✅ Page Optimization → JS Minify |
| Combine CSS | ✅ Combine CSS files | ✅ CSS Combine |
| Combine JS | ⚠️ Cẩn thận — test kỹ | ⚠️ Cẩn thận — test kỹ |

> ⚠️ **Lưu ý:** Combine JS có thể gây lỗi trên WooCommerce. Luôn test checkout flow sau khi bật.

### 3.2 Defer Non-Critical JS

**Mục tiêu:** Chỉ load JS cần thiết cho above-the-fold trước, defer phần còn lại.

**WP Rocket:**
- File Optimization → Load JavaScript deferred: ✅ ON
- Delay JavaScript execution: ✅ ON (delay cho đến user interaction)

**Danh sách JS cần defer:**

| Script | Defer? | Lý do |
| --- | --- | --- |
| jQuery | ❌ Không | WooCommerce phụ thuộc |
| WooCommerce cart JS | ❌ Không | Cần cho add-to-cart |
| Google Analytics (gtag) | ✅ Defer | Không ảnh hưởng UX |
| Facebook Pixel | ✅ Defer | Không ảnh hưởng UX |
| Zalo Chat widget | ✅ Defer | Load sau khi trang hiển thị |
| Slider/Carousel JS | ✅ Defer | Nếu không ở above-the-fold |
| Review/Rating JS | ✅ Defer | Thường ở dưới fold |

### 3.3 Critical CSS Inline

**Mục tiêu:** Inline CSS cần thiết cho above-the-fold content → Trang hiển thị nhanh hơn mà không cần chờ load CSS file.

**WP Rocket:**
- File Optimization → Optimize CSS delivery: ✅ ON
- Plugin tự động generate critical CSS cho mỗi loại trang

**LiteSpeed Cache:**
- Page Optimization → Load CSS Asynchronously: ✅ ON
- Generate Critical CSS: ✅ ON

**Kiểm tra:**
1. Tắt cache → Load trang
2. View Source → Kiểm tra có `<style>` tag inline trong `<head>`
3. CSS file chính phải có attribute `media="print" onload="this.media='all'"`

### 3.4 Preload Key Resources

Thêm vào `<head>` (qua plugin hoặc functions.php):

```html
<!-- Preload font chính -->
<link rel="preload" href="/wp-content/themes/motta/assets/fonts/main-font.woff2"
      as="font" type="font/woff2" crossorigin>

<!-- Preload hero image trang chủ -->
<link rel="preload" href="/wp-content/uploads/hero-banner.webp"
      as="image" type="image/webp">

<!-- Preconnect tới CDN & third-party -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://www.googletagmanager.com">
<link rel="dns-prefetch" href="https://www.facebook.com">
```

---

## 4. Browser Caching

### 4.1 Cache Headers Configuration

Thêm vào file `.htaccess` (Apache) hoặc cấu hình Nginx:

**Apache (.htaccess):**
```apache
<IfModule mod_expires.c>
  ExpiresActive On

  # Images
  ExpiresByType image/webp "access plus 1 year"
  ExpiresByType image/jpeg "access plus 1 year"
  ExpiresByType image/png "access plus 1 year"
  ExpiresByType image/svg+xml "access plus 1 year"
  ExpiresByType image/x-icon "access plus 1 year"

  # CSS & JS
  ExpiresByType text/css "access plus 1 year"
  ExpiresByType application/javascript "access plus 1 year"

  # Fonts
  ExpiresByType font/woff2 "access plus 1 year"
  ExpiresByType font/woff "access plus 1 year"

  # HTML
  ExpiresByType text/html "access plus 0 seconds"

  # Default
  ExpiresDefault "access plus 1 month"
</IfModule>

# Cache-Control headers
<IfModule mod_headers.c>
  # Static assets: cache 1 year
  <FilesMatch "\.(css|js|woff2|woff|ttf|svg|webp|jpg|jpeg|png|gif|ico)$">
    Header set Cache-Control "public, max-age=31536000, immutable"
  </FilesMatch>

  # HTML: no cache (hoặc short cache)
  <FilesMatch "\.(html|htm)$">
    Header set Cache-Control "no-cache, must-revalidate"
  </FilesMatch>
</IfModule>
```

### 4.2 Bảng thời gian cache khuyến nghị

| Loại file | Cache TTL | Cache-Control | Ghi chú |
| --- | --- | --- | --- |
| Hình ảnh (WebP, JPEG, PNG) | 1 năm | `max-age=31536000, immutable` | Đổi filename khi update |
| CSS & JS | 1 năm | `max-age=31536000, immutable` | Dùng version query string |
| Fonts (WOFF2) | 1 năm | `max-age=31536000, immutable` | Hiếm khi thay đổi |
| HTML pages | 0 (no-cache) | `no-cache, must-revalidate` | Luôn lấy bản mới nhất |
| API responses | 0 | `no-store` | Dynamic data |
| Favicon | 1 tháng | `max-age=2592000` | Ít thay đổi |

> 💡 **Mẹo:** Dùng `immutable` directive để browser không gửi conditional request cho static assets. Khi cần update file, đổi filename hoặc thêm version query (`style.css?v=2.1`).

---

## 5. Web Vitals Targets

### 5.1 Chỉ số mục tiêu

| Metric | Tên đầy đủ | Target | Mô tả |
| --- | --- | --- | --- |
| **LCP** | Largest Contentful Paint | **< 2.5s** | Thời gian render phần tử lớn nhất (hero image, product image) |
| **FID** | First Input Delay | **< 100ms** | Thời gian phản hồi tương tác đầu tiên (click, tap) |
| **INP** | Interaction to Next Paint | **< 200ms** | Thay thế FID từ 03/2024 — đo mọi interaction |
| **CLS** | Cumulative Layout Shift | **< 0.1** | Mức độ layout bị dịch chuyển khi load |
| **TTFB** | Time to First Byte | **< 600ms** | Thời gian server phản hồi byte đầu tiên |
| **FCP** | First Contentful Paint | **< 1.8s** | Thời gian render nội dung đầu tiên |

### 5.2 Cách cải thiện từng chỉ số

**LCP < 2.5s:**
- ✅ Preload hero image / ảnh sản phẩm chính
- ✅ Dùng CDN (Cloudflare) để giảm latency
- ✅ Optimize server response time (TTFB < 600ms)
- ✅ Tránh lazy load ảnh LCP element
- ✅ Inline critical CSS
- ❌ Tránh render-blocking CSS/JS

**INP < 200ms (thay thế FID):**
- ✅ Defer non-critical JS
- ✅ Break up long tasks (> 50ms)
- ✅ Tránh heavy JS trên main thread
- ✅ Dùng `requestIdleCallback` cho non-urgent work

**CLS < 0.1:**
- ✅ Set `width` và `height` cho tất cả `<img>` và `<video>`
- ✅ Reserve space cho ads/embeds (aspect-ratio)
- ✅ Tránh inject content phía trên existing content
- ✅ Dùng `font-display: swap` cho web fonts
- ✅ Preload fonts để tránh FOUT (Flash of Unstyled Text)

**TTFB < 600ms:**
- ✅ Bật page caching (WP Rocket / LiteSpeed Cache)
- ✅ Dùng CDN
- ✅ Upgrade hosting nếu cần (shared → VPS)
- ✅ Bật object caching (Redis/Memcached)
- ✅ Tối ưu database queries

---

## 6. Đo lường Performance

### 6.1 Google PageSpeed Insights

**URL:** [pagespeed.web.dev](https://pagespeed.web.dev)

**Cách sử dụng:**
1. Nhập URL: `https://xiaomi247.com`
2. Chờ phân tích → Xem điểm Mobile & Desktop
3. Kiểm tra từng mục trong "Diagnostics" và "Opportunities"

**Target scores:**

| Thiết bị | Score mục tiêu | Ghi chú |
| --- | --- | --- |
| Desktop | ≥ 85 | Dễ đạt hơn mobile |
| Mobile | ≥ 70 | Khó hơn, ưu tiên tối ưu |

**Trang cần test:**
- Trang chủ: `xiaomi247.com`
- Trang danh mục: `xiaomi247.com/danh-muc/dien-thoai`
- Trang sản phẩm: `xiaomi247.com/san-pham/xiaomi-14-ultra`
- Trang checkout: `xiaomi247.com/checkout`

### 6.2 GTmetrix

**URL:** [gtmetrix.com](https://gtmetrix.com)

**Cách sử dụng:**
1. Đăng ký tài khoản miễn phí
2. Nhập URL → Chọn **Test Server: Hong Kong** (gần Việt Nam nhất)
3. Xem kết quả: Grade, Web Vitals, Waterfall chart

**Lưu ý quan trọng:**
- Chọn server Hong Kong hoặc Singapore để kết quả phản ánh đúng tốc độ cho user Việt Nam
- Kiểm tra **Waterfall chart** để tìm bottleneck (file nào load chậm nhất)
- Tab **Structure** cho biết cụ thể cần fix gì

### 6.3 WebPageTest

**URL:** [webpagetest.org](https://webpagetest.org)

**Cách sử dụng:**
1. Nhập URL
2. Test Location: Chọn **Singapore** hoặc **Tokyo**
3. Browser: Chrome
4. Connection: 4G (mô phỏng mobile thực tế)
5. Chạy test → Xem Waterfall, filmstrip, Web Vitals

**Tính năng nổi bật:**
- **Filmstrip view:** Xem trang load từng frame
- **Waterfall:** Chi tiết từng request
- **Repeat view:** So sánh first visit vs cached visit

### 6.4 Lịch đo lường định kỳ

| Tần suất | Công cụ | Trang test | Ghi chú |
| --- | --- | --- | --- |
| Hàng tuần | PageSpeed Insights | Trang chủ + 1 trang SP | Theo dõi trend |
| Hàng tháng | GTmetrix + WebPageTest | Tất cả trang chính | Phân tích chi tiết |
| Sau mỗi thay đổi lớn | Tất cả công cụ | Trang bị ảnh hưởng | So sánh before/after |
| Hàng quý | Chrome UX Report | Toàn site | Dữ liệu real users |

---

## 7. Checklist tối ưu định kỳ

### 7.1 Checklist hàng tuần

- [ ] Kiểm tra PageSpeed score trang chủ (Mobile ≥ 70, Desktop ≥ 85)
- [ ] Kiểm tra uptime (UptimeRobot không có alert)
- [ ] Kiểm tra cache đang hoạt động (response header có `cf-cache-status: HIT`)
- [ ] Xóa cache nếu có cập nhật nội dung quan trọng

### 7.2 Checklist hàng tháng

- [ ] Chạy GTmetrix full test (server Hong Kong)
- [ ] Kiểm tra Web Vitals trong Google Search Console → Core Web Vitals report
- [ ] Bulk optimize ảnh mới upload trong tháng
- [ ] Kiểm tra có ảnh nào chưa có alt text
- [ ] Kiểm tra có ảnh nào chưa convert WebP
- [ ] Review Cloudflare Analytics → Cache hit ratio (target > 80%)
- [ ] Kiểm tra SSL certificate còn hạn
- [ ] Cập nhật plugin cache (WP Rocket / LiteSpeed Cache)

### 7.3 Checklist hàng quý

- [ ] Full performance audit với WebPageTest (Singapore server)
- [ ] So sánh Web Vitals với quý trước
- [ ] Review Cloudflare Page Rules — còn phù hợp không?
- [ ] Kiểm tra database size → Optimize nếu cần (WP-Optimize plugin)
- [ ] Review plugin list → Xóa plugin không dùng
- [ ] Test checkout flow trên mobile sau các thay đổi
- [ ] Kiểm tra broken images
- [ ] Review hosting performance → Cân nhắc upgrade nếu traffic tăng

### 7.4 Checklist sau khi thay đổi lớn (theme update, plugin mới, redesign)

- [ ] Test PageSpeed trước & sau thay đổi
- [ ] Kiểm tra console errors (F12 → Console)
- [ ] Test add-to-cart hoạt động
- [ ] Test checkout flow hoàn chỉnh
- [ ] Kiểm tra lazy loading vẫn hoạt động
- [ ] Kiểm tra critical CSS được generate lại
- [ ] Purge tất cả cache (Cloudflare + plugin cache + browser)
- [ ] Test trên mobile thực tế (không chỉ DevTools)

---

## Tổng kết ưu tiên thực hiện

| Ưu tiên | Hành động | Thời gian | Impact |
| --- | --- | --- | --- |
| 🔴 Cao | Setup Cloudflare CDN + SSL | 1-2 giờ | Giảm TTFB 40-60% |
| 🔴 Cao | Cài plugin cache (WP Rocket/LiteSpeed) | 30 phút | Giảm load time 50%+ |
| 🔴 Cao | Bulk optimize images + WebP | 1-2 giờ | Giảm page weight 30-50% |
| 🟠 Trung bình | Cấu hình browser caching | 30 phút | Cải thiện repeat visits |
| 🟠 Trung bình | Defer non-critical JS | 1 giờ | Cải thiện FID/INP |
| 🟠 Trung bình | Critical CSS inline | 30 phút | Cải thiện LCP, FCP |
| 🟡 Thấp | Preload key resources | 15 phút | Cải thiện LCP nhẹ |
| 🟡 Thấp | Setup monitoring schedule | 30 phút | Duy trì performance |

---

*Hướng dẫn Performance & CDN — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Phiên bản: 1.0*
