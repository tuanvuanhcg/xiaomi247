# KẾ HOẠCH GOOGLE ADS — XIAOMI247.COM

> **Platform:** Google Ads (Search + Shopping + Display/Remarketing)
> **Tỷ trọng budget:** 30% tổng digital marketing
> **Mục tiêu:** Bắt purchase intent, CPA ≤ 150K, ROAS ≥ 4x
> **Cập nhật:** Tháng 3/2026

---

## 1. SEARCH CAMPAIGNS

### 1.1. Campaign Structure

| Campaign | Mục tiêu | Bid Strategy | Budget/ngày |
|----------|---------|-------------|-------------|
| **Branded Search** | Bảo vệ thương hiệu | Manual CPC | 50K |
| **Non-Branded: Tivi** | Traffic + Conversion | Target CPA | 80K |
| **Non-Branded: Robot hút bụi** | Traffic + Conversion | Target CPA | 60K |
| **Non-Branded: Gia dụng** | Traffic + Conversion | Target CPA | 50K |
| **Non-Branded: Tủ lạnh** (⭐ Low comp) | Quick win | Maximize Clicks → Target CPA | 40K |
| **Non-Branded: Máy lọc KK + Hút ẩm** | Quick win | Maximize Clicks → Target CPA | 30K |

### 1.2. Branded Keywords
| Keyword | Match Type | Bid | Landing Page |
|---------|-----------|-----|-------------|
| xiaomi247 | Exact | 2,000đ | Trang chủ |
| xiaomi247.com | Exact | 2,000đ | Trang chủ |
| xiaomi 247 | Phrase | 1,500đ | Trang chủ |
| xiaomi247 chính hãng | Phrase | 2,000đ | /gioi-thieu/ |

### 1.3. Non-Branded Keywords (từ Keyword Map)

**Cluster 1: Tivi Xiaomi — Top Priority**
| Keyword | Match Type | Bid | Landing Page |
|---------|-----------|-----|-------------|
| mua tivi xiaomi | Exact | 5,000đ | /tivi-xiaomi/ |
| tivi xiaomi 55 inch | Exact | 4,500đ | /tivi-xiaomi/55-inch/ |
| tivi xiaomi 43 inch giá rẻ | Phrase | 4,000đ | /tivi-xiaomi/43-inch/ |
| tivi xiaomi a pro 55 | Exact | 4,500đ | /tivi-xiaomi/a-pro-55/ |
| tivi xiaomi chính hãng giá tốt | Phrase | 4,000đ | /tivi-xiaomi/ |
| mua tivi xiaomi ở đâu uy tín | Phrase | 3,500đ | /gioi-thieu/ |
| tivi xiaomi 65 inch | Exact | 4,000đ | /tivi-xiaomi/65-inch/ |

**Cluster 2: Robot hút bụi — High Intent**
| Keyword | Match Type | Bid | Landing Page |
|---------|-----------|-----|-------------|
| robot hút bụi lau nhà xiaomi | Exact | 5,000đ | /robot-hut-bui-xiaomi/ |
| robot hút bụi xiaomi giá rẻ | Phrase | 4,000đ | /robot-hut-bui-xiaomi/?sort=price |
| robot hút bụi xiaomi x10+ | Exact | 4,500đ | /robot-hut-bui-xiaomi/x10-plus/ |
| robot hút bụi xiaomi chính hãng | Phrase | 4,500đ | /robot-hut-bui-xiaomi/ |
| mua robot hút bụi xiaomi | Exact | 4,500đ | /robot-hut-bui-xiaomi/ |

**Cluster 3: Tủ lạnh — ⭐ Quick Win (Low Competition)**
| Keyword | Match Type | Bid | Landing Page |
|---------|-----------|-----|-------------|
| mua tủ lạnh xiaomi | Exact | 3,500đ | /tu-lanh-xiaomi/ |
| tủ lạnh xiaomi 4 cánh | Exact | 3,000đ | /tu-lanh-xiaomi/4-canh/ |
| tủ lạnh xiaomi chính hãng | Phrase | 3,000đ | /tu-lanh-xiaomi/ |
| tủ lạnh xiaomi side by side | Exact | 3,000đ | /tu-lanh-xiaomi/side-by-side/ |

**Cluster 4: Gia dụng — Mixed Intent**
| Keyword | Match Type | Bid | Landing Page |
|---------|-----------|-----|-------------|
| mua máy lọc không khí xiaomi | Exact | 4,000đ | /may-loc-khong-khi-xiaomi/ |
| máy lọc không khí xiaomi 4 pro | Exact | 3,500đ | /may-loc-khong-khi-xiaomi/4-pro/ |
| mua máy hút ẩm xiaomi | Exact | 3,000đ | /may-hut-am-xiaomi/ |
| gia dụng xiaomi chính hãng | Phrase | 3,000đ | /gia-dung-xiaomi/ |

---

## 2. NEGATIVE KEYWORDS

### 2.1. Account-Level Negatives
```
- miễn phí / free / crack
- cũ / secondhand / thanh lý / đã qua sử dụng
- sửa chữa / repair / fix
- tuyển dụng / việc làm / job
- xiaomi điện thoại / xiaomi phone / redmi / poco (ngoài phạm vi)
- fake / nhái / hàng giả
- hướng dẫn root / rom / firmware
- lazada / shopee / tiki / sendo (marketplace)
```

### 2.2. Campaign-Level Negatives
- **Tivi campaign:** `-điện thoại -phone -laptop -tablet`
- **Robot campaign:** `-roomba -ecovacs -dreame` (competitor brands — chỉ nếu CPC quá cao)
- **Tủ lạnh campaign:** `-samsung -lg -hitachi -panasonic` (evaluate trước khi negative)

---

## 3. GOOGLE SHOPPING

### 3.1. Product Feed Setup
| Yếu tố | Yêu cầu | Chi tiết |
|---------|---------|---------|
| **Platform** | Google Merchant Center | Đăng ký + verify domain |
| **Feed format** | XML / Google Sheets | Cập nhật giá, tồn kho tự động |
| **Product data** | Title, Description, Price, Image, GTIN, Brand | Tối ưu title chứa keyword |
| **Title format** | `[Brand] + [Product Name] + [Key Feature] + [Size/Model]` | VD: "Xiaomi Tivi A Pro 55 inch 4K Google TV" |
| **Image** | Nền trắng, min 800x800px | Ảnh chính + 3-4 ảnh phụ |
| **Shipping** | Cấu hình phí ship theo vùng | Free ship cho đơn >500K |

### 3.2. Shopping Campaign Structure
| Campaign | Products | Bid Strategy | Priority |
|----------|---------|-------------|----------|
| **High Priority — Best Sellers** | Top 10 SP bán chạy | Manual CPC (cao hơn) | High |
| **Medium Priority — Category** | Tất cả SP theo danh mục | Target ROAS | Medium |
| **Low Priority — Catch All** | Tất cả SP còn lại | Maximize Clicks | Low |

### 3.3. Bidding Strategy
- **Giai đoạn 1 (T1):** Manual CPC — kiểm soát chi phí, học data
- **Giai đoạn 2 (T2):** Target ROAS — khi có đủ 30+ conversions
- **Giai đoạn 3 (T3):** Performance Max — tự động tối ưu cross-channel

---

## 4. DISPLAY / REMARKETING

### 4.1. Remarketing Audiences
| Audience | Window | Message | Frequency Cap |
|----------|--------|---------|--------------|
| All visitors (chưa mua) | 30 ngày | "Quay lại Xiaomi247 — Ưu đãi đang chờ bạn" | 5/tuần |
| Product viewers | 14 ngày | Dynamic — hiển thị SP đã xem | 7/tuần |
| Cart abandoners | 7 ngày | "Hoàn tất đơn hàng — Giảm thêm 5%" | 10/tuần |
| Past customers | 60 ngày | Cross-sell phụ kiện, SP mới | 3/tuần |

### 4.2. Banner Sizes cần thiết
| Size | Tên | Vị trí hiển thị |
|------|-----|-----------------|
| 300x250 | Medium Rectangle | In-article, sidebar |
| 728x90 | Leaderboard | Header, between content |
| 320x50 | Mobile Leaderboard | Mobile websites |
| 160x600 | Wide Skyscraper | Sidebar |
| 300x600 | Half Page | Sidebar premium |
| 1200x628 | Responsive Display | Auto-placement |

### 4.3. Display Creative Guidelines
- Logo Xiaomi247 ở góc
- Hình sản phẩm rõ ràng
- Giá + badge "Chính hãng"
- CTA button nổi bật: "Mua ngay" / "Xem chi tiết"
- Màu brand: #FF6900 (Xiaomi orange) + #FFFFFF

---

## 5. BUDGET ALLOCATION

| Campaign Type | % Budget Google | Budget T1 (5M) | Budget T2 (8M) | Budget T3 (12M) |
|--------------|----------------|----------------|----------------|-----------------|
| Branded Search | 10% | 500K | 800K | 1.2M |
| Non-Branded Search | 40% | 2M | 3.2M | 4.8M |
| Google Shopping | 35% | 1.75M | 2.8M | 4.2M |
| Display/Remarketing | 15% | 750K | 1.2M | 1.8M |

---

*🔍 Google Ads Plan — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Review: Hàng tuần*
*Tham chiếu: [Keyword Map](../02-seo/keyword-map.md) | [Digital Marketing Strategy](digital-marketing-strategy.md) | [Ads Budget](ads-budget-proposal.md)*

