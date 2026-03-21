# XIAOMI247.COM — TECHNICAL SEO CHECKLIST

> **Mục tiêu:** Đảm bảo website được Google crawl & index tối ưu
> **Áp dụng cho:** xiaomi247.com (Haravan/WordPress/Custom)
> **Cập nhật:** Tháng 3/2026

---

## 1. SITEMAP.XML SETUP

- [ ] Tạo sitemap.xml tại `https://xiaomi247.com/sitemap.xml`
- [ ] Sitemap chứa tất cả trang quan trọng (sản phẩm, danh mục, blog)
- [ ] Loại bỏ trang không cần index (thank you, cart, checkout)
- [ ] Sitemap tự động cập nhật khi thêm/xoá trang
- [ ] Kích thước sitemap < 50MB, tối đa 50.000 URLs/file
- [ ] Nếu > 50.000 URLs: tạo sitemap index chia theo loại trang
- [ ] Submit sitemap trong Google Search Console
- [ ] Kiểm tra sitemap không chứa URL bị redirect hoặc 404

### Cấu trúc sitemap khuyến nghị
```
sitemap.xml (index)
├── sitemap-pages.xml (trang tĩnh: trang chủ, giới thiệu, liên hệ)
├── sitemap-categories.xml (trang danh mục sản phẩm)
├── sitemap-products.xml (trang sản phẩm)
└── sitemap-blog.xml (bài viết blog)
```

---

## 2. ROBOTS.TXT CONFIGURATION

- [ ] Tạo robots.txt tại `https://xiaomi247.com/robots.txt`
- [ ] Allow Googlebot crawl tất cả trang quan trọng
- [ ] Disallow các trang không cần index
- [ ] Khai báo sitemap trong robots.txt

### Mẫu robots.txt
```
User-agent: *
Allow: /

Disallow: /cart/
Disallow: /checkout/
Disallow: /account/
Disallow: /search?
Disallow: /admin/
Disallow: /*?sort=
Disallow: /*?filter=
Disallow: /*?page=2
Disallow: /thank-you/

Sitemap: https://xiaomi247.com/sitemap.xml
```

---

## 3. GOOGLE SEARCH CONSOLE SETUP

- [ ] Verify domain qua DNS TXT record (ưu tiên) hoặc HTML tag
- [ ] Submit sitemap.xml
- [ ] Kiểm tra tab "Coverage" — fix tất cả errors
- [ ] Kiểm tra tab "Mobile Usability" — fix tất cả issues
- [ ] Đăng ký cả 2 phiên bản: `www` và `non-www` → set preferred
- [ ] Kiểm tra "Core Web Vitals" report
- [ ] Thiết lập email notifications cho critical issues
- [ ] Request indexing cho các trang quan trọng mới

---

## 4. CORE WEB VITALS OPTIMIZATION

### Chỉ số mục tiêu

| Metric | Mục tiêu | Đo bằng |
|--------|----------|---------|
| LCP (Largest Contentful Paint) | < 2.5s | PageSpeed Insights |
| INP (Interaction to Next Paint) | < 200ms | PageSpeed Insights |
| CLS (Cumulative Layout Shift) | < 0.1 | PageSpeed Insights |

### Checklist tối ưu

**LCP — Tốc độ tải nội dung chính:**
- [ ] Tối ưu hình ảnh: WebP format, lazy loading, responsive images
- [ ] Sử dụng CDN cho static assets (Cloudflare/BunnyCDN)
- [ ] Preload font chữ & ảnh hero banner
- [ ] Minify CSS/JS, loại bỏ code không dùng
- [ ] Enable server-side caching (page cache, browser cache)
- [ ] Compress với Gzip/Brotli

**INP — Tương tác mượt mà:**
- [ ] Defer JavaScript không critical
- [ ] Tối ưu third-party scripts (chat widget, analytics)
- [ ] Tránh long tasks > 50ms trên main thread

**CLS — Ổn định layout:**
- [ ] Khai báo width/height cho tất cả ảnh & video
- [ ] Đặt kích thước cố định cho ad slots & banner
- [ ] Tránh inject nội dung động phía trên fold
- [ ] Sử dụng font-display: swap cho web fonts

---

## 5. MOBILE-FIRST INDEXING

- [ ] Website responsive, hiển thị tốt trên mobile
- [ ] Nội dung mobile = nội dung desktop (không ẩn nội dung trên mobile)
- [ ] Structured data có trên cả mobile & desktop
- [ ] Hình ảnh có alt text trên cả 2 phiên bản
- [ ] Font size tối thiểu 16px trên mobile
- [ ] Touch targets (nút bấm) tối thiểu 48x48px
- [ ] Không sử dụng Flash hoặc plugin cũ
- [ ] Viewport meta tag: `<meta name="viewport" content="width=device-width, initial-scale=1">`
- [ ] Test trên Google Mobile-Friendly Test tool

---

## 6. CANONICAL URLs

- [ ] Mỗi trang có thẻ `<link rel="canonical" href="...">` trỏ về URL chính
- [ ] Trang phân trang (page 2, 3...) canonical về chính nó (KHÔNG về page 1)
- [ ] URL có tham số filter/sort canonical về URL gốc không tham số
- [ ] Kiểm tra không có canonical loop (A → B → A)
- [ ] HTTPS canonical (không phải HTTP)
- [ ] Trailing slash nhất quán (chọn có hoặc không, giữ thống nhất)

### Ví dụ canonical
```html
<!-- Trang danh mục -->
<link rel="canonical" href="https://xiaomi247.com/tivi-xiaomi/" />

<!-- Trang filter → canonical về trang gốc -->
<!-- URL: /tivi-xiaomi/?sort=price -->
<link rel="canonical" href="https://xiaomi247.com/tivi-xiaomi/" />

<!-- Trang phân trang → canonical chính nó -->
<!-- URL: /tivi-xiaomi/?page=2 -->
<link rel="canonical" href="https://xiaomi247.com/tivi-xiaomi/?page=2" />
```

---

## 7. HREFLANG (Nếu cần)

- [ ] Hiện tại: **KHÔNG CẦN** — website chỉ phục vụ thị trường Việt Nam
- [ ] Nếu tương lai mở rộng sang tiếng Anh hoặc thị trường khác:
  - Thêm `<link rel="alternate" hreflang="vi" href="..." />`
  - Thêm `<link rel="alternate" hreflang="x-default" href="..." />`
- [ ] Đảm bảo hreflang tags có trên cả 2 phiên bản ngôn ngữ (bidirectional)

---

## 8. 301 REDIRECTS & XỬ LÝ TRANG 404

### 301 Redirects
- [ ] Thiết lập 301 redirect cho tất cả URL cũ → URL mới
- [ ] Redirect HTTP → HTTPS (toàn site)
- [ ] Redirect www → non-www (hoặc ngược lại, chọn 1)
- [ ] Kiểm tra không có redirect chains (A → B → C, tối đa 1 hop)
- [ ] Redirect trailing slash nhất quán

### Trang 404
- [ ] Tạo trang 404 custom thân thiện (không dùng mặc định server)
- [ ] Trang 404 có navigation links, search box, link về trang chủ
- [ ] Monitor 404 errors trong Google Search Console hàng tuần
- [ ] Fix hoặc redirect các trang 404 quan trọng (có backlinks hoặc traffic)

### Mẫu redirect thường gặp
```
# .htaccess hoặc cấu hình server
/san-pham/cu/ → /san-pham/moi/ (301)
/trang-khong-con/ → /danh-muc-phu-hop/ (301)
http://xiaomi247.com/* → https://xiaomi247.com/* (301)
www.xiaomi247.com/* → xiaomi247.com/* (301)
```

---

## 9. CHECKLIST BỔ SUNG

### Security & HTTPS
- [ ] SSL certificate hợp lệ (Let's Encrypt hoặc premium)
- [ ] Toàn bộ resources tải qua HTTPS (không mixed content)
- [ ] HSTS header enabled

### Crawl Efficiency
- [ ] Kiểm tra crawl budget — loại bỏ trang trùng lặp
- [ ] Fix broken internal links (dùng Screaming Frog scan hàng tháng)
- [ ] Tối ưu crawl depth: mọi trang quan trọng ≤ 3 clicks từ trang chủ
- [ ] Loại bỏ orphan pages (trang không có internal link nào trỏ đến)

### Indexing
- [ ] Kiểm tra `noindex` tags — chỉ áp dụng cho trang không cần index
- [ ] Không block CSS/JS trong robots.txt (Google cần render trang)
- [ ] Kiểm tra số trang index trong GSC khớp với sitemap

### Monitoring (Hàng tháng)
- [ ] Chạy Screaming Frog full crawl
- [ ] Kiểm tra Google Search Console errors
- [ ] Đo Core Web Vitals qua PageSpeed Insights
- [ ] Kiểm tra uptime & server response time
- [ ] Review 404 errors & redirect chains

