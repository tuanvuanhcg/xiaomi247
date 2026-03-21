# Việt Hóa & Tạo Trang Nội Dung — Xiaomi247.com

> **Ngày tạo:** 21/03/2026
> **Áp dụng cho:** WordPress + WooCommerce + Motta Theme
> **Liên quan:** Bug #7, #8, #9, #10, #11, #12 trong [Bug Fix Checklist](../marketing/01-technical-audit/bug-fix-checklist.md)

---

## Mục lục

- [Phần 1 — Việt Hóa Theme & WooCommerce](#phần-1--việt-hóa-theme--woocommerce)
- [Phần 2 — Tạo Trang Nội Dung](#phần-2--tạo-trang-nội-dung)
- [Phần 3 — Cập Nhật Footer](#phần-3--cập-nhật-footer)

---

# Phần 1 — Việt Hóa Theme & WooCommerce

> **Giải quyết:** Bug #8 (Search placeholder), Bug #9 (Breadcrumb), Bug #10 (WooCommerce strings)

## 1.1. Cài đặt Plugin Loco Translate

### Bước thao tác:

1. **Đăng nhập WP Admin** → `xiaomi247.com/wp-admin`
2. Vào **Plugins → Add New**
3. Tìm kiếm **"Loco Translate"**
4. Nhấn **Install Now** → sau đó nhấn **Activate**
5. Plugin sẽ xuất hiện trong menu trái: **Loco Translate**

## 1.2. Việt hóa Theme Motta

### Bước thao tác:

1. Vào **Loco Translate → Themes**
2. Chọn **Motta** (hoặc Motta Child nếu đang dùng child theme)
3. Nhấn **+ New language**
4. Chọn **Vietnamese (vi)** → Location: **Custom** → Nhấn **Start translating**
5. Dùng thanh **Filter** để tìm từng string tiếng Anh
6. Nhấn vào string → nhập bản dịch tiếng Việt ở ô phía dưới
7. Nhấn **Save** sau khi dịch xong mỗi đợt

> ⚠️ **Quan trọng:** Chọn location **Custom** để bản dịch không bị mất khi cập nhật theme.

## 1.3. Việt hóa WooCommerce

### Bước thao tác:

1. Vào **Loco Translate → Plugins**
2. Chọn **WooCommerce**
3. Kiểm tra xem đã có bản dịch **Vietnamese** chưa
4. Nếu chưa → **+ New language** → Chọn **Vietnamese (vi)** → Location: **Custom**
5. Dịch các string theo bảng bên dưới

## 1.4. Thiết lập ngôn ngữ WordPress

### Bước thao tác:

1. Vào **Settings → General**
2. Mục **Site Language** → chọn **Tiếng Việt**
3. Nhấn **Save Changes**
4. Kiểm tra lại frontend xem các string WooCommerce mặc định đã chuyển sang tiếng Việt chưa

> 💡 **Lưu ý:** Khi đặt Site Language = Tiếng Việt, WordPress & WooCommerce sẽ tự động load bản dịch cộng đồng cho nhiều string. Tuy nhiên, các string của theme Motta vẫn cần dịch thủ công qua Loco Translate.

---

## 1.5. Bảng Strings Cần Việt Hóa

### 🔍 Search & Navigation

| String gốc (English) | Bản dịch tiếng Việt | Vị trí |
|---|---|---|
| Search | Tìm kiếm | Header |
| Search products… | Tìm kiếm sản phẩm... | Search placeholder |
| Search for products | Tìm kiếm sản phẩm | Search placeholder (variant) |
| No results found | Không tìm thấy kết quả | Search results |
| Home | Trang chủ | Breadcrumb, Menu |
| Shop | Cửa hàng | Breadcrumb, Menu |
| All categories | Tất cả danh mục | Category filter |
| Menu | Menu | Mobile menu |
| Close | Đóng | Popup, Modal |
| Back | Quay lại | Navigation |
| View All | Xem tất cả | Category, Product listing |

### 🛒 WooCommerce — Sản phẩm

| String gốc (English) | Bản dịch tiếng Việt | Vị trí |
|---|---|---|
| Add to cart | Thêm vào giỏ hàng | Product page, Product card |
| Buy now | Mua ngay | Product page |
| Add to wishlist | Thêm vào yêu thích | Product page |
| Out of stock | Hết hàng | Product page |
| In stock | Còn hàng | Product page |
| On sale | Đang giảm giá | Product badge |
| Sale! | Giảm giá! | Product badge |
| New | Mới | Product badge |
| Hot | Hot | Product badge |
| SKU | Mã SP | Product detail |
| Category | Danh mục | Product detail |
| Categories | Danh mục | Product detail |
| Tag | Nhãn | Product detail |
| Tags | Nhãn | Product detail |
| Description | Mô tả | Product tab |
| Additional information | Thông tin bổ sung | Product tab |
| Reviews | Đánh giá | Product tab |
| Related products | Sản phẩm liên quan | Product page |
| You may also like | Bạn cũng có thể thích | Product page |
| Quick View | Xem nhanh | Product card |
| Compare | So sánh | Product card |
| Share | Chia sẻ | Product page |

### 🛒 WooCommerce — Giỏ hàng & Thanh toán

| String gốc (English) | Bản dịch tiếng Việt | Vị trí |
|---|---|---|
| Cart | Giỏ hàng | Header, Page |
| Shopping Cart | Giỏ hàng | Cart page |
| Your cart is empty | Giỏ hàng của bạn đang trống | Cart page |
| Continue shopping | Tiếp tục mua sắm | Cart page |
| View cart | Xem giỏ hàng | Mini cart |
| Update cart | Cập nhật giỏ hàng | Cart page |
| Remove this item | Xóa sản phẩm này | Cart page |
| Subtotal | Tạm tính | Cart, Checkout |
| Total | Tổng cộng | Cart, Checkout |
| Coupon | Mã giảm giá | Cart page |
| Apply coupon | Áp dụng mã giảm giá | Cart page |
| Coupon code | Nhập mã giảm giá | Cart page |
| Checkout | Thanh toán | Cart page, Header |
| Proceed to checkout | Tiến hành thanh toán | Cart page |
| Shipping | Vận chuyển | Checkout |
| Free shipping | Miễn phí vận chuyển | Checkout |
| Flat rate | Phí cố định | Checkout |
| Billing details | Thông tin thanh toán | Checkout |
| Ship to a different address? | Giao đến địa chỉ khác? | Checkout |
| Order notes | Ghi chú đơn hàng | Checkout |
| Place order | Đặt hàng | Checkout |
| Order received | Đã nhận đơn hàng | Thank you page |
| Thank you. Your order has been received. | Cảm ơn bạn. Đơn hàng của bạn đã được tiếp nhận. | Thank you page |
| Payment method | Phương thức thanh toán | Checkout |
| Cash on delivery | Thanh toán khi nhận hàng (COD) | Checkout |
| Bank transfer | Chuyển khoản ngân hàng | Checkout |

### 👤 WooCommerce — Tài khoản

| String gốc (English) | Bản dịch tiếng Việt | Vị trí |
|---|---|---|
| My Account | Tài khoản của tôi | Header, Page |
| Login | Đăng nhập | Login page |
| Register | Đăng ký | Register page |

### 🏷️ Motta Theme — Strings riêng

| String gốc (English) | Bản dịch tiếng Việt | Vị trí |
|---|---|---|
| Recently Viewed | Đã xem gần đây | Product section |
| Best Sellers | Bán chạy nhất | Homepage section |
| Featured Products | Sản phẩm nổi bật | Homepage section |
| New Arrivals | Sản phẩm mới | Homepage section |
| Top Rated | Đánh giá cao nhất | Homepage section |
| Trending | Xu hướng | Homepage section |
| Deal of the day | Deal trong ngày | Homepage section |
| Flash Sale | Flash Sale | Homepage section |
| Sold | Đã bán | Product card |
| items | sản phẩm | Product count |
| Filter | Lọc | Shop page |
| Sort by | Sắp xếp theo | Shop page |
| Default sorting | Mặc định | Sort option |
| Sort by popularity | Phổ biến nhất | Sort option |
| Sort by average rating | Đánh giá cao nhất | Sort option |
| Sort by latest | Mới nhất | Sort option |
| Sort by price: low to high | Giá: thấp đến cao | Sort option |
| Sort by price: high to low | Giá: cao đến thấp | Sort option |
| Showing all %d results | Hiển thị tất cả %d sản phẩm | Shop page |
| Showing %1$d–%2$d of %3$d results | Hiển thị %1$d–%2$d trong %3$d sản phẩm | Shop page |
| Load more | Xem thêm | Product listing |
| Previous | Trước | Pagination |
| Next | Tiếp | Pagination |
| Read more | Xem thêm | Blog/Product |
| View more | Xem thêm | General |

### 📧 WooCommerce — Email & Thông báo

| String gốc (English) | Bản dịch tiếng Việt | Vị trí |
|---|---|---|
| Your order is on-hold | Đơn hàng đang chờ xử lý | Email |
| Your order is processing | Đơn hàng đang được xử lý | Email |
| Your order is complete | Đơn hàng đã hoàn thành | Email |
| Order #%s | Đơn hàng #%s | Email, Account |
| Date | Ngày | Order detail |
| Status | Trạng thái | Order detail |
| Pending | Chờ thanh toán | Order status |
| Processing | Đang xử lý | Order status |
| On hold | Chờ xử lý | Order status |
| Completed | Hoàn thành | Order status |
| Cancelled | Đã hủy | Order status |
| Refunded | Đã hoàn tiền | Order status |
| Failed | Thất bại | Order status |

### 📝 Form Fields

| String gốc (English) | Bản dịch tiếng Việt | Vị trí |
|---|---|---|
| First name | Họ | Checkout, Account |
| Last name | Tên | Checkout, Account |
| Company name (optional) | Tên công ty (tùy chọn) | Checkout |
| Country / Region | Quốc gia | Checkout |
| Street address | Địa chỉ | Checkout |
| Apartment, suite, unit, etc. (optional) | Số nhà, tòa nhà, tầng... (tùy chọn) | Checkout |
| Town / City | Thành phố / Tỉnh | Checkout |
| State / County | Quận / Huyện | Checkout |
| Postcode / ZIP | Mã bưu điện | Checkout |
| Phone | Số điện thoại | Checkout |
| Email address | Địa chỉ email | Checkout |
| Create an account? | Tạo tài khoản? | Checkout |
| Save my information for faster checkout | Lưu thông tin để thanh toán nhanh hơn | Checkout |

> 💡 **Mẹo:** Sau khi dịch xong, mở một cửa sổ ẩn danh (Incognito) và duyệt qua tất cả các trang để kiểm tra xem còn string tiếng Anh nào sót không.

---

# Phần 2 — Tạo Trang Nội Dung

> **Giải quyết:** Bug #11 (Trang "Về chúng tôi"), Bug #12 (Thiếu trang Chính sách)
> **Nội dung tham chiếu:** Xem thư mục `marketing/04-trust-building/`

## 2.1. Tạo trang "Về Xiaomi247"

> **Nguồn nội dung:** [`marketing/04-trust-building/about-us-page-content.md`](../marketing/04-trust-building/about-us-page-content.md)

### Bước thao tác:

1. Vào **WP Admin → Pages → Add New**
2. **Tiêu đề trang:** `Về Xiaomi247`
3. **Slug (URL):** `ve-chung-toi`
4. Chọn **Page Template:** Full Width (hoặc template phù hợp của Motta)
5. **Copy nội dung** từ file `about-us-page-content.md` vào editor
6. Cấu trúc nội dung theo các section:

#### Section 1: Giới Thiệu Xiaomi247
- Tiêu đề H2: **"🏪 Giới Thiệu Xiaomi247"**
- Đoạn mô tả về cửa hàng, sứ mệnh
- Quote nổi bật: *"Tại Xiaomi247, mỗi sản phẩm bán ra đều là một lời cam kết..."*

#### Section 2: Sứ Mệnh & Tầm Nhìn
- Tiêu đề H2: **"🎯 Sứ Mệnh & Tầm Nhìn"**
- 3 mục: Sứ mệnh, Tầm nhìn, Giá trị cốt lõi (dùng bảng hoặc icon box)

#### Section 3: Cam Kết Chất Lượng
- Tiêu đề H2: **"✅ Cam Kết Chất Lượng"**
- 5 cam kết với icon: Chính hãng, Bảo hành, Giao hàng, Đổi trả, Hỗ trợ 24/7
- Dùng **Icon Box** hoặc **Feature Box** của Motta/Elementor

#### Section 4: Đội Ngũ
- Tiêu đề H2: **"👥 Đội Ngũ Của Chúng Tôi"**
- Bảng hoặc card layout: Tư vấn, Kỹ thuật, Vận chuyển, Content

#### Section 5: Đối Tác & Chứng Nhận
- Tiêu đề H2: **"🤝 Đối Tác & Chứng Nhận"**
- Logo đối tác vận chuyển: GHN, GHTK, Viettel Post
- Logo thanh toán: VNPay, MoMo, COD

#### Section 6: Thông Tin Liên Hệ
- Bảng thông tin: Website, Hotline, Zalo, Facebook, Email, Địa chỉ, MST

7. **SEO Settings** (Yoast SEO / Rank Math):
   - Meta title: `Về Xiaomi247 - Đại Lý Xiaomi Chính Hãng Uy Tín`
   - Meta description: `Xiaomi247.com - Chuyên cung cấp sản phẩm Xiaomi chính hãng với giá tốt nhất. Bảo hành chính hãng 12-24 tháng, giao hàng toàn quốc, đổi trả 7 ngày.`
8. Nhấn **Publish**
9. Thêm trang vào **menu chính** (Appearance → Menus → chọn "Về chúng tôi" → Add to Menu)

---

## 2.2. Tạo trang "Chính Sách Bảo Hành"

> **Nguồn nội dung:** [`marketing/04-trust-building/policy-pages/bao-hanh.md`](../marketing/04-trust-building/policy-pages/bao-hanh.md)

### Bước thao tác:

1. Vào **WP Admin → Pages → Add New**
2. **Tiêu đề trang:** `Chính Sách Bảo Hành`
3. **Slug (URL):** `chinh-sach-bao-hanh`
4. Chọn **Page Template:** Full Width
5. **Copy nội dung** từ file `bao-hanh.md` vào editor, bao gồm:

#### Các section cần có:
- **Thời gian bảo hành** — Bảng theo nhóm sản phẩm (Điện thoại 18 tháng, Tablet 12 tháng, Tai nghe 6 tháng...)
- **Điều kiện được bảo hành** — Checklist ✅ (5 điều kiện)
- **Trường hợp KHÔNG được bảo hành** — Checklist ❌ (8 trường hợp)
- **Quy trình bảo hành** — 5 bước: Liên hệ → Xác nhận → Gửi SP → Xử lý → Nhận SP
- **Chính sách 1 đổi 1** — Trong 30 ngày đầu
- **Liên hệ bảo hành** — Hotline, Zalo, Email, Giờ tiếp nhận

6. **SEO Settings:**
   - Meta title: `Chính Sách Bảo Hành | Xiaomi247 - Đại Lý Xiaomi Chính Hãng`
   - Meta description: `Chính sách bảo hành sản phẩm Xiaomi chính hãng tại Xiaomi247.com. Bảo hành 12-24 tháng, 1 đổi 1 trong 30 ngày đầu, hỗ trợ bảo hành tận nơi.`
7. Nhấn **Publish**

---

## 2.3. Tạo trang "Chính Sách Đổi Trả"

> **Nguồn nội dung:** [`marketing/04-trust-building/policy-pages/doi-tra.md`](../marketing/04-trust-building/policy-pages/doi-tra.md)

### Bước thao tác:

1. Vào **WP Admin → Pages → Add New**
2. **Tiêu đề trang:** `Chính Sách Đổi Trả`
3. **Slug (URL):** `chinh-sach-doi-tra`
4. Chọn **Page Template:** Full Width
5. **Copy nội dung** từ file `doi-tra.md` vào editor, bao gồm:

#### Các section cần có:
- **Thời gian đổi trả** — Bảng: Đổi mới (30 ngày), Đổi/trả đổi ý (7 ngày), Hoàn tiền (7 ngày)
- **Điều kiện đổi trả** — ✅ Được đổi/trả khi & ❌ KHÔNG chấp nhận khi
- **Quy trình đổi trả** — 5 bước: Gửi yêu cầu → Xác nhận → Gửi SP → Kiểm tra → Đổi/Hoàn tiền
- **Chính sách hoàn tiền** — Bảng: phương thức gốc → hình thức hoàn → thời gian
- **Lưu ý quan trọng** — Khuyến nghị quay video mở hàng
- **Liên hệ đổi trả** — Hotline, Zalo, Email

6. **SEO Settings:**
   - Meta title: `Chính Sách Đổi Trả Hàng | Xiaomi247 - Đại Lý Xiaomi Chính Hãng`
   - Meta description: `Chính sách đổi trả sản phẩm Xiaomi tại Xiaomi247.com. Đổi trả miễn phí trong 7 ngày, hoàn tiền 100%, quy trình nhanh chóng đơn giản.`
7. Nhấn **Publish**

---

## 2.4. Tạo trang "Chính Sách Vận Chuyển"

> **Nguồn nội dung:** [`marketing/04-trust-building/policy-pages/van-chuyen.md`](../marketing/04-trust-building/policy-pages/van-chuyen.md)

### Bước thao tác:

1. Vào **WP Admin → Pages → Add New**
2. **Tiêu đề trang:** `Chính Sách Vận Chuyển`
3. **Slug (URL):** `chinh-sach-van-chuyen`
4. Chọn **Page Template:** Full Width
5. **Copy nội dung** từ file `van-chuyen.md` vào editor, bao gồm:

#### Các section cần có:
- **Phí vận chuyển** — Bảng: giá trị đơn × khu vực → phí ship (Miễn phí từ 500K)
- **Thời gian giao hàng** — Bảng: Nội thành HN 1-2 ngày, HCM 2-3 ngày, Tỉnh 3-5 ngày
- **Đối tác vận chuyển** — GHN, GHTK, Viettel Post, Grab Express
- **Hình thức thanh toán khi nhận hàng** — COD, Chuyển khoản, Ví điện tử
- **Quy trình kiểm tra hàng** — 3 bước khi nhận hàng
- **Các trường hợp đặc biệt** — Giao thất bại, thất lạc, hư hỏng do vận chuyển
- **Liên hệ hỗ trợ** — Hotline, Zalo, Tra cứu đơn hàng

6. **SEO Settings:**
   - Meta title: `Chính Sách Vận Chuyển & Giao Hàng | Xiaomi247`
   - Meta description: `Chính sách vận chuyển Xiaomi247.com. Miễn phí ship đơn từ 500K, giao hàng toàn quốc 1-5 ngày, hỗ trợ kiểm tra hàng trước khi thanh toán COD.`
7. Nhấn **Publish**

---

## 2.5. Checklist sau khi tạo trang

| Trang | Đã tạo? | Đã publish? | Đã thêm vào menu? | SEO đã cấu hình? |
|---|---|---|---|---|
| Về Xiaomi247 (`/ve-chung-toi`) | ⬜ | ⬜ | ⬜ | ⬜ |
| Chính sách bảo hành (`/chinh-sach-bao-hanh`) | ⬜ | ⬜ | ⬜ | ⬜ |
| Chính sách đổi trả (`/chinh-sach-doi-tra`) | ⬜ | ⬜ | ⬜ | ⬜ |
| Chính sách vận chuyển (`/chinh-sach-van-chuyen`) | ⬜ | ⬜ | ⬜ | ⬜ |

---

# Phần 3 — Cập Nhật Footer

> **Giải quyết:** Bug #7 (Footer chưa cập nhật thông tin)

## 3.1. Truy cập cài đặt Footer

### Bước thao tác:

1. Vào **WP Admin → Appearance → Customize → Footer**
   - Hoặc: **Appearance → Widgets** (nếu footer dùng widget areas)
   - Hoặc: **Motta Options → Footer** (nếu theme có options panel riêng)
2. Xác định footer có bao nhiêu cột (thường 3-4 cột)

## 3.2. Cột 1 — Thông Tin Công Ty

### Nội dung cần thêm:

```
[Logo Xiaomi247]

Xiaomi247 - Đại lý Xiaomi chính hãng
Chuyên cung cấp sản phẩm Xiaomi chính hãng
với giá tốt nhất Việt Nam.

📍 [Địa chỉ văn phòng/kho hàng]
📞 Hotline: 1900.xxxx
📧 Email: support@xiaomi247.com
🕐 8h00 - 21h00 (Thứ 2 - Chủ Nhật)
```

### Bước thao tác:
1. Chọn widget area **Footer Column 1**
2. Thêm widget **Image** → Upload logo Xiaomi247
3. Thêm widget **Text/HTML** → Paste nội dung trên
4. Lưu

## 3.3. Cột 2 — Links Chính Sách

### Nội dung cần thêm:

```
CHÍNH SÁCH
• Chính sách bảo hành → /chinh-sach-bao-hanh
• Chính sách đổi trả → /chinh-sach-doi-tra
• Chính sách vận chuyển → /chinh-sach-van-chuyen
• Chính sách bảo mật → /chinh-sach-bao-mat
• Hướng dẫn mua hàng → /huong-dan-mua-hang
```

### Bước thao tác:
1. Vào **Appearance → Menus**
2. Tạo menu mới tên **"Footer - Chính sách"**
3. Thêm các trang chính sách đã tạo ở Phần 2 vào menu
4. Vào **Appearance → Widgets** hoặc **Customize → Footer**
5. Chọn widget area **Footer Column 2**
6. Thêm widget **Navigation Menu** → chọn menu "Footer - Chính sách"
7. Đặt tiêu đề widget: **"Chính sách"**
8. Lưu

## 3.4. Cột 3 — Hỗ Trợ Khách Hàng

### Nội dung cần thêm:

```
HỖ TRỢ KHÁCH HÀNG
• Liên hệ → /lien-he
• Về Xiaomi247 → /ve-chung-toi
• Tin tức → /blog
• Câu hỏi thường gặp → /faq
• Tra cứu đơn hàng → /tra-cuu-don-hang
```

### Bước thao tác:
1. Tạo menu **"Footer - Hỗ trợ"** (tương tự bước ở mục 3.3)
2. Thêm vào widget area **Footer Column 3**
3. Đặt tiêu đề widget: **"Hỗ trợ khách hàng"**
4. Lưu

## 3.5. Cột 4 — Social Media & Thanh Toán

### Bước thao tác cho Social Media Icons:

1. Vào **Appearance → Customize → Footer** (hoặc Motta Options → Footer → Social)
2. Nếu Motta có tùy chọn Social Icons:
   - Thêm **Facebook:** `https://fb.com/xiaomi247`
   - Thêm **Instagram:** `https://instagram.com/xiaomi247`
   - Thêm **YouTube:** `https://youtube.com/@xiaomi247`
   - Thêm **TikTok:** `https://tiktok.com/@xiaomi247`
   - Thêm **Zalo:** Link Zalo OA (hoặc dùng icon custom)
3. Nếu không có tùy chọn sẵn:
   - Thêm widget **Social Icons** (hoặc dùng HTML custom)
   - Hoặc cài plugin **Simple Social Icons**

### Bước thao tác cho Logo Thanh Toán:

1. Thêm widget **Image** hoặc **Custom HTML** vào Footer Column 4
2. Thêm hình ảnh logo các phương thức thanh toán:
   - VNPay, MoMo, ZaloPay, Visa, Mastercard, COD
3. Thêm text: **"Hỗ trợ thanh toán"** làm tiêu đề

## 3.6. Footer Bottom Bar

### Bước thao tác:

1. Vào **Appearance → Customize → Footer → Bottom Bar** (hoặc Copyright)
2. Cập nhật text copyright:

```
© 2026 Xiaomi247.com - Đại lý Xiaomi chính hãng. Bảo lưu mọi quyền.
GPKD số: [Số GPKD] do Sở KH&ĐT [Tỉnh/TP] cấp ngày [DD/MM/YYYY]
```

3. Lưu

## 3.7. Checklist Footer

| Hạng mục | Hoàn thành? |
|---|---|
| Logo + thông tin công ty (Cột 1) | ⬜ |
| Links chính sách (Cột 2) | ⬜ |
| Links hỗ trợ khách hàng (Cột 3) | ⬜ |
| Social media icons (Cột 4) | ⬜ |
| Logo thanh toán (Cột 4) | ⬜ |
| Copyright text (Bottom bar) | ⬜ |
| Kiểm tra trên Desktop | ⬜ |
| Kiểm tra trên Mobile | ⬜ |

---

## ✅ Tổng kết

| Phần | Mô tả | Bug liên quan |
|---|---|---|
| Phần 1 | Việt hóa theme Motta + WooCommerce bằng Loco Translate | #8, #9, #10 |
| Phần 2 | Tạo 4 trang nội dung: Về chúng tôi, 3 trang chính sách | #11, #12 |
| Phần 3 | Cập nhật footer: thông tin, links, social, logo | #7 |

### Thứ tự thực hiện đề xuất:
1. **Bước 1:** Cài Loco Translate + đặt ngôn ngữ Tiếng Việt (Phần 1.1 + 1.4)
2. **Bước 2:** Dịch strings theme Motta (Phần 1.2)
3. **Bước 3:** Dịch strings WooCommerce còn thiếu (Phần 1.3)
4. **Bước 4:** Tạo 4 trang nội dung (Phần 2.1 → 2.4)
5. **Bước 5:** Cập nhật footer (Phần 3)
6. **Bước 6:** Kiểm tra tổng thể trên Desktop + Mobile

---

*Hướng dẫn Việt hóa & Tạo trang nội dung — Xiaomi247.com*
*Ngày tạo: 21/03/2026*

