# My-CV-TiT - Portfolio CV của Lê Đức Anh

## Tên dự án

**My-CV-TiT** là trang CV và portfolio cá nhân của Lê Đức Anh, định hướng Frontend Developer.

## Mô tả

Dự án là một website tĩnh, giới thiệu thông tin cá nhân, kỹ năng, các dự án tiêu biểu và cách liên hệ. Giao diện được xây dựng theo hướng responsive để sử dụng trên điện thoại, máy tính bảng và máy tính. Nội dung trang được viết trực tiếp trong HTML và kiểu dáng được quản lý bằng một tệp CSS riêng.

## Chức năng

- Điều hướng đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ ngay trên một trang.
- Hiển thị ảnh đại diện, thông tin giới thiệu và danh sách kỹ năng.
- Trình bày bốn dự án dưới dạng thẻ có ảnh, mô tả và nhãn công nghệ.
- Bố cục dự án tự thay đổi theo kích thước màn hình: một cột trên màn hình nhỏ, hai cột từ 768px và ba cột từ 1280px.
- Cung cấp liên kết email để liên hệ và nút quay về đầu trang.

> Các thẻ dự án hiện chỉ là nội dung giới thiệu tĩnh; một số liên kết chi tiết và hồ sơ mạng xã hội vẫn là liên kết placeholder (`#`).

## Công nghệ

- HTML5
- CSS3: Flexbox, CSS Grid, custom properties, media queries và hỗ trợ `prefers-reduced-motion`
- Python 3 (tùy chọn, chỉ dùng máy chủ HTTP đơn giản để xem thử)
- Docker và Nginx (tùy chọn, để chạy website trong container)

Trang hiện không cần JavaScript, Node.js, npm, cơ sở dữ liệu hoặc dịch vụ backend.

## Yêu cầu môi trường

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để chạy máy chủ xem thử: Python 3. Nếu chỉ mở trực tiếp `index.html`, không cần cài Python.
- Để chạy bằng Docker: Docker Engine hoặc Docker Desktop đang hoạt động. Lần chạy đầu cần truy cập Internet để tải image `nginx:alpine`.

## Cài đặt

Tải mã nguồn hoặc clone repository về máy. Nếu đã có URL repository, thay `<URL-repository>` bằng URL đó:

```bash
git clone <URL-repository> My-CV-TiT
cd My-CV-TiT
```

Không cần cài thư viện hay chạy lệnh build. Nếu mã nguồn đã được tải về, mở terminal tại thư mục gốc của dự án, nơi chứa `index.html`.

## Cấu hình

Dự án không có bước cấu hình môi trường và không sử dụng tệp `.env`.

- Nội dung, tiêu đề và liên kết được chỉnh sửa trong `index.html`.
- Kiểu dáng và breakpoint responsive được chỉnh sửa trong `assets/css/styles.css`.
- Ảnh nằm trong `assets/css/img/`. Khi thay ảnh, cập nhật đường dẫn `src` tương ứng trong `index.html` và giữ đúng tên tệp.
- Trước khi đưa trang lên sử dụng, hãy thay các liên kết placeholder bằng URL dự án và hồ sơ thực tế.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có trên máy, thử `python -m http.server 8000`.

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

### Linux

Mở terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Sau khi máy chủ khởi động, mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`. Nếu không muốn dùng máy chủ cục bộ, có thể mở trực tiếp tệp `index.html` trong trình duyệt.

### Kiểm tra nhanh

- Thử các mục điều hướng và nút trên trang để xác nhận chúng cuộn đến đúng phần.
- Kiểm tra ảnh đại diện và ảnh dự án có tải thành công.
- Thu nhỏ cửa sổ hoặc dùng chế độ thiết bị di động của trình duyệt để kiểm tra bố cục responsive.
- Nhấn liên kết email để xác nhận trình duyệt mở ứng dụng email mặc định.

Dự án hiện chưa có bộ kiểm thử tự động.

## Chạy bằng Docker

Các lệnh dưới đây cần được chạy tại thư mục gốc dự án và yêu cầu Docker đang hoạt động. Chúng dùng Nginx để phục vụ trực tiếp các tệp tĩnh, không cần tạo image riêng.

### Windows PowerShell

```powershell
docker run --rm -d --name my-cv-tit -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

### Windows Command Prompt (CMD)

```cmd
docker run --rm -d --name my-cv-tit -p 8080:80 -v "%cd%:/usr/share/nginx/html:ro" nginx:alpine
```

### macOS và Linux

```bash
docker run --rm -d --name my-cv-tit -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080> để xem trang. Dừng container bằng:

```bash
docker stop my-cv-tit
```

Nếu cổng `8080` đang được sử dụng, đổi phần `8080:80` thành một cổng trống khác, ví dụ `8081:80`, rồi mở cổng tương ứng trên trình duyệt.

## Thông tin liên hệ

- **Tên:** Lê Đức Anh
- **Email:** [anhleduc197@gmail.com](mailto:anhleduc197@gmail.com)
- **GitHub:** [github.com/anhleduc197-creator](https://github.com/anhleduc197-creator)
- **LinkedIn:** linkedin.com/in/leduc (cần cập nhật liên kết đích trong trang)
