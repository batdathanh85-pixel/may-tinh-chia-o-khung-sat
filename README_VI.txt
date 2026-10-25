MÁY TÍNH CHIA Ô KHUNG SẮT — PWA DÙNG NGOẠI TUYẾN

Trong thư mục có:
- index.html: giao diện máy tính
- manifest.webmanifest: thông tin để thêm vào màn hình chính
- sw.js: lưu ứng dụng vào bộ nhớ đệm để dùng ngoại tuyến
- icons/: biểu tượng ứng dụng

QUAN TRỌNG
Để Chrome Android cho thêm vào màn hình chính như một ứng dụng và chạy ngoại tuyến, cần đưa các tệp này lên một địa chỉ HTTPS (ví dụ GitHub Pages). Không mở trực tiếp index.html từ thư mục Tải xuống, vì chế độ cài PWA/service worker thường không hoạt động với file://.

CÁCH ĐƯA LÊN GITHUB PAGES (miễn phí)
1. Trên điện thoại hoặc máy tính, mở https://github.com/ và đăng nhập/tạo tài khoản.
2. Tạo repository mới (New repository). Đặt tên ví dụ: may-tinh-chia-o-khung-sat. Chọn Public, rồi Create repository.
3. Trong repository, chọn Add file > Upload files.
4. Giải nén ZIP này trước. Tải LÊN CÁC TỆP BÊN TRONG thư mục may_tinh_chia_o_khung_sat_pwa, không tải nguyên thư mục lồng bên trong. Đảm bảo index.html nằm ngay ở thư mục gốc repository; cùng cấp có manifest.webmanifest, sw.js và thư mục icons.
5. Chọn Commit changes.
6. Vào Settings > Pages. Ở phần Build and deployment, chọn Deploy from a branch.
7. Chọn Branch: main và folder: /(root), rồi Save.
8. Chờ GitHub tạo trang. Địa chỉ thường có dạng https://TEN-TAI-KHOAN.github.io/may-tinh-chia-o-khung-sat/ . Hãy dùng đúng URL GitHub Pages hiển thị trong Settings > Pages.

CÁCH THÊM VÀO MÀN HÌNH CHÍNH ANDROID
1. Bật mạng và mở URL GitHub Pages bằng Chrome.
2. Chờ trang máy tính tải hoàn toàn; bấm Tính phương án thử một lần.
3. Bấm dấu ba chấm ⋮ trong Chrome.
4. Chọn “Cài đặt ứng dụng” hoặc “Thêm vào màn hình chính” (tên mục tùy phiên bản Chrome).
5. Xác nhận Cài đặt/Thêm.
6. Mở biểu tượng “Chia ô sắt” ở màn hình chính. Sau khi trang đã tải và service worker lưu thành công, ứng dụng có thể mở khi không có mạng.

KIỂM TRA NGOẠI TUYẾN
- Mở ứng dụng khi đang có mạng ít nhất một lần và chờ tải xong.
- Đóng ứng dụng, tắt Wi-Fi/dữ liệu di động rồi mở lại biểu tượng.
- Nếu chưa hoạt động offline: bật mạng, mở lại URL, tải lại trang một lần, đợi vài giây rồi thử lại.

CẬP NHẬT SAU NÀY
Nếu sửa các tệp, tải phiên bản mới lên GitHub. Đã tăng CACHE_NAME trong sw.js thành phiên bản mới (ví dụ chia-o-khung-sat-v2) để buộc làm mới bộ nhớ đệm. Trên điện thoại, mở ứng dụng khi có mạng để nhận bản mới.
