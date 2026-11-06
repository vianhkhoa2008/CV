# CV-1.0 - Portfolio Cá Nhân

## 1. Tên dự án
CV-1.0 - Portfolio CV cá nhân

## 2. Mô tả
Dự án này là một trang web portfolio cá nhân được xây dựng bằng HTML5 và CSS3, nhằm giới thiệu thông tin cá nhân, kỹ năng, dự án tiêu biểu và thông tin liên hệ. Trang web được thiết kế theo phong cách hiện đại, tối ưu cho màn hình desktop, tablet và mobile.

Dự án phù hợp để:
- Hiển thị CV/portfolio cá nhân
- Tạo hồ sơ nghề nghiệp trực tuyến
- Dùng làm landing page cá nhân hoặc portfolio cho developer
- Làm mẫu dự án học tập front-end cơ bản

## 3. Chức năng
- Hiển thị phần giới thiệu cá nhân
- Hiển thị thông tin nghề nghiệp, vai trò và mục tiêu
- Thể hiện kỹ năng chuyên môn
- Hiển thị các dự án tiêu biểu dưới dạng card
- Tạo liên kết tới email, GitHub, LinkedIn
- Thiết kế responsive cho nhiều kích thước màn hình
- Tối ưu tốc độ tải và dễ mở trực tiếp trên trình duyệt

## 4. Công nghệ sử dụng
- HTML5
- CSS3
- Flexbox & CSS Grid
- Responsive Design
- Git & GitHub
- Chrome / Edge / Firefox để kiểm tra giao diện

## 5. Cấu trúc thư mục
```text
CV-1.0/
├── index.html
├── README.md
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── img/
│       └── (hình ảnh minh họa, avatar, dự án)
└── .gitignore
```

## 6. Yêu cầu môi trường
Để chạy dự án, bạn cần:

- Một trình duyệt hiện đại: Chrome, Edge, Firefox, Safari
- Máy tính có cài đặt trình duyệt web
- Nếu muốn chạy qua máy chủ local: Node.js hoặc Python (tùy chọn)
- Docker (nếu muốn chạy trong container)

### Yêu cầu tối thiểu
- CPU: 1 core trở lên
- RAM: 512MB trở lên
- Bộ nhớ trống: tối thiểu 100MB
- Hệ điều hành: Windows 10/11, macOS, Linux

## 7. Cài đặt
### 7.1 Cài đặt trên Windows
1. Tải hoặc clone dự án về máy:
```bash
git clone https://github.com/your-username/CV-1.0.git
```
2. Mở thư mục dự án:
```bash
cd CV-1.0
```
3. Mở file `index.html` trực tiếp trong trình duyệt, hoặc sử dụng trình duyệt mở đường dẫn đến thư mục.

### 7.2 Cài đặt trên macOS
1. Mở Terminal.
2. Clone dự án:
```bash
git clone https://github.com/your-username/CV-1.0.git
```
3. Di chuyển vào thư mục:
```bash
cd CV-1.0
```
4. Mở file `index.html` bằng trình duyệt hoặc chạy server local nếu cần:
```bash
python3 -m http.server 8000
```
5. Truy cập:
```text
http://localhost:8000
```

### 7.3 Cài đặt trên Linux
1. Mở Terminal.
2. Clone repository:
```bash
git clone https://github.com/your-username/CV-1.0.git
```
3. Vào thư mục:
```bash
cd CV-1.0
```
4. Mở trực tiếp `index.html` bằng trình duyệt hoặc chạy:
```bash
python3 -m http.server 8000
```
5. Truy cập địa chỉ:
```text
http://localhost:8000
```

## 8. Cấu hình
Dự án hiện tại là site tĩnh, nên cấu hình rất đơn giản.

### Các file cần chỉnh sửa
- `index.html`: nội dung chính của trang CV
- `assets/css/styles.css`: định dạng giao diện, màu sắc, layout, spacing
- `assets/img/`: lưu ảnh đại diện và hình ảnh dự án

### Ví dụ cấu hình phổ biến
- Thay tên, mô tả, email, GitHub, LinkedIn trong `index.html`
- Thay màu chủ đạo trong file `styles.css`
- Thay avatar và ảnh dự án trong thư mục `assets/img/`

## 9. Chạy thử
### Phương án 1: Mở trực tiếp
- Nhấn đúp vào file `index.html`
- Hoặc kéo file vào trình duyệt

### Phương án 2: Chạy local server
#### Với Python
```bash
cd CV-1.0
python3 -m http.server 8000
```
Mở trình duyệt và truy cập:
```text
http://localhost:8000
```

#### Với Node.js (nếu đã cài đặt live-server)
```bash
npx live-server
```

## 10. Hướng dẫn chạy bằng Docker
Nếu bạn muốn chạy dự án trong môi trường container, bạn có thể tạo `Dockerfile` và chạy theo các bước sau.

### 10.1 Tạo Dockerfile
```dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

### 10.2 Build Docker image
```bash
docker build -t cv-1.0 .
```

### 10.3 Chạy container
```bash
docker run -d -p 8080:80 --name cvportfolio cv-1.0
```

### 10.4 Truy cập ứng dụng
```text
http://localhost:8080
```

### 10.5 Dừng container
```bash
docker stop cvportfolio
```

## 11. Kiểm tra và debug
- Kiểm tra xem ảnh có được load đúng không
- Đảm bảo đường dẫn trong HTML đúng với thư mục `assets/`
- Kiểm tra responsive bằng cách mở DevTools và thử các kích thước màn hình khác nhau
- Nếu CSS không áp dụng, kiểm tra lại tên file và link trong `index.html`

## 12. Lưu ý phát triển
- Dự án này là static page nên không cần database
- Nếu muốn mở rộng, có thể tích hợp thêm:
  - Form liên hệ
  - Dark mode
  - Animation
  - Project detail page
  - CMS hoặc React/Vite
- Bạn có thể chuyển đổi dự án sang React hoặc Next.js khi cần phát triển lớn hơn

## 13. Thông tin liên hệ
- Họ tên: Vi Anh Khoa
- Email: an.nguthe817@gmail.com
- GitHub: github.com/vianhkhoa2008
- LinkedIn: linkedin.com/in/vianhkhoa
- Mục tiêu: Frontend Developer / UI Developer / Web Designer

## 14. Giấy phép
Dự án này được cung cấp miễn phí cho mục đích học tập và cá nhân. Nếu bạn muốn sử dụng cho mục đích thương mại, vui lòng liên hệ trước khi triển khai.

## 15. Kết luận
Dự án `CV-1.0` là một trang portfolio cá nhân đơn giản nhưng đầy đủ chức năng giới thiệu bản thân, phù hợp cho người mới học HTML/CSS và muốn tạo mẫu CV trực tuyến. Với hướng dẫn trên, bạn có thể dễ dàng chạy dự án trên Windows, macOS, Linux và Docker.

Nếu bạn muốn, tôi có thể tiếp tục giúp bạn:
- Chuyển đổi giao diện sang dark mode
- Tạo thêm project detail page
- Chuyển sang React/Vite
- Viết Dockerfile và file `.dockerignore` hoàn chỉnh
- Cải thiện UI để trông chuyên nghiệp hơn
