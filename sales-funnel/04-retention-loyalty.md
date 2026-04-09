# CHIẾN LƯỢC GIỮ CHÂN KHÁCH HÀNG & CHƯƠNG TRÌNH LOYALTY — XIAOMI247.COM

> **Ngành:** Phân phối sản phẩm Xiaomi chính hãng & Smart Home
> **Website:** xiaomi247.com
> **Mục tiêu:** Tăng repeat purchase rate lên 35% trong 12 tháng, xây dựng cộng đồng khách hàng trung thành
> **Cập nhật:** Tháng 4/2026

---

## Mục lục

1. [Tại sao Retention quan trọng](#1-tại-sao-retention-quan-trọng)
2. [Customer Lifetime Value (CLV)](#2-customer-lifetime-value-clv)
3. [Customer Segmentation cho Retention](#3-customer-segmentation-cho-retention)
4. [Loyalty Program Design](#4-loyalty-program-design)
5. [Referral Program](#5-referral-program)
6. [Review & UGC Program](#6-review--ugc-program)
7. [Cross-sell & Upsell Playbook](#7-cross-sell--upsell-playbook)
8. [Churn Prediction & Win-back](#8-churn-prediction--win-back)
9. [Zalo OA Retention Workflows](#9-zalo-oa-retention-workflows)
10. [Post-Purchase Experience](#10-post-purchase-experience)
11. [KPIs & Metrics](#11-kpis--metrics)
12. [Checklist triển khai](#12-checklist-triển-khai)

---

## 1. TẠI SAO RETENTION QUAN TRỌNG

### 1.1. Acquisition vs Retention Cost

```
┌──────────────────────────────────────────────────────────────┐
│          CHI PHÍ THU HÚT vs GIỮ CHÂN KHÁCH HÀNG             │
│                                                              │
│  Thu hút khách mới:  ████████████████████████████  500K-1M   │
│  Giữ chân khách cũ:  ████ 70-150K                           │
│                                                              │
│  → Chi phí thu hút = 5-7 lần chi phí giữ chân               │
│  → Tăng retention 5% → Tăng lợi nhuận 25-95%                │
│  → Khách cũ có conversion rate 60-70% (vs 5-20% khách mới)  │
└──────────────────────────────────────────────────────────────┘
```

### 1.2. Tác động của Retention đến lợi nhuận

| Chỉ số | Khách mới | Khách cũ | Chênh lệch |
|--------|-----------|----------|------------|
| **Chi phí tiếp cận** | 500K-1M VNĐ (ads, content, SEO) | 70-150K VNĐ (email, Zalo, push) | **5-7x thấp hơn** |
| **Conversion rate** | 5-20% | 60-70% | **3-14x cao hơn** |
| **AOV (Giá trị đơn)** | 2-2.5M VNĐ | 3-4M VNĐ (mua thêm phụ kiện) | **1.5-2x cao hơn** |
| **Tỷ lệ trả hàng** | 8-10% | 3-5% | **2x thấp hơn** |
| **Referral** | Hiếm khi giới thiệu | 20-30% giới thiệu bạn bè | **Miễn phí acquisition** |

### 1.3. Tầm quan trọng của CLV (Customer Lifetime Value)

Thay vì tối ưu **doanh thu từng đơn hàng**, Xiaomi247 cần tối ưu **giá trị trọn đời khách hàng**:

- **Hệ sinh thái Xiaomi:** 1 khách mua Tivi → tiềm năng mua thêm robot hút bụi, máy lọc KK, camera, loa... trong 3-5 năm
- **Phụ kiện & linh kiện thay thế:** Bộ lọc, chổi, remote → doanh thu định kỳ
- **Giá trị giới thiệu:** 1 khách trung thành giới thiệu 2-3 bạn bè → giảm CAC (Customer Acquisition Cost)

> 📊 **Số liệu mục tiêu:** Retention +5% → Profit +25-95% (Harvard Business Review). Đây là lý do retention phải là ưu tiên hàng đầu song song với acquisition.

---

## 2. CUSTOMER LIFETIME VALUE (CLV)

### 2.1. Công thức tính CLV

```
CLV = AOV × Purchase Frequency × Customer Lifespan × Gross Margin

Trong đó:
- AOV (Average Order Value): Giá trị trung bình mỗi đơn hàng
- Purchase Frequency: Số lần mua trung bình / năm
- Customer Lifespan: Thời gian trung bình khách hàng gắn bó (năm)
- Gross Margin: Biên lợi nhuận gộp (%)
```

### 2.2. Ví dụ tính CLV cho Xiaomi247

**Dữ liệu cơ sở (ước tính):**

| Thông số | Giá trị hiện tại | Mục tiêu sau 12 tháng |
|----------|-----------------|----------------------|
| AOV | 2,500,000 VNĐ | 3,000,000 VNĐ |
| Purchase Frequency | 1.3 lần/năm | 2.0 lần/năm |
| Customer Lifespan | 2 năm | 3 năm |
| Gross Margin | 25-30% | 28-32% |

**Tính CLV hiện tại:**

```
CLV hiện tại = 2,500,000 × 1.3 × 2 × 0.28
            = 1,820,000 VNĐ / khách hàng

CLV mục tiêu = 3,000,000 × 2.0 × 3 × 0.30
             = 5,400,000 VNĐ / khách hàng

→ Tăng CLV 197% = Tăng lợi nhuận đáng kể mà không cần tăng traffic
```

### 2.3. CLV theo Segment

| Segment | AOV | Frequency/năm | Lifespan | Gross Margin | CLV | % Tổng KH |
|---------|-----|--------------|----------|-------------|-----|-----------|
| **New Customer** | 2.0M | 1.0 | 1 năm | 25% | 500K | 45% |
| **Active Customer** | 2.5M | 1.5 | 2 năm | 28% | 2.1M | 25% |
| **At-Risk** | 2.0M | 0.5 | 1 năm | 25% | 250K | 15% |
| **Lapsed** | — | 0 | — | — | 0 | 10% |
| **VIP** | 4.0M | 3.0 | 4 năm | 32% | 15.4M | 5% |

> 💡 **Insight:** VIP chiếm 5% khách hàng nhưng đóng góp ~40% doanh thu. Đầu tư vào retention VIP có ROI cao nhất.

### 2.4. Template theo dõi CLV hàng tháng

| Tháng | Tổng KH | New | Active | At-Risk | Lapsed | VIP | CLV TB | CLV Target |
|-------|---------|-----|--------|---------|--------|-----|--------|-----------|
| T1 | — | — | — | — | — | — | — | 2.0M |
| T3 | — | — | — | — | — | — | — | 2.5M |
| T6 | — | — | — | — | — | — | — | 3.0M |
| T12 | — | — | — | — | — | — | — | 4.0M |

---


## 3. CUSTOMER SEGMENTATION CHO RETENTION

### 3.1. RFM Analysis (Recency, Frequency, Monetary)

RFM là framework phân tích khách hàng dựa trên 3 yếu tố:

| Yếu tố | Mô tả | Cách đo | Ý nghĩa |
|---------|--------|---------|---------|
| **Recency (R)** | Lần mua gần nhất cách đây bao lâu | Ngày từ đơn hàng cuối | R càng gần → khả năng mua lại càng cao |
| **Frequency (F)** | Tần suất mua hàng | Số đơn hàng trong 12 tháng | F càng cao → khách càng trung thành |
| **Monetary (M)** | Tổng chi tiêu | Tổng giá trị đơn hàng (VNĐ) | M càng cao → giá trị khách càng lớn |

**Scoring RFM (thang 1-5):**

| Score | Recency | Frequency | Monetary |
|-------|---------|-----------|----------|
| 5 | < 7 ngày | 5+ đơn | > 15M VNĐ |
| 4 | 8-30 ngày | 3-4 đơn | 10-15M VNĐ |
| 3 | 31-60 ngày | 2 đơn | 5-10M VNĐ |
| 2 | 61-90 ngày | 1 đơn | 2-5M VNĐ |
| 1 | > 90 ngày | 0 đơn (chỉ browse) | < 2M VNĐ |

### 3.2. 5 Customer Segments

#### 🟢 Segment 1: NEW (Khách hàng mới)

| Tiêu chí | Chi tiết |
|----------|---------|
| **Điều kiện** | 1 đơn hàng, mua trong 30 ngày gần nhất |
| **Hành vi** | Tìm hiểu brand, so sánh giá, mua thử lần đầu |
| **% Tổng KH** | ~45% |
| **Rủi ro churn** | Cao (70% không quay lại nếu không nurture) |

| Retention Strategy | Offer | Channel | Timing |
|-------------------|-------|---------|--------|
| Welcome series email/Zalo | Mã giảm 5% đơn tiếp theo (WELCOME5) | Email + Zalo OA | Ngay sau mua |
| Hướng dẫn sử dụng sản phẩm | QR code → video setup | Email + QR trong hộp | 1-3 ngày sau giao |
| Xin review + tặng loyalty points | 50 điểm/review, 100 điểm/review có ảnh | Email + Zalo | 7 ngày sau giao |
| Cross-sell phụ kiện liên quan | Bundle giảm 10% | Email | 14 ngày sau mua |
| Mời tham gia Xiaomi247 Club | Giới thiệu chương trình loyalty | Email + Zalo | 7 ngày sau mua |

#### 🔵 Segment 2: ACTIVE (Khách hàng tích cực)

| Tiêu chí | Chi tiết |
|----------|---------|
| **Điều kiện** | 2+ đơn hàng, mua trong 90 ngày gần nhất |
| **Hành vi** | Quay lại mua, mở email, tương tác Zalo OA |
| **% Tổng KH** | ~25% |
| **Rủi ro churn** | Trung bình |

| Retention Strategy | Offer | Channel | Timing |
|-------------------|-------|---------|--------|
| Exclusive deals (early access) | Flash sale trước 24h | Email VIP + Zalo | Trước mỗi campaign |
| Cross-sell hệ sinh thái Smart Home | Bundle 2 SP giảm 12% | Email + Website | Hàng tháng |
| Loyalty points boost (x1.5 điểm) | Điểm thưởng x1.5 cuối tuần | Zalo push + Website | Weekend |
| Invite viết review chi tiết | 200 điểm cho review video | Email | Sau mỗi đơn hàng |
| Referral program activation | 100K voucher cho mỗi referral | Email + Zalo | Hàng tháng |

#### 🟡 Segment 3: AT-RISK (Có nguy cơ rời bỏ)

| Tiêu chí | Chi tiết |
|----------|---------|
| **Điều kiện** | 1 đơn hàng, 60-90 ngày không mua lại |
| **Hành vi** | Giảm tương tác, không mở email, không visit website |
| **% Tổng KH** | ~15% |
| **Rủi ro churn** | Cao |

| Retention Strategy | Offer | Channel | Timing |
|-------------------|-------|---------|--------|
| "Chúng tôi nhớ bạn" campaign | Mã giảm 10% (COMEBACK10) | Email + Zalo | Ngày 60 |
| Sản phẩm mới phù hợp lịch sử mua | Personalized recommendations | Email | Ngày 65 |
| Flash sale exclusive | Giảm thêm 5% chỉ cho At-Risk | Zalo push | Ngày 75 |
| Survey "Bạn cần gì thêm?" | Nhận 50 điểm loyalty khi trả lời | Email | Ngày 80 |
| Last chance offer | Free shipping + giảm 15% (MISSYOU15) | Email + SMS | Ngày 90 |

#### 🔴 Segment 4: LAPSED (Đã rời bỏ)

| Tiêu chí | Chi tiết |
|----------|---------|
| **Điều kiện** | 0 đơn hàng trong > 90 ngày |
| **Hành vi** | Không tương tác, không mở email, không visit |
| **% Tổng KH** | ~10% |
| **Rủi ro churn** | Rất cao (gần như đã churn) |

| Retention Strategy | Offer | Channel | Timing |
|-------------------|-------|---------|--------|
| Win-back email series (3 email) | Progressive: 5% → 10% → 15% | Email | Ngày 90, 105, 120 |
| Retargeting ads Facebook/Google | Dynamic ads SP đã xem + deal | Facebook + Google | Ngày 90+ |
| Zalo/SMS nhắc nhở | "SP bạn từng quan tâm đang giảm giá" | Zalo + SMS | Ngày 100 |
| Phone call (nếu đơn trước > 5M) | CSKH gọi hỏi thăm, offer VIP | Phone | Ngày 110 |
| Final offer | Free shipping + 20% off + quà tặng | Email + SMS | Ngày 120 |

> ⚠️ Nếu không phản hồi sau 120 ngày → chuyển sang "Dormant", giảm tần suất, xóa khỏi active list sau 180 ngày.

#### ⭐ Segment 5: VIP (Khách hàng VIP)

| Tiêu chí | Chi tiết |
|----------|---------|
| **Điều kiện** | 3+ đơn hàng HOẶC tổng chi tiêu > 10M VNĐ |
| **Hành vi** | Mua thường xuyên, viết review, giới thiệu bạn bè |
| **% Tổng KH** | ~5% |
| **Rủi ro churn** | Thấp (nhưng hậu quả nặng nếu mất) |

| Retention Strategy | Offer | Channel | Timing |
|-------------------|-------|---------|--------|
| VIP-only deals & early access | Giảm 10-15% + early access 48h | Email VIP + Zalo 1-1 | Trước mỗi launch |
| Free shipping mọi đơn | Miễn phí ship không điều kiện | Auto-apply | Luôn luôn |
| Quà sinh nhật đặc biệt | Voucher 200K + quà Xiaomi (tai nghe/pin sạc) | Email + Zalo | Ngày sinh nhật |
| Priority support | CSKH riêng qua Zalo, response < 30 phút | Zalo 1-1 + Phone | Luôn luôn |
| Referral bonus x2 | 200K voucher/referral (thay vì 100K) | Email + Zalo | Hàng tháng |
| Preview sản phẩm mới | Mời test & review SP trước launch | Email + Phone | Trước launch |

> 📊 **Tham chiếu:** [Sales Funnel — Customer Segmentation](01-sales-funnel-strategy.md#12-customer-segmentation) — RFM scoring chi tiết

---

## 4. LOYALTY PROGRAM DESIGN

### 4.1. Tổng quan chương trình

| Thông tin | Chi tiết |
|----------|---------|
| **Tên chương trình** | **Xiaomi247 Club** (phụ đề: "Mua thông minh — Tích điểm lớn") |
| **Mô hình** | Points-based + Tiered membership |
| **Đối tượng** | Tất cả khách hàng đã mua hàng hoặc đăng ký tài khoản |
| **Nền tảng** | WooCommerce + Plugin Points & Rewards |
| **Mục tiêu** | Repeat purchase rate 25-35%, CLV tăng 50% trong 12 tháng |

### 4.2. Points System (Hệ thống tích điểm)

**Quy tắc tích điểm:**

| Hành động | Điểm thưởng | Giới hạn | Ghi chú |
|-----------|------------|----------|---------|
| Mua hàng | 1 VNĐ = 1 điểm | Không giới hạn | Tính trên giá sau giảm, trước shipping |
| Đăng ký tài khoản | 500 điểm | 1 lần | Welcome bonus |
| Viết review sản phẩm | 50 điểm | 1 review/SP | Chỉ tính review đã duyệt |
| Review có ảnh/video | 100 điểm | 1 review/SP | Thay thế 50 điểm review text |
| Sinh nhật | 200 điểm | 1 lần/năm | Auto-add vào ngày sinh nhật |
| Giới thiệu bạn (referral) | 500 điểm | 5 lần/tháng | Khi bạn mới mua đơn đầu tiên |
| Follow Zalo OA | 100 điểm | 1 lần | Xác minh qua Zalo link |
| Hoàn thành profile (địa chỉ, SĐT, ngày sinh) | 200 điểm | 1 lần | Giúp personalization |

**Quy đổi điểm:**

```
10,000 điểm = 10,000 VNĐ voucher (tỷ lệ 1:1)

Ví dụ:
- Mua 1 Robot hút bụi 5,000,000 VNĐ → Nhận 5,000 điểm
- Mua 2 lần tổng 10M → 10,000 điểm = Voucher 10K
- VIP tier (x2 điểm): Mua 5M → 10,000 điểm = Voucher 10K

Điểm hết hạn sau 12 tháng kể từ ngày tích.
Tối thiểu 5,000 điểm mới được quy đổi.
```

> 💰 **Phân tích margin:** Tỷ lệ quy đổi 1:1 = chi phí loyalty ~0.1-0.2% doanh thu (rất hợp lý với gross margin 25-30%). Nếu khách mua 10M VNĐ/năm → chi phí loyalty = 10K VNĐ voucher = 0.1% giá trị đơn. Với VIP (x2): chi phí = 0.2%.

### 4.3. Membership Tiers (Cấp bậc thành viên)

| | 🥉 BRONZE | 🥈 SILVER | 🥇 GOLD/VIP |
|---|-----------|----------|------------|
| **Điều kiện** | 0 - 500K tổng mua | 500K - 3M tổng mua | > 3M tổng mua |
| **Điểm multiplier** | x1 (cơ bản) | x1.5 | x2 |
| **Free shipping** | Đơn > 500K | Đơn > 300K | Mọi đơn hàng |
| **Early access** | Không | Flash sale trước 12h | Flash sale trước 48h + SP mới |
| **Birthday bonus** | 200 điểm | 500 điểm + Voucher 50K | 1,000 điểm + Voucher 200K + Quà |
| **Exclusive deals** | Newsletter deals | Deals riêng hàng tháng | VIP deals + private Zalo group |
| **Support** | Email + Zalo (24h) | Zalo ưu tiên (12h) | Zalo 1-1 + Phone (30 phút) |
| **Đổi trả** | 7 ngày | 14 ngày | 30 ngày |
| **Quà Tết/Lễ** | Không | Thiệp + Voucher 50K | Quà Xiaomi + Voucher 200K |

**Tier maintenance:** Đánh giá lại hàng năm. Nếu không đạt mức chi tiêu → giảm 1 tier (có grace period 30 ngày thông báo).

### 4.4. Rewards Catalog (Danh mục phần thưởng)

| Phần thưởng | Điểm cần | Giá trị thực | Margin cost | Phù hợp tier |
|-------------|---------|-------------|-------------|--------------|
| Voucher giảm 50K | 50,000 điểm | 50K VNĐ | ~15K (30% margin) | Bronze+ |
| Voucher giảm 100K | 100,000 điểm | 100K VNĐ | ~30K | Silver+ |
| Voucher giảm 200K | 200,000 điểm | 200K VNĐ | ~60K | Gold/VIP |
| Free shipping 1 đơn | 20,000 điểm | 30-50K VNĐ | 30-50K | Bronze+ |
| Phụ kiện Xiaomi (dây sạc, ốp) | 30,000 điểm | 50-80K VNĐ | ~20K (giá nhập) | Bronze+ |
| Tai nghe Xiaomi Redmi Buds | 500,000 điểm | 350K VNĐ | ~180K | Silver+ |
| Early access SP mới | 10,000 điểm | Không mất tiền | 0 VNĐ | Silver+ |
| Exclusive product (limited) | 1,000,000 điểm | 800K-1.5M VNĐ | ~400-750K | Gold/VIP |

> 💡 **Chi phí loyalty ước tính:** Với redemption rate ~30% và AOV 2.5M, chi phí trung bình = 0.3-0.5% doanh thu. ROI dương khi retention rate tăng ≥ 5%.

### 4.5. Gamification Elements

| Yếu tố | Mô tả | Điểm thưởng |
|---------|--------|-------------|
| **Badges** | Huy hiệu thành tích hiển thị trên profile | — |
| 🛒 "Người mua sắm đầu tiên" | Hoàn thành đơn hàng đầu tiên | 100 điểm |
| ⭐ "Reviewer chuyên nghiệp" | Viết 5+ reviews có ảnh | 300 điểm |
| 🏠 "Smart Home Master" | Mua từ 3 danh mục SP khác nhau | 500 điểm |
| 👥 "Đại sứ thương hiệu" | Giới thiệu 5+ bạn mua hàng | 1,000 điểm |
| 🔥 "Streak Rewards" | Mua hàng 3 tháng liên tiếp | 500 điểm/streak |
| 📸 "Influencer" | Review video được 10+ helpful votes | 500 điểm |
| **Milestones** | Mốc chi tiêu tích lũy | — |
| Mua đủ 2M VNĐ | → Tự động nâng Silver | Welcome Silver gift |
| Mua đủ 5M VNĐ | → Bonus 2,000 điểm | — |
| Mua đủ 10M VNĐ | → Tự động nâng Gold | Welcome Gold gift + CSKH riêng |

### 4.6. Implementation trên WooCommerce

| Plugin | Tính năng | Giá | Đề xuất |
|--------|----------|-----|---------|
| **WooCommerce Points & Rewards** | Tích điểm, quy đổi, tùy chỉnh tỷ lệ | $129/năm | ⭐ Đề xuất chính |
| **YITH WooCommerce Points & Rewards** | Points, tiers, badges, gamification | $149/năm | Alternative (nhiều tính năng hơn) |
| **Sumo Reward Points** | Points, referral, gamification | Free-$49/tháng | Nếu cần SaaS |

**Setup checklist:**
- [ ] Cài đặt plugin Points & Rewards
- [ ] Cấu hình tỷ lệ tích điểm (1 VNĐ = 1 điểm)
- [ ] Cấu hình tỷ lệ quy đổi (10,000 điểm = 10K voucher)
- [ ] Tạo 3 membership tiers (Bronze/Silver/Gold)
- [ ] Tạo rewards catalog
- [ ] Thiết kế "My Rewards" page cho customer dashboard
- [ ] Test flow: mua → tích điểm → quy đổi → dùng voucher
- [ ] Email notification khi đạt tier mới / điểm sắp hết hạn

---

## 5. REFERRAL PROGRAM

### 5.1. Tổng quan: "Giới thiệu bạn — Cả 2 cùng vui"

```
┌──────────────────────────────────────────────────────────────┐
│             XIAOMI247 REFERRAL PROGRAM                       │
│                                                              │
│   👤 Người giới thiệu ──────► 👥 Bạn mới                    │
│   Nhận: Voucher 100K          Nhận: Voucher 50K              │
│   (khi bạn mới mua đơn       (cho đơn hàng đầu tiên         │
│    đầu tiên ≥ 500K)           ≥ 500K)                        │
│                                                              │
│   💰 Win-Win: Cả 2 đều có lợi                               │
└──────────────────────────────────────────────────────────────┘
```

### 5.2. Referral Flow chi tiết

```
Bước 1: Khách hàng → Vào trang "Giới thiệu bạn" trên My Account
        │
        ▼
Bước 2: Nhận referral link cá nhân (unique URL + mã giới thiệu)
        Ví dụ: xiaomi247.com/ref/ABC123
        │
        ▼
Bước 3: Share link qua Zalo / Messenger / Copy link
        │
        ▼
Bước 4: Bạn mới click link → Landing page giới thiệu
        "Bạn được [Tên] giới thiệu! Nhận ngay Voucher 50K"
        │
        ▼
Bước 5: Bạn mới đăng ký tài khoản (tự động gán referral code)
        │
        ▼
Bước 6: Bạn mới mua hàng đầu tiên (≥ 500K VNĐ)
        Voucher 50K tự động áp dụng
        │
        ▼
Bước 7: Hệ thống confirm → Gửi Voucher 100K cho người giới thiệu
        + 500 loyalty points
        │
        ▼
Bước 8: Email/Zalo thông báo cho cả 2 bên
```

### 5.3. Kênh share referral

| Kênh | Cách share | Ưu tiên |
|------|-----------|---------|
| **Zalo** | Nút "Chia sẻ qua Zalo" → tạo tin nhắn template sẵn | ⭐⭐⭐ (phổ biến nhất VN) |
| **Messenger** | Nút "Chia sẻ qua Messenger" → link + message | ⭐⭐⭐ |
| **Copy link** | Nút "Sao chép link" → paste bất kỳ đâu | ⭐⭐ |
| **QR Code** | Hiển thị QR code cá nhân → scan trực tiếp | ⭐ (offline) |

### 5.4. Anti-fraud Rules (Chống gian lận)

| Quy tắc | Chi tiết | Lý do |
|---------|---------|-------|
| Giới hạn referral | Tối đa 5 referral thành công/người/tháng | Tránh abuse |
| Đơn tối thiểu | Bạn mới phải mua đơn ≥ 500K VNĐ | Đảm bảo đơn thật |
| Không tự giới thiệu | Email/SĐT không trùng với người giới thiệu | Chống tự tạo |
| Xác minh | Đơn hàng phải hoàn tất (giao thành công, không trả) | Chống fraud |
| Thời hạn link | Referral link valid 30 ngày kể từ lúc tạo | Quản lý campaign |
| 1 referral/người | Mỗi khách mới chỉ dùng 1 referral code | Tránh stack |

### 5.5. KPIs Referral Program

| KPI | Target | Cách đo |
|-----|--------|---------|
| **Referral rate** | 5-10% khách hàng share link | Referrers / Total Customers |
| **Referral conversion** | 15-25% click → mua | Purchases from referral / Referral clicks |
| **Viral coefficient** | ≥ 0.3 | (Referrals × Conv. Rate) / Total Customers |
| **CAC từ referral** | ≤ 150K VNĐ | (Voucher người GT + Voucher bạn mới) / New Customer |
| **Revenue từ referral** | 5-10% tổng revenue sau 6 tháng | Referral revenue / Total revenue |

**Plugin đề xuất:** AutomateWoo Refer A Friend ($79/năm) hoặc WooCommerce Referral Plugin.

---

## 6. REVIEW & UGC PROGRAM

### 6.1. Incentivize Reviews (Khuyến khích đánh giá)

| Loại Review | Incentive | Điều kiện | Mục tiêu |
|-------------|----------|----------|---------|
| **Review text** (≥ 50 từ) | 50 loyalty points | Mua hàng + xác minh | 10% đơn hàng có review |
| **Review có ảnh** (≥ 1 ảnh) | 100 loyalty points | Ảnh sản phẩm thật | 5% đơn hàng |
| **Review video** (unboxing/sử dụng) | Voucher giảm 10% đơn tiếp | Video ≥ 30s, chất lượng tốt | 1% đơn hàng |
| **Review chi tiết** (≥ 200 từ + ảnh) | 200 loyalty points | Đánh giá chuyên sâu | 2% đơn hàng |

### 6.2. Photo Contest hàng tháng

| Thông tin | Chi tiết |
|----------|---------|
| **Tên** | #Xiaomi247Review — Cuộc thi ảnh hàng tháng |
| **Cách tham gia** | Upload ảnh SP Xiaomi đang dùng + caption + hashtag #Xiaomi247Review |
| **Nền tảng** | Facebook + Instagram + Zalo OA |
| **Giải thưởng** | Best photo: Voucher 500K + Feature trên website & social |
| **Runner-up** | 2 giải: Voucher 200K mỗi giải |
| **Tiêu chí chấm** | Chất lượng ảnh 40%, sáng tạo 30%, engagement (likes) 30% |
| **Timeline** | Ngày 1-25: nhận bài → Ngày 26-28: chấm → Ngày 30: công bố |

### 6.3. Video Testimonial Program

- **Đối tượng:** Khách hàng đã mua ≥ 2 đơn hoặc SP giá trị ≥ 3M
- **Incentive:** Voucher giảm 10% cho đơn tiếp theo (không giới hạn giá trị)
- **Yêu cầu video:** Unboxing hoặc review sử dụng, ≥ 60s, chất lượng HD
- **Sử dụng:** Product page, homepage slider, Facebook/TikTok ads (có sự đồng ý)
- **Template gợi ý:** Gửi email hướng dẫn quay video + câu hỏi gợi ý (sản phẩm là gì, dùng thế nào, ưu điểm nổi bật)

### 6.4. Display UGC (Hiển thị nội dung người dùng)

| Vị trí | Loại UGC | Cách hiển thị |
|--------|---------|--------------|
| **Product page** | Reviews + photos | Tab reviews bên dưới mô tả SP |
| **Homepage** | Top reviews + video | Section "Khách hàng nói gì?" carousel |
| **Social media** | Ảnh/video khách hàng | Re-share trên FB/IG/TikTok với credit |
| **Email** | Best reviews | Trong welcome series & promotional email |
| **Ads** | Video testimonial | Facebook/TikTok ads (Spark Ads) |

### 6.5. WooCommerce Review Management

| Công việc | Công cụ/Plugin | Chi phí |
|----------|---------------|---------|
| Thu thập review | **YITH Advanced Reviews** hoặc WooCommerce mặc định | Free-$99/năm |
| Email xin review tự động | Mailchimp / AutomateWoo | Đã có |
| Hiển thị ảnh trong review | YITH hoặc custom CSS | — |
| Moderation (duyệt review) | WooCommerce Admin → Comments | Free |
| Báo cáo review metrics | Metorik hoặc manual | $50/tháng hoặc Free |

> 📊 **Tham chiếu:** [Trust Strategy — Social Proof & Review Collection](../marketing/04-trust-building/trust-strategy.md#2-trust-signals-cần-thiết) — Quy trình thu thập review chi tiết

---

## 7. CROSS-SELL & UPSELL PLAYBOOK

### 7.1. Bảng mapping Cross-sell chi tiết

| Sản phẩm chính | Cross-sell 1 | Cross-sell 2 | Cross-sell 3 | Bundle giảm |
|----------------|-------------|-------------|-------------|------------|
| **Tivi Xiaomi** | Soundbar Xiaomi (2-4M) | Loa Bluetooth Xiaomi (500K-1.5M) | Kệ TV / Giá treo (300K-800K) | Combo Tivi + Soundbar: **giảm 12%** |
| **Robot hút bụi** | Bộ lọc thay thế (200-400K) | Chổi/brush thay thế (150-300K) | Dock giặt tự động (3-5M) | Combo Robot + 3 bộ lọc: **giảm 15%** |
| **Tủ lạnh Xiaomi** | Máy lọc nước Xiaomi (3-6M) | Hộp bảo quản thực phẩm (100-300K) | Nhiệt kế tủ lạnh smart (200K) | Combo Tủ lạnh + Lọc nước: **giảm 10%** |
| **Máy lọc không khí** | Bộ lọc thay thế (300-600K) | Máy tạo ẩm Xiaomi (1-2M) | Cảm biến chất lượng KK (500K) | Combo Lọc KK + 2 bộ lọc: **giảm 15%** |
| **Máy hút ẩm** | Máy lọc không khí (3-5M) | Quạt Xiaomi (1-2M) | Nhiệt ẩm kế smart (200K) | Combo Hút ẩm + Lọc KK: **giảm 10%** |
| **Camera an ninh** | Hub Xiaomi Gateway (800K-1.2M) | Cảm biến cửa/chuyển động (200-400K) | Thẻ nhớ MicroSD (150-300K) | Combo Camera + Hub + Sensor: **giảm 12%** |
| **Máy giặt Xiaomi** | Nước giặt/xả (100-200K) | Giá phơi thông minh (500K-1M) | Bàn ủi hơi nước (1-2M) | — |
| **Nồi cơm điện** | Bộ nồi Xiaomi (500K-1M) | Máy xay sinh tố (800K-1.5M) | Bình đun siêu tốc (500-800K) | Combo Bếp Xiaomi 3 SP: **giảm 10%** |

### 7.2. Timing Cross-sell & Upsell

| Thời điểm | Loại | Vị trí / Kênh | Offer | Conversion Rate kỳ vọng |
|-----------|------|--------------|-------|------------------------|
| **Product page** | Cross-sell | Section "Sản phẩm thường mua cùng" | Hiển thị giá bundle | 3-5% |
| **Cart page** | Upsell + Cross-sell | "Thêm sản phẩm này để được giảm thêm" | Bundle discount | 5-8% |
| **Checkout** | Cross-sell nhỏ | "Bạn có muốn thêm bộ lọc thay thế?" | Add 1-click | 2-3% |
| **Thank you page** | Cross-sell | "Khách mua [SP] cũng mua..." | Voucher 5% đơn tiếp | 1-2% |
| **Email post-purchase** | Cross-sell | Email ngày 14 sau mua | Bundle giảm 10-15% | 2-4% |
| **Zalo push** | Flash deal | Tin nhắn cá nhân hóa | Deal 24h | 3-5% |

### 7.3. "Frequently Bought Together" Section

**Vị trí:** Bên dưới nút "Thêm vào giỏ" trên product page

```
┌─────────────────────────────────────────────────────────┐
│  🔗 THƯỜNG ĐƯỢC MUA CÙNG                               │
│                                                         │
│  [Ảnh SP chính]  +  [Ảnh SP 2]  +  [Ảnh SP 3]         │
│  Robot hút bụi      Bộ lọc x3      Chổi thay thế      │
│  5,990,000 ₫        890,000 ₫      450,000 ₫           │
│                                                         │
│  Mua combo 3 sản phẩm: 6,230,000 ₫ (GIẢM 1,100,000₫) │
│                                                         │
│  [  THÊM CẢ 3 VÀO GIỎ HÀNG  ]  ← CTA nổi bật        │
└─────────────────────────────────────────────────────────┘
```

**Plugin:** WooCommerce Frequently Bought Together (Free) hoặc YITH Frequently Bought Together ($79/năm).

### 7.4. Bundle Deals Strategy

| Loại Bundle | Giảm giá | Điều kiện | Ví dụ |
|------------|---------|----------|-------|
| **2-product bundle** | 10% | 2 SP cùng danh mục liên quan | Tivi + Soundbar |
| **3-product bundle** | 15% | 3 SP hệ sinh thái Smart Home | Camera + Hub + Sensor |
| **Accessories bundle** | 15-20% | SP chính + 2-3 phụ kiện thay thế | Robot + 3 bộ lọc + 2 chổi |
| **Starter kit** | 12% | Combo cho người mới bắt đầu Smart Home | Hub + Camera + Sensor + Đèn |

> ⚠️ **Margin check:** Bundle giảm 10-15% trên gross margin 25-30% → Net margin ~10-20%. Đảm bảo không bán lỗ. Phụ kiện có margin cao hơn (40-50%) nên có thể giảm mạnh hơn.

---

## 8. CHURN PREDICTION & WIN-BACK

### 8.1. Churn Signals (Dấu hiệu khách sắp rời bỏ)

| Signal | Mức độ nghiêm trọng | Hành động |
|--------|---------------------|----------|
| Không mở email 30 ngày | 🟡 Warning | Đổi subject line, gửi lại lúc khác |
| Không mở email 60 ngày | 🟠 Serious | Trigger win-back flow |
| Không visit website 60 ngày | 🟠 Serious | Retargeting ads + Zalo push |
| Không visit website 90 ngày | 🔴 Critical | Escalation đa kênh |
| Hủy đơn hàng | 🟡 Warning | Follow-up CSKH hỏi lý do |
| Hủy 2+ đơn | 🔴 Critical | CSKH gọi điện, offer đặc biệt |
| Unsubscribe email | 🟠 Serious | Chuyển sang Zalo/SMS channel |
| Unfollow Zalo OA | 🟠 Serious | Retarget qua Facebook/Google |
| Review tiêu cực (1-2 sao) | 🔴 Critical | CSKH liên hệ ngay, resolve issue |

### 8.2. Automated Win-back Triggers

```
WIN-BACK ESCALATION FLOW:

Ngày 30 (Warning):
│  → Email: "Sản phẩm mới tại Xiaomi247" (soft reminder)
│  → Không offer discount
│
▼
Ngày 45 (nếu không phản hồi):
│  → Email: "Chúng tôi nhớ bạn!" + Mã giảm 5% (COMEBACK5)
│  → Zalo push: Tin nhắn cá nhân hóa
│
▼
Ngày 60 (nếu vẫn không phản hồi):
│  → Email: "Ưu đãi đặc biệt cho bạn" + Mã giảm 10% (COMEBACK10)
│  → Zalo: Tin nhắn với SP phù hợp lịch sử mua
│  → Facebook/Google retargeting ads: Dynamic product ads
│
▼
Ngày 75 (nếu vẫn không phản hồi):
│  → SMS: "Xiaomi247 giảm 15% cho bạn! Dùng mã MISSYOU15"
│  → Email: "Lần cuối — Ưu đãi 15% sắp hết hạn"
│
▼
Ngày 90 (cho VIP/High-value customers):
│  → Phone call từ CSKH: Hỏi thăm + offer đặc biệt
│  → Voucher 200K không điều kiện
│
▼
Ngày 120 (Final):
│  → Tag "Dormant" → giảm tần suất liên lạc
│  → 1 email cuối "Bạn còn muốn nhận thông tin?"
│  → Nếu không phản hồi → xóa khỏi active list sau 180 ngày
```

### 8.3. Win-back Offers (Progressive Discount)

| Giai đoạn | Discount | Mã code | Điều kiện | Valid |
|----------|---------|---------|----------|-------|
| Nhẹ (30-45 ngày) | 5% | COMEBACK5 | Đơn ≥ 500K | 14 ngày |
| Vừa (45-60 ngày) | 10% | COMEBACK10 | Đơn ≥ 300K | 14 ngày |
| Mạnh (60-90 ngày) | 15% | MISSYOU15 | Không điều kiện | 7 ngày |
| VIP rescue (90+ ngày) | 20% hoặc Voucher 200K | VIPRESCUE | VIP segment only | 7 ngày |

### 8.4. Re-engagement Ads

| Kênh | Audience | Ad Type | Budget/tháng |
|------|---------|---------|-------------|
| **Facebook** | Website visitors 60-90d, chưa mua lại | Dynamic Product Ads + offer | 3-5M VNĐ |
| **Google** | RLSA — past customers searching competitors | Search Ads + higher bid | 2-3M VNĐ |
| **Google Display** | Past customers, display remarketing | Banner với deal | 1-2M VNĐ |
| **TikTok** | Custom audience — past customers | Video review + offer | 1-2M VNĐ |

> 📊 **Tham chiếu:** [Email Marketing — Win-back Flow](02-email-marketing.md#7-flow-4-win-back) — Email win-back template chi tiết | [Ads Optimization — Remarketing](../ads-social/04-ads-optimization.md#8-remarketing-optimization) — Retargeting strategy

---

## 9. ZALO OA RETENTION WORKFLOWS

### 9.1. Push Notification Schedule

| Ngày | Nội dung | Loại | Mục tiêu |
|------|---------|------|---------|
| **Thứ 2** | Flash sale đầu tuần (1 SP featured) | Promotional | Traffic + Sales |
| **Thứ 4** | Tips sử dụng / Mẹo hay Smart Home | Educational | Engagement |
| **Thứ 6** | Deal cuối tuần / New arrival | Promotional | Sales |
| **Tùy chọn** | Breaking news (SP mới, event đặc biệt) | News | Awareness |

> ⚠️ **Tần suất:** 2-3 tin/tuần. Không gửi quá 4 tin/tuần để tránh unfollow. Giữ tỷ lệ content: 40% educational + 40% promotional + 20% news.

### 9.2. Content Types cho Zalo OA

| Loại content | Mô tả | Ví dụ | Tần suất |
|-------------|--------|-------|----------|
| **Flash Sale** | Deal giới hạn thời gian 24-48h | "⚡ Robot hút bụi Dreame giảm 30% — Chỉ hôm nay!" | 1-2/tuần |
| **New Product** | Thông báo sản phẩm mới | "🆕 Tivi Xiaomi A Pro 55 inch — Đặt trước giảm 500K" | 1-2/tháng |
| **Tips & Tricks** | Hướng dẫn sử dụng SP | "💡 5 mẹo để robot hút bụi hoạt động hiệu quả hơn" | 1/tuần |
| **Exclusive for followers** | Ưu đãi chỉ cho Zalo followers | "🎁 Mã ZALOVIP giảm 8% — Chỉ cho bạn!" | 1-2/tháng |
| **Loyalty update** | Cập nhật điểm, tier | "🏆 Chúc mừng! Bạn đã lên hạng Silver!" | Khi có thay đổi |
| **Survey** | Khảo sát ý kiến | "Bạn muốn Xiaomi247 bán thêm SP gì?" | 1/tháng |

### 9.3. Personalized Messages theo Purchase History

| Trigger | Message | Timing |
|---------|---------|--------|
| Mua Tivi | "📺 Bạn đã setup Tivi rồi chưa? Xem hướng dẫn kết nối WiFi + Soundbar" | 3 ngày sau giao |
| Mua Robot hút bụi | "🤖 Tip: Nên thay bộ lọc mỗi 3-6 tháng. Mua bộ lọc thay thế giảm 15%!" | 90 ngày sau mua |
| Mua 1 SP Smart Home | "🏠 Bạn đã bắt đầu Smart Home! Xem combo tiết kiệm để mở rộng hệ sinh thái" | 14 ngày sau mua |
| Birthday | "🎂 Sinh nhật vui vẻ! Nhận voucher 50-200K tại Xiaomi247" | Ngày sinh nhật |
| Loyalty tier change | "⭐ Chúc mừng bạn lên tier [Gold]! Xem quyền lợi mới" | Khi đạt tier |

### 9.4. Zalo Mini App (Kế hoạch tương lai)

| Tính năng | Mô tả | Ưu tiên |
|----------|--------|---------|
| **Check điểm loyalty** | Xem số điểm hiện tại, lịch sử tích/dùng | ⭐⭐⭐ |
| **Redeem rewards** | Đổi điểm lấy voucher/phần thưởng | ⭐⭐⭐ |
| **Track đơn hàng** | Theo dõi trạng thái giao hàng | ⭐⭐⭐ |
| **Referral** | Tạo & share referral link | ⭐⭐ |
| **Flash deals** | Xem deal exclusive cho Zalo followers | ⭐⭐ |
| **Lịch sử mua** | Xem đơn hàng cũ, đặt lại phụ kiện | ⭐ |

> 📊 **Tham chiếu:** [Digital Marketing — Zalo OA](../marketing/05-digital-marketing/digital-marketing-strategy.md#1-channel-mix) — Vai trò Zalo OA trong channel mix

---

## 10. POST-PURCHASE EXPERIENCE

### 10.1. Unboxing Experience

| Yếu tố | Chi tiết | Chi phí ước tính |
|---------|---------|-----------------|
| **Đóng gói đẹp** | Hộp carton in logo Xiaomi247, giấy lót, bubble wrap | 5-10K/đơn |
| **Thank you card** | Thiệp cảm ơn in đẹp, có mã QR review + mã giảm giá 5% | 1-2K/tấm |
| **QR code → Review** | In trên card: scan → trang review SP + nhận 50 loyalty points | 0 (in chung) |
| **QR code → Warranty** | Scan → đăng ký bảo hành online + nhận email xác nhận | 0 (in chung) |
| **Sticker Xiaomi247** | Sticker logo nhỏ, dễ thương → brand recall | 500đ/sticker |
| **Gói quà tặng (đơn > 5M)** | Túi vải Xiaomi247 hoặc ốp lưng Xiaomi | 20-50K/đơn |

**Tổng chi phí unboxing:** 7-15K/đơn (đơn thường) → ~0.3-0.6% AOV. ROI dương qua repeat purchase.

### 10.2. Setup Guide (Hướng dẫn cài đặt)

| Sản phẩm | Hình thức hướng dẫn | Kênh |
|----------|-------------------|------|
| Tivi Xiaomi | Video 3-5 phút: kết nối WiFi, cài app, setup | QR trên hộp → YouTube |
| Robot hút bụi | Video: kết nối app Xiaomi Home, setup lịch hút | QR → YouTube + blog |
| Camera an ninh | Video: lắp đặt, kết nối WiFi, setup app | QR → YouTube |
| Máy lọc KK | Video: lắp bộ lọc, kết nối app, đặt vị trí tối ưu | QR → YouTube |
| Smart Home Hub | Video: kết nối thiết bị, tạo automation | QR → YouTube + blog chi tiết |

### 10.3. Follow-up Timeline

```
POST-PURCHASE FOLLOW-UP:

Ngày 0:  Đơn hàng xác nhận → Email/Zalo: "Cảm ơn! Đơn hàng đang được chuẩn bị"
         │
Ngày 1-2: Giao hàng → Email/Zalo: "Đơn hàng đã giao. Tracking: [link]"
         │
Ngày 3:  Email: Hướng dẫn setup + QR video + "Cần hỗ trợ gì không?"
         │
Ngày 7:  Zalo: "Dùng sản phẩm thế nào rồi? 😊 Có cần hỗ trợ gì không?"
         │
Ngày 14: Email: Cross-sell phụ kiện + bundle deal
         │
Ngày 21: Email/Zalo: "Viết review nhận 50-100 loyalty points!"
         │
Ngày 30: Email: Sản phẩm liên quan + loyalty program update
         │
Ngày 60: Check: Nếu không tương tác → trigger At-Risk flow
```

### 10.4. Warranty Activation (Đăng ký bảo hành)

- **Quy trình:** QR code trên hộp → Trang đăng ký bảo hành → Nhập mã đơn + SĐT → Xác nhận email
- **Incentive đăng ký:** Tặng thêm 200 loyalty points khi đăng ký bảo hành online
- **Nhắc nhở:** Email/Zalo sau 3 ngày: "Đừng quên đăng ký bảo hành để được hỗ trợ tốt nhất!"
- **Data thu thập:** SĐT, email, sản phẩm, ngày mua → dùng cho personalization & cross-sell

### 10.5. Support Channels

| Kênh | Thời gian hỗ trợ | Response time | Phù hợp cho |
|------|-----------------|--------------|-------------|
| **Zalo OA Chat** | 8:00 - 22:00 hàng ngày | < 30 phút (< 10 phút VIP) | Hỏi SP, tracking, warranty |
| **Hotline** | 8:00 - 21:00 T2-T7 | Ngay lập tức | Khiếu nại, VIP support |
| **Email** | 24/7 (trả lời giờ HC) | < 24 giờ | Warranty claim, chi tiết |
| **Facebook Messenger** | 8:00 - 22:00 | < 1 giờ | Hỏi nhanh, casual |
| **Live Chat Website** | 8:00 - 22:00 | < 5 phút | Hỗ trợ mua hàng real-time |

---

## 11. KPIs & METRICS

### 11.1. Retention KPIs tổng quan

| KPI | Target T3 | Target T6 | Target T12 | Cách đo |
|-----|-----------|-----------|-----------|---------|
| **Repeat Purchase Rate** | 15% | 25% | 35% | Customers mua ≥ 2 lần / Total customers |
| **CLV trung bình** | 2.0M | 2.5M | 4.0M | AOV × Frequency × Lifespan × Margin |
| **NPS (Net Promoter Score)** | ≥ 30 | ≥ 40 | ≥ 50 | Survey: "Bạn giới thiệu Xiaomi247 ?" (0-10) |
| **Referral Rate** | 3% | 5% | 10% | Referrers / Total Customers |
| **Review Rate** | 5% | 10% | 15% | Reviews / Total Orders |
| **Loyalty Enrollment** | 15% | 30% | 50% | Loyalty members / Total Customers |
| **Churn Rate** | < 50% | < 40% | < 30% | Customers không mua lại trong 12 tháng |
| **Email Retention Open Rate** | ≥ 30% | ≥ 35% | ≥ 40% | Opens / Sent (post-purchase emails) |
| **Zalo OA Followers** | 1,000 | 3,000 | 8,000 | Zalo OA Admin |
| **Cross-sell Revenue %** | 5% | 10% | 15% | Revenue từ cross-sell / Total Revenue |

### 11.2. KPI theo Segment

| Segment | KPI chính | Target T3 | Target T12 |
|---------|----------|-----------|-----------|
| **New** | 2nd purchase rate | 15% | 30% |
| **Active** | Purchase frequency | 1.5/năm | 2.5/năm |
| **At-Risk** | Recovery rate | 10% | 20% |
| **Lapsed** | Win-back rate | 5% | 10% |
| **VIP** | Retention rate | 80% | 90% |

### 11.3. Bảng Tracking Monthly

| Metric | T1 | T2 | T3 | T4 | T5 | T6 | T7 | T8 | T9 | T10 | T11 | T12 | Status |
|--------|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Total Customers | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| New Customers | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| Repeat Customers | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| Repeat Rate (%) | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| CLV trung bình | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| Loyalty Members | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| Points Issued | — | — | — | — | — | — | — | — | — | — | — | — | — |
| Points Redeemed | — | — | — | — | — | — | — | — | — | — | — | — | — |
| Referrals | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| Reviews Collected | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| NPS Score | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| Churn Rate | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| Cross-sell Revenue | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |
| Zalo OA Followers | — | — | — | — | — | — | — | — | — | — | — | — | 🟢/🟡/🔴 |

### 11.4. Retention Revenue Impact (Ước tính)

```
Giả sử: 100 khách hàng/tháng, AOV = 2.5M

KHÔNG CÓ RETENTION:
  Revenue = 100 × 2.5M = 250M/tháng
  Repeat rate: 5% → 5 khách quay lại → +12.5M
  Tổng: 262.5M/tháng

CÓ RETENTION PROGRAM (sau 6 tháng):
  Revenue = 100 × 2.5M = 250M/tháng
  Repeat rate: 25% → 25 khách quay lại → +62.5M
  Cross-sell upsell: +15% AOV → +9.4M
  Referral: 5% → 5 khách mới miễn phí → +12.5M
  Tổng: 334.4M/tháng → TĂNG 27.4% so với không có retention

Chi phí retention: ~5-8M/tháng (loyalty + email + Zalo + unboxing)
ROI retention: (71.9M extra revenue × 28% margin) / 8M cost = 2.5x
```

---

## 12. CHECKLIST TRIỂN KHAI

### Phase 1: Nền tảng (Tuần 1-2)

- [ ] Cài đặt WooCommerce Points & Rewards plugin
- [ ] Cấu hình points system (1 VNĐ = 1 điểm, 10K điểm = 10K voucher)
- [ ] Tạo 3 membership tiers (Bronze/Silver/Gold)
- [ ] Thiết kế trang "Xiaomi247 Club" (landing page giới thiệu chương trình)
- [ ] Thiết kế "My Rewards" dashboard trong customer account
- [ ] Setup email notifications cho loyalty (welcome, tier up, points expiry)
- [ ] Tạo thank you card + QR code cho đóng gói
- [ ] Setup Zalo OA content calendar

### Phase 2: Review & Referral (Tuần 3-4)

- [ ] Cài đặt YITH Advanced Reviews plugin
- [ ] Cấu hình review incentive (50-100 points/review)
- [ ] Setup email automation xin review (ngày 7 sau giao)
- [ ] Cài đặt Referral plugin (AutomateWoo Refer A Friend)
- [ ] Tạo referral landing page
- [ ] Cấu hình anti-fraud rules
- [ ] Test referral flow end-to-end
- [ ] Tạo share templates cho Zalo/Messenger

### Phase 3: Cross-sell & Post-purchase (Tuần 5-6)

- [ ] Cài đặt Frequently Bought Together plugin
- [ ] Cấu hình cross-sell mapping (tivi → soundbar, robot → bộ lọc...)
- [ ] Tạo bundle deals (10-15% discount combos)
- [ ] Setup post-purchase email flow (tham chiếu 02-email-marketing.md)
- [ ] Tạo setup guide videos cho top 5 sản phẩm
- [ ] Setup warranty activation page
- [ ] In ấn thank you cards + QR codes

### Phase 4: Win-back & Optimization (Tuần 7-8)

- [ ] Setup churn detection triggers (email không mở 60d, không visit 90d)
- [ ] Tạo win-back email series (3 emails progressive discount)
- [ ] Setup retargeting ads cho lapsed customers
- [ ] Cấu hình Zalo OA push notification schedule
- [ ] Tạo personalized Zalo messages theo purchase history
- [ ] Launch photo contest #Xiaomi247Review
- [ ] Setup KPI tracking dashboard

### Phase 5: Review & Scale (Tháng 3+)

- [ ] Đánh giá KPIs tháng 1-2
- [ ] Tối ưu points/rewards dựa trên redemption data
- [ ] A/B test referral incentive (100K vs 150K)
- [ ] Mở rộng bundle deals dựa trên cross-sell data
- [ ] Đánh giá chuyển đổi sang YITH Points & Rewards (nếu cần tính năng nâng cao)
- [ ] Lên kế hoạch Zalo Mini App (nếu followers > 5,000)
- [ ] Tối ưu win-back flow dựa trên churn data
- [ ] Review ngân sách loyalty vs ROI

---

## 📊 TỔNG KẾT

### Chi phí Retention Program ước tính

| Hạng mục | Chi phí/tháng | Ghi chú |
|----------|-------------|---------|
| Loyalty plugin (WooCommerce) | ~250K (chia 12 tháng) | $129/năm |
| Review plugin (YITH) | ~200K (chia 12 tháng) | $99/năm |
| Referral plugin | ~150K (chia 12 tháng) | $79/năm |
| Cross-sell plugin | ~150K (chia 12 tháng) | $79/năm |
| Loyalty rewards (redemption) | 1-3M | ~0.3-0.5% doanh thu |
| Referral vouchers | 1-2M | 100K/referral × 10-20 referrals |
| Review incentive (points cost) | 500K-1M | Points value |
| Photo contest prizes | 900K | 500K + 200K × 2 |
| Unboxing materials | 500K-1M | 7-15K/đơn × 50-100 đơn |
| Setup guide videos | 1-2M (T1), 500K sau đó | Thuê quay hoặc tự làm |
| **TỔNG** | **5-10M VNĐ/tháng** | |

### ROI dự kiến

```
CHI PHÍ: 5-10M VNĐ/tháng
REVENUE BỔ SUNG (sau 6 tháng):
- Repeat purchases: +60M/tháng (25% repeat × 100 KH × 2.5M AOV)
- Cross-sell: +9M/tháng (+15% AOV)
- Referral: +12M/tháng (5 KH mới miễn phí × 2.5M)
- Tổng extra: ~81M/tháng

GROSS PROFIT BỔ SUNG: 81M × 28% = 22.7M/tháng
NET ROI: (22.7M - 8M) / 8M = 1.84x → ROI DƯƠNG

→ Đầu tư 8M/tháng cho retention → Thu về 22.7M gross profit bổ sung
```

---

*🔄 Chiến Lược Retention & Loyalty — Xiaomi247.com*
*Ngày tạo: 09/04/2026 | Review: Hàng tháng*
*Tham chiếu: [Sales Funnel Strategy](01-sales-funnel-strategy.md) | [Email Marketing](02-email-marketing.md) | [Trust Strategy](../marketing/04-trust-building/trust-strategy.md) | [Digital Marketing](../marketing/05-digital-marketing/digital-marketing-strategy.md) | [Ads Optimization](../ads-social/04-ads-optimization.md)*