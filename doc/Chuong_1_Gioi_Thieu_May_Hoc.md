# CHƯƠNG 1: GIỚI THIỆU VỀ MÁY HỌC (MACHINE LEARNING)

> **Tài liệu học tập & Tổng hợp chi tiết từ Giáo trình Máy học**  
> **Chủ đề:** Khái niệm cơ bản, Phân loại hệ thống máy học và Các thách thức chính.

---

## MỤC LỤC
1. [1.1 Máy học là gì?](#11-máy-học-là-gì)
2. [1.2 Tại sao cần sử dụng Máy học?](#12-tại-sao-cần-sử-dụng-máy-học)
3. [1.3 Các dạng bài toán Máy học phổ biến](#13-các-dạng-bài-toán-máy-học-phổ-biến)
4. [1.4 Kiểm thử (Testing) & Thẩm định (Validation)](#14-kiểm-thử-testing--thẩm-định-validation)
5. [1.5 Phân loại các hệ thống Máy học](#15-phân-loại-các-hệ-thống-máy-học)
6. [1.6 Các thách thức chính của Máy học](#16-các-thách-thức-chính-của-máy-học)

---

## 1.1 Máy học là gì?

* **Định nghĩa của Arthur Samuel (1959):**  
  > *"Machine Learning is the field of study that gives computers the ability to learn without being explicitly programmed."*  
  *(Máy học là lĩnh vực nghiên cứu cho phép máy tính có khả năng tự học hỏi mà không cần phải được lập trình một cách chi tiết/rõ ràng).*

* **Định nghĩa hình thức của Tom Mitchell (1997):**  
  > *"A computer program is said to learn from experience **E**, with respect to some task **T** and some performance measure **P**, if its performance on **T**, as measured by **P**, improves with experience **E**."*  
  *(Một chương trình máy tính được gọi là học từ kinh nghiệm **E**, đối với một nhóm bài toán/tác vụ **T** và thước đo hiệu năng **P**, nếu hiệu năng của nó khi thực hiện **T** (đo bằng **P**) cải thiện theo kinh nghiệm **E**).*

* **So sánh Lập trình truyền thống vs Lập trình Máy học:**
  - **Lập trình truyền thống:** Con người tự nghiên cứu dữ liệu → Viết thủ công các quy tắc (Rules/If-Else) → Đưa Dữ liệu + Quy tắc vào máy tính → Cho ra Kết quả.
  - **Máy học (Machine Learning):** Con người đưa Dữ liệu + Kết quả mong muốn (Nhãn) vào mô hình → Máy học tự động rút ra các Quy tắc (Patterns/Rules) → Áp dụng quy tắc đó cho dữ liệu mới.

---

## 1.2 Tại sao cần sử dụng Máy học?

1. **Đơn giản hóa mã nguồn:** Các bài toán phức tạp đòi hỏi danh sách dài các quy tắc thủ công (ví dụ: lọc thư rác Spam). Máy học giúp mã nguồn ngắn gọn, dễ bảo trì và đạt độ chính xác cao hơn.
2. **Giải quyết bài toán chưa có lời giải truyền thống:** Nhận dạng tiếng nói (nhiều giọng vùng miền, môi trường ồn), nhận dạng khuôn mặt, dịch tự động...
3. **Thích ứng với ngữ cảnh biến động:** Khi dữ liệu thay đổi liên tục, mô hình máy học có thể tự động học lại trên dữ liệu mới mà không cần con người viết lại mã nguồn.
4. **Hỗ trợ con người khám phá tri thức (Data Mining):** Máy học giúp phát hiện ra các quy luật ẩn sâu trong tập dữ liệu lớn mà con người không nhận ra.

---

## 1.3 Các dạng bài toán Máy học phổ biến

* **Phân loại (Classification):** Dự đoán nhãn rời rạc (Dương tính/Âm tính, Spam/Non-Spam, Nhận dạng chữ số 0-9).
* **Hồi quy (Regression):** Dự đoán giá trị liên tục (Giá nhà, giá xe, doanh thu, nhiệt độ).
* **Xếp hạng (Ranking):** Xếp hạng danh sách kết quả tìm kiếm (Google Search, Hệ thống gợi ý).
* **Phát hiện bất thường (Anomaly / Fraud Detection):** Phát hiện giao dịch tín dụng gian lận, cảnh báo tiêu thụ điện bất thường.
* **Tìm kiểu mẫu (Finding Patterns / Association Rule Learning):** Phát hiện các hành vi đi kèm (ví dụ: 80% khách hàng mua "khẩu trang" cũng sẽ mua "nước rửa tay").

---

## 1.4 Kiểm thử (Testing) & Thẩm định (Validation)

Để xây dựng một hệ thống máy học tin cậy, dữ liệu cần được phân chia thành 3 tập riêng biệt:
1. **Tập huấn luyện (Training Set):** Dùng để mô hình học các tham số.
2. **Tập thẩm định (Validation / Development / Dev Set):** Dùng để đánh giá trong quá trình phát triển, tinh chỉnh các siêu tham số (Hyperparameters) và chọn mô hình tốt nhất.
3. **Tập kiểm thử (Test Set):** Dùng để đánh giá hiệu năng cuối cùng của hệ thống trước khi đưa vào vận hành thực tế.

> ⚠️ **Cảnh báo lỗi nghiêm trọng trong Máy học:** Không bao giờ được đánh giá hiệu năng hệ thống trên tập dữ liệu đã dùng để huấn luyện hoặc tinh chỉnh tham số! Điều này gây ra hiện tượng *Data Leakage* (Rò rỉ dữ liệu) và đánh giá sai bản chất của mô hình.

---

## 1.5 Phân loại các hệ thống Máy học

Các hệ thống máy học được phân loại dựa trên 3 tiêu chí chính:

### 1. Theo sự giám sát của con người
* **Học có giám sát (Supervised Learning):** Dữ liệu huấn luyện kèm theo nhãn (Label).  
  *Thuật toán phổ biến:* Linear Regression, Logistic Regression, k-Nearest Neighbors (k-NN), Support Vector Machines (SVM), Decision Trees, Random Forests, Neural Networks.
* **Học không giám sát (Unsupervised Learning):** Dữ liệu không có nhãn. Mô hình tự tìm cấu trúc ẩn.  
  *Gom cụm (Clustering):* k-Means, Hierarchical Cluster Analysis (HCA), Expectation Maximization (EM).  
  *Giảm số chiều & Trực quan hóa (Dimensionality Reduction):* PCA, Kernel PCA, LLE, t-SNE.  
  *Học luật kết hợp:* Apriori, FP-Growth.
* **Học bán giám sát (Semi-Supervised Learning):** Dữ liệu gồm một lượng nhỏ có nhãn và một lượng lớn không có nhãn (ví dụ: Phân loại ảnh Google Photos).
* **Học củng cố (Reinforcement Learning):** Tác tử (Agent) quan sát môi trường, thực hiện hành động (Actions), nhận thưởng/phạt (Rewards/Penalties) và tự học chiến lược (Policy) tối ưu nhất (ví dụ: AlphaGo, xe tự lái).

### 2. Theo khả năng học tích lũy (Batch vs. Online Learning)
* **Học theo lô (Batch / Offline Learning):** Mô hình được huấn luyện trên toàn bộ dữ liệu có sẵn. Khi muốn cập nhật dữ liệu mới phải tiến hành huấn luyện lại toàn bộ từ đầu. Tốn thời gian và tài nguyên tính toán.
* **Học trực tuyến (Online / Incremental Learning):** Mô hình cập nhật liên tục theo từng mẫu hoặc nhóm mẫu nhỏ (mini-batch). Phù hợp với dữ liệu luồng (Streaming data, chứng khoán) hoặc dữ liệu siêu lớn không thể chứa vừa bộ nhớ RAM (*Out-of-core learning*).  
  - *Tốc độ học (Learning Rate):* Siêu tham số kiểm soát mức độ thay đổi của mô hình theo dữ liệu mới.

### 3. Theo khả năng tổng quát hóa (Instance-Based vs. Model-Based)
* **Học dựa trên mẫu (Instance-Based Learning):** Hệ thống ghi nhớ các mẫu dữ liệu huấn luyện. Khi gặp dữ liệu mới, nó so sánh khoảng cách/độ tương đồng (*similarity measure*) với các mẫu đã biết (ví dụ: k-NN).
* **Học dựa trên mô hình (Model-Based Learning):** Hệ thống xây dựng một mô hình toán học (phương trình/hàm số) từ dữ liệu huấn luyện, sau đó dùng mô hình này để dự đoán dữ liệu mới.

---

## 1.6 Các thách thức chính của Máy học

Thách thức đến từ **dữ liệu không tốt** hoặc **thuật toán không phù hợp**:

### 1. Thách thức do Dữ liệu không tốt
* **Thiếu dữ liệu huấn luyện:** Máy học cần hàng nghìn đến hàng triệu mẫu dữ liệu để đạt hiệu năng cao.
* **Dữ liệu không có tính đại diện:**
  - *Nhiễu do lấy mẫu (Sampling noise):* Tập dữ liệu quá nhỏ gây ra mẫu sai lệch.
  - *Lệch do lấy mẫu (Sampling bias):* Phương pháp thu thập dữ liệu bị lỗi làm mất tính đại diện cho thực tế.
* **Dữ liệu chất lượng kém:** Chứa nhiều lỗi, nhiều nhiễu, giá trị ngoại biên (outliers) hoặc thiếu giá trị (missing values). Cần làm sạch dữ liệu (*Data Cleaning*).
* **Đặc trưng không phù hợp (Irrelevant Features):** Dữ liệu chứa nhiều thuộc tính thừa. Cần áp dụng **Chế tác đặc trưng (Feature Engineering)**:
  - *Lựa chọn đặc trưng (Feature Selection):* Chọn thuộc tính hữu ích nhất.
  - *Rút trích đặc trưng (Feature Extraction):* Kết hợp các thuộc tính cũ tạo thành thuộc tính mới giàu thông tin hơn (ví dụ: PCA).
  - *Tạo đặc trưng mới:* Thu thập thêm dữ liệu hoặc tính toán chỉ số mới.

### 2. Thách thức do Thuật toán không tốt
* **Quá khớp (Overfitting):** Mô hình quá phức tạp, học thuộc lòng luôn cả nhiễu trong tập huấn luyện.
  - *Dấu hiệu:* Kết quả trên tập huấn luyện rất cao nhưng trên tập test lại kém.
  - *Giải pháp:* Đơn giản hóa mô hình (giảm số tham số, giảm bậc đa thức), giảm số đặc trưng, tăng ràng buộc (Chính quy hóa - *Regularization*), thu thập thêm dữ liệu, làm sạch nhiễu.
* **Chưa khớp (Underfitting):** Mô hình quá đơn giản không học được cấu trúc của dữ liệu.
  - *Giải pháp:* Chọn mô hình mạnh mẽ hơn, thêm đặc trưng tốt hơn, giảm chính quy hóa.

---

> **Tài liệu tham khảo:** *Hands-on Machine Learning with Scikit-Learn, Keras & TensorFlow (2nd Edition)* – Aurélien Géron.
