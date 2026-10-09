# 📝 BỘ CÂU HỎI TRẮC NGHIỆM - CHƯƠNG 3: PHÂN LỚP VÀ ĐÁNH GIÁ BỘ PHÂN LỚP

> **Hướng dẫn:** Chọn đáp án đúng nhất cho mỗi câu hỏi. **Đáp án chi tiết và giải thích nằm ở cuối file.**

---

### Câu 1: Bộ dữ liệu MNIST gồm bao nhiêu hình ảnh chữ số viết tay và được chia như thế nào?
- A. 50.000 ảnh (40k train / 10k test).
- B. 70.000 ảnh (60k train / 10k test).
- C. 100.000 ảnh (80k train / 20k test).
- D. 10.000 ảnh (5k train / 5k test).

### Câu 2: Trong Ma trận nhầm lẫn (Confusion Matrix), ký hiệu FP (False Positive) đại diện cho trường hợp nào?
- A. Thực tế là Dương tính và được dự đoán đúng là Dương tính.
- B. Thực tế là Âm tính nhưng bị dự đoán nhầm thành Dương tính (Lỗi Loại I).
- C. Thực tế là Âm tính và được dự đoán đúng là Âm tính.
- D. Thực tế là Dương tính nhưng bị dự đoán nhầm thành Âm tính (Lỗi Loại II).

### Câu 3: Công thức tính Độ chính xác Precision là gì?
- A. $\text{Precision} = \frac{\text{TP}}{\text{TP} + \text{FP}}$
- B. $\text{Precision} = \frac{\text{TP}}{\text{TP} + \text{FN}}$
- C. $\text{Precision} = \frac{\text{TP} + \text{TN}}{\text{TP} + \text{TN} + \text{FP} + \text{FN}}$
- D. $\text{Precision} = \frac{\text{TN}}{\text{TN} + \text{FP}}$

### Câu 4: Công thức tính Độ phủ Recall (Sensitivity) là gì?
- A. $\text{Recall} = \frac{\text{TP}}{\text{TP} + \text{FP}}$
- B. $\text{Recall} = \frac{\text{TP}}{\text{TP} + \text{FN}}$
- C. $\text{Recall} = \frac{\text{TN}}{\text{TN} + \text{FP}}$
- D. $\text{Recall} = \frac{\text{FP}}{\text{FP} + \text{FN}}$

### Câu 5: Tại sao chỉ số Accuracy KHÔNG phải là thước đo tốt cho tập dữ liệu lệch (Imbalanced Dataset)?
- A. Vì Accuracy tính toán quá chậm.
- B. Vì một mô hình ngây thơ luôn dự đoán lớp chiếm đa số vẫn đạt Accuracy rất cao mà không học được gì.
- C. Vì Accuracy luôn trả về giá trị âm.
- D. Vì Accuracy chỉ áp dụng cho bài toán Hồi quy.

### Câu 6: Trong bài toán "Phát hiện video độc hại cho trẻ em", ta nên ưu tiên chỉ số nào cao hơn?
- A. Recall cao (thà bắt nhầm còn hơn bỏ sót).
- B. Precision cao (đã duyệt video nào là phải đảm bảo tuyệt đối an toàn).
- C. Accuracy thấp.
- D. FPR cao.

### Câu 7: Trong bài toán "Phát hiện bệnh hiểm nghèo (Ung thư)", ta nên ưu tiên chỉ số nào cao hơn?
- A. Precision cao.
- B. Recall cao (thà chẩn đoán nhầm để kiểm tra lại chứ tuyệt đối không bỏ sót người bệnh).
- C. Specificity thấp.
- D. FP cao.

### Câu 8: Chỉ số F1-Score là loại trung bình nào của Precision và Recall?
- A. Trung bình cộng (Arithmetic Mean).
- B. Trung bình nhân (Geometric Mean).
- C. Trung bình điều hòa (Harmonic Mean).
- D. Trung bình trọng số đơn giản.

### Câu 9: Đường cong ROC (Receiver Operating Characteristic) biểu diễn mối quan hệ giữa hai đại lượng nào?
- A. Precision và Recall.
- B. TPR (True Positive Rate / Recall) và FPR (False Positive Rate).
- C. Accuracy và Loss.
- D. TP và TN.

### Câu 10: Một bộ phân lớp ngẫu nhiên (Random Classifier) có diện tích dưới đường cong ROC (AUC) bằng bao nhiêu?
- A. 1.0.
- B. 0.0.
- C. 0.5.
- D. 0.9.

### Câu 11: Để phân loại $N$ lớp bằng các bộ phân lớp nhị phân theo chiến lược One-vs-One (OvO), cần phải xây dựng bao nhiêu bộ phân lớp nhị phân?
- A. $N$ bộ.
- B. $N - 1$ bộ.
- C. $\frac{N(N-1)}{2}$ bộ.
- D. $N^2$ bộ.

### Câu 12: Đối với thuật toán Support Vector Machine (SVM) vốn huấn luyện chậm trên tập dữ liệu lớn, chiến lược phân lớp đa lớp nào thường được ưu tiên?
- A. One-vs-Rest (OvR).
- B. One-vs-One (OvO) (vì mỗi bộ phân lớp chỉ cần huấn luyện trên tập dữ liệu con của 2 lớp).
- C. Multioutput classification.
- D. Binary Cross Entropy.

### Câu 13: Bài toán nhận dạng một bức ảnh chứa chữ số viết tay và dự đoán 2 đầu ra: "Có phải số lớn hơn 7 không?" và "Có phải số lẻ không?" thuộc loại bài toán nào?
- A. Phân lớp Nhị phân (Binary Classification).
- B. Phân lớp Đa lớp (Multiclass Classification).
- C. Phân lớp Đa nhãn (Multilabel Classification).
- D. Phân lớp Đa đầu vào (Multioutput Classification).

### Câu 14: Bài toán Khử nhiễu ảnh (Image Denoising) - trong đó đầu vào là ảnh nhiễu và đầu ra dự đoán lại 784 giá trị pixel từ $0$ đến $255$ - thuộc loại bài toán nào?
- A. Phân lớp Nhị phân.
- B. Phân lớp Đa nhãn nhị phân.
- C. Phân lớp Đa đầu vào (Multioutput Multiclass Classification).
- D. Hồi quy đơn biến.

### Câu 15: Trong Scikit-Learn, hàm nào được dùng để tính diện tích dưới đường cong ROC?
- A. `roc_curve()`
- B. `roc_auc_score()`
- C. `confusion_matrix()`
- D. `f1_score()`

---

## 🔑 ĐÁP ÁN VÀ GIẢI THÍCH CHI TIẾT - CHƯƠNG 3

| Câu | Đáp án | Giải thích chi tiết |
| :---: | :---: | :--- |
| **1** | **B** | MNIST gồm 70.000 ảnh $28 \times 28$, phân chia 60.000 ảnh train và 10.000 ảnh test. |
| **2** | **B** | FP (False Positive) là Âm tính thực tế nhưng bị dự đoán sai thành Dương tính (Báo động giả / Lỗi Loại I). |
| **3** | **A** | $\text{Precision} = \frac{\text{TP}}{\text{TP} + \text{FP}}$ (Tỷ lệ dự đoán Dương tính đúng). |
| **4** | **B** | $\text{Recall} = \frac{\text{TP}}{\text{TP} + \text{FN}}$ (Tỷ lệ bắt được các mẫu Dương tính thực tế). |
| **5** | **B** | Với dữ liệu lệch (VD: 99% Âm tính), mô hình phán bừa 100% Âm tính vẫn đạt Accuracy 99% nhưng vô dụng. |
| **6** | **B** | Lọc video an toàn trẻ em cần Precision cao: Đã duyệt video nào thì video đó phải an toàn tuyệt đối. |
| **7** | **B** | Chẩn đoán bệnh hiểm nghèo cần Recall cao: Không được phép bỏ sót bất kỳ bệnh nhân nào. |
| **8** | **C** | $F1 = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}$ là trung bình điều hòa (Harmonic Mean). |
| **9** | **B** | Đường cong ROC biểu diễn TPR (Recall) theo FPR ($1 - \text{Specificity}$). |
| **10** | **C** | Bộ phân lớp ngẫu nhiên (đường gạch đứt chéo) có diện tích $\text{AUC} = 0.5$. Bộ phân lớp hoàn hảo có $\text{AUC} = 1.0$. |
| **11** | **C** | Chiến lược OvO tạo $\frac{N(N-1)}{2}$ bộ phân lớp nhị phân cho từng cặp lớp (MNIST 10 lớp cần 45 bộ). |
| **12** | **B** | OvO ưu tiên cho SVM vì SVM học chậm trên dữ liệu lớn, OvO giúp chia nhỏ dữ liệu train cho từng cặp. |
| **13** | **C** | Bài toán dự đoán nhiều nhãn nhị phân cùng lúc (Số $>7$? và Số lẻ?) là Phân lớp Đa nhãn (Multilabel). |
| **14** | **C** | Khử nhiễu ảnh dự đoán 784 pixel, mỗi pixel có thể nhận nhiều giá trị $[0, 255]$ $\rightarrow$ Multioutput classification. |
| **15** | **B** | `roc_auc_score(y_true, y_scores)` tính chỉ số AUC của đường cong ROC trong Scikit-Learn. |
