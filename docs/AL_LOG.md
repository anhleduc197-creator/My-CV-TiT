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