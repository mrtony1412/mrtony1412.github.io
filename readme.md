# 🔒 Mr. Tony - Ethical Hacker Blog

Website blog kỹ thuật bảo mật tĩnh dành cho ethical hacker, được thiết kế để triển khai dễ dàng trên GitHub Pages.

## 🎯 Tính năng chính

- **Static site** - Không cần backend, hoạt động hoàn hảo với GitHub Pages
- **Tự động phát hiện bài viết** - Chỉ cần thêm file HTML vào thư mục, website tự động cập nhật
- **Responsive design** - Tương thích mọi thiết bị
- **Dark theme** - Thiết kế chuyên nghiệp cho lĩnh vực bảo mật
- **Categories** - Phân loại Exploits, Defense, Pentest Logs
- **Search & Filter** - Tìm kiếm và lọc bài viết dễ dàng

## 📁 Cấu trúc thư mục

```
/
├── index.html              # Trang chủ
├── style.css              # CSS styles (embedded)
├── script.js              # JavaScript logic (embedded)
├── README.md              # Hướng dẫn này
├── /posts/                # Thư mục chứa bài viết
│   ├── /exploits/         # Bài viết về khai thác lỗ hổng
│   ├── /defense/          # Bài viết về phòng thủ
│   └── /pentest-logs/     # Báo cáo pentest
├── /templates/            # Templates mẫu
│   └── post-template.html # Template để tạo bài viết mới
└── /assets/              # Hình ảnh và tài nguyên
    └── images/
```

## 🚀 Triển khai trên GitHub Pages

### Bước 1: Tạo Repository
1. Tạo repository mới trên GitHub với tên `username.github.io` hoặc tên tùy chọn
2. Clone repository về máy local:
```bash
git clone https://github.com/username/your-repo-name.git
cd your-repo-name
```

### Bước 2: Upload Files
1. Copy tất cả files vào thư mục repository
2. Commit và push:
```bash
git add .
git commit -m "Initial website setup"
git push origin main
```

### Bước 3: Kích hoạt GitHub Pages
1. Vào Settings của repository
2. Chọn Pages từ menu bên trái
3. Source: Deploy from a branch
4. Branch: main / (root)
5. Save

Website sẽ có địa chỉ: `https://username.github.io/repo-name`

## ✍️ Cách thêm bài viết mới

### Phương pháp 1: Sử dụng Template (Khuyến nghị)

1. **Copy template:**
```bash
cp templates/post-template.html posts/exploits/my-new-post.html
```

2. **Chỉnh sửa metadata trong `<head>`:**
```html
<title>Tiêu đề bài viết của bạn</title>
<meta name="description" content="Mô tả ngắn gọn">
<meta name="author" content="Mr. Tony">
<meta name="date" content="2025-05-31">
<meta name="category" content="exploit"> <!-- exploit, defense, pentest -->
```

3. **Thêm nội dung vào phần `<div class="post-content">`**

4. **Commit và push:**
```bash
git add posts/exploits/my-new-post.html
git commit -m "Add new exploit post"
git push origin main
```

### Phương pháp 2: Tạo trực tiếp trên GitHub

1. Vào repository trên GitHub
2. Navigate đến thư mục `posts/exploits/` (hoặc thư mục category tương ứng)
3. Click "Add file" > "Create new file"
4. Đặt tên file: `post-name.html`
5. Copy nội dung từ template và chỉnh sửa
6. Commit changes

**Website sẽ tự động cập nhật trong vài phút!**

## 📝 Categories và Thư mục

| Category | Thư mục | Mô tả |
|----------|---------|-------|
| **Exploits** | `/posts/exploits/` | Hướng dẫn khai thác lỗ hổng |
| **Defense** | `/posts/defense/` | Phương pháp bảo vệ hệ thống |
| **Pentest Logs** | `/posts/pentest-logs/` | Báo cáo penetration testing |

## 🎨 Tùy chỉnh giao diện

### Thay đổi thông tin cá nhân
Chỉnh sửa file `index.html`:

```html
<!-- Tìm section About -->
<h3>Nguyễn Lê Toàn (Mr. Tony)</h3>
<p>Thông tin về bản thân...</p>

<!-- Thay đổi thông tin liên hệ -->
<p><strong>Email:</strong> your-email@example.com</p>
```

### Thay đổi màu sắc
Chỉnh sửa CSS variables trong `<style>`:

```css
:root {
    --accent-green: #238636;  /* Màu chính */
    --accent-blue: #1f6feb;   /* Màu phụ */
    --accent-red: #da3633;    /* Màu cảnh báo */
}
```

### Thêm avatar/logo
1. Upload ảnh vào `/assets/images/`
2. Chỉnh sửa class `.avatar` trong CSS
3. Thay đổi emoji thành `<img src="assets/images/avatar.jpg">`

## 🔧 Tính năng nâng cao

### Auto-detection Posts
Website tự động quét các file HTML trong thư mục `/posts/` và hiển thị:
- Tiêu đề từ `<title>` hoặc `<h1>`
- Mô tả từ `meta[name="description"]`
- Ngày từ `meta[name="date"]`
- Category từ `meta[name="category"]`

### Search và Filter
- Tìm kiếm theo tiêu đề và mô tả
- Lọc theo category
- Responsive trên mobile

### Code Highlighting
Sử dụng các class CSS có sẵn:

```html
<div class="code-header">Terminal</div>
<pre><code>nmap -sV target.com</code></pre>
```

### Alert Boxes
```html
<div class="warning-box">Cảnh báo quan trọng</div>
<div class="success-box">Thông tin thành công</div>
<div class="info-box">Thông tin bổ sung</div>
```

## 📊 Thống kê tự động

Website tự động đếm và hiển thị:
- Tổng số bài viết
- Số lượng exploits
- Số lượng pentest reports

## 🛠️ Troubleshooting

### Bài viết không hiển thị
1. Kiểm tra file HTML có đúng syntax không
2. Đảm bảo metadata trong `<head>` đầy đủ
3. Kiểm tra đường dẫn file chính xác
4. Wait 2-3 phút để GitHub Pages rebuild

### GitHub Pages không hoạt động
1. Kiểm tra Settings > Pages đã enable
2
