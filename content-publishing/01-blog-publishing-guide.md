# HƯỚNG DẪN PUBLISH BÀI BLOG LÊN WORDPRESS — XIAOMI247.COM

> **Áp dụng cho:** WordPress + WooCommerce + Motta Theme + Rank Math SEO
> **Website:** xiaomi247.com
> **Tham chiếu:** [Content Calendar Tháng 1](../marketing/03-content-marketing/content-calendar-month1.md) · [On-page SEO Templates](../seo-impl/03-onpage-seo-templates.md) · [Content Strategy](../marketing/03-content-marketing/content-strategy.md)
> **Cập nhật:** Tháng 3/2026

---

## MỤC LỤC

1. [Chuẩn bị Blog trên WordPress](#1-chuẩn-bị-blog-trên-wordpress)
2. [Quy trình Publish Step-by-step](#2-quy-trình-publish-step-by-step)
3. [SEO On-page cho Blog Posts (Rank Math)](#3-seo-on-page-cho-blog-posts-rank-math)
4. [Image Optimization cho Blog](#4-image-optimization-cho-blog)
5. [Internal Linking Checklist](#5-internal-linking-checklist)
6. [Social Sharing Setup](#6-social-sharing-setup)
7. [Pre-publish Checklist](#7-pre-publish-checklist)
8. [Post-publish Checklist](#8-post-publish-checklist)
9. [Cấu hình cụ thể cho 8 bài tháng 1](#9-cấu-hình-cụ-thể-cho-8-bài-tháng-1)

---

## 1. CHUẨN BỊ BLOG TRÊN WORDPRESS

### 1.1 Tạo Categories cho Blog

Vào **WP Admin → Posts → Categories**, tạo 4 categories chính tương ứng với 4 content pillars:

| Category | Slug | Mô tả | Content Pillar |
|----------|------|--------|----------------|
| **Review & So sánh** | `review` | Đánh giá chi tiết, so sánh sản phẩm Xiaomi | Pillar 1 (40%) |
| **Hướng dẫn** | `huong-dan` | Tutorial, buying guide, hướng dẫn sử dụng | Pillar 2 (30%) |
| **Tin tức** | `tin-tuc` | Tin tức công nghệ, sản phẩm mới Xiaomi | Pillar 3 (15%) |
| **Khuyến mãi** | `khuyen-mai` | Deal, flash sale, combo tiết kiệm | Pillar 4 (15%) |

**Cách tạo:**
1. Vào **Posts → Categories**
2. Nhập **Name** (ví dụ: "Review & So sánh")
3. Nhập **Slug** (ví dụ: `review`)
4. Nhập **Description** — mô tả ngắn cho category
5. Click **Add New Category**
6. Lặp lại cho 4 categories

### 1.2 Cấu hình Reading Settings

Vào **Settings → Reading:**

| Setting | Giá trị | Ghi chú |
|---------|---------|---------|
| Your homepage displays | A static page | Trang chủ dùng Elementor |
| Homepage | Trang chủ (Elementor) | Chọn trang đã thiết kế |
| Posts page | Blog | Tạo trang "Blog" trống |
| Blog pages show at most | 12 posts | Hiển thị 12 bài/trang |

### 1.3 Cấu hình Blog Page Layout trong Motta Theme

Vào **Appearance → Customize → Blog:**

| Setting | Giá trị |
|---------|---------|
| Blog Layout | Grid (3 cột) |
| Sidebar | No Sidebar (full width) |
| Excerpt Length | 25 từ |
| Featured Image | Hiển thị |
| Post Meta | Date, Category, Author |
| Pagination | Load More hoặc Numbered |

**Single Post Layout:**

| Setting | Giá trị |
|---------|---------|
| Layout | Full Width (no sidebar) |
| Featured Image | Hiển thị trên cùng |
| Post Navigation | Bật (Previous/Next) |
| Related Posts | Bật — 3 bài liên quan |
| Social Share Buttons | Bật — Facebook, Zalo, Copy Link |
| Author Box | Bật |

---

## 2. QUY TRÌNH PUBLISH STEP-BY-STEP

### Bước 1: Tạo bài viết mới
1. Vào **WP Admin → Posts → Add New**
2. Chọn **Block Editor** (Gutenberg) hoặc **Classic Editor** tùy preference

### Bước 2: Nhập tiêu đề (H1)
- Paste tiêu đề bài viết vào ô **Title**
- Tiêu đề phải chứa **keyword chính**, ≤ 60 ký tự
- Ví dụ: `Top 5 Tivi Xiaomi Đáng Mua Nhất 2026 — Từ Giá Rẻ Đến Cao Cấp`

### Bước 3: Paste & format nội dung
1. **Copy nội dung** từ file markdown (bỏ phần metadata ở đầu)
2. **Paste vào editor** — WordPress sẽ tự nhận diện headings, lists, tables
3. **Kiểm tra heading hierarchy:**
   - H1 = Tiêu đề bài (tự động)
   - H2 = Các phần chính
   - H3 = Các phần phụ
   - **Không bỏ cấp** (H1 → H2 → H3, không H1 → H3)
4. **Format bảng:** Dùng block Table hoặc plugin TablePress
5. **Bold/Italic:** Kiểm tra lại formatting sau khi paste

### Bước 4: Thêm hình ảnh
1. Click vào vị trí cần chèn ảnh → **Add Block → Image**
2. Upload ảnh đã optimize (xem [Mục 4](#4-image-optimization-cho-blog))
3. Nhập **Alt Text** theo format: `[Mô tả nội dung ảnh] — Xiaomi247`
4. Chọn **Alignment:** Center cho ảnh đơn, Wide cho ảnh banner
5. **Mỗi 300 từ nên có 1 hình ảnh** (5–8 ảnh/bài)

### Bước 5: Cấu hình Post Settings (sidebar phải)

#### 5a. Category & Tags
- **Category:** Chọn 1 category chính (Review, Hướng dẫn, Tin tức, hoặc Khuyến mãi)
- **Tags:** Thêm 3–5 tags liên quan
  - Tag sản phẩm: `tivi-xiaomi`, `robot-hut-bui`
  - Tag chủ đề: `review`, `so-sanh`, `huong-dan`
  - Tag năm: `2026`

#### 5b. Featured Image
1. Click **Set Featured Image** trong sidebar
2. Upload ảnh **1200 × 630px** (tỷ lệ 1.91:1 — chuẩn OG image)
3. Nhập **Alt Text** chứa keyword chính
4. Format: WebP, ≤ 200KB

#### 5c. Excerpt (Tóm tắt)
- Viết 1–2 câu tóm tắt nội dung bài (25–30 từ)
- Chứa keyword chính
- Hiển thị trên trang Blog listing và kết quả tìm kiếm nội bộ

#### 5d. Slug (URL)
- WordPress tự tạo slug từ tiêu đề
- **Chỉnh lại** cho ngắn gọn: 3–5 từ, chứa keyword, không dấu
- Ví dụ: `top-5-tivi-xiaomi-dang-mua-2026`
- Format: `/blog/[slug]/`

### Bước 6: Cấu hình Rank Math SEO
→ Xem chi tiết tại [Mục 3](#3-seo-on-page-cho-blog-posts-rank-math)

### Bước 7: Preview & Publish
1. Click **Preview** → kiểm tra trên Desktop và Mobile
2. Kiểm tra [Pre-publish Checklist](#7-pre-publish-checklist)
3. Chọn **Publish immediately** hoặc **Schedule** theo lịch content calendar
4. Click **Publish**

---

## 3. SEO ON-PAGE CHO BLOG POSTS (RANK MATH)

### 3.1 Cấu hình Rank Math cho mỗi bài

Scroll xuống phần **Rank Math SEO** bên dưới editor (hoặc click icon Rank Math ở sidebar):

#### Tab General — SEO Settings

| Field | Hướng dẫn | Ví dụ |
|-------|-----------|-------|
| **Focus Keyword** | Nhập keyword chính của bài | `tivi xiaomi đáng mua 2026` |
| **SEO Title** | Format: `[Tiêu đề chứa keyword] — 2026 | Xiaomi247` | `Top 5 Tivi Xiaomi Đáng Mua Nhất 2026 | Xiaomi247` |
| **SEO Description** | 120–155 ký tự, chứa keyword, có CTA | `Khám phá top 5 tivi Xiaomi đáng mua nhất 2026... Đọc ngay tại Xiaomi247!` |
| **Slug** | Ngắn gọn, chứa keyword | `top-5-tivi-xiaomi-dang-mua-2026` |

#### Tab Advanced

| Field | Giá trị |
|-------|---------|
| Robots Meta | Index, Follow (mặc định) |
| Canonical URL | Để trống (tự động) |
| Breadcrumb Title | Để trống hoặc nhập tiêu đề ngắn |

### 3.2 Hướng dẫn đạt điểm xanh Rank Math (80/100+)

Rank Math chấm điểm SEO dựa trên các tiêu chí sau. Hãy đảm bảo **tất cả đều xanh (✅)**:

#### Basic SEO (bắt buộc đạt)

| Tiêu chí | Cách đạt |
|----------|----------|
| ✅ Focus keyword trong SEO Title | Đặt keyword ở đầu title |
| ✅ Focus keyword trong Meta Description | Nhắc keyword tự nhiên trong meta |
| ✅ Focus keyword trong URL | Slug chứa keyword |
| ✅ Focus keyword trong 10% đầu nội dung | Nhắc keyword trong 100 từ đầu tiên |
| ✅ Focus keyword trong nội dung | Keyword density 1–2% |
| ✅ Độ dài nội dung | ≥ 1,500 từ cho blog post |
| ✅ Internal link | Có ít nhất 1 internal link |
| ✅ External link | Có ít nhất 1 external link (nguồn uy tín) |
| ✅ Hình ảnh có alt text | Mọi ảnh đều có alt text chứa keyword |

#### Additional SEO (nâng điểm)

| Tiêu chí | Cách đạt |
|----------|----------|
| ✅ Keyword trong H2/H3 | Nhắc keyword trong ít nhất 1 heading H2 |
| ✅ Keyword density | Giữ 1–2%, không nhồi keyword |
| ✅ SEO Title ≤ 60 ký tự | Kiểm tra độ dài title |
| ✅ Meta Description 120–155 ký tự | Kiểm tra độ dài meta |
| ✅ Table of Contents | Thêm TOC cho bài dài |

#### Content Readability (Rank Math)

| Tiêu chí | Cách đạt |
|----------|----------|
| ✅ Đoạn văn ngắn | Mỗi đoạn ≤ 150 từ (3–5 dòng) |
| ✅ Sử dụng subheadings | H2/H3 mỗi 300 từ |
| ✅ Sử dụng media | Ảnh/video mỗi 300 từ |
| ✅ Câu ngắn | Tránh câu quá dài (>20 từ) |

### 3.3 Rank Math Score Target

| Điểm | Đánh giá | Yêu cầu |
|------|----------|---------|
| 🟢 80–100 | Tốt | **Bắt buộc đạt** trước khi publish |
| 🟡 50–79 | Trung bình | Cần cải thiện thêm |
| 🔴 0–49 | Kém | **Không publish** — cần sửa lại |

---

## 4. IMAGE OPTIMIZATION CHO BLOG

### 4.1 Kích thước ảnh chuẩn

| Loại ảnh | Kích thước (px) | Tỷ lệ | Max file size | Format |
|----------|----------------|--------|---------------|--------|
| **Featured Image** | 1200 × 630 | 1.91:1 | 200KB | WebP |
| **In-content Image** | 800px width (auto height) | Tùy ảnh | 150KB | WebP |
| **Infographic** | 800 × auto | — | 300KB | WebP/PNG |
| **Product Photo** | 800 × 800 | 1:1 | 150KB | WebP |
| **Thumbnail** | 400 × 400 | 1:1 | 100KB | WebP |

### 4.2 Alt Text Format cho Blog

| Loại ảnh | Template Alt Text | Ví dụ |
|----------|------------------|-------|
| Featured image | `[Keyword chính] — Xiaomi247` | `Top 5 tivi Xiaomi đáng mua 2026 — Xiaomi247` |
| Ảnh sản phẩm | `[Tên SP] — [chi tiết]` | `Tivi Xiaomi A Pro 55 inch — mặt trước` |
| Ảnh so sánh | `So sánh [A] vs [B] — [tiêu chí]` | `So sánh Roborock vs Ecovacs — lực hút` |
| Ảnh infographic | `[Chủ đề infographic] — Xiaomi247` | `Cách chọn máy lọc không khí theo diện tích — Xiaomi247` |
| Screenshot | `[Mô tả screenshot]` | `Giao diện app Mi Home kết nối thiết bị` |

### 4.3 Quy trình Optimize ảnh trước khi upload

1. **Resize** ảnh về kích thước chuẩn (xem bảng trên)
2. **Compress** bằng tool: [TinyPNG](https://tinypng.com/) hoặc [Squoosh](https://squoosh.app/)
3. **Convert sang WebP** — giảm 25–35% dung lượng so với JPEG
4. **Đặt tên file** theo format: `[loai]-[ten-sp]-[chi-tiet].webp`
   - ✅ `tivi-xiaomi-a-pro-55-inch-mat-truoc.webp`
   - ❌ `IMG_20260101_123456.jpg`
5. **Upload** lên WordPress Media Library
6. **Nhập Alt Text** ngay khi upload

### 4.4 Plugin hỗ trợ (đã cài trên site)

| Plugin | Chức năng |
|--------|-----------|
| **ShortPixel** | Tự động compress + convert WebP khi upload |
| **Lazy Load** | Tải ảnh khi scroll đến (cải thiện page speed) |

---

## 5. INTERNAL LINKING CHECKLIST

### 5.1 Các loại internal link bắt buộc trong mỗi bài blog

| Loại link | Số lượng | Anchor text mẫu | Ví dụ URL |
|-----------|----------|-----------------|-----------|
| **Blog → Product Page** | 2–3 links | "Mua [Tên SP] chính hãng tại Xiaomi247" | `/tivi-xiaomi/a-pro-55-inch-4k/` |
| **Blog → Category Page** | 1 link | "Xem tất cả [danh mục] Xiaomi" | `/tivi-xiaomi/` |
| **Blog → Blog (related)** | 2–3 links | "Tham khảo: [Tiêu đề bài liên quan]" | `/blog/[slug-bai-lien-quan]/` |
| **Blog → Trang chủ** | 0–1 link | "xiaomi247.com" | `/` |

### 5.2 Quy tắc Internal Linking

| Quy tắc | Chi tiết |
|---------|----------|
| **Anchor text** | Chứa keyword, mô tả rõ trang đích — **KHÔNG** dùng "click vào đây" |
| **Vị trí** | Đặt trong nội dung (contextual), không chỉ sidebar/footer |
| **Số lượng** | Mỗi bài ít nhất **5 internal links** tổng cộng |
| **Dofollow** | Tất cả internal links đều dofollow (mặc định WordPress) |
| **Mới → Cũ** | Bài mới phải link về bài cũ liên quan |
| **Cũ → Mới** | Sau khi publish bài mới, **quay lại cập nhật** bài cũ thêm link đến bài mới |
| **Đa dạng** | Không dùng cùng 1 anchor text cho nhiều link khác nhau |

### 5.3 Breadcrumb

Breadcrumb tự động hiển thị qua Rank Math:

```
Trang chủ > Blog > [Tiêu đề bài viết]
```

**Kiểm tra:** Sau khi publish, xem bài viết và đảm bảo breadcrumb hiển thị đúng.

---

## 6. SOCIAL SHARING SETUP

### 6.1 Cấu hình Open Graph (OG Tags) qua Rank Math

Trong mỗi bài viết, vào **Rank Math → Tab Social:**

#### Facebook / Open Graph

| Field | Giá trị |
|-------|---------|
| **OG Title** | Giống SEO Title hoặc tiêu đề hấp dẫn hơn cho social |
| **OG Description** | 1–2 câu tóm tắt hấp dẫn, có emoji nếu phù hợp |
| **OG Image** | Upload ảnh **1200 × 630px** (dùng Featured Image) |

#### Twitter Cards

| Field | Giá trị |
|-------|---------|
| **Card Type** | Summary with Large Image |
| **Twitter Title** | Giống OG Title |
| **Twitter Description** | Giống OG Description |
| **Twitter Image** | Giống OG Image (1200 × 630px) |

### 6.2 Preview trước khi publish

Kiểm tra preview social sharing:
1. **Facebook:** Dùng [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)
2. **Twitter:** Dùng [Twitter Card Validator](https://cards-dev.twitter.com/validator)
3. Paste URL bài viết → kiểm tra title, description, image hiển thị đúng

### 6.3 Template OG Description cho Blog

```
Format: [Emoji] [Tóm tắt hấp dẫn 1-2 câu]. Đọc ngay tại Xiaomi247! 👉
```

**Ví dụ:**
- 📺 Top 5 tivi Xiaomi đáng mua nhất 2026 — từ 5 triệu đến 25 triệu. Xem ngay tại Xiaomi247! 👉
- 🤖 So sánh chi tiết Roborock vs Ecovacs vs Dreame — robot nào đáng tiền nhất? Đọc ngay! 👉

---

## 7. PRE-PUBLISH CHECKLIST

> ⚠️ **Kiểm tra TẤT CẢ các mục bên dưới trước khi nhấn Publish**

### ✅ Nội dung & Format

- [ ] Tiêu đề (H1) chứa keyword chính, ≤ 60 ký tự
- [ ] Heading hierarchy đúng (H1 → H2 → H3, không bỏ cấp)
- [ ] Keyword chính xuất hiện trong 100 từ đầu
- [ ] Keyword density 1–2% (tự nhiên, không nhồi)
- [ ] Nội dung ≥ 1,500 từ
- [ ] Đoạn văn ngắn (3–5 dòng/đoạn)
- [ ] Có Table of Contents cho bài dài
- [ ] Kiểm tra chính tả, ngữ pháp (đọc lại toàn bài)
- [ ] CTA rõ ràng ở cuối bài và trong nội dung

### ✅ SEO (Rank Math)

- [ ] Focus Keyword đã nhập
- [ ] SEO Title ≤ 60 ký tự, chứa keyword, có "Xiaomi247"
- [ ] Meta Description 120–155 ký tự, chứa keyword, có CTA
- [ ] Rank Math Score ≥ 80 (điểm xanh 🟢)
- [ ] Slug ngắn gọn, chứa keyword, không dấu

### ✅ Hình ảnh

- [ ] Featured Image 1200 × 630px, WebP, ≤ 200KB
- [ ] Mọi ảnh in-content có Alt Text
- [ ] Alt Text chứa keyword khi phù hợp
- [ ] Ảnh đã compress và convert WebP
- [ ] Tên file ảnh SEO-friendly (dấu gạch ngang, có keyword)
- [ ] 5–8 ảnh/bài (mỗi 300 từ 1 ảnh)

### ✅ Internal Links

- [ ] Ít nhất 2–3 links đến trang sản phẩm
- [ ] Ít nhất 1 link đến trang danh mục
- [ ] Ít nhất 2 links đến bài blog liên quan
- [ ] Anchor text chứa keyword, mô tả rõ ràng
- [ ] Không có broken links (kiểm tra tất cả links)

### ✅ Post Settings

- [ ] Category đã chọn đúng (1 category chính)
- [ ] Tags đã thêm (3–5 tags)
- [ ] Excerpt đã viết (25–30 từ, chứa keyword)
- [ ] Ngày publish đúng theo content calendar

### ✅ Social Sharing

- [ ] OG Title đã nhập (Rank Math → Social tab)
- [ ] OG Description đã nhập
- [ ] OG Image đã upload (1200 × 630px)
- [ ] Twitter Card đã cấu hình

### ✅ Mobile & Preview

- [ ] Preview Desktop — layout đẹp, ảnh hiển thị đúng
- [ ] Preview Mobile — responsive, text dễ đọc, ảnh không bị cắt
- [ ] Breadcrumb hiển thị đúng

**Tổng: 30 items — Phải đạt 100% trước khi Publish ✅**

---

## 8. POST-PUBLISH CHECKLIST

> ⏱️ **Thực hiện ngay sau khi bài viết được publish**

### Ngay sau publish (trong 1 giờ)

- [ ] **Submit URL lên Google Search Console:**
  1. Vào [Google Search Console](https://search.google.com/search-console)
  2. Nhập URL bài viết vào ô **URL Inspection**
  3. Click **Request Indexing**
- [ ] **Kiểm tra bài viết trên mobile:** Mở bài trên điện thoại, kiểm tra layout, ảnh, links
- [ ] **Kiểm tra 404:** Click tất cả internal links trong bài, đảm bảo không có link hỏng
- [ ] **Kiểm tra Schema:** Dùng [Google Rich Results Test](https://search.google.com/test/rich-results) — kiểm tra Article schema

### Chia sẻ Social Media (trong ngày)

- [ ] **Share Facebook Page:** Đăng bài kèm caption hấp dẫn + link
- [ ] **Share Zalo OA:** Gửi bài đến followers
- [ ] **Share nhóm Facebook** liên quan (nếu có)
- [ ] Kiểm tra OG preview trên Facebook (title, description, image đúng)

### Theo dõi sau 1 tuần

- [ ] **Google Search Console:** Kiểm tra bài đã được index chưa
- [ ] **Google Analytics:** Xem traffic, time on page, bounce rate
- [ ] **Rank Math:** Kiểm tra ranking cho focus keyword
- [ ] **Cập nhật bài cũ:** Thêm internal link từ bài cũ liên quan đến bài mới

### Theo dõi sau 1 tháng

- [ ] Kiểm tra ranking keyword trên GSC
- [ ] Đánh giá performance: pageviews, avg. time on page
- [ ] Cập nhật nội dung nếu cần (thêm thông tin mới, sửa giá)
- [ ] Tối ưu lại nếu chưa đạt top 10 (thêm content, cải thiện internal links)

---

## 9. CẤU HÌNH CỤ THỂ CHO 8 BÀI THÁNG 1

> **Nguồn dữ liệu:** [Content Calendar Tháng 1](../marketing/03-content-marketing/content-calendar-month1.md)
> **Nội dung bài:** [Blog Articles](../marketing/03-content-marketing/blog-articles/)

### Bài 1 — Top 5 Tivi Xiaomi Đáng Mua Nhất 2026

| Thuộc tính | Giá trị |
|-----------|---------|
| **Ngày publish** | Thứ 2, 01/01/2026 |
| **Slug** | `/blog/top-5-tivi-xiaomi-dang-mua-2026` |
| **Category** | Review & So sánh |
| **Tags** | `tivi-xiaomi`, `review`, `so-sanh`, `top-list`, `2026` |
| **Focus Keyword** | `tivi xiaomi đáng mua 2026` |
| **SEO Title** | `Top 5 Tivi Xiaomi Đáng Mua Nhất 2026 — Giá Rẻ Đến Cao Cấp | Xiaomi247` |
| **Meta Description** | `Khám phá top 5 tivi Xiaomi đáng mua nhất 2026 từ giá rẻ đến cao cấp. So sánh chi tiết cấu hình, chất lượng hình ảnh. Cập nhật mới nhất. Đọc ngay tại Xiaomi247!` (155 ký tự) |
| **Featured Image Alt** | `Top 5 tivi Xiaomi đáng mua nhất 2026 — Xiaomi247` |
| **Internal Links** | `/tivi-xiaomi/` · `/tivi-xiaomi/a-pro-55/` · `/tivi-xiaomi/55-inch/` · `/tivi-xiaomi/65-inch/` · `/blog/tivi-xiaomi-a-pro-vs-s-pro-mini-led` (Bài 6) |
| **CTA** | Xem giá & mua tivi Xiaomi chính hãng tại xiaomi247.com |
| **File nội dung** | `blog-articles/01-top-5-tivi-xiaomi-dang-mua-2026.md` |

---

### Bài 2 — So Sánh Roborock vs Ecovacs vs Dreame 2026

| Thuộc tính | Giá trị |
|-----------|---------|
| **Ngày publish** | Thứ 5, 04/01/2026 |
| **Slug** | `/blog/so-sanh-roborock-vs-ecovacs-vs-dreame-2026` |
| **Category** | Review & So sánh |
| **Tags** | `robot-hut-bui`, `so-sanh`, `roborock`, `ecovacs`, `dreame`, `2026` |
| **Focus Keyword** | `so sánh robot hút bụi 2026` |
| **SEO Title** | `So Sánh Roborock vs Ecovacs vs Dreame 2026 — Robot Nào Đáng Mua? | Xiaomi247` |
| **Meta Description** | `So sánh chi tiết Roborock, Ecovacs và Dreame 2026: lực hút, navigation, giá bán. Robot hút bụi nào đáng mua nhất? Cập nhật mới nhất. Đọc ngay tại Xiaomi247!` (152 ký tự) |
| **Featured Image Alt** | `So sánh robot hút bụi Roborock vs Ecovacs vs Dreame 2026 — Xiaomi247` |
| **Internal Links** | `/robot-hut-bui-xiaomi/` · `/robot-hut-bui-xiaomi/x10-plus/` · `/robot-hut-bui-xiaomi/s10-plus/` · `/blog/robot-hut-bui-nha-co-thu-cung` (Bài 5) |
| **CTA** | Xem bộ sưu tập robot hút bụi chính hãng tại xiaomi247.com |
| **File nội dung** | `blog-articles/02-so-sanh-roborock-vs-ecovacs-vs-dreame.md` |

---

### Bài 3 — Review Tủ Lạnh Xiaomi Mijia 430L

| Thuộc tính | Giá trị |
|-----------|---------|
| **Ngày publish** | Thứ 2, 08/01/2026 |
| **Slug** | `/blog/review-tu-lanh-xiaomi-mijia-430l` |
| **Category** | Review & So sánh |
| **Tags** | `tu-lanh-xiaomi`, `review`, `mijia-430l`, `tu-lanh-4-canh`, `2026` |
| **Focus Keyword** | `tủ lạnh xiaomi 430l review` |
| **SEO Title** | `Review Tủ Lạnh Xiaomi Mijia 430L — Có Đáng Mua Không? | Xiaomi247` |
| **Meta Description** | `Review chi tiết tủ lạnh Xiaomi Mijia 430L 4 cánh: thiết kế, công nghệ làm lạnh, tiết kiệm điện. Có đáng mua không? Cập nhật 2026. Đọc ngay tại Xiaomi247!` (150 ký tự) |
| **Featured Image Alt** | `Review tủ lạnh Xiaomi Mijia 430L 4 cánh — Xiaomi247` |
| **Internal Links** | `/tu-lanh-xiaomi/` · `/tu-lanh-xiaomi/4-canh/` · `/tu-lanh-xiaomi/side-by-side/` · `/blog/top-5-tivi-xiaomi-dang-mua-2026` (Bài 1 — cross-link) |
| **CTA** | Mua Tủ lạnh Xiaomi Mijia 430L chính hãng — Giao hàng toàn quốc |
| **File nội dung** | `blog-articles/03-review-tu-lanh-xiaomi-mijia-430l.md` |

---

### Bài 4 — Hướng Dẫn Chọn Máy Lọc Không Khí Theo Diện Tích

| Thuộc tính | Giá trị |
|-----------|---------|
| **Ngày publish** | Thứ 5, 11/01/2026 |
| **Slug** | `/blog/huong-dan-chon-may-loc-khong-khi-theo-dien-tich` |
| **Category** | Hướng dẫn |
| **Tags** | `may-loc-khong-khi`, `huong-dan`, `buying-guide`, `xiaomi-4-pro`, `2026` |
| **Focus Keyword** | `máy lọc không khí cho phòng bao nhiêu m2` |
| **SEO Title** | `Chọn Máy Lọc Không Khí Theo Diện Tích Phòng [2026] | Xiaomi247` |
| **Meta Description** | `Hướng dẫn chọn máy lọc không khí phù hợp diện tích phòng: 15m², 25m², 40m²+. So sánh Xiaomi 4 Lite, 4, 4 Pro. Cập nhật 2026. Đọc ngay tại Xiaomi247!` (148 ký tự) |
| **Featured Image Alt** | `Hướng dẫn chọn máy lọc không khí theo diện tích phòng — Xiaomi247` |
| **Internal Links** | `/may-loc-khong-khi-xiaomi/` · `/may-loc-khong-khi-xiaomi/4-pro/` · `/may-loc-khong-khi-xiaomi/4-lite/` · `/blog/huong-dan-ket-noi-xiaomi-smart-home` (Bài 8) |
| **CTA** | Xem máy lọc không khí Xiaomi — Giá tốt nhất tại xiaomi247.com |
| **File nội dung** | `blog-articles/04-huong-dan-chon-may-loc-khong-khi.md` |

---

### Bài 5 — Robot Hút Bụi Nhà Có Thú Cưng

| Thuộc tính | Giá trị |
|-----------|---------|
| **Ngày publish** | Thứ 2, 15/01/2026 |
| **Slug** | `/blog/robot-hut-bui-nha-co-thu-cung` |
| **Category** | Hướng dẫn |
| **Tags** | `robot-hut-bui`, `thu-cung`, `buying-guide`, `top-list`, `2026` |
| **Focus Keyword** | `robot hút bụi nhà có thú cưng` |
| **SEO Title** | `Robot Hút Bụi Cho Nhà Có Thú Cưng — Top 5 Lựa Chọn 2026 | Xiaomi247` |
| **Meta Description** | `Top 5 robot hút bụi tốt nhất cho nhà có thú cưng 2026. Hút sạch lông chó mèo, lực hút mạnh, chổi chống rối. So sánh chi tiết. Đọc ngay tại Xiaomi247!` (149 ký tự) |
| **Featured Image Alt** | `Robot hút bụi cho nhà có thú cưng — top 5 lựa chọn 2026 — Xiaomi247` |
| **Internal Links** | `/robot-hut-bui-xiaomi/` · `/robot-hut-bui-xiaomi/x10-plus/` · `/phu-kien/robot-hut-bui/` · `/blog/so-sanh-roborock-vs-ecovacs-vs-dreame-2026` (Bài 2) |
| **CTA** | Xem robot hút bụi Xiaomi cho nhà có thú cưng tại xiaomi247.com |
| **File nội dung** | `blog-articles/05-robot-hut-bui-nha-co-thu-cung.md` |

---

### Bài 6 — Tivi Xiaomi A Pro vs S Pro Mini LED

| Thuộc tính | Giá trị |
|-----------|---------|
| **Ngày publish** | Thứ 5, 18/01/2026 |
| **Slug** | `/blog/tivi-xiaomi-a-pro-vs-s-pro-mini-led` |
| **Category** | Review & So sánh |
| **Tags** | `tivi-xiaomi`, `so-sanh`, `a-pro`, `s-pro-mini-led`, `2026` |
| **Focus Keyword** | `xiaomi a pro vs s pro` |
| **SEO Title** | `Tivi Xiaomi A Pro vs S Pro Mini LED — Nên Chọn Dòng Nào? | Xiaomi247` |
| **Meta Description** | `So sánh tivi Xiaomi A Pro và S Pro Mini LED: chất lượng hình ảnh, âm thanh, giá bán. Nên chọn dòng nào phù hợp? Cập nhật 2026. Đọc ngay tại Xiaomi247!` (149 ký tự) |
| **Featured Image Alt** | `So sánh tivi Xiaomi A Pro vs S Pro Mini LED — Xiaomi247` |
| **Internal Links** | `/tivi-xiaomi/` · `/tivi-xiaomi/a-pro-55/` · `/tivi-xiaomi/55-inch/` · `/tivi-xiaomi/65-inch/` · `/blog/top-5-tivi-xiaomi-dang-mua-2026` (Bài 1) |
| **CTA** | Mua Tivi Xiaomi chính hãng — Trả góp 0% tại xiaomi247.com |
| **File nội dung** | `blog-articles/06-tivi-xiaomi-a-pro-vs-s-pro-mini-led.md` |

---

### Bài 7 — Top Máy Hút Ẩm Dưới 5 Triệu

| Thuộc tính | Giá trị |
|-----------|---------|
| **Ngày publish** | Thứ 2, 22/01/2026 |
| **Slug** | `/blog/top-may-hut-am-duoi-5-trieu-2026` |
| **Category** | Review & So sánh |
| **Tags** | `may-hut-am`, `review`, `top-list`, `gia-re`, `mua-nom`, `2026` |
| **Focus Keyword** | `máy hút ẩm dưới 5 triệu` |
| **SEO Title** | `Top Máy Hút Ẩm Dưới 5 Triệu Cho Mùa Nồm 2026 | Xiaomi247` |
| **Meta Description** | `Top máy hút ẩm dưới 5 triệu tốt nhất cho mùa nồm 2026. So sánh Xiaomi Mijia 13L, 22L và các model giá rẻ. Chọn máy nào? Đọc ngay tại Xiaomi247!` (147 ký tự) |
| **Featured Image Alt** | `Top máy hút ẩm dưới 5 triệu cho mùa nồm 2026 — Xiaomi247` |
| **Internal Links** | `/may-hut-am-xiaomi/` · `/gia-dung-xiaomi/` · `/may-loc-khong-khi-xiaomi/` · `/blog/huong-dan-chon-may-loc-khong-khi-theo-dien-tich` (Bài 4) |
| **CTA** | Mua máy hút ẩm Xiaomi chính hãng — Giá tốt tại xiaomi247.com |
| **File nội dung** | `blog-articles/07-top-may-hut-am-duoi-5-trieu.md` |

---

### Bài 8 — Hướng Dẫn Kết Nối Xiaomi Smart Home

| Thuộc tính | Giá trị |
|-----------|---------|
| **Ngày publish** | Thứ 5, 25/01/2026 |
| **Slug** | `/blog/huong-dan-ket-noi-xiaomi-smart-home` |
| **Category** | Hướng dẫn |
| **Tags** | `smart-home`, `huong-dan`, `tutorial`, `mi-home`, `ket-noi`, `2026` |
| **Focus Keyword** | `kết nối nhà thông minh xiaomi` |
| **SEO Title** | `Hướng Dẫn Kết Nối Thiết Bị Xiaomi Smart Home Từ A–Z | Xiaomi247` |
| **Meta Description** | `Hướng dẫn kết nối thiết bị Xiaomi Smart Home từ A–Z: cài app Mi Home, thêm thiết bị, tạo automation. Dễ hiểu cho người mới. Đọc ngay tại Xiaomi247!` (148 ký tự) |
| **Featured Image Alt** | `Hướng dẫn kết nối thiết bị Xiaomi Smart Home — Xiaomi247` |
| **Internal Links** | `/gia-dung-xiaomi/` · `/robot-hut-bui-xiaomi/` · `/may-loc-khong-khi-xiaomi/` · `/blog/huong-dan-chon-may-loc-khong-khi-theo-dien-tich` (Bài 4) · `/blog/robot-hut-bui-nha-co-thu-cung` (Bài 5) |
| **CTA** | Xem trọn bộ thiết bị Xiaomi Smart Home tại xiaomi247.com |
| **File nội dung** | `blog-articles/08-huong-dan-ket-noi-xiaomi-smart-home.md` |

---

## BẢNG TỔNG HỢP 8 BÀI THÁNG 1

| # | Bài viết | Slug | Category | Focus Keyword | Ngày publish |
|---|---------|------|----------|---------------|-------------|
| 1 | Top 5 Tivi Xiaomi Đáng Mua 2026 | `top-5-tivi-xiaomi-dang-mua-2026` | Review & So sánh | tivi xiaomi đáng mua 2026 | 01/01 |
| 2 | So Sánh Roborock vs Ecovacs vs Dreame | `so-sanh-roborock-vs-ecovacs-vs-dreame-2026` | Review & So sánh | so sánh robot hút bụi 2026 | 04/01 |
| 3 | Review Tủ Lạnh Xiaomi Mijia 430L | `review-tu-lanh-xiaomi-mijia-430l` | Review & So sánh | tủ lạnh xiaomi 430l review | 08/01 |
| 4 | Chọn Máy Lọc KK Theo Diện Tích | `huong-dan-chon-may-loc-khong-khi-theo-dien-tich` | Hướng dẫn | máy lọc không khí cho phòng bao nhiêu m2 | 11/01 |
| 5 | Robot Hút Bụi Nhà Có Thú Cưng | `robot-hut-bui-nha-co-thu-cung` | Hướng dẫn | robot hút bụi nhà có thú cưng | 15/01 |
| 6 | Tivi A Pro vs S Pro Mini LED | `tivi-xiaomi-a-pro-vs-s-pro-mini-led` | Review & So sánh | xiaomi a pro vs s pro | 18/01 |
| 7 | Top Máy Hút Ẩm Dưới 5 Triệu | `top-may-hut-am-duoi-5-trieu-2026` | Review & So sánh | máy hút ẩm dưới 5 triệu | 22/01 |
| 8 | Kết Nối Xiaomi Smart Home | `huong-dan-ket-noi-xiaomi-smart-home` | Hướng dẫn | kết nối nhà thông minh xiaomi | 25/01 |

---

> **Tài liệu tham chiếu:**
> - [Content Calendar Tháng 1](../marketing/03-content-marketing/content-calendar-month1.md) — Lịch & metadata 8 bài
> - [Blog Articles](../marketing/03-content-marketing/blog-articles/) — Nội dung 8 bài sẵn sàng
> - [On-page SEO Templates](../seo-impl/03-onpage-seo-templates.md) — Title/meta templates
> - [Content Strategy](../marketing/03-content-marketing/content-strategy.md) — 4 content pillars, personas
> - [Schema Markup](../seo-impl/02-schema-markup.md) — Article schema cho blog

