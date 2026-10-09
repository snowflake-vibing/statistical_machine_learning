# 📝 BỘ CÂU HỎI TRẮC NGHIỆM - CHƯƠNG 2: QUY TRÌNH THỰC HIỆN DỰ ÁN MÁY HỌC

> **Hướng dẫn:** Chọn đáp án đúng nhất cho mỗi câu hỏi. **Đáp án chi tiết và giải thích nằm ở cuối file.**

---

### Câu 1: Quy trình chuẩn thực hiện một dự án Máy học gồm bao nhiêu bước chính?
- A. 5 bước.
- B. 6 bước.
- C. 8 bước.
- D. 10 bước.

### Câu 2: Trong Bước 1 (Xác định bối cảnh & Yêu cầu), việc lựa chọn thước đo hiệu năng (Performance Metric) phụ thuộc vào yếu tố nào?
- A. Ngôn ngữ lập trình được sử dụng.
- B. Loại bài toán (Hồi quy hay Phân loại) và mục tiêu kinh doanh.
- C. Dung lượng ổ đĩa cứng lưu trữ dữ liệu.
- D. Tốc độ đường truyền Internet.

### Câu 3: Thước đo hiệu năng phổ biến nhất cho bài toán Hồi quy (Regression) là gì?
- A. Accuracy.
- B. F1-Score.
- C. RMSE (Root Mean Squared Error).
- D. ROC-AUC.

### Câu 4: Mục đích chính của bước Khám phá dữ liệu (EDA - Exploratory Data Analysis) là gì?
- A. Đóng gói mô hình thành Web service.
- B. Nghiên cứu cấu trúc, phân bố, phát hiện giá trị bất thường và mối tương quan giữa các đặc trưng.
- C. Chạy Grid Search để tìm siêu tham số tốt nhất.
- D. Viết báo cáo tổng kết cho khách hàng.

### Câu 5: Khi gặp thuộc tính bị thiếu giá trị (Missing Values), phương pháp nào sau đây CÓ THỂ áp dụng?
- A. Loại bỏ các dòng chứa giá trị thiếu.
- B. Loại bỏ toàn bộ cột thuộc tính bị thiếu.
- C. Điền giá trị thay thế (Imputation) bằng giá trị trung bình/trung vị.
- D. Tất cả các phương án trên.

### Câu 6: Kỹ thuật One-Hot Encoding được dùng để làm gì?
- A. Chuẩn hóa giá trị số về khoảng $[0, 1]$.
- B. Chuyển đổi thuộc tính dạng phân loại (Categorical) thành các vector nhị phân $(0/1)$.
- C. Giảm số chiều dữ liệu từ 100 cột xuống 2 cột.
- D. Tính toán hệ số tương quan Pearson.

### Câu 7: Phương pháp chuẩn hóa đặc trưng Standardization (`StandardScaler`) biến đổi dữ liệu như thế nào?
- A. Đưa dữ liệu về đoạn từ $0$ đến $1$.
- B. Trừ đi giá trị trung bình $\mu$ và chia cho độ lệch chuẩn $\sigma$ (trung bình $= 0$, phương sai $= 1$).
- C. Chuyển dữ liệu thành dạng số nguyên dương.
- D. Nhân tất cả các giá trị với 100.

### Câu 8: Tại sao cần sử dụng `Pipeline` trong Scikit-Learn?
- A. Để mô hình chạy nhanh hơn 100 lần.
- B. Tự động hóa và đóng gói chuỗi các bước biến đổi dữ liệu + huấn luyện mô hình một cách nhất quán, tránh rò rỉ dữ liệu.
- C. Thay thế hoàn toàn thuật toán học máy.
- D. Giúp hiển thị biểu đồ đồ họa đẹp mắt hơn.

### Câu 9: Phương pháp Thẩm định chéo K-Fold (K-Fold Cross Validation) hoạt động như thế nào?
- A. Chia dữ liệu thành K phần, dùng K-1 phần để huấn luyện và 1 phần để kiểm tra, lặp lại K lần và lấy kết quả trung bình.
- B. Huấn luyện mô hình K lần trên cùng một tập dữ liệu.
- C. Chia mô hình thành K phần rồi gộp lại.
- D. Sử dụng K máy tính khác nhau để chạy song song.

### Câu 10: Sự khác biệt giữa `GridSearchCV` và `RandomizedSearchCV` là gì?
- A. GridSearchCV thử ngẫu nhiên; RandomizedSearchCV thử toàn bộ tổ hợp.
- B. GridSearchCV thử toàn bộ các tổ hợp siêu tham số được định sẵn; RandomizedSearchCV chọn ngẫu nhiên các bộ tham số qua mỗi vòng lặp.
- C. GridSearchCV chỉ dùng cho Phân loại; RandomizedSearchCV chỉ dùng cho Hồi quy.
- D. Cả hai lớp này có chức năng hệt như nhau không khác gì.

### Câu 11: Phương pháp kết hợp nhiều mô hình (Ensemble Methods) như Random Forest có ưu điểm gì?
- A. Kết hợp nhiều mô hình thành phần giúp nâng cao độ chính xác và giảm sai số so với mô hình riêng lẻ.
- B. Giúp giảm thời gian huấn luyện xuống 0 giây.
- C. Không cần sử dụng dữ liệu huấn luyện.
- D. Tự động sửa lỗi sai trong mã nguồn Python.

### Câu 12: Sau khi tinh chỉnh mô hình tốt nhất, bước đánh giá cuối cùng trên tập Kiểm thử (Test Set) có đặc điểm gì?
- A. Nếu kết quả kém, ta được quyền tinh chỉnh siêu tham số tiếp trên tập Test.
- B. Đo đạc hiệu năng thực tế của toàn bộ pipeline trên tập Test và KHÔNG ĐƯỢC cải tiến/tinh chỉnh mô hình thêm nữa.
- C. Xóa bỏ tập Test và lấy kết quả trên tập Train.
- D. Đổi tập Test thành tập Validation.

### Câu 13: Thư viện Python nào thường được dùng để lưu trữ (Save) mô hình Machine Learning và Pipeline ra đĩa cứng?
- A. `matplotlib`.
- B. `joblib` hoặc `pickle`.
- C. `seaborn`.
- D. `requests`.

### Câu 14: Khái niệm "Concept Drift" hoặc "Data Drift" trong quá trình theo dõi (Monitoring) hệ thống ML nghĩa là gì?
- A. Mô hình bị virus tấn công.
- B. Chất lượng mô hình suy giảm theo thời gian do phân bố dữ liệu thực tế thay đổi so với dữ liệu huấn luyện ban đầu.
- C. Máy tính bị hết dung lượng bộ nhớ RAM.
- D. Code Python bị lỗi cú pháp sau khi restart.

### Câu 15: Trong thực tế, giai đoạn nào thường tốn nhiều công sức và chi phí nhất trong vòng đời một hệ thống Machine Learning?
- A. Giai đoạn viết code huấn luyện mô hình ban đầu.
- B. Giai đoạn chọn tên cho mô hình.
- C. Giai đoạn Vận hành, Theo dõi và Bảo trì hệ thống (Monitoring & Maintenance).
- D. Giai đoạn in báo cáo ra giấy.

---

## 🔑 ĐÁP ÁN VÀ GIẢI THÍCH CHI TIẾT - CHƯƠNG 2

| Câu | Đáp án | Giải thích chi tiết |
| :---: | :---: | :--- |
| **1** | **C** | Quy trình chuẩn thực hiện dự án Máy học gồm **8 bước**: Bối cảnh $\rightarrow$ Thu thập $\rightarrow$ EDA $\rightarrow$ Chuẩn bị $\rightarrow$ Huấn luyện $\rightarrow$ Tinh chỉnh $\rightarrow$ Trình bày $\rightarrow$ Vận hành/Bảo trì. |
| **2** | **B** | Thước đo hiệu năng phải phù hợp với loại bài toán (Hồi quy hay Phân loại) và mục tiêu kinh doanh. |
| **3** | **C** | RMSE (Root Mean Squared Error) là thước đo độ đo sai số chuẩn mực nhất cho bài toán Hồi quy. |
| **4** | **B** | EDA (Exploratory Data Analysis) nhằm hiểu sâu cấu trúc dữ liệu, phân bố, tương quan và phát hiện nhiễu. |
| **5** | **D** | Xử lý thiếu dữ liệu có 3 cách: Bỏ dòng, bỏ cột, hoặc Điền giá trị thay thế (Imputation). |
| **6** | **B** | One-Hot Encoding chuyển thuộc tính chuỗi phân loại thành vector nhị phân nhãn $0/1$. |
| **7** | **B** | `StandardScaler`: $x' = \frac{x - \mu}{\sigma}$, làm cho dữ liệu có trung bình bằng 0 và phương sai bằng 1. |
| **8** | **B** | `Pipeline` giúp tự động hóa chuỗi xử lý dữ liệu + mô hình, giữ code sạch sẽ và tránh Data Leakage. |
| **9** | **A** | K-Fold Cross Validation chia $K$ phần, train trên $K-1$ phần và test trên phần còn lại, lặp $K$ lần. |
| **10** | **B** | `GridSearchCV` thử mọi tổ hợp (vét cạn); `RandomizedSearchCV` lấy mẫu ngẫu nhiên tổ hợp tham số. |
| **11** | **A** | Ensemble Methods (như Random Forest) kết hợp nhiều mô hình yếu để tạo thành mô hình mạnh hơn. |
| **12** | **B** | Bước đánh giá trên Test Set là bước cuối cùng, không được tinh chỉnh tham số dựa trên kết quả Test Set. |
| **13** | **B** | Thư viện `joblib` hoặc `pickle` giúp serialize và lưu trữ mô hình ra file `.pkl`/`.joblib`. |
| **14** | **B** | Data Drift / Concept Drift là hiện tượng phân bố dữ liệu thực tế biến đổi làm suy giảm độ chính xác mô hình. |
| **15** | **C** | Giai đoạn vận hành, theo dõi và bảo trì lâu dài (MLOps) tốn nhiều chi phí & công sức nhất trong thực tế. |
