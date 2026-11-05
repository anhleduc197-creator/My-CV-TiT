# BÁO CÁO KIỂM THỬ VÀ ĐÁNH GIÁ TRƯỚC BÀN GIAO

## 1. Thông tin chung

| Trường | Thông tin |
|---|---|
| Tên dự án | My-CV-TiT - Portfolio CV của Lê Đức Anh |
| Phiên bản | v1.0 (theo release note hiện có) |
| Ngày đánh giá | 05/11/2026 |
| Người thực hiện | GitHub Copilot - rà soát tĩnh mã nguồn và tài liệu |
| Người đánh giá/nghiệm thu | Chưa chỉ định |
| Phạm vi | `index.html`, `assets/css/styles.css`, cấu trúc repository và tài liệu bàn giao |
| Phương pháp | Đọc mã nguồn và đối chiếu cấu trúc; chưa chạy kiểm thử trình duyệt, hiệu năng, bảo mật triển khai hoặc Docker |

### Quy ước trạng thái

- **Đạt:** Có thể xác nhận từ phạm vi đánh giá đã thực hiện.
- **Chưa đạt:** Có lỗi hoặc thiếu sót cụ thể cần xử lý trước khi nghiệm thu.
- **Cần cải thiện:** Có cơ sở triển khai nhưng chưa đủ bằng chứng, hoặc cần hoàn thiện thêm.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Chưa đạt | Điều hướng nội bộ có đích; liên kết dự án còn placeholder và markup liên hệ GitHub chưa hợp lệ. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | Có breakpoint responsive và hỗ trợ focus/reduced motion; một số màu nền/viền được khai báo trong suốt, chưa kiểm tra trực quan trên trình duyệt. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Đây là trang tĩnh; chưa có kết quả chạy thử, đo hiệu năng hoặc kiểm tra lỗi tải tài nguyên. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy xử lý dữ liệu người dùng hay cấu hình bí mật trong mã được rà soát; cấu hình máy chủ triển khai chưa được đánh giá. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Chưa đạt | Có phân tách HTML/CSS và tài liệu; cần sửa markup liên hệ và bổ sung kiểm tra tự động hoặc kết quả kiểm thử có thể lặp lại. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Chưa đạt | README có hướng dẫn chạy, nhưng chưa có kết quả xác nhận trên trình duyệt/Docker, log kiểm thử hoặc ảnh minh chứng. |

## 3. Chi tiết đánh giá

### 3.1 Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Các mục điều hướng trỏ đến phần tương ứng | Đạt | `index.html` có các đích `#about`, `#skills`, `#projects`, `#contact`; nút đầu trang trỏ đến `#top`. Xác nhận qua rà soát mã nguồn, chưa thử thao tác trên trình duyệt. |
| Hiển thị các phần giới thiệu, kỹ năng, dự án và liên hệ | Đạt | Các section tương ứng có trong `index.html`; danh sách gồm sáu kỹ năng và bốn thẻ dự án. |
| Liên kết chi tiết dự án hoạt động đúng | Chưa đạt | Cả bốn thẻ dự án dùng `href="#"`, chưa dẫn đến trang chi tiết hoặc repository. |
| Markup của mục liên hệ GitHub hợp lệ | Chưa đạt | Thẻ `<a href="#">` ở mục GitHub chưa được đóng trước phần tử LinkedIn tiếp theo; trình phân tích HTML có thể tự sửa cấu trúc theo cách ngoài dự kiến. |
| Nội dung thẻ dự án khớp với chức năng có thể kiểm chứng | Cần cải thiện | Mô tả nêu Todo App lưu cục bộ và Weather Dashboard dùng API, nhưng repository được rà soát chỉ có trang HTML/CSS tĩnh, không có mã triển khai các chức năng đó. Cần xác nhận đây là mô tả dự án bên ngoài hay sửa lại nội dung. |
| Liên kết email | Đạt | Có `mailto:anhleduc197@gmail.com`; chưa kiểm tra mở ứng dụng email thực tế. |

### 3.2 Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Bố cục responsive | Cần cải thiện | CSS khai báo một cột mặc định, hai cột từ 768px và ba cột từ 1280px; chưa xác nhận bằng kiểm tra trực quan ở các viewport thực tế. |
| Màu nền, vùng nhấn và viền hiển thị | Chưa đạt | Các biến `--color-bg`, `--color-surface`, `--color-border` và `--color-chip` trong `styles.css` kết thúc bằng alpha `00`, tức hoàn toàn trong suốt. Cần xác nhận và chỉnh bảng màu để bảo đảm phân tách nội dung/độ tương phản. |
| Điều hướng bằng bàn phím | Đạt | CSS có kiểu `:focus-visible`; chưa thực hiện kiểm thử bàn phím từ đầu đến cuối. |
| Tôn trọng tùy chọn giảm chuyển động | Đạt | Có media query `prefers-reduced-motion: reduce` tắt animation, transition và cuộn mượt. |
| Tương thích trình duyệt và khả năng tiếp cận | Cần cải thiện | Chưa có ma trận trình duyệt, thiết bị, kiểm tra độ tương phản hoặc trình đọc màn hình. |

### 3.3 Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Có thể phục vụ dưới dạng website tĩnh | Cần cải thiện | Tài liệu hướng dẫn dùng Python HTTP server hoặc Nginx; chưa chạy các lệnh này để xác nhận trang hoạt động. |
| Xử lý lỗi tải ảnh và tài nguyên | Cần cải thiện | Các ảnh được tham chiếu trong HTML có trong thư mục ảnh theo cấu trúc repository; chưa kiểm tra HTTP status, đường dẫn sau triển khai hoặc hành vi khi ảnh lỗi. |
| Hiệu năng tải trang | Cần cải thiện | Không có JavaScript ứng dụng hay backend trong phạm vi rà soát, nhưng chưa đo kích thước ảnh, thời gian tải, Core Web Vitals hoặc hiệu năng mạng. |
| Hành vi lỗi của chức năng động | Đạt | Không phát hiện luồng xử lý dữ liệu động trong HTML/CSS được kiểm tra; tiêu chí này không áp dụng cho các tính năng backend vì dự án hiện là trang tĩnh. |

### 3.4 Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Bí mật/credential được nhúng trong mã giao diện | Đạt | Không thấy API key, mật khẩu hoặc credential trong các tệp HTML/CSS được rà soát; đây không thay thế cho quét toàn repository. |
| Thu thập, lưu trữ và xử lý dữ liệu cá nhân | Đạt | Không thấy form gửi dữ liệu, mã lưu trữ phía trình duyệt hoặc backend trong phạm vi kiểm tra. Email chỉ dùng liên kết `mailto:`. |
| Quản lý cấu hình triển khai | Cần cải thiện | README nêu dự án không cần `.env`; chưa có cấu hình môi trường hoặc kiểm chứng cấu hình Nginx/hosting thực tế. |
| Bảo mật khi triển khai | Cần cải thiện | Chưa kiểm tra HTTPS/TLS, security headers, quyền truy cập máy chủ, chính sách cache hoặc cấu hình CDN/hosting. |
| Liên kết bên ngoài | Cần cải thiện | Liên kết GitHub/LinkedIn và liên kết dự án còn placeholder; cần thay bằng URL chính thức và xác nhận đích trước khi công khai. |

### 3.5 Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Phân tách cấu trúc giao diện | Đạt | HTML ở `index.html`, CSS ở `assets/css/styles.css`, ảnh ở `assets/css/img/`. |
| Tính hợp lệ của HTML | Chưa đạt | Phát hiện thẻ liên kết GitHub chưa đóng trong danh sách liên hệ; chưa chạy HTML validator để rà soát toàn trang. |
| Chất lượng và tính nhất quán nội dung | Cần cải thiện | Một số mô tả dự án nói đến API/lưu trữ cục bộ nhưng repository không có mã tương ứng; cần đối chiếu với sản phẩm thực tế. |
| Tài liệu bàn giao | Đạt | `README.md` có mô tả, yêu cầu môi trường, cấu hình và hướng dẫn chạy; `docs/RELEASENNOTE.md` có thông tin v1.0. Các hướng dẫn chưa được xác nhận bằng chạy thử. |
| Lint, validator và kiểm thử tự động | Chưa đạt | Chưa thấy bộ kiểm thử hoặc cấu hình lint/HTML validation trong cấu trúc repository đã kiểm tra; chưa có kết quả chạy kiểm thử. |

### 3.6 Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Hướng dẫn chạy cục bộ | Cần cải thiện | README có lệnh Python HTTP server cho Windows/macOS/Linux; chưa chạy và ghi nhận kết quả trên các hệ điều hành đó. |
| Hướng dẫn chạy Docker | Cần cải thiện | README có lệnh Docker dùng `nginx:alpine`; repository không có Dockerfile/Compose và lệnh chưa được thực thi để xác nhận. |
| Kiểm thử trên môi trường bàn giao | Chưa đạt | Chưa có môi trường staging/production hoặc kết quả xác minh URL triển khai. |
| Minh chứng kiểm thử | Chưa đạt | Chưa có screenshot, log, checklist đã được người kiểm thử thực thi hoặc kết quả trình duyệt đính kèm. Báo cáo này là rà soát tĩnh, không phải bằng chứng chạy thử. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định

>Sản phẩm có cấu trúc phù hợp cho một portfolio tĩnh đơn giản và đã có hướng dẫn sử dụng cơ bản. Tuy nhiên, **chưa khuyến nghị bàn giao như một sản phẩm đã nghiệm thu**: có lỗi markup cụ thể, một số liên kết chưa hoàn thiện, màu nền/viền đang trong suốt và chưa có bằng chứng kiểm thử runtime. Đánh giá này chỉ dựa trên rà soát tĩnh mã nguồn và tài liệu.

### Việc cần xử lý trước khi bàn giao

1. Sửa markup trong danh sách liên hệ: đóng thẻ GitHub và từng `<li>` đúng cấu trúc; chạy HTML validator sau khi sửa.
2. Thay toàn bộ liên kết `href="#"` bằng URL hợp lệ hoặc bỏ các liên kết chưa sẵn sàng; xác nhận URL GitHub và LinkedIn.
3. Chỉnh các biến màu CSS có alpha `00`, sau đó kiểm tra độ tương phản và trạng thái hover/focus trên nền thực tế.
4. Đối chiếu mô tả bốn dự án với sản phẩm thật; không mô tả chức năng API/lưu trữ nếu không có bằng chứng hoặc đường dẫn đến dự án tương ứng.
5. Chạy smoke test trên trình duyệt ở mobile/tablet/desktop, kiểm tra điều hướng, email và tải ảnh; lưu screenshot và kết quả.
6. Nếu bàn giao qua Docker/hosting, chạy thử triển khai thực tế và kiểm tra HTTPS, security headers, lỗi tài nguyên và thời gian tải.

### Phạm vi chưa xác minh

- Chưa thực hiện kiểm thử chức năng tương tác trên trình duyệt hoặc thiết bị thật.
- Chưa kiểm tra tương thích chéo trình duyệt, accessibility bằng công cụ, bảo mật triển khai hay hiệu năng thực tế.
- Chưa chạy lệnh Python server/Docker trong môi trường thực thi; chưa có log hoặc screenshot kiểm thử.
