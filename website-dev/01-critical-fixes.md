# 🔧 Hướng dẫn Fix lỗi Critical & Dọn dẹp Demo Content — Xiaomi247.com

> **Ngày tạo:** 21/03/2026
> **Áp dụng cho:** WordPress + WooCommerce + Motta Theme
> **Tham chiếu:** [Bug Fix Checklist](../marketing/01-technical-audit/bug-fix-checklist.md) (Bug #1–#6)
> **Thời gian ước tính:** 2–3 giờ

---

## Mục lục

1. [Fix #1: Blog Page 404](#fix-1-blog-page-404)
2. [Fix #2: Contact Page 404](#fix-2-contact-page-404)
3. [Fix #3: Xóa Demo Menu Home v1–v10](#fix-3-xóa-demo-menu-home-v1v10)
4. [Fix #4: Xóa Demo Menu Shop v1–v4](#fix-4-xóa-demo-menu-shop-v1v4)
5. [Fix #5: Xóa Header Demo v1–v10](#fix-5-xóa-header-demo-v1v10)
6. [Fix #6: Tái cấu trúc Menu Navigation](#fix-6-tái-cấu-trúc-menu-navigation)

---

## Fix #1: Blog Page 404

> **Mức độ:** 🔴 Critical | **Bug ref:** #1
> **Vấn đề:** Truy cập `xiaomi247.com/blog` trả về lỗi 404 Not Found

### Vị trí trong WP Admin

- **Tạo trang:** `WP Admin → Pages → Add New`
- **Cấu hình:** `WP Admin → Settings → Reading`
- **Permalink:** `WP Admin → Settings → Permalinks`

### Các bước thực hiện

1. Đăng nhập WP Admin tại `xiaomi247.com/wp-admin`
2. Vào **Pages → Add New Page**
3. Đặt tiêu đề trang: `Blog`
4. **Không cần thêm nội dung** — WordPress sẽ tự động hiển thị danh sách bài viết
5. Đặt slug (URL): `blog`
6. Nhấn **Publish**
7. Vào **Settings → Reading**
8. Tại mục **"Your homepage displays"**, chọn **"A static page"**
9. Tại dropdown **"Posts page"**, chọn trang **Blog** vừa tạo
10. Nhấn **Save Changes**
11. Vào **Settings → Permalinks**
12. Không cần thay đổi gì — chỉ cần nhấn **Save Changes** để flush rewrite rules
13. Thêm trang Blog vào menu (xem [Fix #6](#fix-6-tái-cấu-trúc-menu-navigation))

### Kiểm tra sau khi fix

- [ ] Truy cập `xiaomi247.com/blog` → hiển thị danh sách bài viết (không còn 404)
- [ ] Kiểm tra trên trình duyệt ẩn danh (Incognito/Private)
- [ ] Kiểm tra trên mobile
- [ ] Trang Blog xuất hiện trong menu navigation

### ✅ Xác nhận hoàn thành

- [ ] **Bug #1 đã fix xong** — Blog page hoạt động bình thường

---

## Fix #2: Contact Page 404

> **Mức độ:** 🔴 Critical | **Bug ref:** #2
> **Vấn đề:** Truy cập `xiaomi247.com/contact` trả về lỗi 404 Not Found

### Vị trí trong WP Admin

- **Cài plugin:** `WP Admin → Plugins → Add New`
- **Tạo form:** `WP Admin → Contact → Add New`
- **Tạo trang:** `WP Admin → Pages → Add New`

### Bước A: Cài đặt Contact Form 7

1. Vào **Plugins → Add New**
2. Tìm kiếm: `Contact Form 7`
3. Nhấn **Install Now** → sau đó nhấn **Activate**
4. Sau khi kích hoạt, menu **Contact** sẽ xuất hiện trong sidebar

### Bước B: Tạo Form liên hệ

1. Vào **Contact → Add New**
2. Đặt tên form: `Form Liên hệ Xiaomi247`
3. Trong tab **Form**, thay nội dung mặc định bằng:

```
<div class="contact-form-wrapper">
    <p><label>Họ và tên *</label>
    [text* your-name placeholder "Nhập họ và tên"]</p>

    <p><label>Email *</label>
    [email* your-email placeholder "Nhập email"]</p>

    <p><label>Số điện thoại *</label>
    [tel* your-phone placeholder "Nhập số điện thoại"]</p>

    <p><label>Chủ đề</label>
    [select your-subject "Hỏi về sản phẩm" "Hỗ trợ kỹ thuật" "Khiếu nại / Đổi trả" "Hợp tác kinh doanh" "Khác"]</p>

    <p><label>Nội dung *</label>
    [textarea* your-message placeholder "Nhập nội dung tin nhắn..."]</p>

    <p>[submit class:btn-submit "Gửi tin nhắn"]</p>
</div>
```

4. Trong tab **Mail**, cấu hình:
   - **To:** `info@xiaomi247.com` (hoặc email nhận form)
   - **Subject:** `[Xiaomi247] Liên hệ từ [your-name]: [your-subject]`
   - **Message Body:** bao gồm tất cả các trường
5. Nhấn **Save**
6. **Copy shortcode** hiển thị ở đầu trang (dạng `[contact-form-7 id="xxx" title="Form Liên hệ Xiaomi247"]`)

### Bước C: Tạo trang Liên hệ

1. Vào **Pages → Add New Page**
2. Đặt tiêu đề: `Liên hệ`
3. Đặt slug: `lien-he`
4. Thêm nội dung trang theo cấu trúc sau:

```
<!-- Heading -->
<h2>Liên hệ với Xiaomi247</h2>
<p>Chúng tôi luôn sẵn sàng hỗ trợ bạn. Hãy liên hệ qua form bên dưới hoặc thông tin sau:</p>

<!-- Thông tin liên hệ -->
<div class="contact-info">
    📍 Địa chỉ: [Địa chỉ cửa hàng Xiaomi247]
    📞 Hotline: [Số điện thoại]
    ✉️ Email: info@xiaomi247.com
    🕐 Giờ làm việc: 8:00 – 21:00 (Thứ 2 – Chủ nhật)
</div>

<!-- Paste shortcode Contact Form 7 ở đây -->
[contact-form-7 id="xxx" title="Form Liên hệ Xiaomi247"]

<!-- Google Maps embed (tùy chọn) -->
<iframe src="[Google Maps embed URL]" width="100%" height="400" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
```

5. Thay `[Địa chỉ cửa hàng]`, `[Số điện thoại]`, shortcode ID, và Google Maps URL bằng thông tin thực
6. Nhấn **Publish**

### Kiểm tra sau khi fix

- [ ] Truy cập `xiaomi247.com/lien-he` → trang hiển thị đầy đủ
- [ ] Gửi thử form → nhận được email thông báo
- [ ] Kiểm tra validation: bỏ trống trường bắt buộc → hiện lỗi
- [ ] Kiểm tra trên mobile — form hiển thị đúng, dễ nhập liệu
- [ ] Thông tin liên hệ (địa chỉ, SĐT, email) hiển thị chính xác

### ✅ Xác nhận hoàn thành

- [ ] **Bug #2 đã fix xong** — Trang Liên hệ hoạt động, form gửi thành công

---

## Fix #3: Xóa Demo Menu Home v1–v10

> **Mức độ:** 🔴 Critical | **Bug ref:** #3
> **Vấn đề:** Menu chính hiển thị các mục demo: Home v1, Home v2, ... Home v10

### Vị trí trong WP Admin

- **Menu Editor:** `WP Admin → Appearance → Menus`

### Các bước thực hiện

1. Vào **Appearance → Menus**
2. Tại dropdown **"Select a menu to edit"**, chọn **Primary Menu** (hoặc Main Menu)
3. Nhấn **Select** để load menu
4. Trong danh sách menu items, tìm mục **"Home"** (menu cha)
5. Mở rộng mục Home → sẽ thấy các sub-menu: **Home v1, Home v2, Home v3, ... Home v10**
6. Với **mỗi** mục Home v1 đến Home v10:
   - Click vào mũi tên ▼ để mở rộng
   - Nhấn **Remove** (hoặc "Xóa")
7. Sau khi xóa hết các sub-items, **xóa luôn mục "Home" cha** (nếu nó là label demo)
8. Tạo mục mới: nhấn **Custom Links** ở cột trái
   - **URL:** `/` (hoặc `https://xiaomi247.com`)
   - **Link Text:** `Trang chủ`
   - Nhấn **Add to Menu**
9. Kéo mục **"Trang chủ"** lên vị trí đầu tiên trong menu
10. Nhấn **Save Menu**

### Kiểm tra sau khi fix

- [ ] Menu không còn hiển thị Home v1, v2, ... v10
- [ ] Chỉ có 1 mục **"Trang chủ"** duy nhất
- [ ] Click "Trang chủ" → về đúng trang chủ website
- [ ] Kiểm tra trên mobile (hamburger menu) — không còn demo items

### ✅ Xác nhận hoàn thành

- [ ] **Bug #3 đã fix xong** — Đã xóa toàn bộ demo Home variants khỏi menu

---

## Fix #4: Xóa Demo Menu Shop v1–v4

> **Mức độ:** 🔴 Critical | **Bug ref:** #4
> **Vấn đề:** Menu hiển thị: Shop v1, Shop v2, Shop v3, Shop v4

### Vị trí trong WP Admin

- **Menu Editor:** `WP Admin → Appearance → Menus`
- **Mega Menu (Motta):** Trong menu editor, mỗi item có tab **Motta Mega Menu**

### Các bước thực hiện

1. Vào **Appearance → Menus** (tiếp tục từ Fix #3, cùng Primary Menu)
2. Tìm mục **"Shop"** trong danh sách menu items
3. Mở rộng → xóa **tất cả** sub-items: **Shop v1, Shop v2, Shop v3, Shop v4**
   - Click ▼ → **Remove** cho từng mục
4. **Xóa luôn mục "Shop" cha**
5. Tạo menu mới thay thế:
   - Ở cột trái, chọn tab **Pages** → tìm trang **Shop** → nhấn **Add to Menu**
   - Hoặc dùng **Custom Links**: URL = `/shop`, Link Text = `Sản phẩm`
6. Đổi tên Navigation Label thành: **Sản phẩm**
7. **Cấu hình Mega Menu** (tính năng của Motta theme):
   - Click vào mục "Sản phẩm" vừa tạo → tìm nút **Motta Mega Menu** (hoặc biểu tượng bánh răng)
   - Bật **Enable Mega Menu**
   - Thêm 6 cột danh mục con:

| Cột | Danh mục | Ghi chú |
|-----|----------|---------|
| 1 | Điện thoại Xiaomi | Danh mục chính |
| 2 | Máy tính bảng | Danh mục chính |
| 3 | Đồng hồ thông minh | Danh mục chính |
| 4 | Phụ kiện | Danh mục chính |
| 5 | Thiết bị thông minh | Danh mục chính |
| 6 | Laptop | Danh mục chính |

8. Để thêm danh mục vào mega menu:
   - Ở cột trái, chọn tab **Product Categories**
   - Tick chọn 6 danh mục trên → nhấn **Add to Menu**
   - Kéo thả các danh mục thành **sub-items** của "Sản phẩm"
9. Nhấn **Save Menu**

### Kiểm tra sau khi fix

- [ ] Menu không còn hiển thị Shop v1, v2, v3, v4
- [ ] Mục **"Sản phẩm"** hiển thị mega menu với 6 danh mục
- [ ] Click vào từng danh mục → đến đúng trang danh mục sản phẩm
- [ ] Mega menu hiển thị đẹp trên desktop
- [ ] Trên mobile: danh mục hiển thị dạng dropdown/accordion

### ✅ Xác nhận hoàn thành

- [ ] **Bug #4 đã fix xong** — Đã thay thế demo Shop variants bằng mega menu danh mục

---

## Fix #5: Xóa Header Demo v1–v10

> **Mức độ:** 🟠 High | **Bug ref:** #5
> **Vấn đề:** Header hiển thị demo variants: Header v1, v2, ... v10

### Vị trí trong WP Admin

- **Motta Options:** `WP Admin → Appearance → Theme Options → Header` (hoặc `Motta Options → Header`)
- **Customizer:** `WP Admin → Appearance → Customize → Header`

### Các bước thực hiện

1. Vào **Appearance → Theme Options** (hoặc **Motta Options** trong sidebar)
2. Chọn mục **Header**
3. Tại phần **Header Layout** (hoặc Header Style):
   - Sẽ thấy danh sách các layout: Header v1, v2, ... v10
   - **Chọn 1 layout phù hợp** — khuyến nghị layout có:
     - Logo bên trái
     - Menu navigation ở giữa
     - Icons (search, cart, account) bên phải
   - Thường là **Header v1** hoặc **Header v3** phù hợp cho e-commerce
4. Tắt **Header Switcher / Demo Selector** nếu có:
   - Tìm option "Show Header Switcher" hoặc "Header Demo" → **tắt (disable)**
5. Cấu hình chi tiết header đã chọn:
   - **Logo:** Upload logo Xiaomi247 (nếu chưa có)
   - **Search bar:** Bật hiển thị, đổi placeholder thành `Tìm kiếm sản phẩm...`
   - **Cart icon:** Bật hiển thị
   - **Account icon:** Bật hiển thị
   - **Hotline/Contact:** Thêm số hotline nếu header hỗ trợ
6. Kiểm tra **Header Mobile**:
   - Trong cùng mục Header, tìm tab **Mobile Header**
   - Chọn layout mobile phù hợp (logo giữa, hamburger trái, cart phải)
7. Nhấn **Save Changes** (hoặc **Publish** nếu dùng Customizer)

### Kiểm tra sau khi fix

- [ ] Header không còn hiển thị demo switcher/selector
- [ ] Header hiển thị đúng: logo, menu, search, cart
- [ ] Header desktop hiển thị chuyên nghiệp
- [ ] Header mobile hiển thị đúng (hamburger menu, logo, cart)
- [ ] Sticky header hoạt động bình thường (nếu có)

### ✅ Xác nhận hoàn thành

- [ ] **Bug #5 đã fix xong** — Header đã cấu hình layout cố định, không còn demo variants

---

## Fix #6: Tái cấu trúc Menu Navigation

> **Mức độ:** 🟠 High | **Bug ref:** #6
> **Vấn đề:** Menu cần tái cấu trúc hoàn toàn sau khi xóa demo items

### Vị trí trong WP Admin

- **Menu Editor:** `WP Admin → Appearance → Menus`
- **Menu Locations:** Tab **"Manage Locations"** trong trang Menus

### Cấu trúc menu mục tiêu

```
📋 Primary Menu — Xiaomi247
├── Trang chủ          → / (homepage)
├── Sản phẩm ▼         → /shop (mega menu)
│   ├── Điện thoại Xiaomi
│   ├── Máy tính bảng
│   ├── Đồng hồ thông minh
│   ├── Phụ kiện
│   ├── Thiết bị thông minh
│   └── Laptop
├── Khuyến mãi         → /khuyen-mai (trang hoặc danh mục sale)
├── Blog               → /blog
├── Về chúng tôi       → /ve-chung-toi
└── Liên hệ            → /lien-he
```

### Các bước thực hiện

1. Vào **Appearance → Menus**
2. Nếu menu hiện tại quá rối, tạo menu mới:
   - Nhấn **"create a new menu"**
   - Đặt tên: `Primary Menu - Xiaomi247`
   - Nhấn **Create Menu**
3. Thêm các mục menu theo thứ tự:

**Mục 1 — Trang chủ:**
   - Custom Links → URL: `/` → Link Text: `Trang chủ` → Add to Menu

**Mục 2 — Sản phẩm (đã tạo ở Fix #4):**
   - Nếu tạo menu mới: thêm lại trang Shop + 6 danh mục con (xem Fix #4)
   - Bật Mega Menu cho mục này

**Mục 3 — Khuyến mãi:**
   - Custom Links → URL: `/khuyen-mai` → Link Text: `Khuyến mãi` → Add to Menu
   - Hoặc: tạo trang "Khuyến mãi" trước (Pages → Add New), rồi thêm từ tab Pages

**Mục 4 — Blog:**
   - Tab Pages → tick chọn trang **Blog** (đã tạo ở Fix #1) → Add to Menu

**Mục 5 — Về chúng tôi:**
   - Custom Links → URL: `/ve-chung-toi` → Link Text: `Về chúng tôi` → Add to Menu
   - Hoặc: tạo trang "Về chúng tôi" trước, rồi thêm từ tab Pages

**Mục 6 — Liên hệ:**
   - Tab Pages → tick chọn trang **Liên hệ** (đã tạo ở Fix #2) → Add to Menu

4. **Sắp xếp thứ tự:** Kéo thả các mục theo đúng thứ tự trên
5. **Gán Menu Location:**
   - Ở phần **Menu Settings** (cuối trang), tick chọn:
     - ✅ **Primary Menu** (hoặc Main Navigation)
     - ✅ **Mobile Menu** (nếu có option riêng)
   - Hoặc vào tab **Manage Locations** → gán menu vừa tạo cho Primary
6. Nhấn **Save Menu**

### Kiểm tra sau khi fix

- [ ] Menu hiển thị đúng 6 mục: Trang chủ, Sản phẩm, Khuyến mãi, Blog, Về chúng tôi, Liên hệ
- [ ] Mega menu "Sản phẩm" hiển thị 6 danh mục con
- [ ] Tất cả links hoạt động — không có link trỏ về 404
- [ ] Menu hiển thị đúng trên desktop
- [ ] Menu hiển thị đúng trên mobile (hamburger menu)
- [ ] Không còn bất kỳ demo text nào (Home v1-v10, Shop v1-v4)

### ✅ Xác nhận hoàn thành

- [ ] **Bug #6 đã fix xong** — Menu đã tái cấu trúc hoàn chỉnh

---

## 📋 Checklist tổng hợp

| # | Fix | Mức độ | Trạng thái |
|---|-----|--------|------------|
| 1 | Blog Page 404 | 🔴 Critical | ⬜ |
| 2 | Contact Page 404 | 🔴 Critical | ⬜ |
| 3 | Xóa Demo Menu Home v1–v10 | 🔴 Critical | ⬜ |
| 4 | Xóa Demo Menu Shop v1–v4 | 🔴 Critical | ⬜ |
| 5 | Xóa Header Demo v1–v10 | 🟠 High | ⬜ |
| 6 | Tái cấu trúc Menu Navigation | 🟠 High | ⬜ |

### Thứ tự thực hiện khuyến nghị

1. **Fix #3 + #4** trước (xóa demo menu) — vì ảnh hưởng trực quan nhất
2. **Fix #5** (header) — loại bỏ demo header
3. **Fix #6** (tái cấu trúc menu) — xây dựng menu hoàn chỉnh
4. **Fix #1** (Blog 404) — tạo trang Blog
5. **Fix #2** (Contact 404) — tạo trang Liên hệ + form

> ⚠️ **Lưu ý:** Sau khi hoàn thành tất cả, clear cache (nếu có plugin cache) và kiểm tra lại toàn bộ website trên cả desktop và mobile.

---

*Hướng dẫn Fix Critical — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Tham chiếu: Bug Fix Checklist #1–#6*

