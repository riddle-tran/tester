## Kỹ Thuật Phân Vùng Tương Đương (Equivalence Partitioning)



Kỹ thuật phân vùng tương đương là phương pháp kiểm thử hộp đen (black box testing) chia miền giá trị đầu vào thành các lớp (partition) tương đương, nơi mỗi lớp đại diện cho một tập hợp các giá trị được xử lý giống nhau bởi hệ thống. Mục tiêu là giảm số lượng test case bằng cách chọn một đại diện từ mỗi lớp, giúp phát hiện lỗi hiệu quả hơn.    



- **Nguyên lý hoạt động**: Hệ thống xử lý các giá trị trong cùng một phân vùng một cách nhất quán. Nếu một giá trị trong phân vùng hợp lệ (valid partition) hoạt động đúng, toàn bộ phân vùng đó được coi là đúng; ngược lại với phân vùng không hợp lệ (invalid partition). Điều này dựa trên giả định rằng lỗi thường xảy ra ở ranh giới giữa các phân vùng.   

- **Cách áp dụng step-by-step**:

  1. Xác định miền đầu vào từ yêu cầu (requirements).

  2. Chia thành phân vùng valid (giá trị chấp nhận được) và invalid (giá trị bị từ chối).

  3. Chọn ít nhất một test case đại diện từ mỗi phân vùng.

  4. Thực thi và kiểm tra kết quả mong đợi (expected outcome).   

- **Ví dụ với số điện thoại di động (mobile number)**:

  | Phân vùng | Mô tả | Test case đại diện | Kết quả mong đợi |

  |-----------|-------|---------------------|------------------|

  | Valid | 10 chữ số hợp lệ | 0123456789 | Chấp nhận    |

  | Invalid (quá ngắn) | < 10 chữ số | 123456789 | Từ chối |

  | Invalid (quá dài) | > 10 chữ số | 01234567890 | Từ chối |



  



Kỹ thuật này giúp học viên hiểu cơ chế từ nguyên tắc đầu vào đến kiểm tra hành vi hệ thống, tránh test tất cả giá trị có thể.   



## Kỹ Thuật Phân Tích Giá Trị Biên (Boundary Value Analysis - BVA)



Phân tích giá trị biên tập trung vào các giá trị ở ranh giới (boundary) của các phân vùng, vì lỗi thường xảy ra tại đây do sai sót lập trình như off-by-one (lệch một đơn vị). Kết hợp với EP để tăng độ phủ.   



- **Nguyên lý**: Test các giá trị biên bao gồm biên dưới (min), biên trên (max), và các giá trị liền kề (min-1, min+1, max-1, max+1). Xem xét inclusive (bao gồm biên) hoặc exclusive (không bao gồm).  

- **Cách áp dụng**:

  1. Xác định biên từ yêu cầu (ví dụ: tuổi từ 18 đến 65).

  2. Test 4-6 giá trị quanh mỗi biên.

  3. Kết hợp valid/invalid để kiểm tra hành vi.   

- **Ví dụ với tuổi (age)**:

  | Biên giới | Giá trị test | Valid/Invalid | Lý do |

  |-----------|--------------|---------------|--------|

  | Dưới 18 | 17, 18, 19 | Invalid (17), Valid (18-19) | Kiểm tra inclusive biên dưới    |

  | Trên 65 | 64, 65, 66 | Valid (64-65), Invalid (66) | Kiểm tra biên trên |



  



Kết hợp EP và BVA tạo test case mạnh mẽ, giải thích tại sao biên dễ lỗi: lập trình viên thường nhầm điều kiện <, <=, >, >=.  



## Quy Trình Kiểm Thử Chất Lượng Step-by-Step



Quy trình kiểm thử chất lượng (quality assurance) bao gồm phân tích yêu cầu, thiết kế test case sử dụng EP/BVA, thực thi, và báo cáo. Áp dụng từ high-level đến detail.   



  



Quy trình này đảm bảo phủ sóng toàn diện, từ cấu trúc nội bộ (internal structure) đến xử lý đầu vào, giúp hệ thống đạt chất lượng cao.   



## Ứng Dụng Trong Yêu Cầu Chất Lượng (Quality Requirements)



Yêu cầu chất lượng (quality requirements) định nghĩa hành vi mong đợi, như xử lý valid/invalid input. Sử dụng EP/BVA để verify requirements step-by-step, tránh lỗi ở biên hoặc phân vùng.   



- **Valid input**: Chấp nhận và xử lý đúng (ví dụ: số di động đúng định dạng).

- **Invalid input**: Từ chối gracefully, không crash hệ thống.

- **Lợi ích**: Giảm rework, tăng độ tin cậy, phù hợp cho exam hoặc dự án thực tế.   



Tất cả khái niệm được xây dựng từ cơ bản, giúp học viên áp dụng độc lập.