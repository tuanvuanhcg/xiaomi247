# 🔒 Hướng dẫn Bảo mật — Xiaomi247.com

> **Ngày tạo:** 21/03/2026
> **Phiên bản:** 1.0
> **Áp dụng cho:** WordPress + WooCommerce + Motta Theme
> **Tham chiếu:** [Khuyến nghị Kỹ thuật — Phần 4](../marketing/01-technical-audit/technical-recommendations.md)

---

## Mục lục

1. [SSL/HTTPS](#1-sslhttps)
2. [WordPress Hardening](#2-wordpress-hardening)
3. [Wordfence Configuration](#3-wordfence-configuration)
4. [Security Headers](#4-security-headers)
5. [Backup Strategy](#5-backup-strategy)
6. [Update Policy](#6-update-policy)
7. [Security Audit Checklist](#7-security-audit-checklist-hàng-tháng)
8. [Incident Response Plan](#8-incident-response-plan)

---

## 1. SSL/HTTPS

### 1.1 Kiểm tra SSL Certificate

| Hạng mục | Yêu cầu | Công cụ kiểm tra |
| --- | --- | --- |
| Certificate hợp lệ | Valid, chưa hết hạn | [SSL Labs](https://www.ssllabs.com/ssltest/) |
| Auto-renew | Bật tự động gia hạn | Kiểm tra hosting panel |
| Grade | Đạt A hoặc A+ | SSL Labs Test |
| Certificate chain | Đầy đủ intermediate certs | SSL Labs Test |

**Đề xuất:** Sử dụng Let's Encrypt (miễn phí) hoặc SSL từ Cloudflare.

### 1.2 Force HTTPS Redirect

Thêm vào file `.htaccess` (Apache):

```apache
# Force HTTPS
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

Hoặc thêm vào `wp-config.php`:

```php
define('FORCE_SSL_ADMIN', true);

// Nếu đứng sau reverse proxy (Cloudflare)
if (isset($_SERVER['HTTP_X_FORWARDED_PROTO']) && $_SERVER['HTTP_X_FORWARDED_PROTO'] === 'https') {
    $_SERVER['HTTPS'] = 'on';
}
```

### 1.3 HSTS Header

Thêm vào `.htaccess`:

```apache
# HSTS - Strict Transport Security (1 năm)
Header always set Strict-Transport-Security "max-age=31536000; includeSubDomains; preload"
```

> ⚠️ **Lưu ý:** Chỉ bật HSTS sau khi đã xác nhận HTTPS hoạt động hoàn hảo. Sau khi bật, trình duyệt sẽ từ chối kết nối HTTP trong thời gian `max-age`.

### 1.4 Kiểm tra Mixed Content

1. Mở Chrome DevTools → Console → tìm lỗi "Mixed Content"
2. Sử dụng plugin **Really Simple SSL** để tự động fix
3. Kiểm tra thủ công:
   - Hình ảnh sản phẩm
   - CSS/JS từ bên thứ ba
   - Iframe nhúng (YouTube, Google Maps)
   - Font từ Google Fonts

**Công cụ kiểm tra:** [Why No Padlock](https://www.whynopadlock.com/) hoặc [JitBit SSL Check](https://www.jitbit.com/sslcheck/)

---

## 2. WordPress Hardening

### 2.1 Đổi URL Login

**Plugin:** WPS Hide Login (miễn phí)

1. Cài đặt: Plugins → Add New → tìm "WPS Hide Login"
2. Vào Settings → WPS Hide Login
3. Đổi Login URL: `/wp-admin` → URL tùy chỉnh (ví dụ: `/xm247-admin`)
4. Đặt Redirection URL: `/404` (khi truy cập `/wp-admin` sẽ redirect về 404)

> ⚠️ **Quan trọng:** Ghi nhớ URL mới. Nếu quên, vô hiệu hóa plugin qua FTP.

### 2.2 Vô hiệu hóa XML-RPC

XML-RPC là mục tiêu phổ biến cho brute force attacks. Thêm vào `.htaccess`:

```apache
# Block XML-RPC
<Files xmlrpc.php>
    Order Deny,Allow
    Deny from all
</Files>
```

Hoặc thêm vào `functions.php` của child theme:

```php
// Disable XML-RPC
add_filter('xmlrpc_enabled', '__return_false');

// Remove XML-RPC from HTTP headers
add_filter('wp_headers', function($headers) {
    unset($headers['X-Pingback']);
    return $headers;
});
```

### 2.3 Vô hiệu hóa File Editing

Thêm vào `wp-config.php`:

```php
// Disable file editing in WP Admin (Appearance → Theme Editor, Plugins → Plugin Editor)
define('DISALLOW_FILE_EDIT', true);

// Optional: Disable plugin/theme installation & updates qua admin
// define('DISALLOW_FILE_MODS', true);
```

### 2.4 Giới hạn Login Attempts

**Plugin:** Wordfence (đã bao gồm) hoặc **Limit Login Attempts Reloaded**

Cấu hình khuyến nghị:

| Thiết lập | Giá trị |
| --- | --- |
| Số lần thử tối đa | 5 lần |
| Thời gian khóa | 15 phút |
| Sau N lần khóa | Khóa 24 giờ |
| Thông báo email | Sau 3 lần khóa |

### 2.5 Chính sách Mật khẩu

- ✅ Mật khẩu tối thiểu **12 ký tự**
- ✅ Bao gồm: chữ hoa, chữ thường, số, ký tự đặc biệt
- ✅ Bật **2FA** (Two-Factor Authentication) cho tất cả tài khoản admin

---

## 3. Wordfence Configuration

### 3.1 Cài đặt & Kích hoạt

1. Plugins → Add New → tìm "Wordfence Security"
2. Cài đặt & kích hoạt
3. Nhập email nhận thông báo bảo mật
4. Chọn Free license (đủ cho hầu hết website)

### 3.2 Firewall Rules

Vào Wordfence → Firewall → Manage Firewall:

| Rule | Thiết lập | Mô tả |
| --- | --- | --- |
| Web Application Firewall | **Enabled & Protecting** | Chặn các attack patterns phổ biến |
| Brute Force Protection | **ON** | Chống brute force login |
| Rate Limiting | **ON** | Giới hạn request/phút |
| Block fake Googlebots | **ON** | Chặn bot giả mạo Google |
| Block requests with blank User-Agent | **ON** | Chặn request không có UA |

**Cấu hình Rate Limiting chi tiết:**

| Thiết lập | Giá trị |
| --- | --- |
| Requests/phút (bất kỳ ai) | Throttle sau 240 requests |
| Requests/phút (crawlers) | Throttle sau 120 requests |
| Pages/phút (bất kỳ ai) | Throttle sau 120 pages |
| Pages/phút (crawlers) | Throttle sau 60 pages |
| 404s/phút | Block sau 30 lần |
| Hành động khi vi phạm | Block 5 phút |

**Cấu hình Brute Force Protection:**

| Thiết lập | Giá trị |
| --- | --- |
| Lock out after failures | 5 lần |
| Lock out after forgot password attempts | 5 lần |
| Count failures over | 4 giờ |
| Lock out duration | 4 giờ |
| Immediately lock out invalid usernames | ✅ ON |
| Prevent discovery of usernames | ✅ ON |
| Block IPs that send POST with blank User-Agent & Referer | ✅ ON |

### 3.3 Scan Schedule

Vào Wordfence → Scan → Manage Scan:

| Thiết lập | Giá trị |
| --- | --- |
| Scan type | Standard Scan |
| Lịch scan | **Hàng tuần** (Chủ nhật, 3:00 AM) |
| Scan core files | ✅ ON |
| Scan theme files | ✅ ON |
| Scan plugin files | ✅ ON |
| Scan for malware signatures | ✅ ON |
| Check files against WordPress.org | ✅ ON |
| Scan outside WordPress installation | ✅ ON |
| Scan images, binary, and other files | ✅ ON |
| Check password strength | ✅ ON |

### 3.4 Email Alerts

Vào Wordfence → All Options → Email Alert Preferences:

| Alert | Bật/Tắt |
| --- | --- |
| Email khi IP bị block | ✅ ON |
| Email khi user bị lock out | ✅ ON |
| Email khi phát hiện malware | ✅ ON |
| Email khi có admin login | ✅ ON |
| Email khi Wordfence bị deactivate | ✅ ON |
| Email khi WordPress update available | ✅ ON |
| Email khi plugin update available | ✅ ON |
| Maximum email alerts/giờ | 10 |

**Email nhận alert:** Sử dụng email riêng cho security (ví dụ: `security@xiaomi247.com`)

### 3.5 Country Blocking (Tùy chọn)

> **Lưu ý:** Chỉ áp dụng nếu website chỉ phục vụ khách hàng Việt Nam.

Nếu cần, vào Wordfence → Firewall → Blocking:
- Block tất cả quốc gia **ngoại trừ**: Việt Nam, Singapore, Mỹ (cho Google/APIs)
- Hoặc chỉ block các quốc gia có nhiều attack: Nga, Trung Quốc, Ukraine, Brazil

> ⚠️ Country blocking có thể ảnh hưởng đến SEO nếu block Googlebot. Cần whitelist Google IPs.

---

## 4. Security Headers

### 4.1 Thêm qua .htaccess

Thêm vào file `.htaccess` (trước `# BEGIN WordPress`):

```apache
# ===== SECURITY HEADERS =====

# Chống clickjacking - không cho phép nhúng site trong iframe
Header always set X-Frame-Options "SAMEORIGIN"

# Chống MIME-type sniffing
Header always set X-Content-Type-Options "nosniff"

# Chống XSS (trình duyệt cũ)
Header always set X-XSS-Protection "1; mode=block"

# Referrer Policy - chỉ gửi origin khi cross-origin
Header always set Referrer-Policy "strict-origin-when-cross-origin"

# Permissions Policy - giới hạn browser features
Header always set Permissions-Policy "camera=(), microphone=(), geolocation=(self), payment=(self)"

# Content-Security-Policy
Header always set Content-Security-Policy "\
  default-src 'self'; \
  script-src 'self' 'unsafe-inline' 'unsafe-eval' https://www.googletagmanager.com https://www.google-analytics.com https://connect.facebook.net https://sp.zalo.me; \
  style-src 'self' 'unsafe-inline' https://fonts.googleapis.com; \
  img-src 'self' data: https: blob:; \
  font-src 'self' https://fonts.gstatic.com data:; \
  connect-src 'self' https://www.google-analytics.com https://region1.google-analytics.com; \
  frame-src 'self' https://www.youtube.com https://www.google.com; \
  object-src 'none'; \
  base-uri 'self'; \
  form-action 'self' https://checkout.payments.google.com; \
"
```

> ⚠️ **Quan trọng:** CSP cần được test kỹ. Bắt đầu với `Content-Security-Policy-Report-Only` trước, kiểm tra Console cho violations, rồi mới chuyển sang enforce.

### 4.2 Thêm qua Plugin (thay thế)

**Plugin:** Headers Security Advanced & HSTS WP

1. Cài đặt plugin
2. Vào Settings → Headers Security
3. Bật từng header theo bảng trên
4. Ưu điểm: không cần chỉnh `.htaccess`, dễ quản lý

### 4.3 Kiểm tra Security Headers

- **Công cụ:** [SecurityHeaders.com](https://securityheaders.com/)
- **Mục tiêu:** Đạt grade **A** hoặc **A+**
- **Kiểm tra sau khi cấu hình:** Đảm bảo website vẫn hoạt động bình thường (không bị block scripts/styles)

---

## 5. Backup Strategy

### 5.1 Plugin: UpdraftPlus

**Cài đặt:**
1. Plugins → Add New → "UpdraftPlus"
2. Vào Settings → UpdraftPlus Backups

### 5.2 Lịch Backup

| Loại | Tần suất | Giữ lại |
| --- | --- | --- |
| **Database** | Hàng ngày (2:00 AM) | 14 bản gần nhất |
| **Files** (themes, plugins, uploads) | Hàng tuần (Chủ nhật, 2:00 AM) | 4 bản gần nhất |
| **Full backup** (trước khi update) | Thủ công | Giữ đến khi xác nhận ổn định |

### 5.3 Offsite Storage

| Dịch vụ | Miễn phí | Khuyến nghị |
| --- | --- | --- |
| **Google Drive** | 15 GB | ✅ Đề xuất (dễ cài, đủ dung lượng) |
| Dropbox | 2 GB | Dung lượng hạn chế |
| Amazon S3 | Pay-as-you-go | Cho website lớn |
| Email | Tùy provider | Chỉ cho database nhỏ |

**Cấu hình Google Drive:**
1. Trong UpdraftPlus → Settings → chọn Google Drive
2. Authenticate với tài khoản Google
3. Chọn folder lưu backup
4. Test backup thử 1 lần

### 5.4 Retention Policy

```
Backup hàng ngày (DB):     Giữ 14 ngày → tự động xóa bản cũ
Backup hàng tuần (Files):  Giữ 4 tuần → tự động xóa bản cũ
Backup trước update:       Giữ thủ công → xóa sau 30 ngày nếu ổn định
Backup hàng tháng (Full):  Giữ 3 tháng → archive quan trọng
```

### 5.5 Hướng dẫn Restore

**Trường hợp 1: Restore từ UpdraftPlus Dashboard**

1. Vào Settings → UpdraftPlus Backups
2. Tab "Existing Backups" → chọn bản backup cần restore
3. Click "Restore" → chọn thành phần cần restore:
   - ✅ Plugins
   - ✅ Themes
   - ✅ Uploads
   - ✅ Others
   - ✅ Database
4. Xác nhận → đợi quá trình hoàn tất
5. Kiểm tra website sau khi restore

**Trường hợp 2: Restore khi không truy cập được WP Admin**

1. Truy cập hosting panel (cPanel/DirectAdmin)
2. Vào File Manager → `wp-content/updraft/`
3. Upload file backup (nếu chưa có trên server)
4. Cài lại WordPress fresh
5. Cài UpdraftPlus
6. Vào UpdraftPlus → Rescan local folder → Restore

**Trường hợp 3: Restore Database thủ công**

1. Truy cập phpMyAdmin qua hosting panel
2. Chọn database của website
3. Import file `.sql.gz` từ backup
4. Kiểm tra `wp-config.php` có đúng thông tin database

> ⚠️ **Test restore định kỳ:** Mỗi quý, thực hiện test restore trên staging environment để đảm bảo backup hoạt động.

---

## 6. Update Policy

### 6.1 Quy trình cập nhật an toàn

```
┌─────────────────────────────────────────────────────┐
│  QUY TRÌNH CẬP NHẬT WORDPRESS AN TOÀN              │
│                                                     │
│  1. Backup đầy đủ (DB + Files)                      │
│  2. Test trên Staging (nếu có)                      │
│  3. Cập nhật trên Production                        │
│  4. Kiểm tra website                                │
│  5. Rollback nếu có lỗi                             │
└─────────────────────────────────────────────────────┘
```

### 6.2 Thứ tự cập nhật

| Bước | Hành động | Ghi chú |
| --- | --- | --- |
| 1 | **Backup** đầy đủ | UpdraftPlus → Backup Now |
| 2 | Cập nhật **Plugins** | Từng plugin một, kiểm tra sau mỗi plugin |
| 3 | Cập nhật **Theme** | Kiểm tra giao diện sau khi update |
| 4 | Cập nhật **WordPress Core** | Cuối cùng, sau khi plugins/theme đã tương thích |
| 5 | Cập nhật **PHP version** | Chỉ khi hosting hỗ trợ & đã test |

### 6.3 Lịch cập nhật

| Loại | Tần suất | Ai thực hiện |
| --- | --- | --- |
| Security patches (critical) | **Ngay lập tức** (trong 24h) | Admin |
| Plugin updates | Hàng tuần (Thứ 3) | Admin |
| Theme updates | Hàng tháng | Admin |
| WordPress core (minor) | Tự động | WordPress auto-update |
| WordPress core (major) | Thủ công, sau khi test | Admin |
| PHP version | Mỗi 6-12 tháng | Admin + Hosting |

### 6.4 Staging Environment

**Khuyến nghị:** Tạo staging site để test trước khi update production.

- Nhiều hosting cung cấp staging miễn phí (SiteGround, WP Engine, Cloudways)
- Hoặc dùng plugin **WP Staging** (miễn phí)
- Quy trình: Clone production → Test update trên staging → Nếu OK → Update production

### 6.5 Checklist trước khi Update

- [ ] Đã backup đầy đủ (DB + Files)
- [ ] Đã kiểm tra changelog của bản update
- [ ] Đã kiểm tra compatibility với PHP version hiện tại
- [ ] Đã kiểm tra compatibility giữa plugins
- [ ] Đã test trên staging (nếu major update)
- [ ] Đã thông báo team (nếu có)
- [ ] Thời điểm update: ngoài giờ cao điểm (tránh 9-21h)

---

## 7. Security Audit Checklist (Hàng tháng)

> **Lịch:** Chạy vào ngày 1 hàng tháng. Ghi kết quả vào log.

### 7.1 SSL & HTTPS

- [ ] SSL certificate còn hạn (kiểm tra ngày hết hạn)
- [ ] SSL Labs grade ≥ A
- [ ] Không có mixed content warnings
- [ ] HSTS header hoạt động

### 7.2 WordPress Core

- [ ] WordPress đang chạy phiên bản mới nhất
- [ ] Tất cả plugins đã cập nhật
- [ ] Theme đã cập nhật
- [ ] PHP version được hỗ trợ (≥ 8.1)
- [ ] Không có plugin/theme không sử dụng
- [ ] File editing đã bị vô hiệu hóa
- [ ] XML-RPC đã bị vô hiệu hóa
- [ ] Debug mode đã tắt trên production

### 7.3 User Accounts

- [ ] Không có tài khoản admin không cần thiết
- [ ] Tất cả admin accounts có 2FA
- [ ] Không có user nào dùng username "admin"
- [ ] Mật khẩu đủ mạnh (kiểm tra qua Wordfence)
- [ ] Review user roles (không ai có quyền cao hơn cần thiết)

### 7.4 Wordfence & Security

- [ ] Wordfence firewall đang hoạt động (Enabled & Protecting)
- [ ] Scan gần nhất không có malware
- [ ] Kiểm tra Wordfence logs — có IP đáng ngờ không?
- [ ] Rate limiting đang hoạt động
- [ ] Email alerts đang gửi đúng

### 7.5 Backup

- [ ] Backup tự động đang chạy đúng lịch
- [ ] Backup gần nhất thành công
- [ ] Offsite storage có đủ dung lượng
- [ ] Test restore (mỗi quý)

### 7.6 Security Headers

- [ ] SecurityHeaders.com grade ≥ A
- [ ] CSP không có violations trong Console
- [ ] Tất cả headers đang hoạt động

### 7.7 File System

- [ ] Kiểm tra file permissions (wp-config.php: 400 hoặc 440)
- [ ] Không có file lạ trong thư mục root
- [ ] Không có file lạ trong `wp-content/uploads/`
- [ ] `.htaccess` không bị thay đổi bất thường
- [ ] `wp-config.php` không bị thay đổi bất thường

### 7.8 Database

- [ ] Database prefix không phải `wp_` (nếu cài mới)
- [ ] Không có user lạ trong database
- [ ] Optimize database (WP-Optimize plugin)

---

## 8. Incident Response Plan

### 8.1 Dấu hiệu bị hack

| Dấu hiệu | Mức độ | Hành động |
| --- | --- | --- |
| Website redirect sang trang lạ | 🔴 Critical | Xử lý ngay |
| Google cảnh báo "This site may be hacked" | 🔴 Critical | Xử lý ngay |
| File lạ xuất hiện trên server | 🔴 Critical | Xử lý ngay |
| Admin không login được | 🟠 High | Kiểm tra ngay |
| Website chậm bất thường | 🟡 Medium | Kiểm tra trong 24h |
| Email spam gửi từ server | 🔴 Critical | Xử lý ngay |
| Wordfence alert malware | 🔴 Critical | Xử lý ngay |
| Nội dung lạ xuất hiện trên website | 🟠 High | Kiểm tra ngay |

### 8.2 Quy trình xử lý (Step-by-step)

```
BƯỚC 1: CÁCH LY (trong 30 phút đầu)
├── Bật maintenance mode
├── Đổi tất cả mật khẩu (WP admin, hosting, FTP, database)
├── Revoke tất cả active sessions
└── Thông báo team

BƯỚC 2: ĐÁNH GIÁ (1-2 giờ)
├── Chạy Wordfence full scan
├── Kiểm tra file system (tìm file lạ, file bị sửa đổi)
├── Kiểm tra database (tìm user lạ, content lạ)
├── Kiểm tra access logs (tìm IP tấn công)
└── Xác định phạm vi ảnh hưởng

BƯỚC 3: XỬ LÝ (2-4 giờ)
├── Xóa malware/file lạ
├── Restore từ backup sạch (nếu cần)
├── Cập nhật tất cả plugins/themes/core
├── Xóa plugins/themes không sử dụng
├── Kiểm tra & fix file permissions
└── Cài đặt lại security plugins

BƯỚC 4: KHÔI PHỤC (1-2 giờ)
├── Kiểm tra website hoạt động bình thường
├── Tắt maintenance mode
├── Submit yêu cầu review lên Google (nếu bị flag)
├── Monitor chặt trong 48h tiếp theo
└── Kiểm tra SEO rankings có bị ảnh hưởng

BƯỚC 5: BÁO CÁO & CẢI THIỆN (sau 48h)
├── Viết incident report
├── Xác định nguyên nhân gốc (root cause)
├── Cập nhật security measures
├── Review & cải thiện quy trình
└── Lưu trữ bài học kinh nghiệm
```

### 8.3 Thông tin liên hệ khẩn cấp

| Vai trò | Liên hệ | Ghi chú |
| --- | --- | --- |
| Admin website | [Điền email/SĐT] | Người đầu tiên được thông báo |
| Hosting support | [Điền hotline hosting] | Hỗ trợ server-level |
| Security consultant | [Điền nếu có] | Cho incident nghiêm trọng |
| Google Search Console | [Điền email GSC] | Để submit review request |

### 8.4 Công cụ hỗ trợ xử lý

| Công cụ | Mục đích | Link |
| --- | --- | --- |
| Wordfence CLI | Scan malware từ command line | wordfence.com |
| Sucuri SiteCheck | Scan malware online miễn phí | sitecheck.sucuri.net |
| VirusTotal | Kiểm tra URL/file có malware | virustotal.com |
| Google Safe Browsing | Kiểm tra website có bị flag | transparencyreport.google.com |
| Wayback Machine | Xem phiên bản website trước khi bị hack | web.archive.org |

### 8.5 Template Incident Report

```markdown
# Incident Report — [Ngày]

## Tóm tắt
- **Thời gian phát hiện:** [DD/MM/YYYY HH:MM]
- **Thời gian xử lý xong:** [DD/MM/YYYY HH:MM]
- **Mức độ:** [Critical/High/Medium]
- **Loại incident:** [Malware/Defacement/Data breach/DDoS/Other]

## Mô tả
[Mô tả chi tiết sự cố]

## Nguyên nhân
[Root cause analysis]

## Hành động đã thực hiện
1. [Bước 1]
2. [Bước 2]
...

## Ảnh hưởng
- Downtime: [X giờ]
- Dữ liệu bị ảnh hưởng: [Có/Không]
- Khách hàng bị ảnh hưởng: [Số lượng]

## Biện pháp phòng ngừa
1. [Biện pháp 1]
2. [Biện pháp 2]
...

## Bài học kinh nghiệm
[Lessons learned]
```

---

*Hướng dẫn Bảo mật — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Phiên bản: 1.0*
