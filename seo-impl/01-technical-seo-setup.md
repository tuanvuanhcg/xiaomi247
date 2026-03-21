# 🔧 Technical SEO Setup — Xiaomi247.com

> **Ngày tạo:** 21/03/2026
> **Phiên bản:** 1.0
> **Nền tảng:** WordPress 6.x + WooCommerce 9.x + Motta Theme
> **Tham chiếu:** [Technical SEO Checklist](../marketing/02-seo/technical-seo-checklist.md) · [Plugin Setup](../website-dev/03-plugin-setup.md#2-rank-math-seo)

---

## 1. RANK MATH SEO — CẤU HÌNH CHI TIẾT

> ⚠️ Phần cài đặt & Setup Wizard cơ bản đã hướng dẫn tại [Plugin Setup — Rank Math SEO](../website-dev/03-plugin-setup.md#2-rank-math-seo). Dưới đây là cấu hình bổ sung cho Technical SEO.

### 1.1 Global Settings quan trọng

**WP Admin → Rank Math → General Settings:**

#### Links
- ✅ Strip Category Base: **ON** — URL `/category/tivi-xiaomi/` → `/tivi-xiaomi/`
- ✅ Redirect Attachments: **ON** — redirect trang attachment về post gốc
- ✅ Redirect Orphan Media: **ON** — redirect media không gắn post về trang chủ
- ✅ Nofollow Image File Links: **OFF**
- ✅ Open External Links in New Tab: **ON**

#### Images
- ✅ Add Missing ALT Attributes: **ON** — tự động thêm alt = tên file nếu thiếu
- ✅ Add Missing Title Attributes: **ON**

#### Webmaster Tools
- ✅ Google Search Console: Kết nối (đã làm ở Setup Wizard)
- ✅ Bing Webmaster Tools: Nhập verification code (xem mục 5)
- ✅ Baidu Webmaster Tools: **Bỏ qua** (không target thị trường TQ)

### 1.2 Titles & Meta — Cấu hình nâng cao

**WP Admin → Rank Math → Titles & Meta:**

#### Global Meta
- ✅ Separator: `—` (em dash)
- ✅ Capitalize Titles: **OFF** (giữ nguyên tiếng Việt)

#### Local SEO (Organization)
- ✅ Person or Company: **Organization**
- ✅ Name: `Xiaomi247 - Đại lý Xiaomi chính hãng`
- ✅ Logo: Upload logo (tối thiểu 112×112px, khuyến nghị 600×60px)
- ✅ URL: `https://xiaomi247.com`
- ✅ Phone: `(số hotline)`
- ✅ Email: `contact@xiaomi247.com`
- ✅ Address: `(địa chỉ cửa hàng)`
- ✅ Opening Hours: Thêm giờ mở cửa (Thứ 2 - CN)
- ✅ Price Range: `$$`

#### Noindex Settings
- ✅ Author Archives: **Noindex** (tránh duplicate content)
- ✅ Date Archives: **Noindex**
- ✅ Tag Archives: **Noindex** (trừ khi có chiến lược tag SEO)
- ✅ Empty Category Archives: **Noindex**
- ✅ Search Results Pages: **Noindex**
- ✅ 404 Pages: **Noindex** (mặc định)

### 1.3 Instant Indexing (Tùy chọn)

**Rank Math → Instant Indexing:**
- Kết nối Google Indexing API để đẩy nhanh index trang mới
- Hữu ích khi thêm sản phẩm mới hoặc bài blog mới
- Yêu cầu: Tạo Service Account trên Google Cloud Console

---

## 2. SITEMAP.XML SETUP

> Sitemap được tạo tự động bởi Rank Math. Cấu hình chi tiết dưới đây.

### 2.1 Cấu hình Sitemap qua Rank Math

**WP Admin → Rank Math → Sitemap Settings:**

#### General
- ✅ Sitemap: **ON**
- ✅ Links Per Sitemap: **200** (chia nhỏ để Google crawl hiệu quả)
- ✅ Include Images: **ON**
- ✅ Include Featured Images: **ON**

#### Bật/Tắt theo loại nội dung

| Loại | Sitemap | Lý do |
|------|:---:|---|
| Posts (Bài viết) | ✅ ON | Blog content cần index |
| Pages (Trang) | ✅ ON | Trang tĩnh quan trọng |
| Products | ✅ ON | Sản phẩm — core content |
| Product Categories | ✅ ON | Trang danh mục |
| Product Tags | ❌ OFF | Tránh thin content / duplicate |
| Media/Attachments | ❌ OFF | Không cần index ảnh riêng |
| Author Archives | ❌ OFF | Đã noindex |
| Date Archives | ❌ OFF | Đã noindex |

### 2.2 Exclude trang không cần index

**Rank Math → Sitemap Settings → Exclude Posts:**

Thêm các trang sau vào danh sách exclude:
- Giỏ hàng (`/gio-hang/` hoặc `/cart/`)
- Thanh toán (`/thanh-toan/` hoặc `/checkout/`)
- Tài khoản (`/tai-khoan/` hoặc `/my-account/`)
- Cảm ơn / Thank You page
- Trang chính sách (nếu noindex)

**Cách exclude:**
1. Vào trang cần exclude → Edit
2. Cuộn xuống **Rank Math SEO** meta box
3. Tab **Advanced** → Robots Meta: chọn **Noindex**
4. Trang sẽ tự động bị loại khỏi sitemap

### 2.3 Cấu trúc Sitemap kết quả

```
https://xiaomi247.com/sitemap_index.xml (index chính)
├── post-sitemap.xml          (bài viết blog)
├── page-sitemap.xml          (trang tĩnh: trang chủ, giới thiệu, liên hệ)
├── product-sitemap.xml       (tất cả sản phẩm)
├── product_cat-sitemap.xml   (danh mục sản phẩm)
└── local-sitemap.xml         (Local SEO — nếu bật)
```

### 2.4 Kiểm tra Sitemap

1. Truy cập `https://xiaomi247.com/sitemap_index.xml` — xác nhận hiển thị đúng
2. Click vào từng sitemap con — kiểm tra URL hợp lệ
3. Đảm bảo **KHÔNG** chứa:
   - URL trả về 404
   - URL bị redirect (301/302)
   - URL có tham số `?sort=`, `?filter=`
   - Trang cart, checkout, my-account

### 2.5 Submit Sitemap lên Google Search Console

1. Truy cập [Google Search Console](https://search.google.com/search-console)
2. Chọn property `xiaomi247.com`
3. Menu trái → **Sitemaps**
4. Nhập: `sitemap_index.xml` → Click **Submit**
5. Đợi vài phút → Kiểm tra Status: **Success**
6. Xem số URL discovered vs indexed

---

## 3. ROBOTS.TXT CONFIGURATION

### 3.1 Cấu hình qua Rank Math

**WP Admin → Rank Math → General Settings → Edit robots.txt:**

```
# ==============================================
# ROBOTS.TXT — XIAOMI247.COM (WordPress + WooCommerce)
# ==============================================

User-agent: *
Allow: /

# --- WooCommerce: Trang dynamic không cần index ---
Disallow: /cart/
Disallow: /gio-hang/
Disallow: /checkout/
Disallow: /thanh-toan/
Disallow: /my-account/
Disallow: /tai-khoan/
Disallow: /thank-you/

# --- WordPress: Trang admin & internal ---
Disallow: /wp-admin/
Allow: /wp-admin/admin-ajax.php
Disallow: /wp-login.php
Disallow: /wp-register.php

# --- Tham số filter/sort/search (tránh crawl waste) ---
Disallow: /*?s=
Disallow: /*?orderby=
Disallow: /*?filter_*
Disallow: /*?add-to-cart=
Disallow: /*?removed_item=
Disallow: /*?replytocom=

# --- Feed (tùy chọn — có thể Allow nếu muốn) ---
Disallow: /feed/
Disallow: /comments/feed/

# --- Sitemap ---
Sitemap: https://xiaomi247.com/sitemap_index.xml
```

### 3.3 Giải thích các rules quan trọng

| Rule | Mục đích |
|------|----------|
| `Allow: /wp-admin/admin-ajax.php` | Cho phép Google truy cập AJAX (cần cho render trang) |
| `Disallow: /*?add-to-cart=` | Ngăn crawl URL thêm giỏ hàng |
| `Disallow: /*?orderby=` | Ngăn crawl trang sort (duplicate content) |
| `Disallow: /*?filter_*` | Ngăn crawl trang filter (duplicate content) |
| `Disallow: /feed/` | Ngăn index RSS feed (tùy chọn) |

### 3.4 Kiểm tra robots.txt

1. Truy cập `https://xiaomi247.com/robots.txt` — xác nhận nội dung đúng
2. Google Search Console → **Settings** → **robots.txt** → Kiểm tra
3. Đảm bảo **KHÔNG** block CSS/JS (Google cần render trang để đánh giá)

---

## 4. GOOGLE SEARCH CONSOLE SETUP

### 4.1 Verify Domain (DNS TXT Record — Khuyến nghị)

**Bước 1:** Truy cập [Google Search Console](https://search.google.com/search-console)

**Bước 2:** Click **"Add Property"** → Chọn **"Domain"** → Nhập `xiaomi247.com`

**Bước 3:** Google cung cấp TXT record, ví dụ:
```
google-site-verification=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
```

**Bước 4:** Đăng nhập DNS provider (nơi quản lý domain):
1. Vào phần **DNS Management** / **DNS Records**
2. Thêm record mới:
   - Type: **TXT**
   - Host/Name: `@`
   - Value: `google-site-verification=XXXXXXX...` (paste từ bước 3)
   - TTL: **3600** (hoặc Auto)
3. Lưu lại

**Bước 5:** Quay lại GSC → Click **"Verify"**
- Có thể mất 5-60 phút để DNS propagate
- Nếu chưa verify được, đợi thêm và thử lại

> 💡 **Ưu điểm DNS verification:** Verify toàn bộ domain (bao gồm cả subdomain), không cần thêm code vào website.

### 4.2 Submit Sitemap

1. GSC → Menu trái → **Sitemaps**
2. Nhập URL: `sitemap_index.xml`
3. Click **Submit**
4. Kiểm tra status sau vài phút

### 4.3 Kiểm tra Coverage (Lập chỉ mục)

**GSC → Pages (Indexing):**

| Status | Hành động |
|--------|-----------|
| ✅ Valid | Trang đã được index — OK |
| ⚠️ Valid with warnings | Kiểm tra & fix warnings |
| ❌ Error | Fix ngay — trang quan trọng không được index |
| 🚫 Excluded | Kiểm tra — nếu là trang cần index thì fix |

**Các lỗi thường gặp & cách fix:**

| Lỗi | Nguyên nhân | Cách fix |
|-----|-------------|----------|
| Submitted URL has crawl issue | Server error hoặc timeout | Kiểm tra hosting, tăng PHP memory |
| Submitted URL marked 'noindex' | Có meta noindex | Bỏ noindex trong Rank Math |
| Redirect error | Redirect loop hoặc chain | Fix redirect (xem mục 6) |
| Soft 404 | Trang có nội dung quá ít | Thêm nội dung hoặc redirect |

### 4.4 Kiểm tra Mobile Usability

**GSC → Mobile Usability:**
- Đảm bảo **0 errors**
- Lỗi thường gặp: text quá nhỏ, clickable elements quá gần, content wider than screen
- Fix thông qua CSS responsive hoặc cấu hình Motta Theme

### 4.5 Core Web Vitals

**GSC → Core Web Vitals:**
- Kiểm tra cả **Mobile** và **Desktop**
- Mục tiêu: tất cả URLs ở trạng thái **Good**
- Nếu có URLs **Poor** hoặc **Needs Improvement**: xem chi tiết và tối ưu (tham khảo [Technical SEO Checklist — Core Web Vitals](../marketing/02-seo/technical-seo-checklist.md#4-core-web-vitals-optimization))

### 4.6 Thiết lập Email Notifications

**GSC → Settings → Email preferences:**
- ✅ Enable email notifications: **ON**
- Nhận thông báo khi:
  - Phát hiện lỗi crawl mới
  - Vấn đề Mobile Usability
  - Manual actions (Google penalty)
  - Security issues

### 4.7 Request Indexing cho trang quan trọng

1. GSC → URL Inspection (thanh tìm kiếm phía trên)
2. Nhập URL trang quan trọng (trang chủ, danh mục chính, sản phẩm hot)
3. Click **"Request Indexing"**
4. Giới hạn: ~10-12 requests/ngày

---

## 5. BING WEBMASTER TOOLS

### 5.1 Đăng ký & Import từ GSC

**Bước 1:** Truy cập [Bing Webmaster Tools](https://www.bing.com/webmasters)

**Bước 2:** Đăng nhập bằng Microsoft account

**Bước 3:** Chọn **"Import from Google Search Console"**
- Đăng nhập Google account
- Chọn property `xiaomi247.com`
- Bing sẽ tự động import cấu hình & verify

> 💡 Import từ GSC là cách nhanh nhất — không cần verify lại domain.

**Bước 4:** Sau khi import:
1. Kiểm tra sitemap đã được submit
2. Lấy **verification code** → Nhập vào Rank Math (General Settings → Webmaster Tools → Bing)

### 5.2 Cấu hình Bing Webmaster

- Submit sitemap (nếu chưa tự import): `https://xiaomi247.com/sitemap_index.xml`
- Kiểm tra **Site Scan** — fix các lỗi SEO được phát hiện
- Bật **Adaptive URL Submission** để tự động submit URL mới

---

## 6. 301 REDIRECTS

### 6.1 HTTP → HTTPS (Bắt buộc)

**Cách 1: Qua .htaccess (khuyến nghị)**

Thêm vào đầu file `.htaccess` (trước rules WordPress):

```apache
# Force HTTPS
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

**Cách 2: Qua hosting panel**
- Hầu hết hosting có option "Force HTTPS" trong SSL settings
- Bật option này nếu có

### 6.2 www → non-www (Chọn 1 phiên bản)

> Xiaomi247.com sử dụng phiên bản **non-www** (`https://xiaomi247.com`)

**Thêm vào .htaccess:**

```apache
# Redirect www to non-www
RewriteEngine On
RewriteCond %{HTTP_HOST} ^www\.xiaomi247\.com [NC]
RewriteRule ^(.*)$ https://xiaomi247.com/$1 [L,R=301]
```

### 6.3 Redirect qua Rank Math

**WP Admin → Rank Math → Redirections:**

1. Click **"Add New"**
2. Điền:
   - Source URL: `/url-cu/` (URL cũ)
   - Destination URL: `https://xiaomi247.com/url-moi/` (URL mới)
   - Redirection Type: **301 Permanent**
3. Click **"Add Redirection"**

**Ví dụ redirect thường gặp:**

| Source (URL cũ) | Destination (URL mới) | Lý do |
|-----------------|----------------------|-------|
| `/san-pham-cu/` | `/san-pham-moi/` | Đổi tên sản phẩm |
| `/danh-muc-cu/` | `/danh-muc-moi/` | Restructure danh mục |
| `/product/ten-san-pham/` | `/ten-san-pham/` | Đổi permalink structure |

### 6.4 Bật Auto-Detect 404 & Redirect

**Rank Math → Redirections → Settings:**
- ✅ Monitor: **ON** — tự động phát hiện 404
- ✅ Redirect: **ON** — gợi ý redirect cho 404 mới
- ✅ Log 404 errors: **ON** — lưu log để review

### 6.5 Tránh Redirect Chains

**Nguyên tắc:** Mỗi redirect chỉ nên có **1 hop** (A → B), KHÔNG nên A → B → C.

**Kiểm tra:**
1. Rank Math → Redirections → xem danh sách
2. Đảm bảo destination URL không phải là URL đã bị redirect
3. Dùng tool [Redirect Checker](https://httpstatus.io/) để kiểm tra

---

## 7. CUSTOM 404 PAGE

### 7.1 Tạo trang 404 trong WordPress

**Cách 1: Dùng Rank Math (Đơn giản)**

Rank Math không có tính năng tạo 404 page. Sử dụng cách 2.

**Cách 2: Chỉnh sửa Theme 404 Template**

**WP Admin → Appearance → Theme File Editor → 404.php**

> ⚠️ Nếu dùng Motta Theme, tạo **Child Theme** trước khi chỉnh sửa để tránh mất khi update theme.

Nội dung 404.php khuyến nghị:

```php
<?php get_header(); ?>

<div class="error-404 not-found" style="text-align: center; padding: 60px 20px; max-width: 600px; margin: 0 auto;">

    <h1 style="font-size: 72px; color: #ff6700; margin-bottom: 10px;">404</h1>
    <h2>Trang không tồn tại</h2>
    <p>Xin lỗi, trang bạn tìm kiếm không tồn tại hoặc đã được di chuyển.</p>

    <!-- Search Box -->
    <div style="margin: 30px 0;">
        <p><strong>Thử tìm kiếm sản phẩm:</strong></p>
        <?php get_search_form(); ?>
    </div>

    <!-- Navigation Links -->
    <div style="margin: 30px 0;">
        <p><strong>Hoặc truy cập:</strong></p>
        <ul style="list-style: none; padding: 0;">
            <li><a href="<?php echo home_url(); ?>">🏠 Trang chủ</a></li>
            <li><a href="<?php echo home_url('/shop/'); ?>">🛒 Cửa hàng</a></li>
            <li><a href="<?php echo home_url('/dien-thoai-xiaomi/'); ?>">📱 Điện thoại Xiaomi</a></li>
            <li><a href="<?php echo home_url('/tivi-xiaomi/'); ?>">📺 Tivi Xiaomi</a></li>
            <li><a href="<?php echo home_url('/lien-he/'); ?>">📞 Liên hệ hỗ trợ</a></li>
        </ul>
    </div>

    <!-- Popular Products -->
    <div style="margin: 30px 0;">
        <p><strong>Sản phẩm nổi bật:</strong></p>
        <?php echo do_shortcode('[products limit="4" columns="4" best_selling="true"]'); ?>
    </div>

</div>

<?php get_footer(); ?>
```

### 7.2 Kiểm tra trang 404

1. Truy cập URL không tồn tại: `https://xiaomi247.com/trang-khong-co-that/`
2. Xác nhận hiển thị trang 404 custom (không phải trang trắng hoặc lỗi server)
3. Kiểm tra:
   - ✅ Có search box
   - ✅ Có navigation links
   - ✅ Có link về trang chủ
   - ✅ HTTP status code trả về **404** (không phải 200)

### 7.3 Monitor 404 Errors

- **Rank Math → Redirections → 404 Monitor** — xem danh sách URL 404
- **Google Search Console → Pages** — filter "Not found (404)"
- Review hàng tuần, redirect các URL 404 quan trọng (có backlinks hoặc traffic)

---

## 8. CANONICAL URL CONFIGURATION

### 8.1 Cấu hình mặc định qua Rank Math

Rank Math tự động thêm canonical URL cho mọi trang. Kiểm tra:

**WP Admin → bất kỳ trang/sản phẩm → Rank Math SEO → Advanced:**
- ✅ Canonical URL: tự động điền URL chính của trang
- Chỉ thay đổi khi cần override (ví dụ: sản phẩm trùng lặp)

### 8.2 Canonical cho WooCommerce (Filter/Sort/Pagination)

**Vấn đề:** WooCommerce tạo nhiều URL trùng nội dung:
- `/tivi-xiaomi/?orderby=price` (sort theo giá)
- `/tivi-xiaomi/?filter_color=den` (filter theo màu)
- `/tivi-xiaomi/page/2/` (phân trang)

**Giải pháp — Rank Math xử lý tự động:**

| URL | Canonical | Giải thích |
|-----|-----------|------------|
| `/tivi-xiaomi/?orderby=price` | `/tivi-xiaomi/` | Sort → canonical về trang gốc |
| `/tivi-xiaomi/?filter_color=den` | `/tivi-xiaomi/` | Filter → canonical về trang gốc |
| `/tivi-xiaomi/page/2/` | `/tivi-xiaomi/page/2/` | Pagination → canonical chính nó |
| `http://xiaomi247.com/...` | `https://xiaomi247.com/...` | HTTP → HTTPS canonical |

> ✅ Rank Math xử lý đúng theo best practices của Google: trang phân trang canonical chính nó, trang filter/sort canonical về trang gốc.

### 8.3 Trailing Slash Consistency

**Nguyên tắc:** Chọn **CÓ trailing slash** (WordPress mặc định) và giữ nhất quán.

**WP Admin → Settings → Permalinks:**
- Cấu trúc: `/%postname%/` (có `/` cuối)
- Rank Math tự động canonical với trailing slash

**Kiểm tra:**
- `https://xiaomi247.com/tivi-xiaomi` → redirect 301 → `https://xiaomi247.com/tivi-xiaomi/`
- Tất cả internal links dùng trailing slash

### 8.4 Kiểm tra Canonical

1. Truy cập trang bất kỳ → View Page Source (Ctrl+U)
2. Tìm `<link rel="canonical"` → xác nhận URL đúng
3. Kiểm tra:
   - ✅ Canonical dùng HTTPS
   - ✅ Canonical có trailing slash nhất quán
   - ✅ Canonical không trỏ về trang khác (trừ khi cố ý)
   - ✅ Không có canonical loop

---

## 9. CRAWL OPTIMIZATION

### 9.1 Crawl Depth ≤ 3 Clicks

**Nguyên tắc:** Mọi trang quan trọng phải truy cập được trong **tối đa 3 clicks** từ trang chủ.

**Cấu trúc khuyến nghị:**

```
Trang chủ (0 click)
├── Danh mục chính (1 click) — Menu chính
│   ├── Sản phẩm (2 clicks) — Từ trang danh mục
│   │   └── Sản phẩm liên quan (3 clicks) — Related products
│   └── Danh mục con (2 clicks) — Subcategory
│       └── Sản phẩm (3 clicks)
├── Blog (1 click) — Menu chính
│   └── Bài viết (2 clicks)
└── Trang tĩnh (1 click) — Menu/Footer
```

**Cách đảm bảo:**
1. **Menu chính** chứa tất cả danh mục cấp 1
2. **Footer** chứa links đến trang quan trọng
3. **Breadcrumbs** bật qua Rank Math (đã cấu hình ở Plugin Setup)
4. **Related Products** hiển thị trên trang sản phẩm
5. **Internal linking** trong bài blog trỏ đến sản phẩm/danh mục

### 9.2 Fix Orphan Pages

**Orphan page** = trang không có internal link nào trỏ đến → Google khó phát hiện.

**Cách tìm:**
1. Dùng **Screaming Frog** (free cho ≤ 500 URLs):
   - Crawl `https://xiaomi247.com`
   - Tab **Inlinks** → filter trang có 0 inlinks
2. So sánh danh sách trang trong sitemap vs trang được crawl

**Cách fix:**
- Thêm internal link từ trang liên quan
- Thêm vào menu hoặc footer nếu quan trọng
- Nếu trang không cần thiết → noindex hoặc xóa

### 9.3 Broken Link Check

**Kiểm tra định kỳ (hàng tháng):**

1. **Rank Math → SEO Analysis** → chạy scan
2. **Screaming Frog** → crawl toàn site → filter Response Code 404
3. **Google Search Console → Pages** → filter errors

**Cách fix broken links:**
- Link nội bộ: cập nhật URL đúng hoặc tạo redirect 301
- Link ngoài: thay bằng URL mới hoặc xóa link

### 9.4 Crawl Budget Optimization

**Cho website nhỏ-vừa (<10.000 trang):** Crawl budget thường không phải vấn đề lớn. Tuy nhiên, vẫn nên:

- ✅ Loại bỏ trang trùng lặp (canonical + noindex)
- ✅ Robots.txt block trang không cần crawl (đã cấu hình ở mục 3)
- ✅ Fix tất cả redirect chains
- ✅ Đảm bảo server response time < 500ms
- ✅ Sitemap chỉ chứa URL cần index

---

## 📋 CHECKLIST TỔNG HỢP

Sau khi hoàn thành tất cả các bước trên, kiểm tra:

- [ ] Rank Math SEO cấu hình đầy đủ (Global Settings, Titles & Meta, Schema)
- [ ] Sitemap truy cập được tại `https://xiaomi247.com/sitemap_index.xml`
- [ ] Sitemap không chứa trang cart/checkout/account
- [ ] Robots.txt đúng format tại `https://xiaomi247.com/robots.txt`
- [ ] Google Search Console verified & sitemap submitted
- [ ] Bing Webmaster Tools đã import từ GSC
- [ ] HTTP → HTTPS redirect hoạt động
- [ ] www → non-www redirect hoạt động
- [ ] Trang 404 custom hiển thị đúng (có search, navigation, link trang chủ)
- [ ] Canonical URL đúng trên tất cả trang (kiểm tra view source)
- [ ] Trailing slash nhất quán
- [ ] Crawl depth ≤ 3 clicks cho trang quan trọng
- [ ] Không có broken internal links
- [ ] Email notifications GSC đã bật

---

*Technical SEO Setup — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Phiên bản: 1.0*

