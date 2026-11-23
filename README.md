# Đức Di Lặc – Chuyển Luân Thánh Vương | Ultra 7.2

Website tĩnh bằng HTML, CSS và JavaScript, có thể triển khai miễn phí bằng GitHub Pages.

## Nội dung chính

- Giao diện chủ đề Đức Di Lặc – Chuyển Luân Thánh Vương, Long Hoa và Núi Cấm.
- Khu vực tiện ích, trì tụng và các thành phần tương tác đã có trong bản Ultra.
- Hệ thống mô phỏng Công đức và Phước đức từ 0 đến 9.000.000.000.000.
- Danh sách 2.000 chức vị Hiền Đức được tạo tự động, kèm sức mạnh và phép thuật biểu tượng theo cấp.
- Dữ liệu điểm được lưu trong LocalStorage của trình duyệt đang sử dụng.

> Lưu ý: Điểm số, chức vị, sức mạnh và phép thuật là nội dung mô phỏng trong website; không phải chứng nhận công đức thực tế, quyền năng siêu nhiên hay thẩm quyền tôn giáo.

## Cấu trúc

```text
.
├── index.html
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml
```

## Chạy thử trên máy

Mở `index.html` bằng trình duyệt hiện đại. Website sử dụng một số tài nguyên CDN như Google Fonts, Font Awesome và Supabase JS nên cần kết nối Internet để tải các tài nguyên đó.

## Đưa website lên GitHub Pages

1. Tạo một repository GitHub mới.
2. Tải toàn bộ nội dung thư mục này lên repository, giữ nguyên đường dẫn `.github/workflows/deploy.yml`.
3. Đảm bảo nhánh mặc định của repository là `main` (hoặc sửa tên nhánh trong `deploy.yml` nếu dùng nhánh khác).
4. Mở **Settings → Pages**.
5. Trong **Build and deployment → Source**, chọn **GitHub Actions**.
6. Đẩy (push) commit lên nhánh `main`, hoặc chạy thủ công workflow **Deploy to GitHub Pages** trong tab **Actions**.
7. Khi workflow chạy thành công, mở **Settings → Pages** hoặc phần Deployments để lấy địa chỉ website.

Workflow dùng các action GitHub Pages chính thức: `actions/checkout`, `actions/configure-pages`, `actions/upload-pages-artifact` và `actions/deploy-pages`.

## Dữ liệu và kết nối

- Điểm công đức/phước đức hiện lưu cục bộ bằng LocalStorage; dữ liệu không tự đồng bộ giữa các thiết bị hoặc trình duyệt.
- Phần kết nối phòng trực tuyến (nếu sử dụng) cần cấu hình dự án Supabase Realtime riêng.
- Chỉ sử dụng Supabase **publishable/anon key** ở phía trình duyệt theo đúng chính sách bảo mật của Supabase. Tuyệt đối không đưa `service_role` key hoặc bí mật quản trị vào mã HTML công khai.
- Không nhập thông tin cá nhân nhạy cảm vào các khu vực thử nghiệm.

## Giấy phép

Chưa chỉ định giấy phép phân phối. Nếu muốn người khác sử dụng, sửa đổi hoặc phân phối lại mã nguồn, hãy bổ sung tệp `LICENSE` phù hợp.
