## Phần 5: Liên kết bảng (JOIN)
*(Các câu hỏi ở mức độ Test Data Integration - Kiểm tra tính toàn vẹn liên kết)*

Câu 1: Lấy tên và họ khách hàng (customer) kèm theo tên cửa hàng (store / hoặc manager_staff_id) mà họ là thành viên (INNER JOIN).
Câu 2: Hiển thị tên đầy đủ khách hàng cùng chi tiết địa chỉ (address) nơi họ sống.
Câu 3: Xem các thông tin district từ address thông qua city của mỗi cư dân.
Câu 4: Lấy danh sách thành phố (city) và nối sang xem tên quốc gia (country) của thành phố đó.
Câu 5: Xuất danh sách phim (film) cùng với tên danh mục (category) của chúng qua hai phép nối.
Câu 6: In ra bảng kết hợp họ tên diễn viên (actor) đóng các bộ phim (film). (Nối 3 bảng).
Câu 7: Tìm ra email của từng người đã mượn (rental_id=123) bảng rental liên kết với customer.
Câu 8: Ghép cặp nhân viên (staff) với cửa hàng (store) của chính nhân sự đó.
Câu 9: In ra họ tên khách hàng thực hiện mã payment_id = 50 thông qua JOIN.
Câu 10: Xem số hóa đơn thanh toán (payment) đã đi với kho (rental - inventory - film) như thế nào về tiêu đề bộ phim.
Câu 11: LEFT JOIN bảng film với inventory để tìm các bộ phim không có đĩa trong cửa hàng (IS NULL).
Câu 12: Tìm các thể loại (category) chưa hề được đính kèm vào bộ phim nào (LEFT JOIN).
Câu 13: Cập nhật hóa lịch sử: Bảng rental liên kết payment, hiện các giao dịch không tạo hóa đơn.
Câu 14: Những diễn viên (actor) nào không có bản ghi xuất hiện trong film_actor?
Câu 15: Có địa chỉ (address) nào chưa từng được gắn cho vị khách (customer) nào chưa? (LEFT JOIN).
Câu 16: Liên kết bảng city với country, in ra các quốc gia không có city nào bị ánh xạ.
Câu 17: Xem thống kê tổng amount (payment) trên mỗi khu vực (district - từ address v.v). (Nối customer -> address -> district).
Câu 18: Kết nối danh sách cửa hàng store lấy họ tên người quản lý manager.
Câu 19: Bộ phim "ACADEMY DINOSAUR" có những diễn viên họ tên nào góp mặt?
Câu 20: Tên cửa hàng và thông tin địa chỉ cửa hàng qua table store x address.
Câu 21: Tìm các tập khách hàng cùng một khu vực district bằng cách dùng kĩ thuật Self Join.
Câu 22: Lấy các lượt thuê từ ngày 1/5/2005 kéo chi tiết khách hàng và nhân viên phụ trách.
Câu 23: Join film và language để xem bảng phim đó ngôn ngữ name là gì.
Câu 24: Liệt kê chi tiết khách hàng đã trả rental khoản "payment_p2022_01" và chi phí.
Câu 25: Xem diễn viên "PENELOPE GUINESS" đã đóng tổng số những phim gì qua JOIN.
Câu 26: Tìm cặp diễn viên (actor_id 1 và actor_id 2) đóng chung 1 bộ phim (Self-Join ghép 2 film_actor).
Câu 27: JOIN payment với customer để tính tổng chi phí chia theo từng Email.
Câu 28: Đưa danh mục phim (category.name) đứng cạnh thành tích tổng doanh số (payment amount qua kết nối đa bảng).
Câu 29: Nhân sự staff (Mike) ghi ra bao nhiêu giao dịch payment từ khách tên 'MARY'.
Câu 30: Số lượng rental có kết tình trạng tồn kho chưa return được store 1 giữ lại.
Câu 31: Khớp bảng Payment các vùng chứa với thông tin Rental đối ứng bằng FULL OUTER JOIN.
Câu 32: Đưa ra top 5 phim mượn nhiều nhất bằng cách INNER JOIN film với inventory và rental.
Câu 33: Tên Khách hàng nào sở hữu nhiều địa điểm thuê đĩa qua hai chi nhánh nhất.
Câu 34: Tìm các address chưa cấu hình city chuẩn xác (mất liên kết).
Câu 35: Lấy chuỗi film có số lượng actor nhiều thứ hai bằng cách Join.
Câu 36: Giao dịch phân quyền: Liệt kê rental_id của bộ "ALABAMA DEVIL" được thực hiện lúc cuối tháng.
Câu 37: RIGHT JOIN cho danh sách những address chưa dùng đến ở bảng Store.
Câu 38: Tìm tên (title) những bộ sưu tập Film cùng loại language 1 nhưng chưa được nhập kho.
Câu 39: JOIN bảng phân vùng payment_p2022_02 với Khách hàng xem hóa đơn ngày Valantine 14/2.
Câu 40: Tìm tất cả phim nằm ở nhóm 'Action' và hiển thị giá gốc phim bằng 4 bảng nối lại.
Câu 41: Khách hàng nào cư trú tại "Viet Nam" theo quy trình nối Country > City > Address > Customer?
Câu 42: Các phim có hạng R đang được ai giữ (chưa return_date). Nối dài film > inventory > rental > customer.
Câu 43: Liệt kê các store chứa phim có tên Theatrical theo từng location.
Câu 44: Tìm số trùng giữa khách hàng cũ (đã delete ảo) nhưng chi tiêu payment.
Câu 45: Liên kết 4 bảng để tìm danh sách tổng hợp Customer Names đã đặt phim của Actor 'NICKSON'.
Câu 46: Xem nhân sự thu tiền Staff name khác tên người làm Staff rental như thế nào trong chuỗi giao dịch số 120.
Câu 47: Tìm khách hàng cùng city với khách đang có email 'JERRY.FORSYTHE@sakilacustomer.org' (Self-JOIN vs Sub).
Câu 48: Danh sách các hóa đơn trả 2$ nhưng trị giá phim gốc lên tới 30$.
Câu 49: Khách tại các quận district 'California' thuê category nào nhiều nhất?
Câu 50: Xem tỷ lệ thất thoát đĩa mất nối bảng Inventory và Film không khớp thông tin.