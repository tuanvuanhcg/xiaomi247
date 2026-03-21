# 🚀 Khuyến nghị Kỹ thuật — Xiaomi247.com

> **Ngày tạo:** 21/03/2026
> **Phiên bản:** 1.0
> **Áp dụng cho:** WordPress + WooCommerce + Motta Theme

---

## 1. Caching & Performance

### 1.1 Plugin Caching

| Khuyến nghị | Chi tiết |
| --- | --- |
| Plugin đề xuất | **LiteSpeed Cache** (nếu hosting LiteSpeed) hoặc **WP Rocket** (premium) |
| Thay thế miễn phí | W3 Total Cache, WP Super Cache |
| Cấu hình | Page cache ON, Browser cache ON, Object cache ON |
| Database cache | Bật Redis hoặc Memcached (nếu hosting hỗ trợ) |

### 1.2 Cấu hình cụ thể

- ✅ Bật **Page Caching** — cache HTML tĩnh cho trang sản phẩm, danh mục
- ✅ Bật **Browser Caching** — set cache headers cho static assets (CSS, JS, images)
- ✅ Bật **Object Caching** — giảm database queries
- ✅ Exclude từ cache: trang cart, checkout, my-account (WooCommerce dynamic pages)
- ✅ Purge cache tự động khi cập nhật sản phẩm/giá

## 2. Image Optimization

### 2.1 Tối ưu hình ảnh sản phẩm

| Khuyến nghị | Chi tiết |
| --- | --- |
| Plugin đề xuất | **ShortPixel** hoặc **Imagify** hoặc **Smush Pro** |
| Format | Chuyển sang **WebP** (giảm 25-35% dung lượng so với JPEG) |
| Lazy Loading | Bật lazy loading cho tất cả hình ảnh dưới fold |
| Kích thước | Thumbnail: 300x300 · Product: 600x600 · Full: 1200x1200 |
| Nén | Lossy compression 80-85% quality — đủ cho e-commerce |

### 2.2 Checklist hình ảnh

- ✅ Nén tất cả hình ảnh hiện có (bulk optimize)
- ✅ Bật auto-optimize cho hình upload mới
- ✅ Bật WebP conversion
- ✅ Cấu hình responsive images (srcset)
- ✅ Đặt tên file ảnh có SEO (vd: `xiaomi-14-ultra-chinh-hang.webp`)
- ✅ Thêm alt text tiếng Việt cho tất cả ảnh sản phẩm

## 3. CDN (Content Delivery Network)

### 3.1 Lựa chọn CDN

| CDN | Giá | Phù hợp | Ghi chú |
| --- | --- | --- | --- |
| **Cloudflare** (Free) | Miễn phí | ✅ Khuyến nghị | Free plan đủ tốt, có WAF cơ bản |
| Cloudflare Pro | $20/tháng | Tốt hơn | Thêm image optimization, WAF nâng cao |
| BunnyCDN | ~$1/tháng | Budget thấp | Giá rẻ, tốc độ tốt ở Asia |
| KeyCDN | ~$4/tháng | Thay thế | Tốc độ tốt, dễ cài |

### 3.2 Cấu hình Cloudflare (đề xuất)

- ✅ Trỏ DNS qua Cloudflare
- ✅ Bật SSL mode: Full (Strict)
- ✅ Bật Auto Minify: CSS, JS, HTML
- ✅ Bật Brotli compression
- ✅ Page Rules: Cache everything cho static pages
- ✅ Cấu hình Bypass cache cho WooCommerce cart/checkout

## 4. SSL & Bảo mật

### 4.1 SSL

- ✅ Đảm bảo SSL certificate valid & auto-renew
- ✅ Force HTTPS redirect (tất cả HTTP → HTTPS)
- ✅ Kiểm tra mixed content (hình ảnh/scripts load qua HTTP)
- ✅ HSTS header enabled

### 4.2 Security Plugin

| Plugin | Chức năng |
| --- | --- |
| **Wordfence** (Free) | Firewall, malware scan, login security |
| **Sucuri** (thay thế) | WAF, DDoS protection, malware cleanup |

### 4.3 Security Checklist

- ✅ Đổi URL login mặc định (`/wp-admin` → URL tùy chỉnh)
- ✅ Bật 2FA cho tài khoản admin
- ✅ Giới hạn login attempts (max 5 lần/15 phút)
- ✅ Vô hiệu hóa XML-RPC (nếu không dùng)
- ✅ Vô hiệu hóa file editing trong WP Admin
- ✅ Cập nhật WordPress core, theme, plugins thường xuyên
- ✅ Xóa theme/plugin không sử dụng
- ✅ Backup tự động hàng ngày (UpdraftPlus hoặc BlogVault)
- ✅ Security headers: X-Frame-Options, X-Content-Type-Options, CSP

## 5. Mobile Optimization

### 5.1 Responsive Design

- ✅ Test tất cả breakpoints: 320px, 375px, 414px, 768px, 1024px, 1440px
- ✅ Kiểm tra touch targets ≥ 48x48px (Google recommendation)
- ✅ Kiểm tra font size ≥ 16px trên mobile (tránh auto-zoom)
- ✅ Kiểm tra hamburger menu hoạt động đúng
- ✅ Kiểm tra product gallery swipe trên mobile
- ✅ Kiểm tra checkout flow trên mobile

### 5.2 Mobile Performance

- ✅ Target: PageSpeed Mobile Score ≥ 70
- ✅ Critical CSS inline cho above-the-fold content
- ✅ Defer non-critical JS
- ✅ Preload key resources (fonts, hero image)
- ✅ Tối ưu Web Vitals: LCP < 2.5s, FID < 100ms, CLS < 0.1

## 6. Plugin Recommendations

### 6.1 Plugin cần thiết (Must-have)

| Plugin | Mục đích | Miễn phí? |
| --- | --- | --- |
| **Rank Math SEO** | SEO on-page, sitemap, schema | ✅ Free |
| **WP Rocket** hoặc **LiteSpeed Cache** | Caching & performance | 💰 / ✅ |
| **ShortPixel** | Image optimization & WebP | ✅ Free (100 imgs/tháng) |
| **Wordfence** | Security & firewall | ✅ Free |
| **UpdraftPlus** | Backup tự động | ✅ Free |
| **Loco Translate** | Việt hóa theme & plugins | ✅ Free |
| **Contact Form 7** hoặc **WPForms** | Form liên hệ | ✅ Free |

### 6.2 Plugin khuyến nghị thêm

| Plugin | Mục đích | Miễn phí? |
| --- | --- | --- |
| **WooCommerce Product Filter** | Lọc sản phẩm nâng cao | 💰 Premium |
| **YITH WooCommerce Wishlist** | Danh sách yêu thích | ✅ Free |
| **WooCommerce Currency Switcher** | Hiển thị giá VNĐ đẹp | ✅ Free |
| **Tidio** hoặc **Zalo Chat** | Live chat hỗ trợ | ✅ Free |
| **MonsterInsights** | GA4 dashboard trong WP | ✅ Free |
| **Schema Pro** | Rich snippets cho sản phẩm | 💰 Premium |

### 6.3 Plugin cần kiểm tra & xóa

- ⚠️ Xóa tất cả plugin không sử dụng (giảm attack surface)
- ⚠️ Kiểm tra plugin conflict (deactivate từng plugin để test)
- ⚠️ Không cài quá 20-25 plugin (ảnh hưởng performance)
- ⚠️ Chỉ dùng plugin từ nguồn uy tín (WordPress.org, ThemeForest, CodeCanyon)



## 7. SEO Kỹ thuật

### 7.1 On-page SEO

- ✅ Cài & cấu hình Rank Math SEO
- ✅ Tạo XML Sitemap và submit lên Google Search Console
- ✅ Cấu hình robots.txt (block admin, cart, checkout)
- ✅ Schema markup: Product, Organization, BreadcrumbList
- ✅ Canonical URLs cho tất cả trang
- ✅ Meta title format: `{Tên SP} - Chính hãng | Xiaomi247`
- ✅ Meta description: mỗi sản phẩm có mô tả riêng 120-160 ký tự

### 7.2 Technical SEO

- ✅ Đăng ký Google Search Console
- ✅ Đăng ký Bing Webmaster Tools
- ✅ Kiểm tra & fix broken links (plugin Broken Link Checker)
- ✅ Redirect 301 cho các URL cũ/lỗi
- ✅ Cấu hình hreflang (nếu có multi-language)
- ✅ Tối ưu URL structure: `xiaomi247.com/san-pham/ten-san-pham`

## 8. Monitoring & Analytics

### 8.1 Công cụ giám sát

| Công cụ | Mục đích | Giá |
| --- | --- | --- |
| Google Analytics 4 | Traffic, conversion tracking | Miễn phí |
| Google Search Console | SEO monitoring, indexing | Miễn phí |
| UptimeRobot | Giám sát uptime 24/7 | Miễn phí (50 monitors) |
| GTmetrix | Performance monitoring | Miễn phí |

### 8.2 GA4 Enhanced E-commerce

- ✅ Bật Enhanced E-commerce tracking
- ✅ Track: view_item, add_to_cart, begin_checkout, purchase
- ✅ Cấu hình conversion goals
- ✅ Kết nối Google Ads (nếu chạy ads)

## 9. Lộ trình thực hiện

| Giai đoạn | Thời gian | Công việc | Priority |
| --- | --- | --- | --- |
| **Phase 1** | Tuần 1 | Fix bugs critical (404, demo text, menu) | 🔴 |
| **Phase 2** | Tuần 2 | Việt hóa + tạo trang nội dung | 🟠 |
| **Phase 3** | Tuần 3 | Cài plugin (SEO, cache, security, backup) | 🟠 |
| **Phase 4** | Tuần 4 | Image optimization + CDN setup | 🟡 |
| **Phase 5** | Tuần 5-6 | Mobile optimization + performance tuning | 🟡 |
| **Phase 6** | Ongoing | Monitoring, updates, content | 🟢 |

## 10. Ước tính chi phí

| Hạng mục | Chi phí/năm | Ghi chú |
| --- | --- | --- |
| Hosting (tốt) | 2-5 triệu VNĐ | Shared → VPS nếu traffic cao |
| Domain | ~300.000 VNĐ | Gia hạn hàng năm |
| SSL | Miễn phí | Let's Encrypt hoặc Cloudflare |
| WP Rocket | ~1.2 triệu VNĐ | Hoặc dùng LiteSpeed Cache miễn phí |
| ShortPixel | Miễn phí – 500K | Tùy số lượng ảnh |
| Rank Math Pro | ~1.5 triệu VNĐ | Hoặc dùng bản Free |
| Cloudflare | Miễn phí | Free plan đủ dùng |
| **Tổng ước tính** | **2-8 triệu VNĐ/năm** | Phần lớn dùng giải pháp miễn phí |

---

*Khuyến nghị Kỹ thuật — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Phiên bản: 1.0*