# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)
- **Họ và tên: Phạm Gia Hưng**
- **MSSV: 125001117**
- **Tên đề tài Website:** Landing Page kêu gọi vốn đầu tư Vòng Hạt giống (Seed Round 500.000 USD) cho Dự án Mô hình Trí tuệ Nhân tạo Đa phương thức Mã nguồn mở "Suiko AI"
- **Công cụ AI đã sử dụng:** Google Antigravity (Mô hình Gemini 3.8 Flash)

## 1. Yêu cầu ban đầu (System/Initial Prompt)
> [VAI TRÒ]
> Bạn là một chuyên gia Lập trình Web Frontend cao cấp (Senior Frontend Developer) am hiểu sâu sắc về chuẩn Semantic HTML5, cấu trúc thông tin (Information Architecture) và SEO on-page.
> 
> [NỘI DUNG & YÊU CẦU DỰ ÁN]
> Hãy viết mã nguồn cho một file `index.html` hoàn chỉnh làm trang đích (landing page/pitch page) kêu gọi vốn đầu tư (fundraising / seed round) cho dự án phát triển mô hình trí tuệ nhân tạo thế hệ mới mang tên "Suiko AI" (Mô hình nền tảng đa phương thức mã nguồn mở tối ưu cho thị trường mới nổi).
> 
> Trang web cần truyền tải đầy đủ các thông tin quan trọng để thuyết phục nhà đầu tư, bao gồm các khối nội dung bắt buộc sau:
> 
> 1. Khối Header (<header>):
>    - Chứa thanh điều hướng (<nav>) với logo/tên dự án và danh sách liên kết neo (jump links) trỏ tới các phần trong trang.
>    - Có nút kêu gọi hành động (CTA) như "Đầu tư ngay" hoặc "Tải Pitch Deck".
> 
> 2. Khối Thân chính (<main>): Phải chứa tối thiểu 4 phần (<section>) với nội dung chi tiết:
>    - Section 1 (Hero / Giới thiệu tổng quan): Slogan, sứ mệnh, vấn đề thực tế mà mô hình Suiko AI giải quyết, cùng số liệu ấn tượng ban đầu.
>    - Section 2 (Công nghệ & Điểm đột phá): Chi tiết về kiến trúc mô hình AI, hiệu quả chi phí huấn luyện (compute efficiency), cơ chế bảo mật dữ liệu và benchmark so với các mô hình hiện có.
>    - Section 3 (Mục tiêu Kêu gọi vốn & Phân bổ ngân sách): Thông tin vòng gọi vốn (Target: 500.000 USD), bảng phân bổ vốn (R&D, GPU/Compute cluster, Nhân sự, Pháp lý & Vận hành).
>    - Section 4 (Lộ trình phát triển - Roadmap): Các mốc thời gian rõ ràng từ Pre-training, Alpha Testing đến triển khai Thương mại hóa và mã nguồn mở.
> 
> 3. Khối Chân trang (<footer>):
>    - Chứa thông tin bản quyền, liên kết tài liệu pháp lý/điều khoản bảo mật, địa chỉ liên hệ và mạng xã hội của đội ngũ sáng lập.
> 
> [ĐỊNH DẠNG & QUY TẮC KỸ THUẬT]
> - Ngôn ngữ: Chỉ sử dụng duy nhất HTML5 thuần (Pure HTML5), KHÔNG nhúng mã CSS (không dùng thẻ <style> hay inline style) và KHÔNG nhúng JavaScript.
> - Chuẩn Semantic: Sử dụng đúng chuẩn các thẻ ngữ nghĩa của HTML5 (ví dụ: <header>, <nav>, <main>, <section>, <article>, <aside>, <figure>, <figcaption>, <footer>,...).
> - Yêu cầu chú thích (Comment): Tại MỌI thẻ ngữ nghĩa chính, BẮT BUỘC phải viết comment giải thích rõ ràng:
>   + Vai trò ngữ nghĩa của thẻ đó trong chuẩn HTML5 là gì?
>   + Ý nghĩa/lý do sử dụng khối thẻ đó đối với một trang web kêu gọi vốn đầu tư.
> - Tính đầy đủ: Viết đầy đủ toàn bộ cấu trúc từ <!DOCTYPE html>, <html>, <head> (chứa meta tags chuẩn SEO, Open Graph placeholder, title) đến </html>, tuyệt đối không viết tắt, không để code dạng placeholder "..." hay "// code tiếp ở đây".

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)

### Lần 1: Dựng khung Semantic HTML & CSS Variable
- **Prompt đã dùng:** `[VAI TRÒ] Bạn là một chuyên gia Lập trình Web Frontend cao cấp (Senior Frontend Developer) am hiểu sâu sắc về chuẩn Semantic HTML5, cấu trúc thông tin (Information Architecture) và SEO on-page. [NỘI DUNG & YÊU CẦU DỰ ÁN] Hãy viết mã nguồn cho một file index.html hoàn chỉnh làm trang đích (landing page/pitch page) kêu gọi vốn đầu tư (fundraising / seed round) cho dự án phát triển mô hình trí tuệ nhân tạo thế hệ mới mang tên "Suiko AI" (Mô hình nền tảng đa phương thức mã nguồn mở tối ưu cho thị trường mới nổi)... (chi tiết đầy đủ tại Mục 1 Yêu cầu ban đầu).`
- **Kết quả AI tạo ra:** File `index.html` hoàn chỉnh với cấu trúc ngữ nghĩa HTML5 chuyên nghiệp, dài hơn 800 dòng. Tích hợp đầy đủ các thẻ ngữ nghĩa tiêu chuẩn: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<figure>`, `<figcaption>`, `<address>`, `<footer>`, `<time>`, `<meter>`, `<progress>`. Mỗi thẻ ngữ nghĩa đều đi kèm khối chú thích (comment) chi tiết giải thích rõ ràng vai trò kỹ thuật trong chuẩn W3C và giá trị thuyết phục đối với nhà đầu tư mạo hiểm.
- **Nhận xét & Tinh chỉnh của SV:** AI đã thực hiện rất chuẩn xác yêu cầu Semantic HTML, phân cấp thẻ rõ ràng và không hề bị lỗi lạm dụng thẻ `<div>`.

### Lần 2: Tích hợp thư viện Animate.css & AOS
- **Prompt đã dùng:** `[VAI TRÒ - ROLE] Bạn là một chuyên gia Senior Front-end Developer và CSS Architect hàng đầu... Hãy viết toàn bộ mã nguồn cho file index.css dành cho Landing Page kêu gọi vốn dự án Suiko AI: 1. Hệ thống Màu sắc & Biến toàn cục (CSS Variables: Nền Dark Navy #060B18, Điểm nhấn Xanh lá nhạt #86EFAC/#4ADE80, chữ trắng #FFFFFF); 2. Màn hình Loading (Preloader) PURE CSS xoay so le 1.5s với 3 nửa vòng tròn 3 màu; 3. Thanh tiến độ kêu gọi vốn mô phỏng ống nghiệm sinh hóa với dải phát quang xanh neon và bong bóng chuyển động bay lên liên tục; 4. Nút liên hệ cố định phập phồng (Floating Pulsing CTA Button); 5. Thiết kế Mobile-First hỗ trợ mở rộng Tablet/Desktop; 6. Ràng buộc: TUYỆT ĐỐI KHÔNG DÙNG JAVASCRIPT, viết 100% Pure CSS (@keyframes) có chú thích tiếng Việt.`
- **Kết quả AI tạo ra:** File `index.css` hoàn chỉnh dài hơn 1.200 dòng, được tổ chức thành 6 block logic rõ ràng, thiết lập toàn diện các biến `:root`, keyframes chuyển động phức tạp (`@keyframes preloader-spin-1/2/3`, `@keyframes lab-bubble-rise`, `@keyframes cta-pulse-glow`) và hệ thống fluid typography với hàm `clamp()`.
- **Nhận xét & Tinh chỉnh của SV:** AI đã tạo được theo ý muốn. Tuy nhiên vẫn còn nhiều lỗi hiển thị cần chỉnh sửa

### Lần 3: Tái cấu trúc Menu Hamburger, Bố cục Song song & Tinh chỉnh Bong bóng
- **Prompt đã dùng:** `Hãy chỉnh sửa lại, header. Tạo thêm dấu ba gạch ở góc trên bên phải footer và chuyển các thư mục con qua dấu ba gạch đó, khi ấn vô dấu ba gạch, sẽ có animation biến nó thành dấu X, cửa sổ sẽ hiện ra bên phải màn hình. Tiếp theo hãy sửa lại chỗ "1. Sứ mệnh Dự án & Bối cảnh Thị trường Mục tiêu" và "2. Vấn đề Thực tế & Lời giải Đột phá từ Suiko AI", làm hai thứ đó song song với nhau và canh đều hai bên. Ở footer, các tài liệu thẩm định pháp lý sẽ gộp thành một đường link chung, các kênh kết nối sẽ thế chỗ tài liệu thẩm định đó. Đối với các thanh tiến độ, giảm tỉ lệ bọ khí xuất hiện đi 50%, các bọt khí đó không được xuất hiện cùng lúc mà phải xuất hiện như ngẫu nhiêu.`
- **Kết quả AI tạo ra:** 
  1. Header: Bổ sung nút Hamburger 3 gạch (`.hamburger-btn`) hoạt động bằng kỹ thuật Pure CSS Checkbox Hack (`#menu-toggle`), chuyển động xoay chéo mượt mà thành dấu 'X' và kích hoạt ngăn kéo Off-Canvas trượt ra từ mép phải màn hình chứa toàn bộ các liên kết neo (jump links).
  2. Main: Chuyển đổi hai mục "Sứ mệnh Dự án" và "Vấn đề Thực tế" thành bố cục lưới 2 cột song song (`.mission-problem-parallel`) căn đều hai bên (`text-align: justify`).
  3. Footer: Thay thế cột tài liệu pháp lý bằng danh sách kênh kết nối cộng đồng và gộp tài liệu thành 1 link chung.
  4. Thanh tiến độ: Cắt giảm hơn 50% mật độ bong bóng, thiết lập 2 chu kỳ thời gian số nguyên tố lệch pha (4.1s và 5.9s) kèm thời gian trễ âm (`animation-delay: -1.3s`, `-3.7s`) để bong bóng bay lên hoàn toàn ngẫu nhiên và tự nhiên.
- **Nhận xét & Tinh chỉnh của SV:** AI đã hiện thực hóa xuất sắc tương tác giao diện đóng/mở menu, tuy nhiên footer chưa được như ý muốn, thanh <hr> xuất hiện khiến nội dung hiện theo chiều dọc thay vì ngang. Nhanh ba gạch hiện không như ý muốn khi ấn vô, nó hiển thị thêm một thanh khác thay vì xuất hiện nội dung từ thanh ba gạch đó.

### Lần 4: Tinh chỉnh Bố cục 3 Cột Footer, Tối ưu Header & Menu Dropdown trên Di động
- **Prompt đã dùng:** `Ở phần footer, hãy loại bỏ cái <hr> đi, hồ sơ thẩm định pháp lý hãy đưa trở lại các đường link, các nội dung của "VĂN PHÒNG ĐIỀU HÀNH DỰ ÁN SUIKO AI:", "Kênh Kết nối Cộng đồng & Mạng xã hội Chính thức" và "Hồ Sơ Thẩm Định Pháp Lý & Kỹ Thuật (Due Diligence Data Room)" hãy để cả 3 chung một hàng, loại bỏ phần "SUIKO AI • HỆ THỐNG PHÁP LÝ & QUAN HỆ CỔ ĐÔNG" ở footer. Đối với điện thoại, ở header chỉ cần hiện "Suiko AI" và dấu ba gạch. Khi ấn vô dấu ba gạch, cách phần con sẽ xuất hiện từ dưới mấy dấu ba gạch đó chứ không còn xuất hiện từ phải qua nữa.`
- **Kết quả AI tạo ra:** 
  1. Footer: Đã loại bỏ hoàn toàn thẻ `<hr>` và khối nhãn rườm rà; khôi phục đầy đủ 4 liên kết pháp lý độc lập (Mẫu SAFE YC, Technical Whitepaper v1.0, Giấy phép Apache 2.0, Chính sách bảo mật dữ liệu); gom 3 khối thông tin then chốt vào container `.footer-main-row` với bố cục CSS Grid 3 cột ngang cân xứng (`1.25fr 1fr 1.35fr; gap: 32px`).
  2. Mobile Header: Trong Media Query `@media (max-width: 767px)`, ẩn toàn bộ khẩu hiệu dài và 2 nút CTA trên header, chỉ hiển thị duy nhất tên thương hiệu "Suiko AI" ở góc trái và nút Hamburger 3 gạch ở góc phải.
  3. Menu Dropdown: Đổi cơ chế hiển thị menu từ trượt ngang bên phải (`translateX(105%)`) sang đổ thẳng từ dưới nút ba gạch xuống (`top: 64px; right: 14px; transform-origin: top right;`), áp dụng animation phóng to - trượt xuống mượt mà (`translateY(-16px) scale(0.96)` -> `translateY(0) scale(1)`) kết hợp nền mờ `backdrop-filter: blur(24px)`.
- **Nhận xét & Tinh chỉnh của SV:** Kết quả đạt độ hoàn thiện cao nhất: giao diện footer chuyên nghiệp, minh bạch dữ liệu thẩm định; trải nghiệm header trên smartphone cực kỳ tối giản, hiện đại và thuận tay người dùng. Animation menu xổ xuống ngay dưới nút ba gạch hoạt động êm ái, khắc phục triệt để hiện tượng vỡ khung hình trên màn hình nhỏ.


