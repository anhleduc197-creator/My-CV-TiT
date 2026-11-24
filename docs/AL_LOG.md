# Nhật ký thay đổi lớn

Ghi lại các thay đổi đáng kể về chức năng, cấu trúc hoặc tài liệu. Mỗi mục nên nêu ngày, nội dung, các tệp bị ảnh hưởng và kết quả kiểm tra nếu có. Không cần ghi các chỉnh sửa nhỏ về câu chữ hoặc định dạng.

## 2026-11-05

### Bổ sung tài liệu dự án

- **Tệp:** `README.md`
- Viết hướng dẫn tiếng Việt về dự án, chức năng, công nghệ, yêu cầu môi trường, cài đặt, cấu hình và chạy thử trên Windows, macOS, Linux, cùng hướng dẫn chạy bằng Docker.
- Ghi rõ dự án là website tĩnh, không cần bước build hay cài thư viện ứng dụng.
- **Kiểm tra:** Không phát hiện lỗi tài liệu.

### Tạo release note phiên bản 1.0

- **Tệp:** `docs/RELEASENNOTE.md`
- Ghi ngày phát hành, các chức năng hiện có, tình trạng chưa ghi nhận lỗi sửa và các hạn chế như nội dung tĩnh, liên kết placeholder.
- Không thay đổi mã nguồn ứng dụng.

### Bổ sung báo cáo kiểm thử trước bàn giao

- **Tệp:** `docs/test_report.md`
- Soạn báo cáo theo sáu nhóm tiêu chí: chức năng; giao diện và tương thích; vận hành và hiệu năng; bảo mật và dữ liệu; chất lượng mã nguồn và tài liệu; triển khai, kiểm thử và minh chứng.
- Ghi nhận lỗi markup liên hệ, liên kết placeholder, biến màu CSS trong suốt và các phạm vi chưa được kiểm thử runtime.
- **Kiểm tra:** Không phát hiện lỗi tài liệu; báo cáo nêu rõ đây là rà soát tĩnh, chưa chạy kiểm thử trình duyệt/Docker.
## 2026-11-24 — Phiên bản v2.0

- Yêu cầu: thiết kế lại website cá nhân, thêm animation, cập nhật README và docs.
- `index.html`: giữ thông tin và ảnh gốc, chỉnh mô tả cho phù hợp với nội dung ảnh; sửa cấu trúc liên hệ, liên kết GitHub và liên kết mở ảnh.
- `assets/css/styles.css`: thay giao diện tối xanh đen, nền gradient, bố cục Grid/Flexbox, hiệu ứng rise và hover, hỗ trợ reduced motion.
- `assets/css/img/`: khôi phục tên ba ảnh tiếng Việt để đường dẫn HTML khớp tệp.
- `README.md`, `docs/`: cập nhật hướng dẫn, phiên bản và kiểm thử; thay ba ảnh minh chứng cũ.
- AI hỗ trợ chỉnh sửa HTML/CSS, tài liệu và kiểm thử; người học cần xem lại nội dung trước khi nộp.
- Kiểm tra Chromium ở ba kích thước: không tràn ngang, 5 ảnh tải được, các anchor có đích. Kiểm thử sử dụng bản HTML nhúng tài nguyên; chưa xác nhận triển khai GitHub Pages.

## 2026-11-24 — Phiên bản v2.1

- Yêu cầu: bổ sung bảng thông tin liên hệ cuối trang.
- `index.html`: thay danh sách liên hệ bằng bảng HTML có caption, tiêu đề hàng/cột; thêm nút gửi email. Giữ email và GitHub từ phiên bản trước; LinkedIn chưa xác minh nên để Chưa cập nhật.
- `assets/css/styles.css`: thiết kế bảng cùng tông xanh đen, hover, animation rise và bố cục responsive.
- `README.md`, `docs/`: cập nhật nội dung, kết quả kiểm thử và ảnh minh chứng.
- AI hỗ trợ chỉnh sửa mã nguồn và tài liệu; không thêm JavaScript hoặc backend.

## 2026-11-24 — Phiên bản v2.2

- Thay bảng thông tin cá nhân bằng form liên hệ cho khách truy cập nhập họ tên, email, số điện thoại (tùy chọn), chủ đề và lời nhắn.
- `index.html`: dùng form, label, input, textarea, button và kiểm tra HTML5; gửi qua ứng dụng email bằng mailto.
- `assets/css/styles.css`: thêm hiệu ứng focus, hover, bố cục responsive; giữ các phần khác.
- Cập nhật README, docs và ảnh minh chứng. AI hỗ trợ chỉnh sửa; không thêm JavaScript hoặc backend.

## 2026-11-24 — Phiên bản v2.3

- Đổi tên bốn ảnh dự án sang tên không dấu, không khoảng trắng; đồng bộ src và href trong index.html. Bỏ lazy loading cho bốn ảnh để tải ngay khi mở trang.
- CSS: mở rộng khu vực dự án lên tối đa 1200px, dùng hai cột trên tablet và desktop, một cột trên mobile; ảnh tỉ lệ 4:3, object-fit: contain để giữ toàn bộ nội dung.
- Giữ nguyên form liên hệ, animation và các nội dung khác. Cập nhật README, báo cáo kiểm thử và ảnh minh chứng.
