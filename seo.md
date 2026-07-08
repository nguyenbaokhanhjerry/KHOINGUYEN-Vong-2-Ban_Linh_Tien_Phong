Bạn là một Senior SEO Technical Specialist với 10+ năm kinh nghiệm tối ưu
Core Web Vitals, Technical SEO và Structured Data cho các trang landing
page/one-page SaaS. Tôi có một file HTML tĩnh, một trang (single-page),
tên "Project DNA" — nền tảng AI kết nối Sinh viên – Trường đại học –
Doanh nghiệp thông qua đồ án tốt nghiệp. Trang có 3 ngôn ngữ (VI/EN/JP)
được đổi bằng JavaScript (data-i18n), không đổi URL.

Hãy audit và chỉnh sửa TRỰC TIẾP trong file HTML, theo đúng thứ tự ưu
tiên dưới đây. Với mỗi mục, hãy giải thích ngắn gọn TẠI SAO trước khi sửa,
rồi đưa ra đoạn code cụ thể.

## 1. Meta tags nền tảng (đang thiếu)
- Thêm <link rel="canonical"> trỏ về URL chính thức của trang.
- Thêm <meta name="robots" content="index, follow">.
- Kiểm tra lại <title> (hiện tại) và <meta name="description"> — có đúng
  độ dài khuyến nghị (title ~50-60 ký tự, description ~150-160 ký tự)
  và có chứa từ khóa chính "đồ án tốt nghiệp", "AI kết nối sinh viên
  doanh nghiệp" một cách tự nhiên không? Đề xuất bản tối ưu hơn nếu cần.
- Thêm favicon (<link rel="icon">) và web app manifest — hiện file
  chưa có.

## 2. Open Graph & Twitter Card (đang thiếu hoàn toàn)
Thêm đầy đủ og:title, og:description, og:type, og:url, og:image
(1200x630), og:locale, og:site_name và twitter:card,
twitter:title, twitter:description, twitter:image. Vì trang không có
ảnh sẵn (100% CSS/gradient), hãy đề xuất tôi cần chuẩn bị 1 ảnh OG
riêng — đừng tự chèn ảnh giả.

## 3. Structured Data (Schema.org / JSON-LD) — đang thiếu
Thêm JSON-LD phù hợp với bản chất trang (Organization hoặc
SoftwareApplication/Product, tùy nội dung), gồm name, description,
url. Không bịa số liệu (rating, review, giá) nếu file không có sẵn.

## 4. Đa ngôn ngữ (VI/EN/JP) — vấn đề kỹ thuật quan trọng nhất
Hiện tại 3 ngôn ngữ đổi bằng JavaScript, không đổi URL, nên Google chỉ
index được đúng 1 phiên bản (VI) và bỏ lỡ toàn bộ nội dung EN/JP.
Hãy đề xuất 1 trong 2 hướng và giải thích trade-off:
   a) Tách thành 3 route/file riêng (/vi/, /en/, /jp/) + thẻ
      <link rel="alternate" hreflang="..."> chéo nhau, hoặc
   b) Nếu bắt buộc giữ kiến trúc 1 file JS hiện tại, nêu rõ giới hạn SEO
      của cách này và cách giảm thiểu (ví dụ: prerender từng bản ngôn
      ngữ ở build time).

## 5. Cấu trúc heading & nội dung
- Kiểm tra thứ tự H1 → H2 → H3 có hợp lý, không nhảy cấp không.
- Trang hiện có nhiều <h2> nhưng thiếu <h3> phân cấp con ở một số
  section — chỉ ra section nào cần và đề xuất cấu trúc lại.
- Rà từ khóa: liệt kê 5-8 cụm từ khóa chính/phụ nên xuất hiện tự nhiên
  hơn trong heading và đoạn mở đầu mỗi section.

## 6. Performance / Core Web Vitals
- File hiện load 3 font family qua Google Fonts (Bricolage Grotesque,
  IBM Plex Mono, Inter) — đề xuất font-display, preload font quan
  trọng nhất, và cân nhắc subset.
- CSS và JS đang inline toàn bộ trong <head>/<body> của 1 file HTML
  ~3000 dòng — đánh giá tác động tới render-blocking và đề xuất tách
  file / minify / defer hợp lý mà không phá layout.
- Kiểm tra có ảnh nào cần lazy-load, width/height tường minh không
  (nếu sau này thêm ảnh OG hoặc ảnh minh họa).

## 7. Accessibility liên quan SEO
- Trang hiện không có thẻ <img> nào — nếu tôi bổ sung hình minh họa
  sau này, nhắc tôi luôn cần alt text mô tả, không bỏ trống.
- Kiểm tra các nút tương tác (burger menu, lang-btn) có aria-label /
  aria-expanded đầy đủ chưa (đã có 1 phần, rà lại cho nhất quán).

## 8. Sitemap & robots.txt (file phụ trợ, không nằm trong demo.html)
Đề xuất nội dung sitemap.xml và robots.txt phù hợp với domain thật khi
tôi cung cấp, kèm khuyến nghị submit qua Google Search Console.

## Yêu cầu đầu ra
- Sửa trực tiếp trong file demo.html, giữ nguyên toàn bộ style/JS hiện
  có, không đổi thiết kế.
- Sau khi sửa xong, tóm tắt lại dạng checklist: mục nào đã sửa, mục nào
  cần tôi cung cấp thêm thông tin (domain thật, ảnh OG, số liệu chính
  xác) mới hoàn thiện được.
- Không tự bịa số liệu, tên miền, hay đường link không có trong file gốc.