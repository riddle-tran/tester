## Phần 6: Truy vấn nâng cao & Tổng hợp
*(Các cấu trúc subquery, tổng hợp nâng cao để review Data Architecture Validation)*

Câu 1: Lấy danh sách tên khách hàng có số tiền thanh toán trên một bill (amount) lớn hơn giá trị payment trung bình của toàn hệ thống.
Câu 2: Dùng truy vấn lồng (Subquery) tìm các bộ phim không nằm trong danh sách xếp hạng 'G'.
Câu 3: Viết câu lệnh SELECT lấy danh sách diễn viên đóng trong một bộ phim cụ thể (dùng IN kết hợp subquery, không dùng JOIN).
Câu 4: Liệt kê khách hàng có lượt thuê rental cao hơn khách hàng có id số 10.
Câu 5: Tìm các khu vực (district) nằm trong bảng address nhưng chưa từng có khách hàng (customer).
Câu 6: Subquery tại SELECT: Hiện thị tên phim và tính toán phần trăm rental_rate trên cột lớn nhất max(rental_rate).
Câu 7: Dùng toán tử EXISTS để lọc ra các staff đã xử lý ít nhất một giao dịch có số tiền = 0.
Câu 8: Tạo bảng tạm thời (CTE) tính Sum payment và lấy ra top khách chi nhiều nhất.
Câu 9: Tìm các thành phố thuộc một quốc gia cụ thể "Vietnam" bằng câu lệnh Subquery ở mệnh đề FROM.
Câu 10: Xây dựng truy vấn trả ra số dư bill tháng 1 kết hợp dùng truy vấn Window function (ROW_NUMBER) chia xếp hạng theo user.
Câu 11: Hãy áp dụng UNION để lấy ra tập hợp chung các email từ bảng customer và email từ bảng staff.
Câu 12: Dùng lệnh UNION ALL gộp tên các bộ phim có length = 90 và name các category_id = 2.
Câu 13: EXCEPT (trừ tập hợp): Chọn ra thành phố có trong danh sách bảng gốc mà không mang address nào.
Câu 14: Sinh chuỗi truy vấn phức hợp để tìm ra 5 tựa phim mang lại lợi nhuận dồi dào nhất năm tính theo số hóa đơn thanh toán.
Câu 15: Tạo CTE xử lý trung bình thuê của từng Store và so sánh với nhau lệch chuẩn bao nhiêu bảng.
Câu 16: Window Rank(): Xếp thứ tự giá hóa đơn payment từ lớn xuống bé chia phân nhóm (partition by) theo customer_id.
Câu 17: Window Dense_Rank(): Liệt kê bảng xếp hạng khách hàng theo giá chi trả mua ở các branch nhưng cho phép đồng hạng.
Câu 18: Lấy lượng khách có tên lặp âm đầu như "A%" nhưng tổng payment cao hơn mức của khách VIP "Z%".
Câu 19: Tìm khách thực hiện lệnh giao dịch Rental nhưng người thu ngân không phải người đại diện Store số 1.
Câu 20: Viết subquery tính số lượng diễn viên của Theatrical theo từng film > 20.
Câu 21: Tạo truy vấn WITH rút gọn khách hàng thân thiết (> 40 rental) và cập nhật báo cáo địa chỉ của họ.
Câu 22: Sử dụng CASE WHEN trong hệ SELECT: Nếu amount > 5 xuất "High", amount < 2 "Low", còn lại hiển thị "Normal".
Câu 23: Làm truy vấn đếm SUM lượng diễn viên tham gia bằng CASE WHEN đối chiếu rating.
Câu 24: Tính luồng Rolling Sum doanh thu Payment theo thời gian payment_date.
Câu 25: Nối bảng đa vòng lấy kết quả: Những Customer mượn Film nhóm Category Action với cost tối thiểu 3.00.
Câu 26: Tìm phim nào mà không một khách ở "London" nào chọn xem 1 lần.
Câu 27: Truy xuất Subquery lồng 3 cấp để đọc Customer > Rental_id của bảng staff tên 'Jon'.
Câu 28: Chia nhóm thống kê 2 khoảng tiền Replacement Cost và đếm Customer (Thống kê ma trận dọc ngang Pivot bằng Case When).
Câu 29: Báo cáo xem tỉ số trả nợ chậm Return date so với rental Duration là bao nhiêu phần trăm (Tính % hoàn hảo).
Câu 30: Chọn danh sách Film có chứa chuỗi "Trailers" và không nằm trong các bộ phim ngắn hơn vòng lặp Subquery Avg.
Câu 31: Viết truy vấn chia rổ percentile (NTILE) các chi phí Amount bảng thanh toán.
Câu 32: Dùng CTE kiểm chứng đĩa mất (Inventory vs Rented so sánh với bảng Not Returned).
Câu 33: Tính lãi giả định (Amount - Replacement cost) cho mỗi cửa hàng để in báo cáo KPI.
Câu 34: Lọc Film trùng lặp description với chính những film khác qua Self Join kèm Logic giống nhau của Like.
Câu 35: Lấy chuỗi JSON Aggregation nối mảng String của các bộ Name Categories theo ID Film .
Câu 36: Tính các hàm Coalesce xử lý NULL dữ liệu trường Address2 về thông tin cố định khi thống kê.
Câu 37: Lọc ra chi nhánh nào đạt số doanh thu từ Payment_P2022_01 cao hơn các chi nhánh còn lại qua All Subqueries.
Câu 38: Tìm Country_id có số lượng City biến thiên gấp đôi trung bình của List Country khác.
Câu 39: Tìm diễn viên nào bị phàn nàn vì không bao giờ được xuất hiện trong các đánh giá View rate 'R' .
Câu 40: Dùng Any/Some kiểm tra giá thuê > mọi rate phim cũ năm 2005.
Câu 41: Gom báo cáo theo 3 Store sử dụng CTE và UNION All.
Câu 42: Sử dụng truy vấn hàm nội suy (LAG/LEAD) xét chi phí giao dịch Payment hôm trước so với doanh số hôm sau.
Câu 43: Tính khoảng cách số ngày kể từ ngày thuê rental trước tới lần mượn rental kế của khách 'XYZ' theo DateDiff.
Câu 44: Phân nhóm các đoạn độ dài chữ mô tả Description bằng Length char phân vùng bảng tạm.
Câu 45: Thử lệnh tổng cộng với điều kiện NULL cho Full Join Left-Right tìm các hóa đơn thanh toán giả tạo mạo danh bị thiếu nguồn gốc.
Câu 46: Liệt kê Top 3 người xuất sắc nhất được gộp thông tin ở các bảng ảo bằng CTE trong mảng giao dịch.
Câu 47: Tìm khách hàng đóng chi lớn ở Store 1 nhưng chả có hoạt động nào tại bảng Store số 2 qua INTERSECT / EXCEPT logic.
Câu 48: Xem tổng doanh xu Payment_p* thông qua một truy vấn gộp UNION bảng mẹ Payment và chi nhánh.
Câu 49: Truy vấn khép rào mảng thời gian các thuê đĩa diễn ra trong chủ nhật (DayOfWeek) mà tổng chi trả dưới hàm Min(amount).
Câu 50: Xây dựng toàn bộ hệ View Reporting hoàn chỉnh gồm tên film, tên nhân viên, ngày thuỷ chung, tình trạng đĩa thành 1 truy vấn Master Master Sub.