# ✅ Bug Fix Checklist — Xiaomi247.com

> **Ngày tạo:** 21/03/2026
> **Cập nhật lần cuối:** 21/03/2026
> **Tổng số lỗi:** 15 | **Đã fix:** 0 | **Còn lại:** 15

---

## Hướng dẫn sử dụng

| Ký hiệu | Ý nghĩa |
| --- | --- |
| 🔴 Critical | Ảnh hưởng nghiêm trọng — cần fix ngay trong 24h |
| 🟠 High | Ảnh hưởng lớn — fix trong 48h |
| 🟡 Medium | Ảnh hưởng trung bình — fix trong 1 tuần |
| 🟢 Low | Ảnh hưởng nhỏ — fix khi có thời gian |
| ⬜ | Chưa bắt đầu |
| 🔄 | Đang xử lý |
| ✅ | Đã hoàn thành |

---

## 🔴 Critical Priority (Fix ngay — 24h)

### Bug #1: Blog Page trả lỗi 404

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🔴 Critical |
| Trạng thái | ⬜ Chưa fix |
| URL lỗi | xiaomi247.com/blog |
| Mô tả | Trang Blog trả về HTTP 404 Not Found, khách không truy cập được |
| Ảnh hưởng | Mất kênh content marketing, giảm SEO, mất trust khách hàng |
| **Cách fix** | 1. Vào WP Admin → Pages → tạo trang "Blog" mới |
|  | 2. Settings → Reading → đặt Posts page = trang Blog vừa tạo |
|  | 3. Kiểm tra permalink: Settings → Permalinks → Save lại |
|  | 4. Thêm trang Blog vào menu navigation |
| Người thực hiện | |
| Ngày hoàn thành | |

### Bug #2: Contact Page trả lỗi 404

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🔴 Critical |
| Trạng thái | ⬜ Chưa fix |
| URL lỗi | xiaomi247.com/contact |
| Mô tả | Trang Liên hệ trả về HTTP 404, khách không liên hệ được |
| Ảnh hưởng | Mất lead, không có kênh hỗ trợ, giảm trust, ảnh hưởng Google Business |
| **Cách fix** | 1. Cài plugin Contact Form 7 hoặc WPForms |
|  | 2. Tạo form liên hệ: Họ tên, Email, SĐT, Nội dung |
|  | 3. Tạo trang "Liên hệ" với shortcode form |
|  | 4. Thêm thông tin: địa chỉ, hotline, email, bản đồ Google Maps |
|  | 5. Thêm vào menu navigation |
| Người thực hiện | |
| Ngày hoàn thành | |

### Bug #3: Demo Text trong Menu — Home Variants

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🔴 Critical |
| Trạng thái | ⬜ Chưa fix |
| Vị trí | Main Navigation Menu |
| Mô tả | Menu hiển thị demo items: Home v1, Home v2, Home v3, ... Home v10 |
| Ảnh hưởng | Cực kỳ mất chuyên nghiệp, khách hàng nhầm lẫn, bounce rate cao |
| **Cách fix** | 1. WP Admin → Appearance → Menus |
|  | 2. Chọn Primary Menu (hoặc Main Menu) |
|  | 3. Xóa TẤT CẢ các mục Home v1 đến Home v10 |
|  | 4. Giữ lại hoặc tạo mới 1 mục "Trang chủ" duy nhất trỏ về homepage |
|  | 5. Save Menu |
| Người thực hiện | |
| Ngày hoàn thành | |

### Bug #4: Demo Text trong Menu — Shop Variants

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🔴 Critical |
| Trạng thái | ⬜ Chưa fix |
| Vị trí | Main Navigation Menu |
| Mô tả | Menu hiển thị: Shop v1, Shop v2, Shop v3, Shop v4 |
| Ảnh hưởng | Giao diện rối, khách không biết click vào đâu |
| **Cách fix** | 1. WP Admin → Appearance → Menus |
|  | 2. Xóa TẤT CẢ các mục Shop v1 đến Shop v4 |
|  | 3. Tạo menu "Sản phẩm" trỏ về trang Shop chính |
|  | 4. Thêm mega menu danh mục: Điện thoại, Tablet, Đồng hồ, Phụ kiện, Thiết bị thông minh, Laptop |
|  | 5. Save Menu |
| Người thực hiện | |
| Ngày hoàn thành | |

---

## 🟠 High Priority (Fix trong 48h)

### Bug #5: Header Demo Items (Header v1-v10)

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🟠 High |
| Trạng thái | ⬜ Chưa fix |
| Vị trí | Header section |
| Mô tả | Hiển thị demo header variants: Header v1, v2, ... v10 |
| **Cách fix** | 1. WP Admin → Appearance → Customize → Header (hoặc Motta Options → Header) |
|  | 2. Chọn 1 layout header phù hợp (khuyến nghị: logo trái, menu giữa, cart/search phải) |
|  | 3. Xóa bỏ header switcher/demo selector nếu có |
|  | 4. Lưu & kiểm tra trên cả desktop và mobile |
| Người thực hiện | |
| Ngày hoàn thành | |

### Bug #6: Menu Navigation chưa cấu trúc đúng

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🟠 High |
| Trạng thái | ⬜ Chưa fix |
| Mô tả | Menu chính cần tái cấu trúc hoàn toàn sau khi xóa demo items |
| **Cách fix** | Tạo menu mới với cấu trúc: |
|  | • Trang chủ |
|  | • Sản phẩm (mega menu: 6 danh mục + sản phẩm nổi bật) |
|  | • Khuyến mãi |
|  | • Tin tức / Blog |
|  | • Về chúng tôi |
|  | • Liên hệ |
| Người thực hiện | |
| Ngày hoàn thành | |

### Bug #7: Footer chưa cập nhật thông tin

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🟠 High |
| Trạng thái | ⬜ Chưa fix |
| Mô tả | Kiểm tra footer có thông tin demo hoặc thiếu thông tin liên hệ |
| **Cách fix** | 1. Cập nhật: địa chỉ, SĐT, email, giờ làm việc |
|  | 2. Thêm: links chính sách (đổi trả, bảo hành, vận chuyển) |
|  | 3. Thêm: social media icons (Facebook, Zalo, Instagram) |
|  | 4. Thêm: logo & slogan |
| Người thực hiện | |
| Ngày hoàn thành | |

---

## 🟡 Medium Priority (Fix trong 1 tuần)

### Bug #8: Search Placeholder chưa Việt hóa

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🟡 Medium |

### Bug #11: Trang "Về chúng tôi" thiếu hoặc chưa có nội dung

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🟡 Medium |
| Trạng thái | ⬜ Chưa fix |
| Mô tả | Kiểm tra xem trang giới thiệu đã có nội dung chưa |
| **Cách fix** | 1. Tạo trang "Về Xiaomi247" với nội dung: giới thiệu, cam kết, đội ngũ |
|  | 2. Thêm vào menu chính |
| Người thực hiện | |
| Ngày hoàn thành | |

### Bug #12: Thiếu trang Chính sách

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🟡 Medium |
| Trạng thái | ⬜ Chưa fix |
| Mô tả | Cần có các trang chính sách bắt buộc cho e-commerce |
| **Cách fix** | Tạo 4 trang chính sách: |
|  | • Chính sách đổi trả |
|  | • Chính sách bảo hành |
|  | • Chính sách vận chuyển |
|  | • Chính sách bảo mật thông tin |
| Người thực hiện | |
| Ngày hoàn thành | |

---

## 🟢 Low Priority (Fix khi có thời gian)

### Bug #13: Favicon chưa cập nhật

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🟢 Low |
| Trạng thái | ⬜ Chưa fix |
| Mô tả | Kiểm tra favicon đã là logo Xiaomi247 chưa (có thể đang dùng favicon mặc định WP) |
| **Cách fix** | WP Admin → Appearance → Customize → Site Identity → Upload favicon 512x512px |
| Người thực hiện | |
| Ngày hoàn thành | |

### Bug #14: Meta description mặc định

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🟢 Low |
| Trạng thái | ⬜ Chưa fix |
| Mô tả | Trang chủ và các trang có thể đang dùng meta description mặc định WordPress |
| **Cách fix** | 1. Cài Yoast SEO hoặc Rank Math |
|  | 2. Cấu hình meta title & description cho trang chủ |
|  | 3. Thiết lập template cho product pages, category pages |
| Người thực hiện | |
| Ngày hoàn thành | |

### Bug #15: Open Graph & Social Sharing chưa cấu hình

| Hạng mục | Chi tiết |
| --- | --- |
| Priority | 🟢 Low |
| Trạng thái | ⬜ Chưa fix |
| Mô tả | Khi share link trên Facebook/Zalo có thể hiển thị sai hình ảnh hoặc mô tả |
| **Cách fix** | 1. Cấu hình OG tags qua Yoast SEO / Rank Math |
|  | 2. Set OG image mặc định (1200x630px) |
|  | 3. Test bằng Facebook Debugger |
| Người thực hiện | |
| Ngày hoàn thành | |

---

## 📊 Tổng kết

| Priority | Số lỗi | Mô tả |
| --- | --- | --- |
| 🔴 Critical | 4 | Blog 404, Contact 404, Menu demo (Home), Menu demo (Shop) |
| 🟠 High | 3 | Header demo, Menu cấu trúc, Footer |
| 🟡 Medium | 4 | Search placeholder, Breadcrumb, WooCommerce strings, Về chúng tôi, Chính sách |
| 🟢 Low | 3 | Favicon, Meta description, Open Graph |
| **Tổng** | **15** | |

## 📋 Thứ tự fix đề xuất

1. **Ngày 1:** Fix Bug #3, #4 (xóa demo menu) → Bug #5 (header) → Bug #6 (tái cấu trúc menu)
2. **Ngày 2:** Fix Bug #1 (Blog 404) → Bug #2 (Contact 404) → Bug #7 (Footer)
3. **Ngày 3-4:** Fix Bug #8, #9, #10 (Việt hóa) → Bug #11, #12 (trang nội dung)
4. **Ngày 5:** Fix Bug #13, #14, #15 (SEO & social) → Kiểm tra tổng thể

---

*Bug Fix Checklist — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Cập nhật: 21/03/2026*

