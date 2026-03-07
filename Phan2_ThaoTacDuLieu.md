## Phần 2: Thao tác dữ liệu (INSERT, UPDATE, DELETE)
*(Lưu ý: Sinh viên Tester cần chạy các câu lệnh dưới dạng giao dịch hoặc trên DB ảo để kiểm thử)*

Câu 1: Thêm một diễn viên mới (first_name: 'JOHN', last_name: 'CENA') vào bảng actor.
Câu 2: Thêm một danh mục phim mới (name: 'Vietnamese Cinema') vào bảng category.
Câu 3: Thêm một ngôn ngữ mới tên là 'Vietnamese' vào bảng language.
Câu 4: Thêm một thành phố mới ('Da Nang') liên kết với quốc gia Việt Nam (country_id tương ứng).
Câu 5: Tạo một nhân viên mới trong bảng staff (chỉ điền các trường bắt buộc first_name, last_name, store_id, address_id, username).
Câu 6: Thêm 3 diễn viên cùng lúc bằng một câu lệnh INSERT.
Câu 7: Bổ sung khách hàng mới 'Nguyen Van A' thuộc cửa hàng (store_id) số 1.
Câu 8: Thêm một địa chỉ mới cho thành phố (city_id) số 1.
Câu 9: Thêm một bộ phim mới với tên 'TESTER MOVIE', ngôn ngữ số 1, thời lượng 100.
Câu 10: Nhập thông tin thanh toán (payment) 5.00$ cho nhân viên 1, khách hàng 1.
Câu 11: Cập nhật tên của diễn viên có họ 'CENA' thành 'JOHNNY'.
Câu 12: Đổi tên danh mục 'Vietnamese Cinema' thành 'Asia Cinema'.
Câu 13: Cập nhật thời lượng phim 'TESTER MOVIE' lên 120 phút.
Câu 14: Tăng giá thuê (rental_rate) của tất cả các phim thuộc rating 'G' thêm 0.5$.
Câu 15: Cập nhật trạng thái activebool = false cho khách hàng có email 'nguyen.van.a@test.com'.
Câu 16: Thay đổi số điện thoại (phone) của địa chỉ có address_id = 5 thành '0123456789'.
Câu 17: Chuyển cửa hàng (store_id) quản lý khách hàng số 10 sang cửa hàng số 2.
Câu 18: Đổi họ của tất cả diễn viên có tên 'PENELOPE' thành 'CRUZ'.
Câu 19: Cập nhật ngày tạo (create_date) của khách hàng số 50 bằng ngày hiện tại (CURRENT_DATE).
Câu 20: Tăng phí thay thế (replacement_cost) lên 10% đối với các phim dài quá 150 phút.
Câu 21: Đóng tài khoản (active = 0) của những khách hàng chưa từng thanh toán.
Câu 22: Cập nhật null cho mô tả (description) của phim có mã phim (film_id) là 10.
Câu 23: Tạm ngừng nhân sự (active = false) đối với nhân viên có username là 'Jon'.
Câu 24: Thiết lập tất cả mật khẩu nhân sự về rỗng (nếu hệ thống cho phép null pass).
Câu 25: Đổi múi giờ last_update của mọi dòng trong bảng actor thành thời gian hiện tại.
Câu 26: Cập nhật giá trị tiền (amount) thành 0 cho hóa đơn thanh toán nhầm (payment_id = 15).
Câu 27: Định lại mã ngôn ngữ gốc (original_language_id) cho bản phim 'TESTER' bằng mã của 'Vietnamese'.
Câu 28: Đổi district của tất cả địa chỉ ở 'Texas' thành 'TX'.
Câu 29: Sửa rental_duration lên 5 ngày đối với toàn bộ phim có thuê rate = 0.99.
Câu 30: Hãy vô hiệu hóa ngay (active = 0) 10 khách hàng có customer_id lớn nhất.
Câu 31: Xóa bộ phim giả lập 'TESTER MOVIE' ra khỏi bảng film (lưu ý sẽ lỗi khóa ngoại).
Câu 32: Xóa thanh toán bị lỗi có khung giá là 0$.
Câu 33: Phục hồi lại dữ liệu bằng lệnh Xoá (DELETE) những diễn viên tên 'JOHNNY CENA'.
Câu 34: Xóa toàn bộ nhật ký thuê đĩa (rental) của khách hàng 'Nguyen Van A'.
Câu 35: Hủy đăng ký (Xóa khách hàng) đối với các customer không hoạt động (active = 0) trước năm 2006. (Giao dịch giả định).
Câu 36: Gỡ bỏ ảnh diện (picture) của toàn bộ staff.
Câu 37: Trừ (Xóa) danh mục 'Asia Cinema' khỏi bảng category.
Câu 38: Xoá địa chỉ có mã address_id = 999.
Câu 39: Loại các nhân viên không có (NULL) email.
Câu 40: Xóa các thông tin inventory của store_id 2.
Câu 41: Viết kịch bản thêm một đĩa (inventory) cho film 5 vào store 1, rồi cập nhật nó sang film 6, cuối cùng xóa nó.
Câu 42: Hãy đổi toàn bộ tên quận 'Hanoi' thành 'Ha Noi' trong address, sau đó xóa những địa chỉ không thuộc Ha Noi mới thêm.
Câu 43: Thêm cột `is_tested` boolean vào bảng (chỉ trên logic test schema).
Câu 44: Update song song 2 cột first_name và last_name cho diễn viên có actor_id = 1.
Câu 45: Thực hiện UPDATE giá trị amount=amount-1 cho toàn bộ payment trong tháng 5/2022 (giảm giá bù lỗi).
Câu 46: Thêm 1 giao dịch thuê (rental), sau đó ngay lập tức (return_date) cấp nhật ngày trả.
Câu 47: Tìm và xóa dòng city tên không hợp lệ chứa chuỗi '!@#'.
Câu 48: Làm sạch (Delete) những quốc gia không có tên (country = '').
Câu 49: Trừ đi phí dịch vụ bằng lệnh update payment_id=xxx với amount âm.
Câu 50: Xóa tất cả các logs rental_date vượt quá hiện tại.