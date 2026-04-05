# Giải thích JOIN trong PostgreSQL

## Mục đích
- JOIN được dùng để kết hợp dữ liệu liên quan từ nhiều bảng trong một truy vấn. Trong thiết kế chuẩn hoá (normalized), mỗi bảng chứa một loại thực thể; JOIN cho phép lấy thông tin hoàn chỉnh bằng cách nối các hàng dựa trên khoá (thường là khoá ngoại).
 
## Chuẩn hoá (Normalization)

- **Định nghĩa:** Chuẩn hoá là quá trình tổ chức dữ liệu trong cơ sở dữ liệu quan hệ theo các quy tắc (normal forms) để loại bỏ dư thừa, tránh anomalies khi cập nhật và bảo đảm tính toàn vẹn dữ liệu.
- **Mục tiêu:** giảm trùng lặp, tránh update/insert/delete anomalies, và biểu diễn phụ thuộc hàm một cách rõ ràng.

- **Các dạng chính:**
	- **1NF (First Normal Form):** Mọi thuộc tính phải có giá trị nguyên tử (không lưu danh sách hay bảng lồng trong một ô).
	- **2NF (Second Normal Form):** Ở 1NF và mọi thuộc tính không-phải-khoá phụ thuộc hoàn toàn vào toàn bộ khoá chính (loại bỏ partial dependency). Áp dụng khi khoá chính là phức hợp.
	- **3NF (Third Normal Form):** Ở 2NF và không có phụ thuộc bắc cầu (transitive dependency) — mọi thuộc tính không-khoá chỉ phụ thuộc trực tiếp vào khoá chính.
	- **BCNF (Boyce-Codd Normal Form):** Mạnh hơn 3NF; với mọi phụ thuộc hàm X → Y thì X phải là superkey.

- **Ví dụ ngắn:**
	- Bảng chưa chuẩn: `orders(order_id, customer_name, customer_phone, product, qty)` — thông tin khách hàng lặp lại.
	- Sau chuẩn hoá: `customers(customer_id, name, phone)` và `orders(order_id, customer_id, product, qty)`.

- **Lưu ý:** Chuẩn hoá giảm dư thừa nhưng có thể làm tăng số JOIN khi truy vấn nhiều bảng; trong thực tế thường chuẩn hoá đến 3NF/BCNF rồi cân nhắc denormalize chọn lọc, dùng index hoặc materialized view nếu cần tối ưu hiệu năng.

## Các loại JOIN phổ biến
- INNER JOIN: chỉ trả về các hàng có khớp ở cả hai bảng.
- LEFT JOIN (LEFT OUTER JOIN): trả về tất cả hàng từ bảng trái, kèm hàng khớp từ bảng phải nếu có (NULL nếu không có).
- RIGHT JOIN (RIGHT OUTER JOIN): ngược lại của LEFT JOIN.
- FULL OUTER JOIN: trả về tất cả hàng từ cả hai bảng, hàng không khớp có giá trị NULL cho phía kia.
- CROSS JOIN: tích Descartes (mọi cặp hàng) — dùng thận trọng vì kích thước kết quả lớn.

## Ví dụ minh hoạ

Giả sử có hai bảng:

- `users(id, name)`
- `orders(id, user_id, total)`

- INNER JOIN (chỉ users có orders):

```sql
SELECT u.id, u.name, o.id AS order_id, o.total
FROM users u
JOIN orders o ON o.user_id = u.id;
```

- LEFT JOIN (tất cả users, kèm orders nếu có):

```sql
SELECT u.id, u.name, o.id AS order_id, o.total
FROM users u
LEFT JOIN orders o ON o.user_id = u.id;
```

- FULL OUTER JOIN (tất cả users và orders, ghép nếu khớp):

```sql
SELECT u.id AS user_id, u.name, o.id AS order_id, o.total
FROM users u
FULL OUTER JOIN orders o ON o.user_id = u.id;
```

- CROSS JOIN (mọi cặp user × order):

```sql
SELECT u.id AS user_id, o.id AS order_id
FROM users u
CROSS JOIN orders o;
```

## Khi chọn loại JOIN
- Muốn chỉ lấy bản ghi khớp → `INNER JOIN`.
- Muốn giữ bản ghi chính dù không có quan hệ → `LEFT JOIN`.
- Muốn tất cả từ cả hai bên → `FULL OUTER JOIN`.
- Cẩn thận với `CROSS JOIN` do kích thước kết quả.

## Hiệu năng & Thực hành tốt
- Đặt index trên cột khoá nối (ví dụ `orders.user_id`) để tăng tốc JOIN.
- Chỉ SELECT các cột cần thiết thay vì `SELECT *` để giảm I/O.
- Lọc sớm với `WHERE` hoặc `JOIN ... ON` điều kiện cụ thể để giảm số hàng xử lý.
- Dùng `EXPLAIN ANALYZE` để kiểm tra kế hoạch thực thi và tìm điểm nghẽn.

Ví dụ kiểm tra kế hoạch:

```sql
EXPLAIN ANALYZE
SELECT u.id, u.name, o.total
FROM users u
JOIN orders o ON o.user_id = u.id
WHERE o.total > 100;
```

## Ghi chú cho Supabase
- Supabase sử dụng PostgreSQL; mọi ví dụ và tối ưu ở trên áp dụng trực tiếp.
- Thực hiện truy vấn trong Supabase SQL Editor hoặc qua API của Supabase MCP.
- Nếu muốn, tôi có thể thêm dữ liệu mẫu và kết quả mẫu để bạn chạy thử trong project Supabase của mình.

---

Nếu bạn muốn, tôi sẽ thêm một kịch bản nhỏ (tạo bảng, chèn dữ liệu mẫu, và các truy vấn trên) để bạn có thể copy-paste chạy ngay trong Supabase SQL Editor.
