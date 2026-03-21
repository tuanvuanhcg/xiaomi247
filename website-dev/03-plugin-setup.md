# 🔌 Plugin Setup & Cấu hình — Xiaomi247.com

> **Ngày tạo:** 21/03/2026
> **Phiên bản:** 1.0
> **Nền tảng:** WordPress 6.x + WooCommerce 9.x + Motta Theme
> **Tham chiếu:** [Khuyến nghị Kỹ thuật](../marketing/01-technical-audit/technical-recommendations.md) · [Technical SEO Checklist](../marketing/02-seo/technical-seo-checklist.md)

---

## 📋 Tổng quan Plugin

> **Nguyên tắc:** Giới hạn tổng số plugin ≤ 20. Mỗi plugin thêm vào đều tăng thời gian tải & rủi ro bảo mật.

| # | Plugin | Mục đích | Free/Premium |
|---|--------|----------|:---:|
| 1 | LiteSpeed Cache / WP Rocket | Caching & Performance | ✅ / 💰 |
| 2 | Rank Math SEO | SEO, Sitemap, Schema | ✅ Free |
| 3 | Wordfence Security | Firewall, Malware Scan | ✅ Free |
| 4 | UpdraftPlus | Backup tự động | ✅ Free |
| 5 | ShortPixel Image Optimizer | Nén ảnh & WebP | ✅ Free (100 ảnh/tháng) |
| 6 | Contact Form 7 | Form liên hệ | ✅ Free |
| 7 | Loco Translate | Việt hóa | ✅ Free |
| 8 | WooCommerce Product Filter | Bộ lọc sản phẩm | 💰 Premium |
| 9 | YITH WooCommerce Wishlist | Danh sách yêu thích | ✅ Free |
| 10 | Tidio / Zalo Chat | Live chat hỗ trợ | ✅ Free |

---

## 1. LiteSpeed Cache / WP Rocket — Caching & Performance

### Lựa chọn plugin

| Plugin | Giá | Khi nào dùng |
|--------|-----|---------------|
| **LiteSpeed Cache** | Miễn phí | Hosting dùng LiteSpeed/OpenLiteSpeed (khuyến nghị) |
| **WP Rocket** | $59/năm (~1.4 triệu VNĐ) | Hosting Apache/Nginx, muốn cấu hình đơn giản |

> 🔗 Download: [LiteSpeed Cache](https://wordpress.org/plugins/litespeed-cache/) · [WP Rocket](https://wp-rocket.me/)

### Cài đặt

1. **WordPress Admin** → Plugins → Add New → Tìm "LiteSpeed Cache" → Install → Activate
2. (WP Rocket: Upload file `.zip` mua từ wp-rocket.me → Plugins → Add New → Upload Plugin)

### Cấu hình LiteSpeed Cache

#### General Settings
- **Request Domain Key** từ QUIC.cloud (miễn phí) để bật CDN & Image Optimization
- Auto Upgrade: **ON**

#### Cache Tab
- ✅ Enable Cache: **ON**
- ✅ Cache Logged-in Users: **OFF** (không cache cho user đã login)
- ✅ Cache Mobile: **ON** (dùng chung cache nếu theme responsive)

#### Cache → Excludes (QUAN TRỌNG — WooCommerce)
```
# Exclude các trang WooCommerce dynamic:
/cart/
/checkout/
/my-account/
/gio-hang/
/thanh-toan/
/tai-khoan/
```
> ⚠️ Nếu không exclude, khách hàng sẽ thấy giỏ hàng/checkout của người khác!

#### Browser Cache
- ✅ Browser Cache: **ON**
- Browser Cache TTL: **2592000** (30 ngày)

#### Object Cache
- ✅ Object Cache: **ON** (yêu cầu hosting hỗ trợ Redis hoặc Memcached)
- Method: **Redis** (ưu tiên) hoặc Memcached

#### Page Optimization
- ✅ CSS Minify: **ON**
- ✅ CSS Combine: **ON**
- ✅ JS Minify: **ON**
- ✅ JS Combine: **OFF** (có thể gây lỗi WooCommerce)
- ✅ JS Defer: **ON**
- ✅ HTML Minify: **ON**

#### Purge Settings
- ✅ Purge All On Upgrade: **ON**
- ✅ Auto Purge Rules: Purge khi update post/product

### Cấu hình WP Rocket (nếu dùng thay thế)

- **Caching:** Mobile Cache ON, Separate cache for mobile OFF
- **File Optimization:** Minify CSS ON, Combine CSS OFF, Minify JS ON, Delay JS execution ON
- **Media:** LazyLoad images ON, LazyLoad iframes ON
- **Preload:** Activate Preloading ON, Sitemap-based preloading ON
- **Advanced → Never Cache URLs:**
  ```
  /cart/(.*)
  /checkout/(.*)
  /my-account/(.*)
  /gio-hang/(.*)
  /thanh-toan/(.*)
  ```

---

## 2. Rank Math SEO

> 🔗 Download: [Rank Math](https://wordpress.org/plugins/seo-by-rank-math/)

### Cài đặt
1. Plugins → Add New → Tìm "Rank Math SEO" → Install → Activate
2. Rank Math sẽ hiện **Setup Wizard** — chọn **Advanced Mode**

### Setup Wizard

#### Bước 1: Your Site
- Site Type: **Online Store / WooCommerce**
- Business Name: **Xiaomi247 - Đại lý Xiaomi chính hãng**
- Logo: Upload logo website

#### Bước 2: Search Console
- Kết nối Google Search Console (đăng nhập Google account)

#### Bước 3: Sitemap
- ✅ Sitemap: **ON**
- Include: Posts, Pages, Products, Product Categories
- Exclude: Tags, Author archives, Media attachments
- Links Per Sitemap: **200**

#### Bước 4: SEO Tweaks
- ✅ Noindex empty category/tag archives: **ON**
- ✅ Open External Links in New Tab: **ON**
- ✅ Nofollow External Links: **OFF** (để tự chọn từng link)

### Cấu hình sau Setup Wizard

#### Meta Title/Description Templates
**Rank Math → Titles & Meta:**

| Loại trang | Title Template | Description Template |
|-------------|---------------|---------------------|
| Homepage | `Xiaomi247 - Đại lý Xiaomi chính hãng tại Việt Nam` | `Xiaomi247.com - Chuyên phân phối điện thoại, TV, robot hút bụi Xiaomi chính hãng. Giá tốt nhất, bảo hành 12 tháng, giao hàng toàn quốc.` |
| Products | `%title% - Chính hãng %sep% Xiaomi247` | `Mua %title% chính hãng tại Xiaomi247. %excerpt% Bảo hành 12 tháng, giao hàng toàn quốc.` |
| Product Categories | `%term% Xiaomi chính hãng %sep% Xiaomi247` | `Danh mục %term% Xiaomi chính hãng tại Xiaomi247. Giá tốt nhất, nhiều mẫu mã, bảo hành chính hãng.` |
| Blog Posts | `%title% %sep% Xiaomi247` | `%excerpt%` |

#### Schema Markup (QUAN TRỌNG cho SEO)

**Rank Math → Titles & Meta → Products:**
- ✅ Schema Type: **Product**
- ✅ Tự động lấy giá, tình trạng kho, đánh giá từ WooCommerce

**Rank Math → Titles & Meta → Global:**
- ✅ Organization Schema: **ON**
  - Name: `Xiaomi247`
  - URL: `https://xiaomi247.com`
  - Logo: Upload logo
  - Phone: `(số điện thoại)`
  - Email: `contact@xiaomi247.com`

**Rank Math → General Settings → Breadcrumbs:**
- ✅ Enable Breadcrumbs: **ON**
- Separator: `»`
- Home Label: `Trang chủ`
- Schema: BreadcrumbList (tự động)

#### Sitemap Submit
1. Rank Math tạo sitemap tại: `https://xiaomi247.com/sitemap_index.xml`
2. Vào **Google Search Console** → Sitemaps → Submit URL trên
3. Kiểm tra sitemap không chứa trang cart, checkout, my-account

---

## 3. Wordfence Security

> 🔗 Download: [Wordfence](https://wordpress.org/plugins/wordfence/)

### Cài đặt
1. Plugins → Add New → Tìm "Wordfence Security" → Install → Activate
2. Nhập email để nhận security alerts
3. Chọn Free License

### Cấu hình Firewall

**Wordfence → Firewall:**

- ✅ Web Application Firewall: **Enabled and Protecting**
- ✅ Protection Level: **Extended Protection** (yêu cầu sửa `.htaccess`)
  - Click "Optimize Firewall" → Download `.htaccess` backup → Continue
- ✅ Rate Limiting:
  - Throttle/Block requests from crawlers: **Unlimited** (không block Google)
  - How should we treat Google's crawlers: **Verified Googlebot has unlimited access**
  - If anyone's requests exceed: **240 per minute** → **Throttle it**
  - If a human's page views exceed: **240 per minute** → **Block it**

### Cấu hình Scan

**Wordfence → Scan:**
- ✅ Scan Schedule: **Daily** (tự động)
- ✅ Scan Type: **Standard Scan**
- Scan Options:
  - ✅ Scan core files against repository versions
  - ✅ Scan theme files against repository versions
  - ✅ Scan plugin files against repository versions
  - ✅ Scan for malware signatures
  - ✅ Scan file contents for backdoors

### Login Security

**Wordfence → Login Security:**

#### Brute Force Protection
- ✅ Enable Brute Force Protection: **ON**
- Lock out after how many login failures: **5**
- Lock out after how many forgot password attempts: **3**
- Count failures over what time period: **4 hours**
- Amount of time a user is locked out: **4 hours**
- ✅ Immediately lock out invalid usernames: **ON**

#### Two-Factor Authentication (2FA)
- ✅ Bật 2FA cho **tất cả tài khoản Admin**
- Dùng app: Google Authenticator hoặc Authy
- Setup: Login Security → Two-Factor Authentication → Scan QR code
- ⚠️ **LƯU recovery codes** ở nơi an toàn!

### Cài đặt bổ sung
- **Wordfence → All Options → General:**
  - ✅ Hide WordPress version: **ON**
  - ✅ Disable Code Execution for Uploads directory: **ON**

---

## 4. UpdraftPlus — Backup tự động

> 🔗 Download: [UpdraftPlus](https://wordpress.org/plugins/updraftplus/)

### Cài đặt
1. Plugins → Add New → Tìm "UpdraftPlus" → Install → Activate
2. Settings → UpdraftPlus Backups

### Cấu hình Backup Schedule

**Tab Settings:**

| Loại | Tần suất | Số bản giữ lại |
|------|----------|:---:|
| Files backup | **Daily** | **7** (giữ 7 ngày gần nhất) |
| Database backup | **Daily** | **14** (giữ 14 ngày gần nhất) |

### Remote Storage (Offsite Backup)

> ⚠️ **QUAN TRỌNG:** Luôn lưu backup ở nơi KHÁC server hosting. Nếu server gặp sự cố, backup trên server cũng mất!

**Chọn 1 trong các dịch vụ sau:**

| Storage | Dung lượng miễn phí | Cách kết nối |
|---------|:---:|---|
| **Google Drive** (khuyến nghị) | 15 GB | Click icon Google Drive → Đăng nhập → Authorize |
| **Dropbox** | 2 GB | Click icon Dropbox → Đăng nhập → Authorize |
| **Amazon S3** | Trả phí | Nhập Access Key & Secret Key |
| **FTP/SFTP** | Tùy server | Nhập host, user, password |

### Nội dung Backup
- ✅ Plugins: **Include**
- ✅ Themes: **Include**
- ✅ Uploads: **Include**
- ✅ Any other directories: **Include**
- ✅ Database: **Include**

### Kiểm tra Backup
1. Sau khi cấu hình, click **"Backup Now"** để tạo backup đầu tiên
2. Kiểm tra backup đã upload lên Google Drive/Dropbox thành công
3. **Test restore** ít nhất 1 lần trên staging site để đảm bảo backup hoạt động

---

## 5. ShortPixel Image Optimizer

> 🔗 Download: [ShortPixel](https://wordpress.org/plugins/shortpixel-image-optimiser/)

### Cài đặt
1. Plugins → Add New → Tìm "ShortPixel Image Optimizer" → Install → Activate
2. Đăng ký tài khoản tại [shortpixel.com](https://shortpixel.com) để lấy **API Key**
3. Settings → ShortPixel → Nhập API Key

### Free vs Premium

| Plan | Số ảnh/tháng | Giá |
|------|:---:|---|
| Free | 100 ảnh | Miễn phí |
| Basic | 5.000 ảnh | $4.99/tháng |
| One-time | 10.000 ảnh | $9.99 (mua 1 lần) |

> 💡 **Tip:** Mua gói One-time 10.000-50.000 credits để bulk optimize ảnh hiện có. Sau đó dùng Free plan cho ảnh upload mới.

### Cấu hình

**Settings → ShortPixel → General:**
- ✅ Compression Type: **Lossy** (khuyến nghị cho e-commerce, giảm nhiều dung lượng)
- ✅ Also include thumbnails: **ON**
- ✅ Create WebP: **ON**
- ✅ Deliver WebP: **Using `<picture>` tag** (hoặc qua .htaccess)
- ✅ CMYK to RGB conversion: **ON**
- ✅ Remove EXIF data: **ON** (giảm dung lượng thêm)

**Settings → ShortPixel → Advanced:**
- ✅ Resize large images: **ON**
  - Max width: **1200px** (đủ cho product images)
  - Max height: **1200px**
- ✅ Backup original images: **ON** (để có thể restore nếu cần)

### Bulk Optimize (ảnh hiện có)
1. **Media → ShortPixel Bulk** → Click **"Start Optimizing"**
2. Đợi quá trình hoàn tất (có thể mất vài giờ tùy số lượng ảnh)
3. Kiểm tra kết quả: xem % dung lượng đã giảm được

### Kích thước ảnh sản phẩm khuyến nghị
| Loại | Kích thước | Ghi chú |
|------|:---:|---|
| Thumbnail | 300×300 px | Trang danh mục |
| Product image | 600×600 px | Trang chi tiết |
| Full size | 1200×1200 px | Zoom/Gallery |

---

## 6. Contact Form 7

> 🔗 Download: [Contact Form 7](https://wordpress.org/plugins/contact-form-7/)

### Cài đặt
1. Plugins → Add New → Tìm "Contact Form 7" → Install → Activate
2. Contact → Add New

### Tạo Form Liên hệ cơ bản

**Tên form:** `Form Liên hệ Xiaomi247`

```html
<div class="cf7-form">
  <label>Họ và tên (bắt buộc)</label>
  [text* your-name placeholder "Nhập họ và tên"]

  <label>Email (bắt buộc)</label>
  [email* your-email placeholder "Nhập email"]

  <label>Số điện thoại</label>
  [tel your-phone placeholder "Nhập số điện thoại"]

  <label>Chủ đề</label>
  [select your-subject "Hỏi về sản phẩm" "Bảo hành" "Đổi trả" "Hợp tác kinh doanh" "Khác"]

  <label>Nội dung</label>
  [textarea your-message placeholder "Nhập nội dung tin nhắn"]

  [submit "Gửi tin nhắn"]
</div>
```

### Cấu hình Email

**Tab Mail:**
- To: `contact@xiaomi247.com`
- From: `[your-name] <wordpress@xiaomi247.com>`
- Subject: `[Xiaomi247] Liên hệ: [your-subject]`
- Body:
  ```
  Họ tên: [your-name]
  Email: [your-email]
  SĐT: [your-phone]
  Chủ đề: [your-subject]

  Nội dung:
  [your-message]
  ```

### Chống Spam
- Cài thêm plugin **Flamingo** (lưu tin nhắn vào database, tránh mất email)
- Tích hợp reCAPTCHA v3: Contact → Integration → reCAPTCHA → Nhập Site Key & Secret Key
  - Lấy key tại: [google.com/recaptcha](https://www.google.com/recaptcha/admin)

### Nhúng vào trang
1. Copy shortcode: `[contact-form-7 id="xxx" title="Form Liên hệ Xiaomi247"]`
2. Dán vào trang **Liên hệ** (đã tạo ở [02-localization-content.md](./02-localization-content.md))

---

## 7. Loco Translate

> Đã hướng dẫn chi tiết tại **[02 — Việt hóa & Nội dung](./02-localization-content.md)**

Tóm tắt:
- Dùng Loco Translate để Việt hóa Motta Theme, WooCommerce, và các plugin
- Tạo file dịch custom (không sửa file gốc, tránh mất khi update)
- Ưu tiên Việt hóa: menu, nút bấm, thông báo WooCommerce, trang checkout

---

## 8. Plugin phụ trợ

### 8.1 WooCommerce Product Filter

> 🔗 Plugin khuyến nghị: [FLAVOR - Product Filter](https://flavor.developer.flavor.dev/) hoặc [FLAVOR - FLAVOR WooCommerce Product Filter](https://codecanyon.net/item/woocommerce-product-filter/8514038)

**Mục đích:** Cho phép khách hàng lọc sản phẩm theo giá, thương hiệu, rating, thuộc tính

**Cấu hình:**
- Thêm bộ lọc vào sidebar trang Shop / Danh mục
- Filters cần thiết:
  - ✅ Lọc theo **khoảng giá** (slider)
  - ✅ Lọc theo **danh mục** (checkbox)
  - ✅ Lọc theo **thuộc tính** (màu sắc, dung lượng, kích thước)
  - ✅ Lọc theo **đánh giá** (1-5 sao)
  - ✅ Lọc theo **tình trạng kho** (còn hàng / hết hàng)
- AJAX filtering: **ON** (lọc không cần reload trang)
- Giá: **~$29-39** (mua 1 lần trên CodeCanyon)

### 8.2 YITH WooCommerce Wishlist

> 🔗 Download: [YITH Wishlist](https://wordpress.org/plugins/yith-woocommerce-wishlist/)

**Cài đặt:**
1. Plugins → Add New → Tìm "YITH WooCommerce Wishlist" → Install → Activate
2. YITH → Wishlist → Settings

**Cấu hình:**
- ✅ Add to Wishlist button: **After Add to Cart button**
- ✅ Wishlist page: Tạo trang mới `/danh-sach-yeu-thich/`
- ✅ Remove after Add to Cart: **ON**
- Việt hóa text: "Add to Wishlist" → "Thêm vào yêu thích" (dùng Loco Translate)

### 8.3 Tidio Live Chat / Zalo Chat

**Lựa chọn 1: Tidio (khuyến nghị cho đa kênh)**
> 🔗 Download: [Tidio](https://wordpress.org/plugins/tidio-live-chat/)

- Cài plugin → Đăng ký tài khoản Tidio → Tự động hiển thị chat widget
- Free plan: 50 conversations/tháng, 1 operator
- Hỗ trợ chatbot tự động trả lời câu hỏi thường gặp

**Lựa chọn 2: Zalo Chat Widget (phổ biến tại VN)**
- Truy cập [Zalo OA Admin](https://oa.zalo.me) → Tạo Official Account
- Lấy mã nhúng chat widget
- Dán code vào **Appearance → Theme File Editor → footer.php** hoặc dùng plugin **Insert Headers and Footers**
- Hoặc cài plugin: [Developer Plugin for Zalo](https://wordpress.org/plugins/developer-developer-for-zalo/)

---

## 9. Plugin cần xóa / Kiểm tra

### Checklist xóa plugin

> ⚠️ **Nguyên tắc:** Plugin không dùng = rủi ro bảo mật + ảnh hưởng performance. Xóa ngay!

- [ ] **Hello Dolly** — Plugin mặc định WordPress, không có tác dụng → **XÓA**
- [ ] **Akismet Anti-Spam** — Nếu đã dùng reCAPTCHA trong Contact Form 7 → **XÓA** hoặc giữ nếu có blog comments
- [ ] Plugin demo/sample từ hosting → **XÓA**
- [ ] Plugin trùng chức năng (vd: 2 plugin SEO, 2 plugin cache) → **Giữ 1, xóa cái còn lại**
- [ ] Plugin đã deactivate nhưng chưa xóa → **XÓA hoàn toàn**
- [ ] Plugin không còn được cập nhật (>2 năm) → **Tìm thay thế và XÓA**
- [ ] Plugin nulled/crack → **XÓA NGAY** (chứa malware)

### Cách xóa an toàn
1. **Backup trước** (dùng UpdraftPlus)
2. Plugins → Deactivate plugin cần xóa
3. Kiểm tra website hoạt động bình thường
4. Plugins → Delete plugin
5. Kiểm tra lại website 1 lần nữa

---

## 10. Giới hạn tổng số Plugin

### Danh sách plugin cuối cùng (≤ 20)

| # | Plugin | Bắt buộc? | Ghi chú |
|:---:|--------|:---:|---|
| 1 | WooCommerce | ✅ | Core e-commerce |
| 2 | Motta Addons | ✅ | Theme addons |
| 3 | LiteSpeed Cache / WP Rocket | ✅ | Caching |
| 4 | Rank Math SEO | ✅ | SEO |
| 5 | Wordfence Security | ✅ | Bảo mật |
| 6 | UpdraftPlus | ✅ | Backup |
| 7 | ShortPixel | ✅ | Tối ưu ảnh |
| 8 | Contact Form 7 | ✅ | Form liên hệ |
| 9 | Loco Translate | ✅ | Việt hóa |
| 10 | YITH Wishlist | Nên có | UX tốt hơn |
| 11 | WooCommerce Product Filter | Nên có | UX tốt hơn |
| 12 | Tidio / Zalo Chat | Nên có | Hỗ trợ khách |
| 13 | Flamingo | Tùy chọn | Lưu form submissions |
| 14 | Insert Headers & Footers | Tùy chọn | Thêm tracking code |
| — | **Tổng: 12-14 plugin** | | **✅ Trong giới hạn** |

> 💡 Giữ dưới 15 plugin là lý tưởng. Tuyệt đối không vượt quá 20 plugin.

---

## 11. Bảng ước tính chi phí Plugin

| Plugin | Phiên bản | Chi phí/năm | Ghi chú |
|--------|:---------:|:-----------:|---------|
| LiteSpeed Cache | Free | **0 đ** | Hosting LiteSpeed |
| WP Rocket (thay thế) | Premium | **~1.400.000 đ** | $59/năm (1 site) |
| Rank Math SEO | Free | **0 đ** | Free đủ dùng |
| Rank Math Pro (nâng cấp) | Premium | **~1.500.000 đ** | $6.99/tháng — thêm schema, keyword tracking |
| Wordfence | Free | **0 đ** | Free đủ dùng |
| UpdraftPlus | Free | **0 đ** | Free đủ dùng |
| ShortPixel | Free + One-time | **~250.000 đ** | Gói 10.000 credits ($9.99) |
| Contact Form 7 | Free | **0 đ** | |
| Loco Translate | Free | **0 đ** | |
| YITH Wishlist | Free | **0 đ** | |
| Product Filter | Premium | **~700.000 đ** | ~$29 (mua 1 lần, CodeCanyon) |
| Tidio | Free | **0 đ** | Free 50 chats/tháng |
| **TỔNG (phương án tiết kiệm)** | | **~250.000 đ** | Dùng toàn Free + ShortPixel credits |
| **TỔNG (phương án đầy đủ)** | | **~3.850.000 đ** | WP Rocket + Rank Math Pro + ShortPixel + Filter |

---

## 12. Thứ tự cài đặt khuyến nghị

> Cài theo thứ tự ưu tiên để đảm bảo bảo mật & backup trước khi cấu hình các plugin khác.

```
Bước 1: Wordfence        → Bảo mật website ngay
Bước 2: UpdraftPlus      → Backup trước khi thay đổi gì thêm
Bước 3: LiteSpeed Cache  → Performance cơ bản
Bước 4: Rank Math SEO    → SEO foundation
Bước 5: ShortPixel       → Tối ưu ảnh hiện có
Bước 6: Contact Form 7   → Form liên hệ
Bước 7: Loco Translate   → Việt hóa (xem file 02)
Bước 8: YITH Wishlist    → Tính năng bổ sung
Bước 9: Product Filter   → Tính năng bổ sung
Bước 10: Tidio/Zalo Chat → Live chat
```

---

## 13. Kiểm tra sau cài đặt

- [ ] Website tải nhanh (test bằng [GTmetrix](https://gtmetrix.com) & [PageSpeed Insights](https://pagespeed.web.dev))
- [ ] Giỏ hàng & Checkout hoạt động bình thường (không bị cache)
- [ ] Form liên hệ gửi email thành công
- [ ] Sitemap truy cập được: `https://xiaomi247.com/sitemap_index.xml`
- [ ] Backup tự động chạy đúng lịch & upload offsite thành công
- [ ] Scan Wordfence không phát hiện malware
- [ ] 2FA hoạt động cho tài khoản admin
- [ ] Ảnh sản phẩm hiển thị WebP format
- [ ] Schema markup test pass: [Rich Results Test](https://search.google.com/test/rich-results)
- [ ] Tổng số plugin ≤ 20

---

*Plugin Setup & Cấu hình — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Phiên bản: 1.0*

