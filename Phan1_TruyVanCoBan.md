# Phần 1: Truy vấn cơ bản (SELECT, WHERE, ORDER BY, LIMIT)

Câu 1: Lấy danh sách tất cả các khách hàng (customer) có trong hệ thống.
Câu 2: Hiển thị tên (first_name) và họ (last_name) của tất cả các diễn viên (actor).
Câu 3: Hiển thị tên phim (title), mô tả (description) và năm phát hành (release_year) của tất cả các phim.
Câu 4: Lấy danh sách email của tất cả nhân viên (staff) trong cửa hàng.
Câu 5: Liệt kê các quốc gia (country) đang được lưu trữ trong danh mục.
Câu 6: Lấy danh sách tên thành phố (city).
Câu 7: Lấy toàn bộ thông tin địa chỉ (address, district, postal_code) từ bảng address.
Câu 8: Hiển thị danh sách các ngôn ngữ (name) của bộ phim.
Câu 9: Hiện tên và họ khách hàng, gộp lại thành một cột bí danh là "Ho_Ten".
Câu 10: Hiển thị tên phim và phí thuê (rental_rate), đặt bí danh cho rental_rate là "Phi_Thue".
Câu 11: Tìm danh sách khách hàng thuộc cửa hàng có store_id = 1.
Câu 12: Tìm các bộ phim có thời lượng (length) chuẩn là 120 phút.
Câu 13: Lấy danh sách các diễn viên có tên (first_name) là "PENELOPE".
Câu 14: Lấy danh sách các khách hàng đang bị khóa tài khoản (activebool = false hoặc active = 0).
Câu 15: Tìm các quản lý cửa hàng (manager_staff_id) thuộc store_id = 2.
Câu 16: Tìm các bộ phim có đánh giá (rating) là 'R'.
Câu 17: Hiển thị các khoản thanh toán (payment) có số tiền (amount) lớn hơn 5.00.
Câu 18: Lấy danh sách khách hàng được tạo tài khoản (create_date) đúng vào ngày '2006-02-14'.
Câu 19: Tìm các bộ phim có phí thay thế (replacement_cost) dưới 15.00.
Câu 20: Lấy danh sách các phim có thời gian cho thuê (rental_duration) bằng 3 ngày.
Câu 21: Tìm các khách hàng có tên họ (last_name) bắt đầu bằng chữ 'S'.
Câu 22: Tìm khách hàng có email chứa đuôi '@sakilacustomer.org'.
Câu 23: Lấy danh sách diễn viên có họ (last_name) chứa chuỗi 'SON'.
Câu 24: Tìm các phim mà tiêu đề (title) có kết thúc bằng chữ 'T'.
Câu 25: Tìm các khu vực (district) có tên chứa từ 'California'.
Câu 26: Lấy danh sách phim có chi phí thuê (rental_rate) từ 2.99 đến 4.99.
Câu 27: Tìm các phim có thời lượng (length) nằm trong khoảng từ 90 đến 120 phút.
Câu 28: Tìm danh sách thanh toán được thực hiện trong tháng 2 năm 2007.
Câu 29: Tìm những khách hàng thuộc nhóm store_id 1 HOẶC store_id 2.
Câu 30: Liệt kê diễn viên có họ (last_name) là 'NICKSON' hoặc 'GUINESS'.
Câu 31: Lấy các bộ phim có xếp hạng (rating) thuộc nhóm ('G', 'PG', 'PG-13').
Câu 32: Liệt kê các địa chỉ không thuộc khu vực (district) 'Texas'.
Câu 33: Lấy thông tin khách hàng có store_id = 1 VÀ đang hoạt động (active = 1).
Câu 34: Tìm các phim có giá thuê (rental_rate) > 3.00 VÀ thời lượng (length) > 100.
Câu 35: Tìm các khoản thanh toán của khách hàng có customer_id = 5 lớn hơn mức 2.00.
Câu 36: Lấy danh sách diễn viên, sắp xếp theo tên (first_name) chữ cái A-Z.
Câu 37: Lấy danh sách phim, sắp xếp theo thời lượng (length) giảm dần.
Câu 38: Liệt kê 10 bộ phim có thời lượng dài nhất.
Câu 39: Hiển thị 5 khách hàng được tạo tài khoản mới nhất.
Câu 40: Lấy danh sách 15 khoản thanh toán có giá trị (amount) cao nhất.
Câu 41: Lấy danh sách 20 bộ phim có giá thuê (rental_rate) rẻ nhất.
Câu 42: Hiển thị các địa chỉ, sắp xếp khu vực (district) theo bảng chữ cái.
Câu 43: Liệt kê email khách hàng, sắp xếp thư tự ngược alphabe (Z-A).
Câu 44: Hãy lấy 5 phim đầu tiên sau khi đã bỏ qua (OFFSET) 10 phim ngắn nhất.
Câu 45: Liệt kê danh sách các diễn viên, bỏ qua 50 người đầu, lấy 10 người tiếp theo.
Câu 46: Tìm phim không có mô tả (description bị NULL).
Câu 47: Tìm khách hàng chưa đăng ký email (email là NULL hoặc rỗng).
Câu 48: Lấy danh sách duy nhất (DISTINCT) các mức phí thuê (rental_rate) của phim.
Câu 49: Hiển thị danh sách các năm phát hành (release_year) duy nhất của các phim trong hệ thống.
Câu 50: Lấy ra các khu vực (district) duy nhất từ bảng địa chỉ nơi có cửa hàng.