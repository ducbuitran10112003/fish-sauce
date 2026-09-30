VAN DAO BEP THAN LOYALTY V2.4

Bản này chuyển Loyalty và bổ sung lớp visual polish/interaction. thành một landing page cuộn một trang + dashboard riêng.

Cấu trúc:
- index.html: landing page chính, gồm Hero -> 3 bước -> hạng -> tích điểm -> kho quà/voucher -> khảo sát -> hình ảnh bếp Việt.
- bep-cua-toi.html: dashboard thành viên riêng.
- hang-thanh-vien.html: trang chi tiết 3 hạng.
- assets/: CSS, JS, logo và hình ảnh sản phẩm/ẩm thực.

Luồng đăng ký:
- Họ tên + số điện thoại ở bước 1.
- Bước 2 mô phỏng OTP với mã 123456.
- Không yêu cầu mật khẩu.
- Đăng ký demo cộng +20 V-Point và lưu trên trình duyệt.

Luồng khảo sát:
- Chỉ có một khảo sát dạng modal, không lặp lại trên dashboard.
- 8 câu theo bộ câu hỏi đã cung cấp.
- Bản prototype cộng +30 V-Point khi hoàn thành; tài liệu gốc chưa chốt điểm khảo sát nên có thể đổi trước khi vận hành thật.

Google Sheets:
- Google Sheet mục tiêu: https://docs.google.com/spreadsheets/d/1Cym3AYhO9HJXMdmrZ1T0GTbMrLgClqPA5kRNXDI6_6w/edit?gid=0#gid=0
- Google Sheet URL không tự hoạt động như API. Cần tạo Google Apps Script Web App /exec rồi điền URL vào SHEET_API_URL trong assets/loyalty.js.

Redemption:
- 250ml: 1.000 V-Point
- 500ml: 1.800 V-Point
- Hộp Quà Gỗ 2 x 500ml: 3.800 V-Point
Các mức trên là cơ chế loyalty thử nghiệm theo tỷ lệ 1 điểm = 10đ, không phải tuyên bố giá trị tiền mặt của sản phẩm.


V2.4 visual polish:
- Typography ưu tiên Segoe UI / Noto Sans để hiển thị tiếng Việt ổn định hơn trên Windows, không phụ thuộc font web ngoài.
- Modal có fade + scale transition, khóa scroll khi mở, hỗ trợ Escape/click nền để đóng.
- Nút/card có hover/active/focus state mềm hơn.
- Hero chuyển ảnh mượt hơn và tạm dừng khi tab không hoạt động.
- Navigation có trạng thái active và hiệu ứng underline.
- Scroll reveal nhẹ hơn và hỗ trợ prefers-reduced-motion.
- Dashboard đồng bộ cập nhật điểm/hạng khi localStorage thay đổi trong phiên.
