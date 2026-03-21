# XIAOMI247.COM — HƯỚNG DẪN TRIỂN KHAI SCHEMA.ORG STRUCTURED DATA

> **Nền tảng:** WordPress + WooCommerce + Rank Math SEO
> **Áp dụng cho:** Tất cả trang trên xiaomi247.com
> **Mục tiêu:** Rich snippets trên Google SERP, tăng CTR 20–30%
> **Cập nhật:** Tháng 3/2026

---

## MỤC LỤC

1. [Tổng quan Schema.org](#1-tổng-quan-schemaorg)
2. [Schema Organization — Trang chủ](#2-schema-organization--trang-chủ)
3. [Schema Product — Trang sản phẩm](#3-schema-product--trang-sản-phẩm)
4. [Schema BreadcrumbList — Tất cả trang](#4-schema-breadcrumblist--tất-cả-trang)
5. [Schema FAQPage — Trang danh mục & Blog](#5-schema-faqpage--trang-danh-mục--blog)
6. [Schema Article/BlogPosting — Trang blog](#6-schema-articleblogposting--trang-blog)
7. [Schema LocalBusiness — Showroom](#7-schema-localbusiness--showroom)
8. [Cấu hình qua Rank Math](#8-cấu-hình-qua-rank-math)
9. [Testing & Validation](#9-testing--validation)
10. [Checklist triển khai](#10-checklist-triển-khai)

---

## 1. TỔNG QUAN SCHEMA.ORG

### Schema.org là gì?

Schema.org là bộ từ vựng chuẩn (vocabulary) được Google, Bing, Yahoo và Yandex cùng phát triển, giúp các công cụ tìm kiếm **hiểu rõ nội dung trang web**. Khi triển khai Schema markup dưới dạng JSON-LD, Google có thể hiển thị **rich snippets** (kết quả tìm kiếm nâng cao) với thông tin bổ sung như giá, đánh giá sao, FAQ, breadcrumb...

### Lợi ích cho xiaomi247.com

| Lợi ích | Chi tiết |
|---------|---------|
| **Rich Snippets** | Hiển thị giá, rating ⭐, tình trạng kho trên SERP |
| **Tăng CTR** | Rich results có CTR cao hơn 20–30% so với kết quả thường |
| **FAQ trên SERP** | Chiếm thêm không gian trên trang kết quả tìm kiếm |
| **Breadcrumb** | Hiển thị đường dẫn rõ ràng thay vì URL dài |
| **Knowledge Panel** | Thông tin doanh nghiệp hiển thị bên phải SERP |
| **Voice Search** | Structured data giúp Google trả lời voice search chính xác hơn |

### Các loại Schema cần triển khai

| Schema Type | Áp dụng cho | Rich Result |
|-------------|-------------|-------------|
| `Organization` | Trang chủ | Knowledge Panel, logo trên SERP |
| `Product` | Trang sản phẩm | Giá, rating, availability |
| `BreadcrumbList` | Tất cả trang | Breadcrumb navigation trên SERP |
| `FAQPage` | Danh mục + Blog | FAQ accordion trên SERP |
| `Article/BlogPosting` | Trang blog | Ngày đăng, tác giả, hình ảnh |
| `LocalBusiness` | Trang liên hệ | Địa chỉ, giờ mở cửa, bản đồ |

### Phương pháp triển khai: JSON-LD

Google **khuyến nghị JSON-LD** (JavaScript Object Notation for Linked Data) vì:
- Không ảnh hưởng đến HTML markup
- Dễ thêm/sửa/xóa mà không cần chỉnh template
- Rank Math hỗ trợ tự động generate JSON-LD
- Có thể đặt trong `<head>` hoặc `<body>`

---

## 2. SCHEMA ORGANIZATION — TRANG CHỦ

### Mục đích
Khai báo thông tin doanh nghiệp cho Google Knowledge Panel. Schema này chỉ cần đặt trên **trang chủ**.

### JSON-LD hoàn chỉnh

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Xiaomi247",
  "alternateName": "Xiaomi247.com — Đại lý Xiaomi chính hãng",
  "url": "https://xiaomi247.com",
  "logo": {
    "@type": "ImageObject",
    "url": "https://xiaomi247.com/wp-content/uploads/logo-xiaomi247.png",
    "width": 600,
    "height": 60
  },
  "description": "Xiaomi247 — Đại lý phân phối sản phẩm Xiaomi chính hãng tại Việt Nam. Tivi, Robot hút bụi, Tủ lạnh, Máy lọc không khí, Máy hút ẩm và gia dụng thông minh.",
  "foundingDate": "2024",
  "contactPoint": [
    {
      "@type": "ContactPoint",
      "telephone": "+84-xxx-xxx-xxx",
      "contactType": "customer service",
      "areaServed": "VN",
      "availableLanguage": "Vietnamese",
      "hoursAvailable": {
        "@type": "OpeningHoursSpecification",
        "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"],
        "opens": "08:00",
        "closes": "21:00"
      }
    },
    {
      "@type": "ContactPoint",
      "telephone": "+84-xxx-xxx-xxx",
      "contactType": "sales",
      "areaServed": "VN",
      "availableLanguage": "Vietnamese"
    }
  ],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Địa chỉ cụ thể]",
    "addressLocality": "Hồ Chí Minh",
    "addressRegion": "HCM",
    "postalCode": "700000",
    "addressCountry": "VN"
  },
  "sameAs": [
    "https://www.facebook.com/xiaomi247",
    "https://www.youtube.com/@xiaomi247",
    "https://www.tiktok.com/@xiaomi247",
    "https://zalo.me/xiaomi247",
    "https://shopee.vn/xiaomi247"
  ]
}
```

### Cấu hình qua Rank Math

1. Vào **Rank Math → Titles & Meta → Local SEO**
2. Chọn **Organization** (không phải Person)
3. Điền đầy đủ: Name, Logo, URL, Phone, Address
4. Thêm social profiles tại **Rank Math → Titles & Meta → Social**
5. Rank Math sẽ tự động generate JSON-LD Organization trên trang chủ

> **Lưu ý:** Nếu Rank Math không hỗ trợ đầy đủ các trường (ví dụ `hoursAvailable`), sử dụng **Rank Math → Schema → Custom Schema** hoặc thêm JSON-LD thủ công qua plugin **Insert Headers and Footers**.

---

## 3. SCHEMA PRODUCT — TRANG SẢN PHẨM

### Mục đích
Hiển thị **giá, rating, tình trạng kho** trên Google SERP. Đây là schema quan trọng nhất cho e-commerce.

### JSON-LD hoàn chỉnh (Ví dụ: Tivi Xiaomi A Pro 55 inch)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Tivi Xiaomi A Pro 55 inch 4K Google TV",
  "image": [
    "https://xiaomi247.com/wp-content/uploads/tivi-xiaomi-a-pro-55-inch-mat-truoc.webp",
    "https://xiaomi247.com/wp-content/uploads/tivi-xiaomi-a-pro-55-inch-mat-sau.webp",
    "https://xiaomi247.com/wp-content/uploads/tivi-xiaomi-a-pro-55-inch-remote.webp"
  ],
  "description": "Tivi Xiaomi A Pro 55 inch 4K — Màn hình 4K UHD, Google TV, Dolby Vision & Atmos, viền siêu mỏng. Chính hãng Xiaomi, bảo hành 24 tháng tại Xiaomi247.",
  "sku": "TV-XM-APRO55-4K",
  "mpn": "L55M8-A2SEA",
  "brand": {
    "@type": "Brand",
    "name": "Xiaomi"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://xiaomi247.com/tivi-xiaomi/a-pro-55-inch-4k/",
    "price": "8990000",
    "priceCurrency": "VND",
    "priceValidUntil": "2026-12-31",
    "availability": "https://schema.org/InStock",
    "itemCondition": "https://schema.org/NewCondition",
    "seller": {
      "@type": "Organization",
      "name": "Xiaomi247",
      "url": "https://xiaomi247.com"
    },
    "shippingDetails": {
      "@type": "OfferShippingDetails",
      "shippingRate": {
        "@type": "MonetaryAmount",
        "value": "0",
        "currency": "VND"
      },
      "shippingDestination": {
        "@type": "DefinedRegion",
        "addressCountry": "VN"
      },
      "deliveryTime": {
        "@type": "ShippingDeliveryTime",
        "handlingTime": {
          "@type": "QuantitativeValue",
          "minValue": "0",
          "maxValue": "1",
          "unitCode": "DAY"
        },
        "transitTime": {
          "@type": "QuantitativeValue",
          "minValue": "1",
          "maxValue": "3",
          "unitCode": "DAY"
        }
      }
    },
    "hasMerchantReturnPolicy": {
      "@type": "MerchantReturnPolicy",
      "applicableCountry": "VN",
      "returnPolicyCategory": "https://schema.org/MerchantReturnFiniteReturnWindow",
      "merchantReturnDays": "7",
      "returnMethod": "https://schema.org/ReturnByMail",
      "returnFees": "https://schema.org/FreeReturn"
    }
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.7",
    "bestRating": "5",
    "worstRating": "1",
    "ratingCount": "156",
    "reviewCount": "89"
  },
  "review": [
    {
      "@type": "Review",
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "5",
        "bestRating": "5"
      },
      "author": {
        "@type": "Person",
        "name": "Nguyễn Văn A"
      },
      "datePublished": "2026-02-15",
      "reviewBody": "Tivi chất lượng hình ảnh rất tốt, Google TV mượt mà. Giá hợp lý so với Samsung cùng phân khúc. Giao hàng nhanh, đóng gói cẩn thận."
    }
  ]
}
```

### Cấu hình qua Rank Math + WooCommerce

Rank Math tự động tạo Schema Product cho sản phẩm WooCommerce. Để đảm bảo đầy đủ:

1. **Rank Math → General Settings → WooCommerce**
   - Bật **"Add SEO Controls for Products"**
   - Bật **"Remove WooCommerce Schema"** (để Rank Math quản lý schema, tránh trùng lặp)

2. **Trong mỗi sản phẩm WooCommerce:**
   - Điền đầy đủ: Tên, Mô tả, Giá, SKU, Hình ảnh (tối thiểu 3 ảnh)
   - Tab **Rank Math → Schema**: Kiểm tra Product schema đã tự động generate
   - Thêm **Brand** = "Xiaomi" (cài plugin "Perfect Brands for WooCommerce" hoặc dùng Rank Math custom field)

3. **Aggregate Rating & Reviews:**
   - WooCommerce reviews tự động map sang `aggregateRating` và `review`
   - Bật reviews: **WooCommerce → Settings → Products → Enable reviews**
   - Khuyến khích khách đánh giá sau mua hàng

4. **Các trường bổ sung (thêm qua Rank Math Custom Schema):**
   - `shippingDetails` — thông tin vận chuyển miễn phí
   - `hasMerchantReturnPolicy` — chính sách đổi trả
   - `mpn` — mã sản phẩm nhà sản xuất

> **Quan trọng:** Giá trong schema **phải khớp** với giá hiển thị trên trang. Google sẽ phạt nếu phát hiện sai lệch.

---

## 4. SCHEMA BREADCRUMBLIST — TẤT CẢ TRANG

### Mục đích
Hiển thị **đường dẫn breadcrumb** trên SERP thay vì URL dài. Giúp người dùng hiểu cấu trúc site.

### JSON-LD — Trang sản phẩm (3 cấp)

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Trang chủ",
      "item": "https://xiaomi247.com/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Tivi Xiaomi",
      "item": "https://xiaomi247.com/tivi-xiaomi/"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Tivi Xiaomi A Pro 55 inch 4K"
    }
  ]
}
```

### JSON-LD — Trang danh mục (2 cấp)

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Trang chủ",
      "item": "https://xiaomi247.com/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Robot hút bụi Xiaomi"
    }
  ]
}
```

### JSON-LD — Trang blog (3 cấp)

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Trang chủ",
      "item": "https://xiaomi247.com/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Blog",
      "item": "https://xiaomi247.com/blog/"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Tivi Xiaomi có tốt không? Đánh giá thật 2026"
    }
  ]
}
```

### Cấu hình qua Rank Math

1. **Rank Math → General Settings → Breadcrumbs**
   - Bật **"Enable Breadcrumbs"**
   - Separator: `>`
   - Home Label: `Trang chủ`
   - Home Link: `https://xiaomi247.com/`
   - Bật **"Show Breadcrumbs on Front Page"**: Tắt
2. Rank Math tự động thêm Schema BreadcrumbList cho mọi trang
3. Thêm breadcrumb vào theme: dùng shortcode `[rank_math_breadcrumb]` hoặc function `rank_math_the_breadcrumbs()`

> **Lưu ý:** Item cuối cùng trong breadcrumb (trang hiện tại) **không có trường `item`** — đây là chuẩn schema.org.

---

## 5. SCHEMA FAQPAGE — TRANG DANH MỤC & BLOG

### Mục đích
Hiển thị **FAQ accordion** trên SERP, chiếm thêm không gian và tăng CTR đáng kể.

### FAQ mẫu theo danh mục

#### 5.1. Tivi Xiaomi (`/tivi-xiaomi/`)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Tivi Xiaomi có tốt không?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Tivi Xiaomi được đánh giá cao về chất lượng hình ảnh 4K sắc nét, hệ điều hành Google TV mượt mà với kho ứng dụng phong phú, và mức giá cạnh tranh hơn 30-40% so với Samsung, LG cùng phân khúc. Xiaomi247 phân phối chính hãng với bảo hành 24 tháng."
      }
    },
    {
      "@type": "Question",
      "name": "Tivi Xiaomi giá bao nhiêu?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Giá tivi Xiaomi tại Xiaomi247 dao động từ 3.990.000đ (32 inch) đến 24.990.000đ (75 inch 4K). Dòng bán chạy nhất là Xiaomi A Pro 55 inch 4K giá 8.990.000đ. Hỗ trợ trả góp 0% lãi suất."
      }
    },
    {
      "@type": "Question",
      "name": "Nên mua tivi Xiaomi kích thước nào?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Chọn kích thước tivi dựa trên khoảng cách xem: phòng nhỏ (2-3m) chọn 32-43 inch, phòng trung bình (3-4m) chọn 50-55 inch, phòng lớn (4m+) chọn 65-75 inch. Dòng Xiaomi A Pro 55 inch phù hợp đa số phòng khách Việt Nam."
      }
    },
    {
      "@type": "Question",
      "name": "Mua tivi Xiaomi chính hãng ở đâu uy tín?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Xiaomi247.com là đại lý phân phối Xiaomi chính hãng tại Việt Nam. Cam kết 100% hàng chính hãng, bảo hành 24 tháng, giao hàng miễn phí toàn quốc, hỗ trợ trả góp 0%."
      }
    },
    {
      "@type": "Question",
      "name": "Tivi Xiaomi có hỗ trợ tiếng Việt không?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Có, tất cả tivi Xiaomi bán tại Xiaomi247 đều hỗ trợ đầy đủ tiếng Việt trên giao diện Google TV, điều khiển giọng nói tiếng Việt qua Google Assistant, và remote có phím tắt YouTube/Netflix."
      }
    }
  ]
}
```

#### 5.2. Robot hút bụi Xiaomi (`/robot-hut-bui-xiaomi/`)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Robot hút bụi Xiaomi có tốt không?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Robot hút bụi Xiaomi được đánh giá tốt với lực hút mạnh lên đến 5000Pa, hệ thống navigation LiDAR chính xác, và app Mi Home điều khiển thông minh. Dòng X10+ có thêm dock tự đổ rác, tự giặt giẻ lau. Giá cạnh tranh hơn Roborock, Ecovacs cùng tính năng."
      }
    },
    {
      "@type": "Question",
      "name": "Robot hút bụi Xiaomi giá bao nhiêu?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Giá robot hút bụi Xiaomi tại Xiaomi247 từ 3.990.000đ (dòng cơ bản) đến 15.990.000đ (dòng cao cấp tự đổ rác). Dòng bán chạy nhất là Xiaomi X10+ giá 12.990.000đ. Hỗ trợ trả góp 0%."
      }
    },
    {
      "@type": "Question",
      "name": "Robot Xiaomi có lau nhà được không?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Có, hầu hết robot Xiaomi đời mới đều tích hợp chức năng hút bụi + lau nhà 2 trong 1. Dòng X10+ và S10+ có khả năng lau rung tần số cao, tự giặt giẻ lau, cho sàn sạch bóng."
      }
    },
    {
      "@type": "Question",
      "name": "Nên chọn robot hút bụi Xiaomi nào?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Căn hộ nhỏ (<60m²): chọn Xiaomi Vacuum Mop 2 (giá tốt). Căn hộ trung bình (60-100m²): chọn Xiaomi S10+. Nhà rộng (>100m²) hoặc có thú cưng: chọn Xiaomi X10+ với dock tự đổ rác."
      }
    }
  ]
}
```

#### 5.3. Tủ lạnh Xiaomi (`/tu-lanh-xiaomi/`)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Tủ lạnh Xiaomi có tốt không?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Tủ lạnh Xiaomi sử dụng công nghệ Inverter tiết kiệm điện, khử mùi ion bạc, và thiết kế hiện đại. Dung tích đa dạng từ 160L đến 600L. Giá rẻ hơn 20-30% so với Samsung, Hitachi cùng dung tích. Bảo hành máy nén 10 năm."
      }
    },
    {
      "@type": "Question",
      "name": "Tủ lạnh Xiaomi giá bao nhiêu?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Giá tủ lạnh Xiaomi tại Xiaomi247 từ 4.990.000đ (2 cánh 160L) đến 16.990.000đ (4 cánh 600L side-by-side). Hỗ trợ trả góp 0%, giao hàng miễn phí và lắp đặt tận nơi."
      }
    },
    {
      "@type": "Question",
      "name": "Tủ lạnh Xiaomi có tiết kiệm điện không?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Có, tủ lạnh Xiaomi sử dụng máy nén Inverter tiết kiệm đến 40% điện năng so với tủ lạnh thường. Đạt tiêu chuẩn năng lượng 5 sao, chi phí điện chỉ khoảng 30.000-50.000đ/tháng."
      }
    }
  ]
}
```

#### 5.4. Máy lọc không khí Xiaomi (`/may-loc-khong-khi-xiaomi/`)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Máy lọc không khí Xiaomi có tốt không?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Máy lọc không khí Xiaomi sử dụng màng lọc HEPA H13 lọc 99.97% bụi mịn PM2.5, vi khuẩn, phấn hoa. Tích hợp cảm biến chất lượng không khí real-time, điều khiển qua app Mi Home. Dòng 4 Pro phù hợp phòng đến 60m²."
      }
    },
    {
      "@type": "Question",
      "name": "Nên chọn máy lọc không khí Xiaomi 4 Pro hay 4 Lite?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Xiaomi 4 Pro (giá ~3.990.000đ) phù hợp phòng 35-60m², có màn hình OLED hiển thị chất lượng không khí. Xiaomi 4 Lite (giá ~2.490.000đ) phù hợp phòng 25-43m², thiết kế nhỏ gọn hơn. Cả hai đều dùng màng lọc HEPA H13."
      }
    },
    {
      "@type": "Question",
      "name": "Bao lâu thay màng lọc máy lọc không khí Xiaomi?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Thay màng lọc mỗi 6-12 tháng tùy mức độ ô nhiễm. App Mi Home sẽ thông báo khi cần thay. Giá màng lọc thay thế từ 350.000-500.000đ, mua chính hãng tại Xiaomi247."
      }
    }
  ]
}
```

#### 5.5. Máy hút ẩm Xiaomi (`/may-hut-am-xiaomi/`)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Máy hút ẩm Xiaomi có tốt không?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Máy hút ẩm Xiaomi hoạt động hiệu quả với công suất hút ẩm 12-22L/ngày, phù hợp phòng 20-50m². Tích hợp cảm biến độ ẩm tự động, điều khiển qua app Mi Home, và chế độ sấy quần áo. Tiết kiệm điện hơn so với Sharp, Panasonic cùng công suất."
      }
    },
    {
      "@type": "Question",
      "name": "Máy hút ẩm Xiaomi giá bao nhiêu?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Giá máy hút ẩm Xiaomi tại Xiaomi247 từ 3.490.000đ đến 5.990.000đ. Rẻ hơn 20-30% so với Sharp, Panasonic cùng công suất. Giao hàng miễn phí, bảo hành 12 tháng chính hãng."
      }
    },
    {
      "@type": "Question",
      "name": "Khi nào cần dùng máy hút ẩm?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Nên dùng máy hút ẩm khi độ ẩm phòng trên 70% (kiểm tra qua app Mi Home hoặc ẩm kế). Đặc biệt cần thiết vào mùa mưa, mùa nồm ẩm (tháng 2-4 ở miền Bắc), phòng có trẻ nhỏ hoặc người bị dị ứng."
      }
    }
  ]
}
```


### Cấu hình FAQ Schema qua Rank Math

1. **Cách 1 — Rank Math FAQ Block (Gutenberg):**
   - Trong editor bài viết/trang, thêm block **"FAQ by Rank Math"**
   - Nhập câu hỏi và câu trả lời
   - Rank Math tự động generate FAQPage schema
   - **Ưu điểm:** Dễ dùng, FAQ hiển thị cả trên trang lẫn SERP

2. **Cách 2 — Rank Math Custom Schema:**
   - Vào tab **Rank Math → Schema** trong editor
   - Click **"Add Schema"** → chọn **"FAQ"**
   - Nhập các cặp Q&A
   - **Ưu điểm:** Linh hoạt hơn, có thể thêm FAQ schema mà không hiển thị trên trang

3. **Cách 3 — JSON-LD thủ công (cho trang danh mục WooCommerce):**
   - Thêm code vào `functions.php` hoặc plugin custom:

```php
// Thêm FAQ Schema cho trang danh mục WooCommerce
add_action('wp_head', 'xiaomi247_category_faq_schema');
function xiaomi247_category_faq_schema() {
    if (!is_product_category()) return;

    $term = get_queried_object();
    $faq_data = get_term_meta($term->term_id, '_faq_schema', true);

    if (empty($faq_data)) return;

    echo '<script type="application/ld+json">' . wp_json_encode($faq_data) . '</script>';
}
```

> **Lưu ý:** Google có thể không hiển thị FAQ rich results cho tất cả trang. Ưu tiên thêm FAQ cho các trang danh mục chính và bài blog quan trọng.

---

## 6. SCHEMA ARTICLE/BLOGPOSTING — TRANG BLOG

### Mục đích
Giúp Google hiểu nội dung bài viết, hiển thị **ngày đăng, tác giả, hình ảnh** trên SERP.

### JSON-LD hoàn chỉnh

```json
{
  "@context": "https://schema.org",
  "@type": "BlogPosting",
  "headline": "Tivi Xiaomi có tốt không? Đánh giá thật sau 1 năm sử dụng — 2026",
  "description": "Đánh giá chi tiết tivi Xiaomi sau 1 năm sử dụng thực tế. Chất lượng hình ảnh, âm thanh, Google TV, độ bền và so sánh với Samsung, LG cùng tầm giá.",
  "image": [
    "https://xiaomi247.com/wp-content/uploads/tivi-xiaomi-danh-gia-2026.webp"
  ],
  "author": {
    "@type": "Person",
    "name": "Xiaomi247 Team",
    "url": "https://xiaomi247.com/tac-gia/xiaomi247-team/"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Xiaomi247",
    "logo": {
      "@type": "ImageObject",
      "url": "https://xiaomi247.com/wp-content/uploads/logo-xiaomi247.png",
      "width": 600,
      "height": 60
    }
  },
  "datePublished": "2026-01-15T08:00:00+07:00",
  "dateModified": "2026-03-10T10:30:00+07:00",
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://xiaomi247.com/blog/tivi-xiaomi-co-tot-khong/"
  },
  "wordCount": "2500",
  "articleSection": "Đánh giá sản phẩm",
  "keywords": ["tivi xiaomi có tốt không", "đánh giá tivi xiaomi", "review tivi xiaomi 2026"]
}
```

### Cấu hình qua Rank Math

Rank Math **tự động** tạo Article/BlogPosting schema cho bài viết WordPress. Đảm bảo:

1. **Rank Math → Titles & Meta → Posts:**
   - Schema Type: **Article** (mặc định)
   - Article Type: **Blog Post**

2. **Trong mỗi bài viết:**
   - Điền đầy đủ: Tiêu đề, Excerpt, Featured Image
   - Đặt Author (tạo profile tác giả đầy đủ trong WordPress Users)
   - Rank Math tự động lấy `datePublished` và `dateModified` từ WordPress

3. **Tối ưu thêm:**
   - Thêm **Featured Image** chất lượng cao (tối thiểu 1200×630px)
   - Viết **Excerpt** chứa keyword (dùng làm `description` trong schema)
   - Cập nhật bài viết định kỳ để `dateModified` luôn mới

---

## 7. SCHEMA LOCALBUSINESS — SHOWROOM (SẴN SÀNG KHI MỞ)

### Mục đích
Khi xiaomi247.com mở showroom vật lý, Schema LocalBusiness giúp hiển thị trên **Google Maps, Knowledge Panel** với địa chỉ, giờ mở cửa, đánh giá.

### JSON-LD mẫu (cập nhật thông tin thực khi mở showroom)

```json
{
  "@context": "https://schema.org",
  "@type": "ElectronicsStore",
  "name": "Xiaomi247 — Showroom Xiaomi chính hãng",
  "image": "https://xiaomi247.com/wp-content/uploads/showroom-xiaomi247.webp",
  "url": "https://xiaomi247.com",
  "@id": "https://xiaomi247.com/#localbusiness",
  "telephone": "+84-xxx-xxx-xxx",
  "priceRange": "₫₫",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Số nhà, Tên đường]",
    "addressLocality": "Hồ Chí Minh",
    "addressRegion": "HCM",
    "postalCode": "700000",
    "addressCountry": "VN"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "10.xxxx",
    "longitude": "106.xxxx"
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "08:30",
      "closes": "21:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Saturday", "Sunday"],
      "opens": "09:00",
      "closes": "21:00"
    }
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "bestRating": "5",
    "ratingCount": "250"
  },
  "sameAs": [
    "https://www.facebook.com/xiaomi247",
    "https://www.google.com/maps/place/xiaomi247"
  ]
}
```

### Khi nào triển khai
- **Hiện tại:** Chưa cần (chưa có showroom vật lý)
- **Khi mở showroom:** Cập nhật địa chỉ, tọa độ GPS, hình ảnh showroom
- **Cấu hình:** Rank Math → Titles & Meta → Local SEO → chọn **"Local Business"**

---

## 8. CẤU HÌNH QUA RANK MATH

### 8.1. Global Schema Settings

1. **Rank Math → Titles & Meta → Global Meta:**
   - Bật **"Use Schema Markup"**: ✅
   - Default Schema Type: **Article** (cho posts), **Product** (cho products)

2. **Rank Math → Titles & Meta → Local SEO:**
   - Business Type: **Organization** (hoặc **ElectronicsStore** khi có showroom)
   - Điền đầy đủ: Name, Logo, Phone, Address, Opening Hours
   - About Page: `/gioi-thieu/`
   - Contact Page: `/lien-he/`

3. **Rank Math → Titles & Meta → Social:**
   - Facebook Page URL: `https://www.facebook.com/xiaomi247`
   - YouTube Channel: `https://www.youtube.com/@xiaomi247`
   - TikTok: `https://www.tiktok.com/@xiaomi247`

### 8.2. Per-Page Schema Settings

| Loại trang | Schema mặc định | Schema bổ sung |
|------------|-----------------|----------------|
| Trang chủ | Organization | WebSite (tự động) |
| Trang danh mục | CollectionPage | FAQPage (thêm thủ công) |
| Trang sản phẩm | Product | BreadcrumbList (tự động) |
| Trang blog | BlogPosting | FAQPage (nếu có FAQ section) |
| Trang liên hệ | ContactPage | LocalBusiness (khi có showroom) |

### 8.3. Custom Schema Editor

Khi cần thêm schema mà Rank Math không hỗ trợ mặc định:

1. Mở bài viết/trang trong editor
2. Click tab **Rank Math** ở sidebar → **Schema**
3. Click **"Add Schema"** → chọn loại hoặc **"Custom Schema"**
4. Nhập JSON-LD trực tiếp hoặc dùng form builder
5. **Preview** để kiểm tra trước khi publish

### 8.4. Tránh trùng lặp Schema

⚠️ **Quan trọng:** Nhiều plugin có thể tạo schema trùng lặp. Kiểm tra và xử lý:

```php
// Tắt WooCommerce default schema (để Rank Math quản lý)
add_filter('woocommerce_structured_data_product', '__return_empty_array');
add_filter('woocommerce_structured_data_review', '__return_empty_array');
add_filter('woocommerce_structured_data_breadcrumblist', '__return_empty_array');

// Hoặc cấu hình trong Rank Math:
// Rank Math → General Settings → WooCommerce → "Remove WooCommerce Schema": Bật
```

---

## 9. TESTING & VALIDATION

### 9.1. Công cụ kiểm tra

| Công cụ | URL | Mục đích |
|---------|-----|----------|
| **Google Rich Results Test** | https://search.google.com/test/rich-results | Kiểm tra rich results eligibility |
| **Schema Markup Validator** | https://validator.schema.org/ | Validate cú pháp schema.org |
| **Google Search Console** | GSC → Enhancements | Theo dõi lỗi schema trên toàn site |
| **Rank Math Schema Preview** | Trong editor → Rank Math → Schema | Preview schema trước khi publish |

### 9.2. Quy trình kiểm tra

1. **Trước khi publish:**
   - Mở **Rank Math → Schema** trong editor, kiểm tra schema preview
   - Copy JSON-LD → paste vào **Schema Markup Validator** → kiểm tra không có lỗi

2. **Sau khi publish:**
   - Paste URL vào **Google Rich Results Test**
   - Kiểm tra tất cả schema types được detect
   - Kiểm tra **"Eligible for rich results"** cho Product, FAQ, Breadcrumb

3. **Hàng tuần:**
   - Kiểm tra **GSC → Enhancements** cho từng loại:
     - Products
     - FAQs
     - Breadcrumbs
     - Articles
   - Fix ngay các lỗi/cảnh báo mới

### 9.3. Lỗi thường gặp & Cách sửa

| Lỗi | Nguyên nhân | Cách sửa |
|-----|-------------|----------|
| **"Missing field: price"** | Sản phẩm chưa có giá trong WooCommerce | Điền giá cho tất cả sản phẩm |
| **"Missing field: image"** | Sản phẩm/bài viết chưa có ảnh | Thêm Featured Image |
| **"Missing field: review"** | Chưa có review nào | Khuyến khích khách đánh giá, hoặc tạm bỏ `aggregateRating` |
| **"Price not matching"** | Giá schema ≠ giá hiển thị | Đảm bảo Rank Math lấy giá từ WooCommerce |
| **"Duplicate schema"** | Nhiều plugin tạo schema | Tắt schema từ WooCommerce, chỉ dùng Rank Math |
| **"Invalid date format"** | Sai format ngày | Dùng ISO 8601: `2026-03-21T08:00:00+07:00` |
| **"Logo too small"** | Logo < 112×112px | Upload logo tối thiểu 600×60px |
| **"FAQ: Missing answer"** | Câu trả lời trống | Điền đầy đủ answer cho mọi question |

### 9.4. Monitoring Dashboard

Tạo checklist kiểm tra hàng tháng trong Google Search Console:

- [ ] Products: 0 errors, 0 warnings
- [ ] FAQs: 0 errors
- [ ] Breadcrumbs: 0 errors
- [ ] Articles: 0 errors
- [ ] Sitelinks searchbox: Active
- [ ] Rich results impressions tăng so với tháng trước

---

## 10. CHECKLIST TRIỂN KHAI

### ✅ Trang chủ

- [ ] Schema Organization với đầy đủ: name, url, logo, contactPoint, sameAs, address
- [ ] Cấu hình Rank Math Local SEO
- [ ] Thêm social profiles vào Rank Math
- [ ] Test qua Google Rich Results Test
- [ ] Verify trên Schema Markup Validator

### ✅ Trang sản phẩm (mỗi sản phẩm)

- [ ] Điền đầy đủ thông tin WooCommerce: tên, mô tả, giá, SKU, ảnh (≥3)
- [ ] Thêm Brand = "Xiaomi" (qua plugin hoặc custom field)
- [ ] Bật WooCommerce reviews
- [ ] Tắt WooCommerce default schema (dùng Rank Math)
- [ ] Kiểm tra Product schema trong Rank Math → Schema
- [ ] Thêm shippingDetails và returnPolicy qua Custom Schema
- [ ] Test rich results: giá, rating, availability hiển thị đúng

### ✅ Breadcrumb (tất cả trang)

- [ ] Bật Rank Math Breadcrumbs
- [ ] Cấu hình Home Label = "Trang chủ"
- [ ] Thêm breadcrumb vào theme template
- [ ] Kiểm tra breadcrumb hiển thị đúng trên frontend
- [ ] Test BreadcrumbList schema qua Rich Results Test

### ✅ FAQ (trang danh mục + blog)

- [ ] Thêm FAQ block (Rank Math) cho 5 danh mục chính:
  - [ ] Tivi Xiaomi — 5 FAQ
  - [ ] Robot hút bụi Xiaomi — 4 FAQ
  - [ ] Tủ lạnh Xiaomi — 3 FAQ
  - [ ] Máy lọc không khí Xiaomi — 3 FAQ
  - [ ] Máy hút ẩm Xiaomi — 3 FAQ
- [ ] Thêm FAQ cho các bài blog quan trọng
- [ ] Test FAQPage schema qua Rich Results Test

### ✅ Blog/Article (mỗi bài viết)

- [ ] Đặt Author profile đầy đủ trong WordPress
- [ ] Thêm Featured Image (≥1200×630px)
- [ ] Viết Excerpt chứa keyword
- [ ] Kiểm tra Article schema tự động từ Rank Math
- [ ] Test qua Rich Results Test

### ✅ LocalBusiness (khi mở showroom)

- [ ] Cập nhật địa chỉ, SĐT, tọa độ GPS
- [ ] Upload ảnh showroom
- [ ] Cấu hình giờ mở cửa
- [ ] Chuyển Rank Math Local SEO sang LocalBusiness
- [ ] Đăng ký Google Business Profile
- [ ] Test LocalBusiness schema

### ✅ Kiểm tra tổng thể

- [ ] Không có schema trùng lặp (kiểm tra view-source)
- [ ] Tất cả JSON-LD hợp lệ trên Schema Markup Validator
- [ ] Google Search Console → Enhancements: 0 errors
- [ ] Rich results hiển thị trên SERP (kiểm tra sau 1-2 tuần)
- [ ] Thiết lập monitoring hàng tuần trong GSC

---

> **Tài liệu tham chiếu:**
> - [Schema.org Documentation](https://schema.org/docs/documents.html)
> - [Google Structured Data Guidelines](https://developers.google.com/search/docs/appearance/structured-data)
> - [Rank Math Schema Documentation](https://rankmath.com/kb/rich-snippets/)
> - [On-page Optimization Guide](../marketing/02-seo/onpage-optimization-guide.md) — Phần 5
> - [Keyword Map](../marketing/02-seo/keyword-map.md)