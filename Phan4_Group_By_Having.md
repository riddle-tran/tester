## Phần 4: Nhóm dữ liệu (GROUP BY & HAVING)

Câu 1: Đếm số lượng khách hàng thuộc về mỗi store_id.
Câu 2: Nhóm số lượng bộ phim theo mỗi loại xếp hạng (rating - G, PG, R...).
Câu 3: Đếm số lượng thành phố có ở mỗi country_id.
Câu 4: Tính tổng số tiền thu được do mỗi nhân viên (staff_id) phụ trách trong bảng payment.
Câu 5: Xem mỗi khách hàng (customer_id) đã tổng chi tiêu bao nhiêu tiền.
Câu 6: Đếm xem mỗi khách hàng đã có bao nhiêu lượt thuê đĩa (rental_id).
Câu 7: Thời lượng phim trung bình của mỗi loại rating.
Câu 8: Tổng giá phí (rental_rate) đối với từng giới hạn thuê (rental_duration).
Câu 9: Đếm số lượng đĩa (inventory_id) theo mỗi store_id trong kho.
Câu 10: Xem bộ phim nào được phân vào bao nhiêu inventory khác nhau.
Câu 11: Đếm số diễn viên góp mặt trong mỗi bộ phim (film_id) ở bảng film_actor.
Câu 12: Đếm số bộ phim thuộc từng thể loại (category_id) tại bảng film_category.
Câu 13: Thống kê số lượng địa chỉ ở từng quận (district).
Câu 14: Chỉ hiển thị các quận (district) có trên 5 địa chỉ. (Sử dụng HAVING).
Câu 15: Hiển thị các khách hàng (customer_id) có tổng số tiền chi trên 100$.
Câu 16: Hiển thị những nhân viên thu thập trên 50 hóa đơn thanh toán.
Câu 17: Chỉ in ra những rating phim có thời lượng trung bình lớn hơn 115 phút.
Câu 18: Lọc ra các store (store_id) quản lý trên 250 khách hàng.
Câu 19: Tìm khách hàng thực hiện quá 30 lần rental.
Câu 20: Phân nhóm phim theo release_year và đếm số bộ phim phát hành trong năm.
Câu 21: Tìm ra country_id có nhiều hơn 10 thành phố bên trong.
Câu 22: Thống kê ngày tháng (rút gọn payment_date ra Date) kiếm được nhiều doanh thu nhất.
Câu 23: Lấy bộ phim sở hữu hơn 5 diễn viên trong film_actor.
Câu 24: Thống kê bảng thanh toán phân vùng payment_p2022_01 theo mỗi ngày (date).
Câu 25: Mỗi staff đã approve bao nhiêu yêu cầu rental (staff_id nhóm rental).
Câu 26: Cho biết customer_id nào có tiền payment amount bé hơn 1.0 trung bình mỗi bill?
Câu 27: Gom nhóm language_id và đếm lượng phim tương ứng.
Câu 28: Nhóm những ngày (rental_date) có số phim được mượn vượt 50 lượt.
Câu 29: Những film_id nào hiện có hơn 4 bản sao trữ trong các cửa hàng? (nhóm bảng inventory).
Câu 30: Cửa hàng nào có tổng phí trả (replacement_cost) kho lớn nhất?
Câu 31: Group By rating và đếm, nhưng dùng HAVING bỏ qua rating 'NC-17'.
Câu 32: Đếm lượng hóa đơn payment chia theo customer_id VÀ staff_id (Nhóm đa cấp).
Câu 33: Liệt kê số tiền thanh toán Min, Max theo từng khách.
Câu 34: Có bao nhiêu lần trùng tên (first_name) ở danh sách các diễn viên? (Hiển thị các tên trên 2 lần).
Câu 35: Trong bảng customer, thống kê số khách hàng Active vs Inactive dựa trên activebool.
Câu 36: Tiền thanh toán gộp trong từng tháng thanh toán payment, HAVING > 1000$.
Câu 37: Chỉ ra những hóa đơn trễ mà (return - rental) > 5. (Trích xuất logic group theo rental).
Câu 38: Nhóm theo category_id chỉ lấy kết quả khi danh mục có hơn 60 bài phim.
Câu 39: District (Khu vực) có doanh thu gộp (cần Join nhưng dùng groupby qua subquery). (Hoặc group district đếm mail).
Câu 40: Nhóm theo độ dài (length) và tìm xem độ dài nào phổ biến nhất (xuất hiện nhiều nhất).
Câu 41: Gom đánh giá thời hạn rental_duration có ít hơn 100 phim.
Câu 42: Các diễn viên (actor_id) tham gia quá 25 phim.
Câu 43: Báo cáo số tiền hóa đơn cao nhất cho từng ngày thu của nhân viên 2.
Câu 44: Xác định khách hàng chỉ có duy nhất 1 lần thanh toán payment = 0.
Câu 45: Nhóm giá thuê thay thế replacement_cost, đếm số phim thuộc nhóm đó HAVING cost > 20.
Câu 46: Tổng hợp doanh số nhóm các khách hàng theo cửa hàng phân cấp 1.
Câu 47: Tìm những năm tạo khách hàng có trên 1 người tham gia (create_date year).
Câu 48: Tính Average (amount) có Group by customer_id và điều kiện Having Sum > 150.
Câu 49: Đếm số bảng film_actor ứng với actor_id, sắp xếp mảng có giảm dần Count.
Câu 50: Tập hợp số giờ mượn trung bình (ngày) gom khách tìm các vị khách thuê chậm nhất (thường xuyên return late).