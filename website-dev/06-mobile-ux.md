# 📱 Hướng dẫn Tối ưu Mobile & UX — Xiaomi247.com

> **Ngày tạo:** 21/03/2026
> **Phiên bản:** 1.0
> **Áp dụng cho:** WordPress + WooCommerce + Motta Theme
> **Tham chiếu:**
> - [Khuyến nghị Kỹ thuật — Phần 5](../marketing/01-technical-audit/technical-recommendations.md)
> - [Conversion Optimization](../marketing/04-trust-building/conversion-optimization.md)
> - [Website Audit Report — Phần 4, 5](../marketing/01-technical-audit/website-audit-report.md)

---

## Mục lục

1. [Mobile Responsive Testing Checklist](#1-mobile-responsive-testing-checklist)
2. [Touch Target Optimization](#2-touch-target-optimization)
3. [Mobile Menu & Navigation](#3-mobile-menu--navigation)
4. [Product Gallery trên Mobile](#4-product-gallery-trên-mobile)
5. [Checkout Flow Mobile](#5-checkout-flow-mobile)
6. [Homepage Layout](#6-homepage-layout)
7. [Product Page UX](#7-product-page-ux)
8. [CTA Optimization](#8-cta-optimization)

---

## 1. Mobile Responsive Testing Checklist

> **Công cụ test:** Chrome DevTools (Device Mode), BrowserStack, Responsively App
> **Nguyên tắc:** Test trên thiết bị thật khi có thể, ưu tiên Android (thị trường VN ~70%)

### 1.1 Breakpoint 320px — iPhone SE / Điện thoại nhỏ

- [ ] Logo hiển thị đúng, không bị cắt
- [ ] Hamburger menu icon hiển thị rõ ràng
- [ ] Search bar không bị tràn
- [ ] Banner/slider hiển thị đúng tỷ lệ, text đọc được
- [ ] Product card: ảnh + tên + giá hiển thị đủ (grid 1 cột hoặc 2 cột nhỏ)
- [ ] Nút "Thêm vào giỏ" không bị che khuất
- [ ] Footer links không bị chồng chéo
- [ ] Form inputs chiếm full-width
- [ ] Font size ≥ 14px cho body text
- [ ] Không có horizontal scroll

### 1.2 Breakpoint 375px — iPhone 12/13/14/15

- [ ] Layout 2 cột cho product grid
- [ ] Banner text đọc rõ, CTA button đủ lớn
- [ ] Product gallery ảnh hiển thị đúng
- [ ] Sticky header không chiếm quá 60px chiều cao
- [ ] Cart icon + số lượng hiển thị đúng
- [ ] Breadcrumb không bị tràn (truncate nếu dài)
- [ ] Tab content (mô tả/đánh giá) hiển thị đúng
- [ ] Trust badges hiển thị đủ, không bị cắt
- [ ] Popup/modal hiển thị trong viewport
- [ ] Zalo/chat widget không che nội dung quan trọng

### 1.3 Breakpoint 414px — iPhone Plus / Android phổ biến

- [ ] Product grid 2 cột cân đối
- [ ] Giá sản phẩm + giá gốc hiển thị trên 1 dòng
- [ ] Rating stars + số đánh giá hiển thị đúng
- [ ] Nút CTA đủ lớn (min 48px height)
- [ ] Category icons/thumbnails hiển thị đều
- [ ] Sidebar filters (nếu có) chuyển thành bottom sheet hoặc modal
- [ ] Checkout form fields đủ rộng
- [ ] Payment method icons hiển thị đúng
- [ ] Error messages hiển thị rõ ràng
- [ ] Loading states/skeleton screens hoạt động

### 1.4 Breakpoint 768px — iPad / Tablet dọc

- [ ] Layout chuyển sang 3-4 cột cho product grid
- [ ] Sidebar có thể hiển thị bên cạnh (không cần hamburger)
- [ ] Banner hiển thị phiên bản tablet (nếu có)
- [ ] Product page: gallery bên trái, info bên phải
- [ ] Checkout form 2 cột (họ tên | SĐT)
- [ ] Footer hiển thị multi-column
- [ ] Mega menu có thể hiển thị dạng dropdown
- [ ] Search bar mở rộng hơn
- [ ] Trust badges hiển thị hàng ngang đầy đủ
- [ ] Related products grid 3-4 cột

### 1.5 Breakpoint 1024px — iPad ngang / Laptop nhỏ

- [ ] Layout desktop bắt đầu áp dụng
- [ ] Navigation menu đầy đủ (không hamburger)
- [ ] Sidebar filters hiển thị cố định bên trái
- [ ] Product grid 4-5 cột
- [ ] Hover effects hoạt động (quick view, add to cart)
- [ ] Mega menu dropdown hiển thị đúng
- [ ] Banner full-width với text overlay
- [ ] Checkout layout 2 cột (form | order summary)
- [ ] Header: logo + menu + search + cart + account
- [ ] Sticky header hoạt động mượt

### 1.6 Breakpoint 1440px — Desktop Full HD

- [ ] Content max-width không quá 1400px (tránh quá rộng)
- [ ] Product grid 5-6 cột
- [ ] Ảnh sản phẩm hiển thị chất lượng cao
- [ ] Whitespace cân đối, không quá trống
- [ ] Font size tăng phù hợp (body 16px, heading 24-32px)
- [ ] Sidebar width cố định (~280px)
- [ ] Footer layout đầy đủ 4-5 cột
- [ ] Banner/slider hiển thị full resolution
- [ ] Hover animations mượt mà
- [ ] Không có element nào bị stretch quá mức


---

## 2. Touch Target Optimization

> **Tiêu chuẩn:** Google khuyến nghị touch target tối thiểu **48x48px** (CSS pixels)
> **Khoảng cách:** Tối thiểu **8px** giữa các touch targets

### 2.1 Checklist Elements cần kiểm tra

#### Buttons
- [ ] Nút "THÊM VÀO GIỎ HÀNG" — min 48px height, full-width trên mobile
- [ ] Nút "MUA NGAY" — min 48px height
- [ ] Nút "ĐẶT HÀNG" (checkout) — min 52px height, nổi bật
- [ ] Nút quantity (+/-) — min 44x44px mỗi nút
- [ ] Nút "Xem thêm" / "Load more" — min 48px height
- [ ] Nút đóng popup/modal (X) — min 44x44px
- [ ] Nút back/quay lại — min 44x44px

#### Links & Navigation
- [ ] Menu items trong hamburger menu — min 48px height mỗi item
- [ ] Breadcrumb links — min 32px height, padding đủ
- [ ] Category links trên homepage — min 48px touch area
- [ ] Footer links — min 44px height, line-height đủ
- [ ] Pagination links — min 44x44px mỗi số trang
- [ ] "Xem tất cả" links — min 44px height
- [ ] Social media icons — min 44x44px

#### Form Inputs
- [ ] Text input fields — min 48px height
- [ ] Dropdown/select — min 48px height
- [ ] Checkbox — min 24x24px visual + 48x48px touch area
- [ ] Radio buttons — min 24x24px visual + 48x48px touch area
- [ ] Search input — min 48px height
- [ ] Coupon code input — min 48px height

#### Product Elements
- [ ] Product card (toàn bộ) — touch area rõ ràng
- [ ] Wishlist icon (trái tim) — min 44x44px
- [ ] Compare icon — min 44x44px
- [ ] Color/variant swatches — min 40x40px, spacing 8px
- [ ] Gallery thumbnail — min 48x48px
- [ ] Rating stars (nếu clickable) — min 44px height
- [ ] Tab headers (Mô tả/Đánh giá/FAQ) — min 48px height

### 2.2 CSS Implementation

```css
/* Touch target base styles cho mobile */
@media (max-width: 768px) {
  .single-product .single_add_to_cart_button,
  .checkout .place-order button {
    min-height: 52px;
    font-size: 16px;
    width: 100%;
    padding: 14px 24px;
  }

  .mobile-menu li a {
    min-height: 48px;
    display: flex;
    align-items: center;
    padding: 12px 16px;
  }

  input[type="text"],
  input[type="email"],
  input[type="tel"],
  input[type="number"],
  input[type="password"],
  select,
  textarea {
    min-height: 48px;
    font-size: 16px; /* Tránh auto-zoom trên iOS */
    padding: 12px 16px;
  }

  .quantity .qty-btn {
    min-width: 44px;
    min-height: 44px;
  }

  .woocommerce-pagination a,
  .woocommerce-pagination span {
    min-width: 44px;
    min-height: 44px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
  }

  .woocommerce-tabs .tabs li a {
    min-height: 48px;
    padding: 12px 16px;
  }
}
```

---

## 3. Mobile Menu & Navigation

### 3.1 Hamburger Menu UX

#### Checklist thiết kế
- [ ] Icon hamburger (☰) rõ ràng, kích thước ≥ 44x44px
- [ ] Vị trí: góc trái trên hoặc phải trên (nhất quán)
- [ ] Animation mở/đóng mượt (slide từ trái hoặc overlay)
- [ ] Overlay tối nền khi menu mở (opacity 0.5)
- [ ] Nút đóng (X) rõ ràng, ≥ 44x44px
- [ ] Tap outside menu để đóng
- [ ] Swipe để đóng menu (gesture support)
- [ ] Menu không che mất header/search bar

#### Cấu trúc menu mobile đề xuất

```
☰ MENU
├── 🏠 Trang chủ
├── 📱 Điện thoại Xiaomi
│   ├── Xiaomi 14 Series
│   ├── Redmi Note Series
│   ├── POCO Series
│   └── Xem tất cả →
├── 💻 Laptop
├── ⌚ Đồng hồ thông minh
├── 📦 Phụ kiện
├── 🏠 Thiết bị thông minh
├── 🏷️ Khuyến mãi HOT 🔥
├── ──────────────────
├── 📞 Liên hệ: 1900.xxxx
├── 🏪 Hệ thống cửa hàng
├── 📋 Tra cứu đơn hàng
└── 👤 Tài khoản
```

#### Lưu ý quan trọng
- [ ] **Xóa tất cả demo items** (Home v1-v10, Shop v1-v4, Header v1-v10)
- [ ] Submenu mở bằng tap (không hover) — dùng icon mũi tên (›)
- [ ] Submenu có nút "Quay lại" rõ ràng
- [ ] Hiển thị tối đa 2 cấp menu trên mobile
- [ ] Menu items có icon để dễ nhận diện
- [ ] Highlight mục "Khuyến mãi" bằng màu đỏ/cam

### 3.2 Mega Menu trên Mobile

| Desktop | Mobile |
| --- | --- |
| Hover để mở mega menu | Tap để mở submenu |
| Hiển thị ảnh + nhiều cột | Danh sách dọc, không ảnh |
| Hiển thị tất cả subcategories | Chỉ hiển thị cấp 1, tap để xem cấp 2 |
| Banner quảng cáo trong menu | Ẩn banner, chỉ giữ links |

#### Checklist Mega Menu Mobile
- [ ] Chuyển mega menu thành accordion/drill-down trên mobile
- [ ] Ẩn hình ảnh quảng cáo trong menu mobile (giảm load)
- [ ] Giữ lại category icons nhỏ (24x24px)
- [ ] Animation transition mượt giữa các cấp menu
- [ ] Hiển thị số lượng sản phẩm bên cạnh category (vd: "Điện thoại (40)")

### 3.3 Search Bar Mobile

#### Checklist
- [ ] Search icon trên header, tap để mở full-screen search
- [ ] Search input auto-focus khi mở (bàn phím tự hiện)
- [ ] Placeholder tiếng Việt: "Tìm kiếm sản phẩm..."
- [ ] Auto-suggest/autocomplete khi gõ (hiển thị ảnh + tên + giá)
- [ ] Lịch sử tìm kiếm gần đây (3-5 từ khóa)
- [ ] Từ khóa phổ biến/trending hiển thị khi chưa gõ
- [ ] Nút xóa text (X) trong input field
- [ ] Nút "Hủy" hoặc "Đóng" rõ ràng
- [ ] Kết quả tìm kiếm hiển thị dạng list (ảnh nhỏ + tên + giá)
- [ ] "Không tìm thấy" — gợi ý sản phẩm tương tự

---

## 4. Product Gallery trên Mobile

### 4.1 Swipe Gallery

#### Checklist
- [ ] Swipe trái/phải để chuyển ảnh (gesture mượt)
- [ ] Dots indicator hiển thị vị trí ảnh hiện tại
- [ ] Số ảnh hiển thị (vd: "3/8") ở góc
- [ ] Ảnh đầu tiên load nhanh (preload, priority)
- [ ] Các ảnh sau lazy load
- [ ] Ảnh hiển thị full-width trên mobile
- [ ] Tỷ lệ ảnh nhất quán (1:1 hoặc 4:3)
- [ ] Không bị layout shift khi ảnh load (set width/height)

### 4.2 Zoom trên Mobile

#### Checklist
- [ ] Pinch-to-zoom hoạt động trên ảnh sản phẩm
- [ ] Double-tap để zoom in/out
- [ ] Khi zoom: có thể pan (kéo) để xem chi tiết
- [ ] Nút zoom icon (🔍) hiển thị trên ảnh
- [ ] Tap vào ảnh → mở fullscreen gallery (lightbox)
- [ ] Fullscreen gallery: swipe + zoom + đóng (X hoặc swipe down)
- [ ] Zoom level tối đa 3x (đủ xem chi tiết sản phẩm)

### 4.3 Thumbnail Navigation

#### Checklist
- [ ] Thumbnails hiển thị dạng horizontal scroll dưới ảnh chính
- [ ] Thumbnail active có border highlight (vd: border cam)
- [ ] Thumbnail size: 48x48px đến 60x60px
- [ ] Tap thumbnail → chuyển ảnh chính (không cần swipe)
- [ ] Video thumbnail có icon play (▶️)
- [ ] Thumbnail strip không chiếm quá 80px chiều cao
- [ ] Scroll indicator nếu có nhiều thumbnails (> 5)

### 4.4 Video trong Gallery

- [ ] Video sản phẩm (nếu có) hiển thị trong gallery
- [ ] Thumbnail video có icon play overlay
- [ ] Video không tự động phát (tiết kiệm data)
- [ ] Video player controls đủ lớn cho touch
- [ ] Hỗ trợ fullscreen video
- [ ] Fallback: link YouTube nếu embed không hoạt động

---

## 5. Checkout Flow Mobile

### 5.1 Nguyên tắc chung

- Tối đa **2-3 bước** checkout
- **Không bắt buộc** tạo tài khoản (guest checkout)
- Progress bar hiển thị bước hiện tại
- Trust signals hiển thị xuyên suốt

### 5.2 Bước 1: Thông tin giao hàng

#### Checklist
- [ ] Form fields full-width trên mobile
- [ ] Input height ≥ 48px
- [ ] Label hiển thị phía trên input (không placeholder-only)
- [ ] Họ tên — text input, autocomplete="name"
- [ ] Số điện thoại — input type="tel", autocomplete="tel", keyboard số
- [ ] Tỉnh/Thành phố — dropdown/select, dữ liệu 63 tỉnh thành
- [ ] Quận/Huyện — dropdown, auto-load theo tỉnh đã chọn
- [ ] Phường/Xã — dropdown, auto-load theo quận đã chọn
- [ ] Địa chỉ chi tiết — text input
- [ ] Ghi chú — textarea (tùy chọn, collapsed mặc định)
- [ ] Validation real-time (hiển thị lỗi ngay khi blur)
- [ ] Error message màu đỏ, rõ ràng, tiếng Việt
- [ ] Nút "TIẾP TỤC" — full-width, sticky bottom, min 52px height

#### Error Messages tiếng Việt
| Field | Error |
| --- | --- |
| Họ tên | "Vui lòng nhập họ tên" |
| SĐT | "Số điện thoại không hợp lệ" |
| Tỉnh/TP | "Vui lòng chọn tỉnh/thành phố" |
| Địa chỉ | "Vui lòng nhập địa chỉ giao hàng" |

### 5.3 Bước 2: Thanh toán & Xác nhận

#### Checklist
- [ ] Tóm tắt đơn hàng: ảnh nhỏ + tên SP + số lượng + giá
- [ ] Có thể chỉnh số lượng hoặc xóa SP ngay tại đây
- [ ] Phí vận chuyển tự động tính theo địa chỉ
- [ ] Input mã giảm giá — nút "Áp dụng" rõ ràng
- [ ] Thông báo khi mã giảm giá hợp lệ/không hợp lệ
- [ ] Tổng tiền hiển thị nổi bật (font lớn, màu đậm)

#### Phương thức thanh toán
- [ ] COD (Thanh toán khi nhận hàng) — mặc định, phổ biến nhất VN
- [ ] Chuyển khoản ngân hàng — hiển thị thông tin TK khi chọn
- [ ] Ví MoMo — redirect hoặc QR code
- [ ] VNPay — redirect đến cổng thanh toán
- [ ] Thẻ Visa/Mastercard — form nhập thẻ inline
- [ ] Mỗi phương thức có icon/logo nhận diện
- [ ] Radio button đủ lớn (48px touch area)

#### Trust Signals tại Checkout
- [ ] 🔒 Icon khóa + "Thanh toán an toàn & bảo mật"
- [ ] 🔄 "Đổi trả miễn phí trong 7 ngày"
- [ ] 🛡️ "Sản phẩm chính hãng 100%"
- [ ] Logo các đối tác thanh toán (MoMo, VNPay, Visa, MC)
- [ ] Nút "ĐẶT HÀNG" — full-width, màu cam (#FF6D00), min 52px, sticky bottom

### 5.4 Bước 3: Xác nhận thành công

#### Checklist
- [ ] Icon ✅ lớn + "Đặt hàng thành công!"
- [ ] Mã đơn hàng hiển thị rõ (có thể copy)
- [ ] Tóm tắt: sản phẩm + tổng tiền + địa chỉ giao
- [ ] Thời gian giao dự kiến
- [ ] Link/nút "Tra cứu đơn hàng"
- [ ] Nút "Tiếp tục mua sắm"
- [ ] Gợi ý sản phẩm mua thêm (cross-sell)
- [ ] Thông báo qua SMS/Zalo đã được gửi

### 5.5 Mobile-Specific Checkout UX

- [ ] Sticky order summary bar ở bottom (hiển thị tổng tiền)
- [ ] Keyboard phù hợp: number pad cho SĐT, email keyboard cho email
- [ ] Auto-scroll đến field lỗi khi submit
- [ ] Nút back browser không mất dữ liệu đã nhập
- [ ] Loading state rõ ràng khi đang xử lý đơn hàng
- [ ] Disable nút "ĐẶT HÀNG" khi đang xử lý (tránh double submit)
- [ ] Timeout handling: thông báo nếu quá 30s chưa phản hồi

---

## 6. Homepage Layout

### 6.1 Layout Mobile đề xuất (từ trên xuống)

```
┌──────────────────────────────┐
│ [☰] [Logo Xiaomi247] [🔍][🛒]│  ← Sticky header
├──────────────────────────────┤
│ 📞 Hotline: 1900.xxxx       │  ← Top bar (có thể ẩn khi scroll)
│ 🛡️ Chính hãng 100%          │
├──────────────────────────────┤
│ ┌──────────────────────────┐ │
│ │    BANNER / SLIDER       │ │  ← Auto-slide, swipe, dots
│ │    (Hero image + CTA)    │ │
│ └──────────────────────────┘ │
├──────────────────────────────┤
│ [📱][💻][⌚][📦][🏠][🏷️]    │  ← Category icons (scroll ngang)
│ ĐT  Laptop Watch PK SmH Sale│
├──────────────────────────────┤
│ 🔥 FLASH SALE               │
│ ⏰ Kết thúc sau: 02:15:30   │
│ [SP1 ảnh] [SP2 ảnh] [SP3 →] │  ← Horizontal scroll
├──────────────────────────────┤
│ 📱 ĐIỆN THOẠI NỔI BẬT       │
│ [SP] [SP]                    │  ← Grid 2 cột
│ [SP] [SP]                    │
│ [Xem tất cả điện thoại →]   │
├──────────────────────────────┤
│ 🛡️ TẠI SAO CHỌN XIAOMI247? │
│ ✅ Chính hãng  🚚 Free ship │  ← Trust badges section
│ 🔧 BH 18 tháng 🔄 Đổi 7N   │
├──────────────────────────────┤
│ ⭐ ĐÁNH GIÁ TỪ KHÁCH HÀNG  │
│ [Review 1] [Review 2] →     │  ← Carousel reviews
├──────────────────────────────┤
│ 📰 TIN TỨC & KHUYẾN MÃI    │
│ [Bài 1] [Bài 2]             │
│ [Xem tất cả →]              │
├──────────────────────────────┤
│ FOOTER                       │
│ Thông tin | Chính sách | ... │
│ © 2026 Xiaomi247             │
└──────────────────────────────┘
```

### 6.2 Banner/Slider

#### Checklist
- [ ] Tối đa 3-5 slides (không quá nhiều)
- [ ] Auto-slide mỗi 5 giây
- [ ] Swipe gesture hoạt động
- [ ] Dots indicator ở dưới
- [ ] Ảnh banner tối ưu cho mobile (tỷ lệ 16:9 hoặc 2:1)
- [ ] Text trên banner đọc được trên mobile (font ≥ 18px)
- [ ] CTA button trên banner đủ lớn và rõ ràng
- [ ] Lazy load cho slides sau slide đầu tiên
- [ ] Không gây CLS (set width/height cố định)

### 6.3 CTA Placement trên Homepage

| Vị trí | CTA | Mục đích |
| --- | --- | --- |
| Banner chính | "MUA NGAY" / "XEM KHUYẾN MÃI" | Dẫn đến SP/danh mục sale |
| Flash Sale section | "Xem tất cả Flash Sale →" | Tăng traffic vào sale page |
| Mỗi section SP | "Xem tất cả [danh mục] →" | Dẫn vào category page |
| Trust badges | "Tìm hiểu thêm" | Dẫn đến trang chính sách |
| Cuối trang | "ĐĂNG KÝ NHẬN TIN KHUYẾN MÃI" | Thu lead email/SĐT |

### 6.4 Featured Products

#### Checklist
- [ ] Grid 2 cột trên mobile (< 768px)
- [ ] Mỗi product card: ảnh + tên + giá + giá gốc + % giảm
- [ ] Badge "HOT" / "MỚI" / "-20%" trên ảnh
- [ ] Nút "Thêm vào giỏ" hoặc "Xem chi tiết"
- [ ] Lazy load ảnh sản phẩm
- [ ] Skeleton loading khi đang tải
- [ ] "Xem tất cả" link ở cuối mỗi section

### 6.5 Category Grid

#### Checklist
- [ ] Horizontal scroll trên mobile (không wrap)
- [ ] Icon + tên danh mục dưới icon
- [ ] Icon size: 48x48px đến 64x64px
- [ ] Khoảng cách đều giữa các items
- [ ] Scroll indicator (fade ở cạnh phải)
- [ ] Tap → dẫn đến category page

### 6.6 Trust Badges Section

#### Checklist
- [ ] Grid 2x2 trên mobile
- [ ] Mỗi badge: icon + text ngắn
- [ ] Nội dung tiếng Việt rõ ràng:
  - ✅ "Chính hãng 100%"
  - 🚚 "Miễn phí vận chuyển đơn từ 500K"
  - 🔧 "Bảo hành chính hãng 18 tháng"
  - 🔄 "Đổi trả miễn phí trong 7 ngày"
- [ ] Background nhẹ để nổi bật (vd: #FFF3E0)
- [ ] Không quá 4 badges trên mobile

---

## 7. Product Page UX

### 7.1 Layout Product Page Mobile (từ trên xuống)

```
┌──────────────────────────────┐
│ ← Quay lại    [🔍] [🛒(2)]  │  ← Header với back button
├──────────────────────────────┤
│ Trang chủ > ĐT > Xiaomi 14  │  ← Breadcrumb (truncated)
├──────────────────────────────┤
│ ┌──────────────────────────┐ │
│ │                          │ │
│ │    ẢNH SẢN PHẨM         │ │  ← Swipe gallery, full-width
│ │    (swipe ← →)           │ │
│ │              🔍  3/8     │ │
│ └──────────────────────────┘ │
│ [thumb1][thumb2][thumb3][▶️]  │  ← Thumbnail strip
├──────────────────────────────┤
│ Xiaomi 14 Ultra 512GB        │  ← Tên SP (H1)
│ ⭐⭐⭐⭐⭐ 4.8 (125 đánh giá)  │  ← Rating
├──────────────────────────────┤
│ 12.990.000đ                  │  ← Giá sale (lớn, đỏ/cam)
│ 14.990.000đ  -13%            │  ← Giá gốc (gạch ngang) + %
├──────────────────────────────┤
│ Màu sắc: [Đen] [Trắng] [Xanh]│ ← Variant swatches
│ Phiên bản: [256GB] [512GB]   │
├──────────────────────────────┤
│ 🛡️ Chính hãng | 🔧 BH 18T   │  ← Trust badges compact
│ 🚚 Free ship  | 🔄 Đổi 7N   │
├──────────────────────────────┤
│ [🛒 THÊM VÀO GIỎ HÀNG    ] │  ← CTA chính (cam, full-width)
│ [📞 GỌI: 1900.xxxx        ] │  ← CTA phụ
│ [💬 TƯ VẤN QUA ZALO       ] │  ← CTA phụ
├──────────────────────────────┤
│ ⏰ Đặt trước 15h → giao     │
│    trong ngày (nội thành)    │
│ 👥 23 người đang xem SP này │
│ 📦 Đã bán 456 sản phẩm      │
├──────────────────────────────┤
│ [Mô tả] [Thông số] [Đánh giá│  ← Tabs
│  (125)] [FAQ]                │
├──────────────────────────────┤
│ NỘI DUNG TAB ĐANG CHỌN      │
├──────────────────────────────┤
│ 🛍️ SẢN PHẨM LIÊN QUAN      │
│ [SP] [SP] [SP →]             │  ← Horizontal scroll
├──────────────────────────────┤
│ 🎁 MUA KÈM GIẢM GIÁ        │
│ [Ốp lưng -30%] [Sạc -20%]   │
└──────────────────────────────┘

┌──────────────────────────────┐
│ 12.990.000đ [THÊM VÀO GIỎ]  │  ← Sticky bottom bar
└──────────────────────────────┘
```

### 7.2 Ảnh sản phẩm

#### Checklist
- [ ] Tối thiểu 5 ảnh, tối đa 8-10 ảnh
- [ ] Ảnh 1: ảnh chính, góc 3/4
- [ ] Ảnh 2-3: các góc khác (trước, sau, cạnh)
- [ ] Ảnh 4-5: chi tiết (camera, cổng sạc, nút bấm)
- [ ] Ảnh 6: ảnh trong hộp (unboxing)
- [ ] Ảnh 7-8: ảnh lifestyle (người dùng thực tế)
- [ ] 1-2 video ngắn (30-60s) nếu có
- [ ] Ảnh chất lượng cao (min 800x800px)
- [ ] Background trắng hoặc nhất quán
- [ ] Alt text tiếng Việt cho mỗi ảnh

### 7.3 Thông tin giá

#### Checklist
- [ ] Giá bán hiển thị lớn, nổi bật (font ≥ 24px, màu đỏ/cam)
- [ ] Giá gốc gạch ngang bên cạnh (font nhỏ hơn, màu xám)
- [ ] Phần trăm giảm giá hiển thị badge (vd: "-13%")
- [ ] Format giá VNĐ đúng: "12.990.000đ" (có dấu chấm phân cách)
- [ ] Giá trả góp (nếu có): "Chỉ từ 2.165.000đ/tháng"
- [ ] Thông tin "Giá đã bao gồm VAT"

### 7.4 Nút mua hàng

#### Checklist
- [ ] "THÊM VÀO GIỎ HÀNG" — nút chính, màu cam (#FF6D00), full-width
- [ ] "MUA NGAY" — nút phụ, cho phép checkout nhanh 1 bước
- [ ] "GỌI ĐẶT HÀNG" — hiển thị số hotline, tap để gọi (tel: link)
- [ ] "TƯ VẤN QUA ZALO" — mở Zalo chat
- [ ] Min height 52px cho nút chính
- [ ] Icon phù hợp trước text (🛒, 📞, 💬)
- [ ] Hover/active state rõ ràng

### 7.5 Tabs (Mô tả / Thông số / Đánh giá / FAQ)

#### Checklist
- [ ] Tabs hiển thị dạng horizontal scroll trên mobile
- [ ] Tab active có indicator rõ ràng (underline hoặc background)
- [ ] Tab height ≥ 48px
- [ ] Nội dung tab lazy load (chỉ load khi tap)
- [ ] Tab "Đánh giá" hiển thị số lượng: "Đánh giá (125)"

#### Tab Mô tả
- [ ] Nội dung HTML format đẹp (heading, list, ảnh)
- [ ] Ảnh trong mô tả responsive (max-width: 100%)
- [ ] "Xem thêm" nếu nội dung dài (collapse sau 500px)
- [ ] Bảng thông số responsive (horizontal scroll nếu cần)

#### Tab Đánh giá
- [ ] Rating tổng quan: sao trung bình + phân bố (5★: 80%, 4★: 15%...)
- [ ] Nút "VIẾT ĐÁNH GIÁ" nổi bật
- [ ] Mỗi review: tên + sao + ngày + nội dung + ảnh (nếu có)
- [ ] Filter theo số sao
- [ ] Pagination hoặc "Xem thêm đánh giá"
- [ ] Ảnh từ review hiển thị gallery nhỏ

### 7.6 Related Products & Cross-sell

#### Checklist
- [ ] "Sản phẩm liên quan" — horizontal scroll, 2-3 items visible
- [ ] "Mua kèm giảm giá" — hiển thị SP phụ kiện + giá combo
- [ ] "Khách hàng cũng mua" — dựa trên data thực
- [ ] Mỗi card: ảnh + tên + giá (compact)
- [ ] Swipe gesture hoạt động mượt

### 7.7 Sticky Add-to-Cart Bar

#### Checklist
- [ ] Hiển thị khi scroll qua nút "Thêm vào giỏ" gốc
- [ ] Nội dung: giá + nút "THÊM VÀO GIỎ" (hoặc "MUA NGAY")
- [ ] Height: 56-64px
- [ ] Background trắng + shadow nhẹ phía trên
- [ ] Z-index cao hơn content nhưng thấp hơn modal
- [ ] Animation slide-up mượt khi xuất hiện
- [ ] Không che chat widget (Zalo/FB)

---

## 8. CTA Optimization

### 8.1 Danh sách CTA cần thêm/tối ưu

| # | CTA | Vị trí | Wording tiếng Việt | Màu/Style | Priority |
| --- | --- | --- | --- | --- | --- |
| 1 | Thêm vào giỏ | Product page | "🛒 THÊM VÀO GIỎ HÀNG" | Cam #FF6D00, full-width | 🔴 |
| 2 | Mua ngay | Product page | "⚡ MUA NGAY" | Đỏ #E53935, outline | 🔴 |
| 3 | Gọi đặt hàng | Product page | "📞 GỌI ĐẶT HÀNG: 1900.xxxx" | Xanh lá #43A047 | 🔴 |
| 4 | Tư vấn Zalo | Product page + floating | "💬 TƯ VẤN QUA ZALO" | Xanh Zalo #0068FF | 🔴 |
| 5 | Đặt hàng | Checkout | "🛒 ĐẶT HÀNG" | Cam #FF6D00, full-width | 🔴 |
| 6 | Sticky add-to-cart | Product page (bottom) | "12.990.000đ — THÊM VÀO GIỎ" | Cam, sticky bottom | 🟠 |
| 7 | Xem khuyến mãi | Homepage banner | "🔥 XEM KHUYẾN MÃI" | Trắng trên nền cam | 🟠 |
| 8 | Flash sale | Homepage | "⏰ XEM TẤT CẢ FLASH SALE →" | Đỏ, text link | 🟠 |
| 9 | Xem tất cả | Category sections | "Xem tất cả [Danh mục] →" | Text link cam | 🟡 |
| 10 | Đăng ký nhận tin | Homepage footer | "📧 ĐĂNG KÝ NHẬN TIN KHUYẾN MÃI" | Cam, full-width | 🟡 |
| 11 | Tra cứu đơn hàng | Header/menu | "📋 Tra cứu đơn hàng" | Text link | 🟡 |
| 12 | Viết đánh giá | Product page tab | "⭐ VIẾT ĐÁNH GIÁ" | Outline cam | 🟡 |
| 13 | So sánh sản phẩm | Product page | "⚖️ So sánh" | Icon button | 🟢 |
| 14 | Thêm vào yêu thích | Product page | "❤️ Yêu thích" | Icon button | 🟢 |
| 15 | Chia sẻ | Product page | "📤 Chia sẻ" | Icon button | 🟢 |

### 8.2 Nguyên tắc CTA hiệu quả

#### Checklist thiết kế CTA
- [ ] **Màu nổi bật:** Cam (#FF6D00) cho CTA chính — tương phản với nền trắng
- [ ] **Kích thước:** Min 48px height, full-width trên mobile
- [ ] **Font:** Bold, ≥ 16px, chữ IN HOA cho CTA chính
- [ ] **Icon:** Thêm emoji/icon trước text để tăng nhận diện
- [ ] **Spacing:** Padding 14-16px vertical, 24px horizontal
- [ ] **Border-radius:** 4-8px (bo góc nhẹ)
- [ ] **Shadow:** Nhẹ cho nút chính (box-shadow)
- [ ] **Hierarchy:** Chỉ 1 CTA chính (cam), còn lại là phụ (outline/text)

#### Checklist wording
- [ ] Dùng **động từ hành động**: "Mua ngay", "Thêm vào giỏ", "Đặt hàng"
- [ ] **Ngắn gọn:** Tối đa 4-5 từ
- [ ] **Tiếng Việt tự nhiên:** Không dùng tiếng Anh (trừ brand name)
- [ ] **Tạo urgency:** "Mua ngay", "Đặt ngay hôm nay"
- [ ] **Giá trị rõ ràng:** "Miễn phí vận chuyển", "Giảm 20%"

### 8.3 CTA theo từng trang

#### Homepage
- [ ] Banner: 1 CTA chính dẫn đến sale/sản phẩm hot
- [ ] Flash Sale: countdown + "Xem tất cả"
- [ ] Mỗi section sản phẩm: "Xem tất cả [danh mục] →"
- [ ] Cuối trang: form đăng ký nhận tin

#### Product Page
- [ ] "THÊM VÀO GIỎ HÀNG" — CTA chính, above the fold
- [ ] "MUA NGAY" — skip cart, checkout trực tiếp
- [ ] "GỌI ĐẶT HÀNG" — cho khách thích gọi điện
- [ ] "TƯ VẤN QUA ZALO" — cho khách cần tư vấn
- [ ] Sticky bar khi scroll xuống

#### Category/Shop Page
- [ ] Nút "Thêm vào giỏ" trên mỗi product card
- [ ] "Quick View" (desktop) hoặc tap để xem chi tiết (mobile)
- [ ] Filter/Sort buttons rõ ràng

#### Cart Page
- [ ] "TIẾN HÀNH THANH TOÁN" — CTA chính, nổi bật
- [ ] "Tiếp tục mua sắm" — CTA phụ, text link
- [ ] Input mã giảm giá + nút "Áp dụng"

#### Checkout Page
- [ ] "ĐẶT HÀNG" — CTA duy nhất, cam, full-width, sticky bottom
- [ ] Trust badges ngay trên nút đặt hàng

### 8.4 CSS cho CTA chính

```css
/* CTA chính — Thêm vào giỏ / Mua ngay */
.cta-primary {
  background-color: #FF6D00;
  color: #FFFFFF;
  font-size: 16px;
  font-weight: 700;
  text-transform: uppercase;
  min-height: 52px;
  width: 100%;
  border: none;
  border-radius: 6px;
  padding: 14px 24px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  box-shadow: 0 2px 8px rgba(255, 109, 0, 0.3);
  transition: background-color 0.2s, transform 0.1s;
}

.cta-primary:hover {
  background-color: #E65100;
}

.cta-primary:active {
  transform: scale(0.98);
}

/* CTA phụ — Gọi đặt hàng */
.cta-secondary {
  background-color: transparent;
  color: #43A047;
  font-size: 15px;
  font-weight: 600;
  min-height: 48px;
  width: 100%;
  border: 2px solid #43A047;
  border-radius: 6px;
  padding: 12px 24px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}

/* Sticky bottom CTA bar */
.sticky-cta-bar {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: #FFFFFF;
  padding: 8px 16px;
  box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
}

.sticky-cta-bar .price {
  font-size: 18px;
  font-weight: 700;
  color: #E53935;
  white-space: nowrap;
}

.sticky-cta-bar .cta-primary {
  flex: 1;
  min-height: 44px;
}
```

---

*Hướng dẫn Tối ưu Mobile & UX — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Phiên bản: 1.0*