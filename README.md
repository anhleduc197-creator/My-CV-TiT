# My-CV-TiT — Portfolio Lê Đức Anh

Website cá nhân giới thiệu bản thân, kỹ năng, sở thích và thông tin liên hệ. Phiên bản 2.3 sử dụng giao diện tối xanh đen, điểm nhấn xanh ngọc và bố cục responsive.

## Chức năng
- Giới thiệu bản thân và ảnh đại diện.
- Hiển thị sáu kỹ năng đang học tập, rèn luyện.
- Bốn thẻ nội dung cá nhân có ảnh và liên kết mở ảnh gốc.
- Điều hướng cuộn mượt, nút về đầu trang, biểu mẫu liên hệ cuối trang (họ tên, email, số điện thoại, chủ đề, lời nhắn), nút gửi lời nhắn và liên kết GitHub.
- Hiệu ứng xuất hiện khi tải trang, hover trên nút, kỹ năng và thẻ nội dung.
- Hỗ trợ tùy chọn giảm chuyển động của hệ điều hành.

## Công nghệ
HTML5 semantic, CSS3, Flexbox, Grid, Media Queries, CSS animation và transition. Website không sử dụng JavaScript, backend hay thư viện ngoài.

## Cấu trúc thư mục
```text
My-CV-TiT-main/
├── index.html
├── assets/css/
│   ├── styles.css
│   └── img/ (5 ảnh gốc)
├── README.md
└── docs/
    ├── AL_LOG.md
    ├── RELEASENNOTE.md
    ├── test_report.md
    └── screenshots/ (3 ảnh minh chứng)
```

## Cách chạy
1. Giải nén hoặc clone repository.
2. Mở thư mục bằng VS Code.
3. Mở `index.html` bằng trình duyệt hoặc dùng Live Server.

Có thể chạy máy chủ cục bộ bằng Python: `python -m http.server 8000`, rồi mở `http://localhost:8000`.

## Responsive
- Mobile: dưới 768px, dự án 1 cột.
- Tablet: từ 768px, dự án 2 cột.
- Desktop: từ 1280px, dự án 2 cột rộng hơn.

## Minh chứng giao diện v2.3
[Desktop 1440×900](docs/screenshots/responsive-desktop-1440x900.png) · [Tablet 768×1024](docs/screenshots/responsive-tablet-768x1024.png) · [Mobile 390×844](docs/screenshots/responsive-mobile-390x844.png)

Ảnh chụp toàn trang từ Chromium với giao diện v2.3 (kiểm thử HTML nhúng tài nguyên do môi trường chặn máy chủ cục bộ). Bốn ảnh dự án gốc được giữ nguyên nội dung, đổi sang tên không dấu, không khoảng trắng; đường dẫn ảnh và liên kết mở ảnh được cập nhật. Khung ảnh dùng object-fit: contain để không cắt mất nội dung.

## Triển khai GitHub Pages
Đẩy nội dung thư mục dự án lên repository, vào Settings → Pages, chọn Deploy from a branch → main → / (root) → Save. Kiểm tra địa chỉ website sau khi triển khai.

## Tài liệu
- [Nhật ký thay đổi](docs/AL_LOG.md)
- [Ghi chú phiên bản](docs/RELEASENNOTE.md)
- [Báo cáo kiểm thử](docs/test_report.md)

## Hạn chế
Biểu mẫu dùng HTML với `required`, `type="email"` và `mailto:`. Nút gửi mở ứng dụng email đã được cấu hình trên thiết bị; người dùng cần tự xác nhận gửi. Chưa có backend, không lưu dữ liệu và không gửi trực tiếp từ website. Các thẻ cá nhân mở ảnh minh họa, không phải liên kết ứng dụng đã triển khai.

Tác giả: Lê Đức Anh.
