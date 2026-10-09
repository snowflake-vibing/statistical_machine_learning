# 📝 BỘ CÂU HỎI TRẮC NGHIỆM - CHƯƠNG 1: GIỚI THIỆU VỀ MÁY HỌC

> **Hướng dẫn:** Chọn đáp án đúng nhất cho mỗi câu hỏi. **Đáp án chi tiết và giải thích nằm ở cuối file.**

---

### Câu 1: Theo Tom Mitchell (1997), một chương trình máy tính được gọi là học từ kinh nghiệm E đối với tác vụ T và thước đo P nếu:
- A. Thước đo P cải thiện khi thực hiện tác vụ T thông qua kinh nghiệm E.
- B. Kinh nghiệm E tăng lên khi thực hiện tác vụ T dưới sự giám sát của con người.
- C. Tác vụ T được lập trình chi tiết để cải thiện kinh nghiệm E.
- D. Thước đo P giữ nguyên bất kể kinh nghiệm E thay đổi như thế nào.

### Câu 2: Sự khác biệt cốt lõi giữa Lập trình truyền thống và Máy học (Machine Learning) là gì?
- A. Lập trình truyền thống không sử dụng máy tính, còn Máy học dùng máy tính.
- B. Lập trình truyền thống đầu vào là Dữ liệu + Quy tắc để ra Kết quả; Máy học đầu vào là Dữ liệu + Kết quả (Nhãn) để máy tự rút ra Quy tắc.
- C. Máy học không bao giờ mắc lỗi, còn Lập trình truyền thống luôn có lỗi.
- D. Lập trình truyền thống áp dụng cho trí tuệ nhân tạo, còn Máy học áp dụng cho vi mạch.

### Câu 3: Bài toán nào sau đây thuộc dạng bài toán Hồi quy (Regression)?
- A. Nhận diện thư rác (Spam / Non-spam).
- B. Dự đoán giá nhà dựa trên diện tích và vị trí.
- C. Xếp hạng danh sách kết quả tìm kiếm Google.
- D. Phát hiện giao dịch thẻ tín dụng gian lận.

### Câu 4: Bài toán phát hiện 80% khách hàng mua "khẩu trang" cũng mua "nước rửa tay" thuộc dạng bài toán nào?
- A. Hồi quy (Regression).
- B. Phân loại nhị phân (Binary Classification).
- C. Học luật kết hợp (Association Rule Learning / Finding Patterns).
- D. Học củng cố (Reinforcement Learning).

### Câu 5: Khi chia dữ liệu để phát triển hệ thống Máy học, tập dữ liệu nào được sử dụng để tinh chỉnh các siêu tham số (Hyperparameters) và chọn mô hình tốt nhất?
- A. Tập huấn luyện (Training Set).
- B. Tập thẩm định (Validation / Dev Set).
- C. Tập kiểm thử (Test Set).
- D. Tập dữ liệu thô (Raw Data Set).

### Câu 6: Hành vi nào sau đây là LỖI NGHIÊM TRỌNG trong Machine Learning?
- A. Sử dụng Cross Validation trên tập huấn luyện.
- B. Đánh giá hiệu năng cuối cùng của hệ thống trên tập kiểm thử (Test Set).
- C. Đánh giá mô hình trên chính tập dữ liệu đã dùng để huấn luyện hoặc tinh chỉnh tham số.
- D. Chuẩn hóa đặc trưng dữ liệu trước khi đưa vào mô hình.

### Câu 7: Thuật toán nào sau đây thuộc nhóm Học KHÔNG giám sát (Unsupervised Learning)?
- A. Linear Regression.
- B. Support Vector Machines (SVM).
- C. k-Means Clustering.
- D. Decision Trees.

### Câu 8: Kỹ thuật t-SNE và PCA thường được sử dụng cho mục đích nào trong Học không giám sát?
- A. Dự đoán giá trị liên tục.
- B. Trực quan hóa và Giảm số chiều dữ liệu (Dimensionality Reduction).
- C. Phân loại đa nhãn.
- D. Huấn luyện tác tử chơi game.

### Câu 9: Học củng cố (Reinforcement Learning) hoạt động dựa trên cơ chế nào?
- A. Máy tính học từ dữ liệu được con người dán nhãn 100%.
- B. Tác tử (Agent) thực hiện hành động, nhận phần thưởng/hình phạt và tự tối ưu chiến lược (Policy).
- C. Gom cụm dữ liệu không nhãn dựa trên độ tương đồng khoảng cách.
- D. Chia nhỏ dữ liệu thành các mini-batch để huấn luyện trực tuyến.

### Câu 10: Đặc điểm chính của Học trực tuyến (Online Learning) là gì?
- A. Phải kết nối Internet liên tục thì mô hình mới chạy được.
- B. Mô hình được huấn luyện cập nhật liên tục theo từng mẫu hoặc nhóm mẫu nhỏ (mini-batch).
- C. Mô hình học trên toàn bộ dữ liệu có sẵn trong một lần duy nhất.
- D. Không bao giờ xảy ra hiện tượng quá khớp (Overfitting).

### Câu 11: Khái niệm "Out-of-core learning" trong Học trực tuyến được áp dụng khi nào?
- A. Khi mô hình chạy trên điện thoại di động.
- B. Khi dữ liệu quá lớn không thể chứa vừa bộ nhớ RAM của máy tính.
- C. Khi dữ liệu hoàn toàn không có nhãn.
- D. Khi không thể tính toán được độ lệch chuẩn của dữ liệu.

### Câu 12: Sự khác biệt giữa Học dựa trên mẫu (Instance-based) và Học dựa trên mô hình (Model-based) là gì?
- A. Học dựa trên mẫu so sánh độ tương đồng với dữ liệu cũ; Học dựa trên mô hình xây dựng phương trình toán học từ dữ liệu huấn luyện.
- B. Học dựa trên mô hình không cần dữ liệu huấn luyện.
- C. Học dựa trên mẫu chạy nhanh hơn Học dựa trên mô hình đối với dữ liệu siêu lớn.
- D. Cả hai phương pháp đều là Học củng cố.

### Câu 13: Hiện tượng Quá khớp (Overfitting) xảy ra khi nào?
- A. Mô hình quá đơn giản không học được cấu trúc của dữ liệu.
- B. Mô hình quá phức tạp, học thuộc lòng cả các nhiễu trong dữ liệu huấn luyện.
- C. Dữ liệu huấn luyện quá nhiều và có chất lượng quá tốt.
- D. Tốc độ học (Learning rate) quá nhỏ.

### Câu 14: Biện pháp nào KHÔNG giúp khắc phục hiện tượng Overfitting?
- A. Đơn giản hóa mô hình bằng cách giảm số lượng tham số hoặc đặc trưng.
- B. Thêm ràng buộc cho mô hình (Chính quy hóa - Regularization).
- C. Thu thập thêm dữ liệu huấn luyện.
- D. Tăng độ phức tạp của mô hình bằng đa thức bậc cao hơn.

### Câu 15: Công đoạn Chế tác đặc trưng (Feature Engineering) bao gồm các bước nào?
- A. Lựa chọn đặc trưng (Feature Selection), Rút trích đặc trưng (Feature Extraction), Tạo đặc trưng mới.
- B. Điền thiếu dữ liệu, Xóa rác, Đổi tên cột.
- C. Huấn luyện mô hình, Đánh giá F1-score, Deploy.
- D. Grid Search, Random Search, Cross Validation.

---

## 🔑 ĐÁP ÁN VÀ GIẢI THÍCH CHI TIẾT - CHƯƠNG 1

| Câu | Đáp án | Giải thích chi tiết |
| :---: | :---: | :--- |
| **1** | **A** | Theo Tom Mitchell: "A computer program is said to learn from experience E with respect to task T and performance measure P if its performance at tasks in T, as measured by P, improves with experience E." |
| **2** | **B** | Lập trình truyền thống: `Dữ liệu + Quy tắc (Code) -> Kết quả`. Máy học: `Dữ liệu + Kết quả (Nhãn) -> Quy tắc (Model)`. |
| **3** | **B** | Dự đoán giá nhà là giá trị số liên tục (USD) $\rightarrow$ Bài toán Hồi quy (Regression). |
| **4** | **C** | Đây là bài toán Học luật kết hợp (Association Rule Learning / Finding Patterns) trong siêu thị. |
| **5** | **B** | Tập thẩm định (Validation / Dev Set) dùng để đánh giá mô hình trong quá trình phát triển và chọn siêu tham số. |
| **6** | **C** | Lỗi Data Leakage / Đánh giá lạc quan quá mức: Không bao giờ đánh giá mô hình trên chính dữ liệu đã dùng để huấn luyện/tinh chỉnh. |
| **7** | **C** | k-Means là thuật toán gom cụm (Clustering) thuộc nhóm Học không giám sát (Unsupervised). |
| **8** | **B** | t-SNE và PCA là các kỹ thuật giảm số chiều dữ liệu (Dimensionality Reduction) và trực quan hóa 2D/3D. |
| **9** | **B** | Học củng cố dựa trên tác tử (Agent) nhận thưởng/phạt từ môi trường để tối ưu chiến lược (Policy). |
| **10** | **B** | Học trực tuyến (Online Learning) cập nhật mô hình theo từng mẩu dữ liệu nhỏ (mini-batch) một cách liên tục. |
| **11** | **B** | Out-of-core learning chia nhỏ dữ liệu đĩa cứng để học từng phần khi dữ liệu quá lớn không vừa RAM. |
| **12** | **A** | Instance-based dùng độ đo tương đồng (như k-NN); Model-based xây dựng mô hình/hàm số toán học. |
| **13** | **B** | Overfitting xảy ra khi mô hình quá phức tạp, học luôn cả nhiễu của dữ liệu huấn luyện. |
| **14** | **D** | Tăng độ phức tạp của mô hình sẽ làm Overfitting trầm trọng hơn, không phải cách khắc phục. |
| **15** | **A** | Feature Engineering gồm: Lựa chọn đặc trưng (Selection), Rút trích đặc trưng (Extraction) và Tạo đặc trưng mới. |
