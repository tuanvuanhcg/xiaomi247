# Hướng Dẫn Tối Ưu Conversion Rate (CRO) — Xiaomi247.com

> **Mục tiêu:** Tăng conversion rate từ 1-2% lên 3-5% trong 3 tháng

---

## 1. Tối Ưu Trang Sản Phẩm (Product Page)

### 1.1. Layout tối ưu (từ trên xuống)

```
┌──────────────────────────────────────────────┐
│ Breadcrumb: Trang chủ > Điện thoại > Xiaomi  │
├───────────────────┬──────────────────────────┤
│                   │ Tên sản phẩm (H1)        │
│   Gallery ảnh     │ Rating ⭐⭐⭐⭐⭐ (125 đánh giá) │
│   (5-8 ảnh +      │ ─────────────────────────│
│    1-2 video)     │ Giá: 4.990.000đ          │
│                   │ Giá gốc: 5.990.000đ (-17%)│
│                   │ ─────────────────────────│
│                   │ [Chọn màu] [Chọn phiên bản] │
│                   │ ─────────────────────────│
│                   │ 🛡️ Chính hãng | 🔧 BH 18T │
│                   │ 🚚 Free ship  | 🔄 Đổi 7 ngày │
│                   │ ─────────────────────────│
│                   │ [🛒 THÊM VÀO GIỎ HÀNG]  │
│                   │ [📞 GỌI NGAY: 1900.xxxx] │
│                   │ [💬 TƯ VẤN QUA ZALO]     │
│                   │ ─────────────────────────│
│                   │ ⏰ Đặt trước 15h - Giao  │
│                   │    trong ngày (nội thành) │
│                   │ 👥 23 người đang xem SP   │
│                   │ 📦 Đã bán 456 sản phẩm   │
├───────────────────┴──────────────────────────┤
│ Tab: Mô tả | Thông số | Đánh giá (125) | FAQ │
├──────────────────────────────────────────────┤
│ Sản phẩm liên quan / Mua kèm giảm giá      │
└──────────────────────────────────────────────┘
```

### 1.2. CTA (Call-to-Action) tối ưu
- **Nút chính:** "THÊM VÀO GIỎ HÀNG" — màu cam (#FF6D00), to, nổi bật
- **Nút phụ 1:** "MUA NGAY" — cho phép checkout 1 bước
- **Nút phụ 2:** "GỌI ĐẶT HÀNG" — hiển thị số hotline
- **Sticky CTA:** Khi scroll xuống, hiển thị thanh CTA cố định ở bottom (mobile)
- **Font size:** ≥16px cho nút CTA, ≥18px trên mobile

### 1.3. Urgency & Scarcity (tạo cảm giác gấp)
- **Countdown timer:** "⏰ Giá ưu đãi còn 2 ngày 15:30:22" (cho sản phẩm sale)
- **Stock counter:** "⚠️ Chỉ còn 5 sản phẩm" (khi tồn kho < 10)
- **Người xem:** "👥 23 người đang xem sản phẩm này"
- **Đơn hàng gần đây:** "Nguyễn V.A vừa mua sản phẩm này 15 phút trước" (popup nhỏ)

> ⚠️ **Lưu ý:** Chỉ hiển thị thông tin **thật**. Fake urgency sẽ phản tác dụng và vi phạm niềm tin.

### 1.4. Social Proof trên trang sản phẩm
- Rating trung bình + số lượng đánh giá ngay dưới tên SP
- 3 review mới nhất hiển thị dạng compact
- Gallery ảnh từ review của khách hàng
- Badge "Sản phẩm bán chạy" cho top sellers
- "X người đã mua trong 7 ngày qua"

---

## 2. Tối Ưu Checkout Flow

### 2.1. Nguyên tắc
- **Càng ít bước càng tốt** — Mục tiêu: 2-3 bước tối đa
- **Không bắt buộc tạo tài khoản** — Cho phép mua hàng không cần đăng ký
- **Hiển thị trust signals** xuyên suốt checkout

### 2.2. Checkout flow đề xuất

```
Bước 1: Thông tin giao hàng
├── Họ tên (bắt buộc)
├── Số điện thoại (bắt buộc)  
├── Tỉnh/Thành phố (dropdown)
├── Quận/Huyện (dropdown, auto-load)
├── Địa chỉ chi tiết
├── Ghi chú đơn hàng (tùy chọn)
└── [TIẾP TỤC]

Bước 2: Thanh toán & Xác nhận
├── Tóm tắt đơn hàng (ảnh + tên + giá)
├── Phí vận chuyển (tự động tính)
├── Mã giảm giá (input)
├── Phương thức thanh toán:
│   ├── COD (mặc định, phổ biến nhất)
│   ├── Chuyển khoản ngân hàng
│   ├── Ví MoMo / VNPay
│   └── Thẻ Visa/Mastercard
├── 🔒 Trust badges: "Thanh toán an toàn" + "Đổi trả 7 ngày"
└── [ĐẶT HÀNG]

Bước 3: Xác nhận thành công
├── Mã đơn hàng
├── Thông tin giao hàng
├── Thời gian giao dự kiến
├── Link tra cứu đơn hàng
└── Gợi ý sản phẩm mua thêm
```

### 2.3. Tối ưu trên mobile
- Input fields đủ lớn (height ≥48px)
- Auto-fill cho SĐT, địa chỉ
- Keyboard phù hợp (number pad cho SĐT)
- Nút "ĐẶT HÀNG" full-width, sticky bottom
- Progress bar hiển thị bước hiện tại

---

## 3. Trust Badges Placement

| Vị trí | Badges | Mục đích |
|---|---|---|
| **Header (sticky)** | Hotline + "Chính hãng 100%" | Tạo trust ngay khi vào site |
| **Product page** (dưới giá) | 5 badges đầy đủ | Giảm lo ngại trước khi add to cart |
| **Cart page** | "Đổi trả 7 ngày" + "Thanh toán an toàn" | Giữ chân khi xem giỏ hàng |
| **Checkout** | SSL + "Bảo mật thông tin" + "Đổi trả" | Tăng trust khi thanh toán |
| **Footer** | Logo thanh toán + Bộ Công Thương | Tạo trust chung cho site |

---

## 4. Live Chat / Zalo OA Setup

### 4.1. Zalo OA (Ưu tiên #1)
- **Tạo Zalo Official Account** cho Xiaomi247
- **Widget chat:** Góc phải dưới, icon Zalo quen thuộc
- **Auto-reply:** Gửi menu options khi khách nhắn tin

**Template auto-reply Zalo OA:**
```
Chào bạn! 👋 Cảm ơn bạn đã liên hệ Xiaomi247.

Vui lòng chọn mục bạn cần hỗ trợ:
1️⃣ Tư vấn sản phẩm
2️⃣ Kiểm tra đơn hàng
3️⃣ Bảo hành / Đổi trả
4️⃣ Khác

Nhân viên sẽ phản hồi trong 5 phút (8h-21h hàng ngày) 😊
```

### 4.2. Tawk.to Live Chat (Miễn phí)
- **Cài đặt:** Thêm script vào footer WordPress
- **Trigger:** Hiển thị sau 30 giây trên trang sản phẩm
- **Proactive message:** "Bạn cần tư vấn về sản phẩm này không?"
- **Offline form:** Thu thập SĐT/email khi ngoài giờ làm việc

### 4.3. Facebook Messenger
- Thêm plugin chat Facebook ở góc trái (Zalo phải, FB trái)
- Chỉ hiển thị nếu khách đã đăng nhập Facebook

---

## 5. Exit-Intent Popup

### 5.1. Thiết kế popup

Khi phát hiện chuột rời khỏi viewport (desktop) hoặc nhấn nút back (mobile):

```
┌─────────────────────────────────────┐
│           ❌ (nút đóng)             │
│                                     │
│   🎁 KHOAN ĐÃ!                     │
│                                     │
│   Nhận ngay mã giảm 100.000đ       │
│   cho đơn hàng đầu tiên!           │
│                                     │
│   ┌─────────────────────────────┐   │
│   │ Nhập số điện thoại / email  │   │
│   └─────────────────────────────┘   │
│   [  NHẬN MÃ GIẢM GIÁ NGAY  ]     │
│                                     │
│   🛡️ Chính hãng | 🔄 Đổi trả 7N   │
│   ⭐ 4.8/5 từ 500+ đánh giá        │
│                                     │
└─────────────────────────────────────┘
```

### 5.2. Quy tắc hiển thị
- Chỉ hiển thị **1 lần/session** (dùng cookie)
- Không hiển thị cho khách quay lại trong 7 ngày
- Không hiển thị trên trang checkout (gây phiền)
- Delay: hiển thị sau khi khách ở trang ≥30 giây
- **Plugin đề xuất:** OptinMonster, ConvertPro, hoặc Elementor Popup

### 5.3. Biến thể popup theo trang

| Trang | Nội dung popup | Mục đích |
|---|---|---|
| Trang sản phẩm | Giảm giá 5-10% cho SP đang xem | Giữ chân mua hàng |
| Trang danh mục | Mã giảm chung 100K | Thu lead |
| Blog | "Đăng ký nhận tin khuyến mãi" | Thu email subscriber |
| Cart (abandon) | "Đơn hàng chưa hoàn tất + free ship" | Recovery |

---

## 6. Cart Abandonment Recovery

### 6.1. Tỷ lệ abandon trung bình
- Desktop: ~70% | Mobile: ~85%
- **Mục tiêu recovery:** 10-15% đơn bị bỏ

### 6.2. Flow recovery tự động

```
Khách bỏ giỏ hàng
  ↓ (30 phút)
Email/Zalo 1: "Bạn quên giỏ hàng rồi!"
  - Hiển thị ảnh sản phẩm trong giỏ
  - Nút "Quay lại giỏ hàng"
  - Trust badges
  ↓ (24 giờ - nếu chưa mua)
Email/Zalo 2: "Sản phẩm sắp hết hàng!"
  - Urgency: "Chỉ còn X sản phẩm"
  - Thêm mã giảm 5% (tùy chọn)
  ↓ (72 giờ - nếu chưa mua)
Email/Zalo 3: "Ưu đãi cuối cùng!"
  - Mã giảm 10% hoặc free ship
  - Có hạn 24 giờ
```

### 6.3. Template tin nhắn recovery

**Email 1 (30 phút):**
```
Subject: Giỏ hàng của bạn đang chờ! 🛒

Chào [TÊN],

Bạn vừa để quên [TÊN SẢN PHẨM] trong giỏ hàng.
Đừng lo, chúng tôi đã giữ lại cho bạn!

[HÌNH SẢN PHẨM]
[TÊN SẢN PHẨM] — [GIÁ]

[QUAY LẠI GIỎ HÀNG]

🛡️ Chính hãng | 🔄 Đổi trả 7 ngày | 🚚 Free ship đơn 500K
```

**Zalo 2 (24 giờ):**
```
Chào [TÊN]! 👋

[TÊN SẢN PHẨM] bạn quan tâm sắp hết hàng rồi ạ!
Hiện chỉ còn [X] sản phẩm.

👉 Hoàn tất đơn hàng: [LINK]

Cần tư vấn thêm? Nhắn em ngay nhé! 😊
```

### 6.4. Plugin & Tools đề xuất

| Tool | Giá | Tính năng |
|---|---|---|
| **CartFlows** (WooCommerce) | Free/Pro $239/yr | Recovery email, custom checkout |
| **Retainful** | Free (300 emails/th) | Abandoned cart emails tự động |
| **WooCommerce Follow-Ups** | $99/yr | Email + SMS follow-up |
| **Zalo ZNS** | Theo gói tin nhắn | Gửi Zalo tự động qua API |

---

## 7. Checklist Triển Khai CRO

### Ưu tiên cao (Tuần 1-2)
- [ ] Thêm trust badges lên trang sản phẩm
- [ ] Thêm sticky CTA trên mobile
- [ ] Bật đánh giá sản phẩm (WooCommerce Reviews)
- [ ] Thêm Zalo chat widget
- [ ] Tối ưu nút "Thêm vào giỏ" (màu, kích thước, vị trí)

### Ưu tiên trung bình (Tuần 3-4)
- [ ] Setup exit-intent popup
- [ ] Cài đặt cart abandonment emails
- [ ] Thêm social proof notifications (recent purchases)
- [ ] Tối ưu checkout flow (bỏ bước không cần thiết)
- [ ] Thêm "Mua ngay" button (skip cart)

### Ưu tiên thấp (Tháng 2-3)
- [ ] A/B test CTA colors & text
- [ ] Thêm product video
- [ ] Triển khai recommended products (AI)
- [ ] Setup SMS recovery (Zalo ZNS)
- [ ] Tối ưu tốc độ tải trang (<3 giây)

