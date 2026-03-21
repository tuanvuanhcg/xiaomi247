# ĐO LƯỜNG, BÁO CÁO & TỐI ƯU QUẢNG CÁO — XIAOMI247.COM

> **Mục tiêu:** Hướng dẫn đo lường hiệu quả, báo cáo performance, và tối ưu quảng cáo trên tất cả kênh
> **Áp dụng cho:** Facebook/Instagram Ads, Google Ads, TikTok Ads, Zalo OA Ads
> **Cập nhật:** Tháng 3/2026

---

## 1. DASHBOARD SETUP — CẤU HÌNH BẢNG ĐIỀU KHIỂN

### 1.1. Facebook Ads Manager

**Columns cần hiển thị (Custom Columns → Save as preset "Xiaomi247 Standard"):**

| Nhóm | Columns | Mục đích |
|------|---------|----------|
| **Performance** | Impressions, Reach, Frequency | Đo lường phạm vi tiếp cận |
| **Engagement** | Clicks (All), Link Clicks, CTR (Link), CPC (Link) | Đo lường tương tác |
| **Conversion** | Purchases, Purchase Value, Cost per Purchase, ROAS | Đo lường chuyển đổi |
| **Cost** | Amount Spent, CPM, CPC | Đo lường chi phí |
| **Quality** | Quality Ranking, Engagement Ranking, Conversion Ranking | Đo lường chất lượng ads |

**Custom Reports cần tạo:**
- **Daily Performance:** Breakdown by Day → theo dõi trend hàng ngày
- **Creative Analysis:** Breakdown by Ad → so sánh creative performance
- **Audience Insights:** Breakdown by Age, Gender, Placement → tối ưu targeting
- **Funnel Report:** Custom columns: Impressions → Clicks → Add to Cart → Purchase

### 1.2. Google Ads

**Columns cần hiển thị:**

| Nhóm | Columns | Mục đích |
|------|---------|----------|
| **Performance** | Impressions, Clicks, CTR, Avg. CPC | Cơ bản |
| **Conversion** | Conversions, Conv. Rate, Cost/Conv., Conv. Value | Chuyển đổi |
| **Quality** | Quality Score, Expected CTR, Ad Relevance, Landing Page Exp. | Chất lượng |
| **Competitive** | Search Impr. Share, Search Top IS, Search Abs. Top IS | Cạnh tranh |

**Custom Reports:**
- **Search Terms Report:** Xem actual search queries → thêm negative keywords
- **Auction Insights:** So sánh với đối thủ (mivietnam, mihanoi)
- **Landing Page Report:** Performance theo landing page → tối ưu CRO
- **Device Report:** Performance theo thiết bị → adjust bid

### 1.3. TikTok Ads Manager

**Columns cần hiển thị:**

| Nhóm | Columns | Mục đích |
|------|---------|----------|
| **Reach** | Impressions, Reach, Frequency, CPM | Phạm vi |
| **Video** | Video Views (2s/6s/100%), Avg. Watch Time, Video Play Actions | Video performance |
| **Engagement** | Clicks, CTR, CPC, Likes, Comments, Shares | Tương tác |
| **Conversion** | Conversions, CVR, CPA, Total Purchase Value, ROAS | Chuyển đổi |

### 1.4. Google Analytics 4 (GA4)

**Reports cần cấu hình:**
- **Acquisition → Traffic Acquisition:** Xem traffic theo source/medium
- **Monetization → Ecommerce Purchases:** Revenue, transactions, AOV
- **Advertising → Attribution Paths:** Customer journey cross-channel
- **Explore → Funnel Exploration:** Custom funnel: Session Start → View Item → Add to Cart → Purchase

**Custom Dashboard (Looker Studio):**
- Kết nối GA4 + Google Ads + Facebook Ads (via Supermetrics/Funnel.io)
- Tạo dashboard tổng hợp cross-channel performance

---

## 2. KPI FRAMEWORK — CHỈ SỐ MỤC TIÊU THEO KÊNH

### 2.1. Facebook/Instagram Ads

| KPI | Target T1 | Target T2 | Target T3 | Cách đo | Action nếu không đạt |
|-----|-----------|-----------|-----------|---------|----------------------|
| **ROAS** | ≥ 3x | ≥ 4x | ≥ 5x | Revenue / Ad Spend | Review creative + audience |
| **CPA** | ≤ 200K | ≤ 150K | ≤ 120K | Spend / Purchases | Tối ưu targeting, landing page |
| **CTR (Link)** | ≥ 1.5% | ≥ 2% | ≥ 2.5% | Link Clicks / Impressions | Đổi creative, headline, CTA |
| **CPM** | ≤ 50K | ≤ 45K | ≤ 40K | (Spend / Impressions) × 1000 | Mở rộng audience, giảm frequency |
| **Frequency** | ≤ 3 | ≤ 3 | ≤ 3 | Impressions / Reach | Refresh creative, mở audience |
| **Conv. Rate** | ≥ 2% | ≥ 3% | ≥ 4% | Purchases / Link Clicks | Tối ưu landing page |

### 2.2. Google Ads

| KPI | Target T1 | Target T2 | Target T3 | Cách đo | Action nếu không đạt |
|-----|-----------|-----------|-----------|---------|----------------------|
| **ROAS** | ≥ 4x | ≥ 5x | ≥ 6x | Conv. Value / Cost | Tối ưu keywords, bids |
| **CPA** | ≤ 150K | ≤ 120K | ≤ 100K | Cost / Conversions | Thêm negative KW, tối ưu ad copy |
| **CTR** | ≥ 2% | ≥ 3% | ≥ 4% | Clicks / Impressions | Cải thiện ad copy, extensions |
| **Quality Score** | ≥ 7 | ≥ 7 | ≥ 8 | Google Ads dashboard | Tối ưu ad relevance + landing page |
| **Search Impr. Share** | ≥ 50% | ≥ 60% | ≥ 70% | Impressions / Eligible Impressions | Tăng budget hoặc bid |
| **Conv. Rate** | ≥ 3% | ≥ 4% | ≥ 5% | Conversions / Clicks | Tối ưu landing page, offer |

### 2.3. TikTok Ads

| KPI | Target T1 | Target T2 | Target T3 | Cách đo | Action nếu không đạt |
|-----|-----------|-----------|-----------|---------|----------------------|
| **CPV (Cost Per View)** | ≤ 500đ | ≤ 400đ | ≤ 300đ | Spend / Video Views | Cải thiện hook 3s đầu |
| **CTR** | ≥ 1% | ≥ 1.5% | ≥ 2% | Clicks / Impressions | Đổi creative, CTA rõ hơn |
| **Engagement Rate** | ≥ 3% | ≥ 4% | ≥ 5% | (Likes+Comments+Shares) / Views | Content entertaining hơn |
| **Avg. Watch Time** | ≥ 5s | ≥ 7s | ≥ 10s | TikTok Analytics | Hook mạnh hơn, content ngắn gọn |
| **CPA** | ≤ 300K | ≤ 200K | ≤ 150K | Spend / Conversions | Tối ưu funnel, retarget |

### 2.4. Zalo OA Ads

| KPI | Target T1 | Target T2 | Target T3 | Cách đo | Action nếu không đạt |
|-----|-----------|-----------|-----------|---------|----------------------|
| **Open Rate** | ≥ 40% | ≥ 45% | ≥ 50% | Opens / Sent | Tối ưu tiêu đề, thời gian gửi |
| **CTR** | ≥ 5% | ≥ 6% | ≥ 7% | Clicks / Opens | CTA rõ ràng, offer hấp dẫn |
| **Follower Growth** | +500/tháng | +1000/tháng | +1500/tháng | Zalo OA Admin | Chạy ads follow, cross-promote |
| **Unfollow Rate** | ≤ 5% | ≤ 4% | ≤ 3% | Unfollows / Total Followers | Giảm tần suất, content giá trị hơn |

---

## 3. WEEKLY ADS REPORT TEMPLATE — BÁO CÁO QUẢNG CÁO HÀNG TUẦN

*Tuần: [DD/MM] — [DD/MM/YYYY]*
*Người báo cáo: [Tên] | Ngày: [DD/MM/YYYY]*

### 3.1. Tổng quan Performance theo kênh

| Kênh | Budget | Spend | Impressions | Clicks | CTR | CPC | Conversions | CPA | Revenue | ROAS | vs Target |
|------|--------|-------|-------------|--------|-----|-----|-------------|-----|---------|------|-----------|
| Meta Ads |  |  |  |  |  |  |  |  |  |  | 🟢/🟡/🔴 |
| Google Search |  |  |  |  |  |  |  |  |  |  | 🟢/🟡/🔴 |

### 3.2. Performance theo Campaign

| Campaign | Kênh | Objective | Spend | Clicks | CTR | Conv. | CPA | ROAS | Status |
|----------|------|-----------|-------|--------|-----|-------|-----|------|--------|
| FB Awareness - Video Views |  | Video Views |  |  |  |  |  |  | 🟢/🟡/🔴 |
| FB Traffic - Interest |  | Link Clicks |  |  |  |  |  |  | 🟢/🟡/🔴 |
| FB Conversion - Retargeting |  | Conversions |  |  |  |  |  |  | 🟢/🟡/🔴 |
| FB Conversion - Lookalike |  | Conversions |  |  |  |  |  |  | 🟢/🟡/🔴 |
| Google Branded Search |  | Conversions |  |  |  |  |  |  | 🟢/🟡/🔴 |
| Google Non-Branded (Tivi) |  | Conversions |  |  |  |  |  |  | 🟢/🟡/🔴 |
| Google Non-Branded (Robot) |  | Conversions |  |  |  |  |  |  | 🟢/🟡/🔴 |
| Google Shopping |  | Conversions |  |  |  |  |  |  | 🟢/🟡/🔴 |
| TikTok Spark Ads |  | Traffic |  |  |  |  |  |  | 🟢/🟡/🔴 |
| TikTok In-feed |  | Traffic |  |  |  |  |  |  | 🟢/🟡/🔴 |

### 3.3. Performance theo Creative

| Creative | Format | Kênh | Impressions | CTR | Conv. Rate | CPA | ROAS | Ghi chú |
|----------|--------|------|-------------|-----|------------|-----|------|---------|
|  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |

### 3.4. Top & Worst Performers

**🏆 Top 3 Campaigns (ROAS cao nhất):**

| # | Campaign | Kênh | ROAS | CPA | Spend | Recommendation |
|---|----------|------|------|-----|-------|----------------|
| 1 |  |  |  |  |  | SCALE — Tăng budget 20% |
| 2 |  |  |  |  |  |  |
| 3 |  |  |  |  |  |  |

**🔴 Bottom 3 Campaigns (cần action):**

| # | Campaign | Kênh | ROAS | CPA | Vấn đề | Action |
|---|----------|------|------|-----|--------|--------|
| 1 |  |  |  |  |  | KILL / FIX / PAUSE |
| 2 |  |  |  |  |  |  |
| 3 |  |  |  |  |  |  |

### 3.5. Budget Tracking

| Kênh | Budget tháng | Đã chi tuần này | Tổng đã chi | Còn lại | % Used | Pace |
|------|-------------|----------------|-------------|---------|--------|------|
| Meta Ads | 14M |  |  |  |  | On/Over/Under |
| Google Ads | 10.5M |  |  |  |  | On/Over/Under |
| TikTok Ads | 7M |  |  |  |  | On/Over/Under |
| Zalo/Other | 3.5M |  |  |  |  | On/Over/Under |
| **TỔNG** | **35M** | **___** | **___** | **___** | **___** | |

### 3.6. Recommendations tuần tới

| Priority | Action | Kênh | Expected Impact | Owner |
|----------|--------|------|-----------------|-------|
| P1 |  |  |  |  |
| P1 |  |  |  |  |
| P2 |  |  |  |  |
| P2 |  |  |  |  |

---

## 4. MONTHLY ADS REVIEW FRAMEWORK — ĐÁNH GIÁ QUẢNG CÁO HÀNG THÁNG

### 4.1. Budget Reallocation Rules

| Điều kiện | Action | Ví dụ |
|-----------|--------|-------|
| Kênh có ROAS > target + CPA < target | Tăng budget 20-30% từ kênh kém | Google ROAS 5x → chuyển budget từ TikTok |
| Kênh có ROAS < 2x liên tục 2 tuần | Giảm budget 30-50%, chuyển sang kênh tốt hơn | TikTok ROAS 1.5x → giảm 30% |
| Campaign type Awareness chiếm > 25% budget | Giảm Awareness, tăng Conversion | Awareness 30% → giảm xuống 20% |
| Kênh mới chưa test | Allocate 5-10% budget test | Test Zalo Ads mới |

**Quy trình reallocation:**
1. Export data tháng từ tất cả platforms
2. Tính ROAS, CPA, CTR trung bình theo kênh
3. Rank kênh theo ROAS (cao → thấp)
4. Chuyển 10-20% budget từ kênh bottom → kênh top
5. Giữ ít nhất 5% cho testing

### 4.2. Winning/Losing Campaign Analysis

**Winning Campaign Criteria:**
- ✅ ROAS ≥ target liên tục 3+ tuần
- ✅ CPA ≤ target
- ✅ CTR ≥ benchmark kênh
- ✅ Frequency ≤ 3 (chưa bão hòa)

**Losing Campaign Criteria:**
- 🔴 ROAS < 2x sau 2 tuần optimize
- 🔴 CPA > 2x target
- 🔴 CTR < 0.5%
- 🔴 Frequency > 5 (audience bão hòa)

**Action Matrix:**

| Winning | Action |
|---------|--------|
| ROAS cao + Spend thấp | Scale budget 20-30% |
| ROAS cao + Spend cao | Maintain, test new audiences |
| ROAS cao + Frequency cao | Refresh creative, giữ audience |

| Losing | Action |
|--------|--------|
| CPA cao + CTR tốt | Fix landing page / offer |
| CPA cao + CTR kém | Fix creative / copy |
| Frequency cao + ROAS giảm | Pause, refresh creative |
| Không có conversions sau 7 ngày | Kill campaign |

### 4.3. Creative Fatigue Detection

**Dấu hiệu creative fatigue:**
- CTR giảm > 20% so với tuần đầu
- Frequency > 4 trên cùng audience
- CPM tăng > 30% so với tuần đầu
- Engagement rate giảm liên tục 3 ngày

**Giải pháp:**
1. Rotate creative mới mỗi 2-3 tuần
2. Chuẩn bị sẵn 3-5 creative variants
3. Thay đổi format: Image → Video → Carousel → Collection
4. Thay đổi hook/headline giữ visual cũ (nếu visual vẫn tốt)

### 4.4. Audience Saturation Check

| Metric | Ngưỡng bão hòa | Action |
|--------|----------------|--------|
| Frequency > 5/tuần | Audience quá nhỏ | Mở rộng audience, thêm interests |
| Reach < 30% audience size | Đã tiếp cận hết | Tạo Lookalike mới, mở rộng geo |
| CPA tăng > 30% MoM | Audience cạn kiệt | Test audience mới hoàn toàn |
| CTR giảm + Frequency tăng | Audience mệt mỏi | Refresh creative + mở audience |

---

## 5. A/B TESTING METHODOLOGY — PHƯƠNG PHÁP THỬ NGHIỆM

### 5.1. What to Test (Ưu tiên theo impact)

| Yếu tố | Impact | Ví dụ test | Kênh |
|---------|--------|-----------|------|
| **Creative (Visual)** | ⭐⭐⭐⭐⭐ | Video vs Image vs Carousel | FB, TikTok |
| **Copy (Headline)** | ⭐⭐⭐⭐ | Giá rẻ vs Chính hãng vs Free ship | FB, Google |
| **Audience** | ⭐⭐⭐⭐ | Interest vs Lookalike vs Broad | FB, TikTok |
| **Placement** | ⭐⭐⭐ | Feed vs Stories vs Reels | FB, IG |
| **Landing Page** | ⭐⭐⭐⭐⭐ | Product page vs Collection page vs Promo page | All |
| **Offer** | ⭐⭐⭐⭐ | Giảm giá % vs Giảm giá VNĐ vs Free ship | All |
| **CTA** | ⭐⭐⭐ | Mua ngay vs Xem thêm vs Nhận ưu đãi | FB, Google |
| **Bidding** | ⭐⭐ | Lowest cost vs Cost cap vs Bid cap | FB |

### 5.2. Sample Size & Duration

**Quy tắc cơ bản:**
- Minimum budget per variant: 50 conversions hoặc 5x CPA (tùy cái nào đến trước)
- Minimum duration: 7 ngày (để cover cả weekday + weekend)
- Maximum duration: 14 ngày (tránh external factors ảnh hưởng)
- Chỉ test 1 biến số tại 1 thời điểm

**Sample Size Calculator (ước tính):**

| Daily Budget/Variant | CPA trung bình | Ngày cần chạy | Tổng budget test |
|----------------------|----------------|---------------|-----------------|
| 100K/ngày | 150K | 10 ngày | 200K × 10 = 2M |
| 200K/ngày | 150K | 7 ngày | 400K × 7 = 2.8M |
| 300K/ngày | 150K | 7 ngày | 600K × 7 = 4.2M |

**Statistical Significance:**
- Sử dụng Facebook A/B Test tool (tự động tính significance)
- Google Ads: Experiments tab (tự động split traffic)
- Manual: Cần ≥ 95% confidence level → dùng tool: [AB Test Calculator](https://abtestguide.com/calc/)

### 5.3. Testing Calendar (Tháng 1)

| Tuần | Test | Biến số | Kênh | Budget | Expected Learning |
|------|------|---------|------|--------|-------------------|
| W1-W2 | Creative Format | Video vs Image vs Carousel | Facebook | 1.5M | Winning format |
| W2-W3 | Headline | Giá rẻ vs Chính hãng vs Ưu đãi | Facebook | 1M | Winning message |
| W3-W4 | Audience | Interest vs Lookalike vs Broad | Facebook | 1.5M | Best audience type |
| W3-W4 | Ad Copy | 3 variants | Google Search | 500K | Best ad copy |
| W4 | Landing Page | Product page vs Collection page | All | 500K | Best conversion page |

**Quy tắc test:**
1. Chỉ test 1 biến số/lần — giữ nguyên các yếu tố khác
2. Chạy đủ 7 ngày trước khi kết luận
3. Winner = variant có CPA thấp nhất HOẶC ROAS cao nhất
4. Áp dụng winner → test biến số tiếp theo
5. Document kết quả vào bảng "Test Results Log"


---

## 6. OPTIMIZATION PLAYBOOK — CẨM NANG TỐI ƯU

### 6.1. Decision Tree — Cây quyết định

```
                    ┌─────────────────────┐
                    │  KIỂM TRA CAMPAIGN  │
                    │    PERFORMANCE      │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │   ROAS vs Target?   │
                    └──────────┬──────────┘
                     ┌─────────┴─────────┐
                     │                   │
              ┌──────▼──────┐     ┌──────▼──────┐
              │ ROAS > Target│     │ ROAS < Target│
              └──────┬──────┘     └──────┬──────┘
                     │                   │
              ┌──────▼──────┐     ┌──────▼──────┐
              │ Spend check │     │  CTR check  │
              └──────┬──────┘     └──────┬──────┘
               ┌─────┴─────┐      ┌─────┴─────┐
               │           │      │           │
        ┌──────▼───┐ ┌─────▼────┐ ┌▼──────┐ ┌─▼─────┐
        │Spend <   │ │Spend =   │ │CTR    │ │CTR    │
        │Budget    │ │Budget    │ │Good   │ │Bad    │
        └──────┬───┘ └─────┬────┘ └┬──────┘ └─┬─────┘
               │           │       │           │
        ┌──────▼───┐ ┌─────▼────┐ ┌▼──────┐ ┌─▼─────┐
        │ 🟢 SCALE │ │🟡MAINTAIN│ │🟠 FIX │ │🔴 FIX │
        │Tăng 20%  │ │+ Test new│ │Landing│ │Creative│
        │budget/ngày│ │audiences │ │Page   │ │+ Copy │
        └──────────┘ └──────────┘ └───────┘ └───────┘
```

### 6.2. Chi tiết từng action

**🟢 SCALE — Khi ROAS > target + Spend < budget:**
- Tăng budget 20%/ngày (KHÔNG tăng quá 20% để tránh reset learning phase)
- Duplicate ad set winning → test audience mới với cùng creative
- Mở rộng Lookalike từ 1% → 2% → 3%
- Thêm placement mới (Stories, Reels, Audience Network)

**🟡 MAINTAIN — Khi ROAS > target + Spend = budget:**
- Giữ nguyên budget, không thay đổi
- Test audience mới song song (10-20% budget)
- Chuẩn bị creative mới để thay thế khi fatigue
- Monitor frequency — nếu > 3 thì chuẩn bị refresh

**🟠 FIX LANDING PAGE — Khi ROAS < target + CTR tốt:**
- Vấn đề: Người dùng click nhưng không mua → landing page/offer có vấn đề
- Check: Page load speed (< 3s), mobile responsive, CTA rõ ràng
- Check: Giá cạnh tranh, trust signals (review, bảo hành), urgency
- A/B test landing page: layout, CTA position, offer

**🔴 FIX CREATIVE — Khi ROAS < target + CTR kém:**
- Vấn đề: Người dùng không click → creative/copy không hấp dẫn
- Thay đổi: Visual (ảnh/video mới), headline, CTA
- Test: Format mới (video nếu đang dùng image, carousel nếu đang dùng single)
- Review: Ad copy có match với audience intent không?

**⛔ KILL — Khi CPA > 2x target:**
- Pause campaign ngay lập tức
- Phân tích: Audience sai? Creative sai? Landing page sai?
- Nếu đã optimize 7 ngày mà không cải thiện → tắt vĩnh viễn
- Chuyển budget sang campaign đang winning

### 6.3. Daily Optimization Checklist

| Thời gian | Action | Tool |
|-----------|--------|------|
| 9:00 AM | Check spend pace — có overspend không? | Ads Manager |
| 9:00 AM | Check CPA campaigns — có campaign CPA > 2x? | Ads Manager |
| 10:00 AM | Review search terms (Google) — thêm negative KW | Google Ads |
| 14:00 PM | Check frequency — có ad set frequency > 4? | FB Ads Manager |
| 16:00 PM | Review performance — scale winners, pause losers | All platforms |
| 17:00 PM | Update daily tracking sheet | Google Sheets |

---

## 7. ATTRIBUTION MODEL — MÔ HÌNH PHÂN BỔ

### 7.1. GA4 Data-Driven Attribution Setup

**Bước 1: Cấu hình GA4**
1. GA4 → Admin → Attribution Settings
2. Chọn **Data-driven attribution** (mặc định từ GA4)
3. Lookback window: 30 ngày cho acquisition, 90 ngày cho other conversions
4. Bật **Google Signals** để tracking cross-device

**Bước 2: Liên kết platforms**
- Google Ads → GA4: Admin → Google Ads Links → Link account
- Facebook: UTM parameters trên tất cả ads (`utm_source=facebook&utm_medium=paid&utm_campaign={campaign_name}`)
- TikTok: UTM parameters (`utm_source=tiktok&utm_medium=paid&utm_campaign={campaign_name}`)

**Bước 3: UTM Convention**

| Parameter | Format | Ví dụ |
|-----------|--------|-------|
| utm_source | platform name | facebook, google, tiktok, zalo |
| utm_medium | paid/organic/email | paid, cpc, social |
| utm_campaign | campaign name | fb_retarget_tivi_t1 |
| utm_content | ad/creative name | video_unboxing_v1 |
| utm_term | keyword (Google) | mua_tivi_xiaomi |

### 7.2. Cross-Channel Attribution

**Báo cáo cần xem trong GA4:**
- **Model Comparison:** So sánh Last Click vs Data-driven → hiểu kênh nào bị undervalue
- **Conversion Paths:** Xem customer journey phổ biến nhất
- **Assisted Conversions:** Kênh nào assist nhiều nhất (thường là Awareness channels)

**Ví dụ customer journey điển hình:**
```
TikTok Video (Awareness) → Facebook Retarget (Consideration) → Google Search (Purchase)
     ↑ Assist                    ↑ Assist                         ↑ Last Click
```

> ⚠️ **Lưu ý:** Không chỉ đánh giá kênh bằng Last Click. TikTok/FB Video có thể ROAS thấp theo Last Click nhưng assist rất nhiều conversions.

### 7.3. Assisted Conversions Report

| Kênh | Last Click Conv. | Assisted Conv. | Assisted/Last Click Ratio | Vai trò chính |
|------|-----------------|----------------|--------------------------|---------------|
| Google Search | Cao | Thấp | < 1 | Closer (kênh chốt đơn) |
| Facebook Retarget | Trung bình | Trung bình | ≈ 1 | Hybrid |
| TikTok | Thấp | Cao | > 1 | Assister (kênh hỗ trợ) |
| Facebook Video | Thấp | Cao | > 1 | Introducer (kênh giới thiệu) |

---

## 8. REMARKETING OPTIMIZATION — TỐI ƯU REMARKETING

### 8.1. Frequency Capping

| Audience | Frequency Cap | Lý do |
|----------|--------------|-------|
| Web Visitors (7 ngày) | 3-5 lần/tuần | Đủ nhắc nhở, không spam |
| Cart Abandoners | 5-7 lần/tuần | Urgency cao, cần push mạnh hơn |
| Product Viewers | 3-4 lần/tuần | Nurture, không quá aggressive |
| Past Customers | 2-3 lần/tuần | Đã mua rồi, chỉ cần nhẹ nhàng |
| Lookalike Audiences | 2-3 lần/tuần | Cold audience, tránh annoy |

### 8.2. Audience Refresh Schedule

| Audience Window | Refresh | Lý do |
|----------------|---------|-------|
| **7 ngày** | Tự động refresh (rolling window) | Visitors gần đây nhất, intent cao |
| **14 ngày** | Tự động refresh | Mở rộng pool, intent trung bình |
| **30 ngày** | Tự động refresh | Pool lớn nhất, intent thấp hơn |
| **Custom (Cart 3 ngày)** | Tự động refresh | Cart abandoners nóng nhất |

**Exclude rules:**
- Exclude purchasers 7 ngày gần nhất khỏi retarget campaigns
- Exclude người đã convert khỏi awareness campaigns
- Exclude audience quá nhỏ (< 1000 users) — không đủ data optimize

### 8.3. Creative Rotation cho Remarketing

| Ngày sau visit | Message | Creative type | Offer |
|---------------|---------|---------------|-------|
| Ngày 1-3 | "Bạn quên sản phẩm trong giỏ hàng!" | Dynamic Product Ad | Không cần offer |
| Ngày 4-7 | "Ưu đãi đặc biệt cho bạn" | Carousel sản phẩm đã xem | Giảm 5% hoặc Free ship |
| Ngày 8-14 | "Sản phẩm bạn quan tâm đang giảm giá" | Single image + urgency | Giảm 10% (limited time) |
| Ngày 15-30 | "Khám phá sản phẩm mới từ Xiaomi" | Video/Carousel sản phẩm mới | Bundle deal |

### 8.4. Sequential Messaging

```
Lần 1 (Ngày 1-2):   "Chào bạn! Cảm ơn đã ghé thăm Xiaomi247"
                      → Brand awareness, không bán hàng

Lần 2 (Ngày 3-5):   "Sản phẩm bạn xem đang có ưu đãi"
                      → Product-focused, social proof (reviews)

Lần 3 (Ngày 6-10):  "Chỉ còn 2 ngày — Giảm 10% cho đơn đầu tiên"
                      → Urgency + Offer

Lần 4 (Ngày 11-14): "Khách hàng nói gì về sản phẩm này?"
                      → Testimonials, UGC, trust building
```

---

## 9. ROI CALCULATOR — BẢNG TÍNH LỢI NHUẬN QUẢNG CÁO

### 9.1. Công thức tính

```
Budget → Impressions → Clicks → Sessions → Add to Cart → Purchases → Revenue → ROAS

Impressions  = Budget / CPM × 1000
Clicks       = Impressions × CTR
Sessions     ≈ Clicks × 0.9 (10% bounce trước khi load)
Add to Cart  = Sessions × Add-to-Cart Rate
Purchases    = Add to Cart × Checkout Rate
Revenue      = Purchases × AOV
ROAS         = Revenue / Budget
Profit       = Revenue - COGS - Budget - Operating Costs
```

### 9.2. Ví dụ cụ thể: Budget 35M VNĐ (Tháng 1)

| Bước | Metric | Meta Ads (14M) | Google Ads (10.5M) | TikTok (7M) | Zalo (1.75M) | Dự phòng (1.75M) | **TỔNG** |
|------|--------|---------------|-------------------|-------------|-------------|------------------|----------|
| 1 | **Budget** | 14,000,000đ | 10,500,000đ | 7,000,000đ | 1,750,000đ | 1,750,000đ | **35,000,000đ** |
| 2 | **CPM** | 50,000đ | 60,000đ | 40,000đ | 30,000đ | — | — |
| 3 | **Impressions** | 280,000 | 175,000 | 175,000 | 58,333 | — | **688,333** |
| 4 | **CTR** | 1.5% | 2.5% | 1% | 5% | — | — |
| 5 | **Clicks** | 4,200 | 4,375 | 1,750 | 2,917 | — | **13,242** |
| 6 | **CPC** | 3,333đ | 2,400đ | 4,000đ | 600đ | — | **2,643đ** |
| 7 | **Sessions (×0.9)** | 3,780 | 3,938 | 1,575 | 2,625 | — | **11,918** |
| 8 | **Add-to-Cart Rate** | 7% | 10% | 5% | 8% | — | — |
| 9 | **Add to Cart** | 265 | 394 | 79 | 210 | — | **947** |
| 10 | **Checkout Rate** | 30% | 35% | 25% | 30% | — | — |
| 11 | **Purchases** | 79 | 138 | 20 | 63 | — | **300** |
| 12 | **AOV** | 2,500,000đ | 2,500,000đ | 2,500,000đ | 2,500,000đ | — | — |
| 13 | **Revenue** | 198M | 345M | 49M | 158M | — | **750M** |
| 14 | **ROAS** | **14.2x** | **32.8x** | **7.1x** | **90x** | — | **21.4x** |

> ⚠️ **Lưu ý quan trọng:** Đây là ước tính lý tưởng với conversion rates tối ưu. Thực tế tháng đầu ROAS sẽ thấp hơn nhiều do đang trong giai đoạn learning phase. **Target thực tế tháng 1: ROAS 3-5x** (theo ads-budget-proposal.md).

### 9.3. Scenario Analysis (Budget 35M)

| Scenario | ROAS | Revenue | Purchases | CPA | Đánh giá |
|----------|------|---------|-----------|-----|----------|
| **Pessimistic** | 2x | 70M | 28 đơn | 1,250K | 🔴 Cần optimize gấp |
| **Conservative** | 3x | 105M | 42 đơn | 833K | 🟡 Đạt minimum target |
| **Expected** | 4x | 140M | 56 đơn | 625K | 🟢 On track |
| **Optimistic** | 5x | 175M | 70 đơn | 500K | 🟢 Scale thêm |
| **Best Case** | 6x+ | 210M+ | 84+ đơn | 417K | 🟢 Tăng budget mạnh |

### 9.4. Break-even Analysis

```
Break-even ROAS = 1 / Gross Margin %

Ví dụ Xiaomi247:
- Giá bán trung bình (AOV): 2,500,000đ
- Giá vốn (COGS): ~70% = 1,750,000đ
- Gross Margin: 30% = 750,000đ
- Break-even ROAS = 1 / 0.30 = 3.33x

→ ROAS ≥ 3.33x mới có lãi từ ads
→ Target ROAS ≥ 4x để có lợi nhuận đủ cover operating costs
```

### 9.5. Monthly ROI Tracking

| Tháng | Budget | Revenue | ROAS | Purchases | CPA | Gross Profit | Net Profit (sau ads) | Status |
|-------|--------|---------|------|-----------|-----|-------------|---------------------|--------|
| T1 | 35M |  |  |  |  |  |  | 🟢/🟡/🔴 |
| T2 | 50M |  |  |  |  |  |  | 🟢/🟡/🔴 |
| T3 | 70M |  |  |  |  |  |  | 🟢/🟡/🔴 |
| **Q1** | **155M** | **___** | **___** | **___** | **___** | **___** | **___** | |

---

*📊 Ads Performance & Optimization Guide — Xiaomi247.com*
*Ngày tạo: 21/03/2026 | Review: Hàng tuần*
*Tham chiếu: [Ads Budget Proposal](../marketing/05-digital-marketing/ads-budget-proposal.md) | [Digital Marketing Strategy](../marketing/05-digital-marketing/digital-marketing-strategy.md) | [KPIs Dashboard](../marketing/06-measurement/kpis-dashboard.md) | [Weekly Report](../marketing/06-measurement/weekly-report-template.md)*