# CHƯƠNG 3: PHÂN LỚP VÀ ĐÁNH GIÁ BỘ PHÂN LỚP (CLASSIFICATION & METRICS)

> **Tài liệu học tập & Tổng hợp chi tiết từ Giáo trình Máy học**  
> **Chủ đề:** Phân lớp nhị phân, phân lớp đa lớp, đa nhãn, đa đầu vào và các thước đo hiệu năng.

---

## MỤC LỤC
1. [3.1 Bộ dữ liệu MNIST](#31-bộ-dữ-liệu-mnist)
2. [3.2 Bài toán Phân lớp Nhị phân (Binary Classification)](#32-bài-toán-phân-lớp-nhị-phân-binary-classification)
3. [3.3 Đánh giá hiệu quả Phân lớp](#33-đánh-giá-hiệu-quả-phân-lớp)
   - [Ma trận nhầm lẫn (Confusion Matrix)](#ma-trận-nhầm-lẫn-confusion-matrix)
   - [Độ chính xác (Accuracy) & Vấn đề dữ liệu lệch (Imbalanced Data)](#độ-chính-xác-accuracy--vấn-đề-dữ-liệu-lệch-imbalanced-data)
   - [Precision, Recall & F1-Score](#precision-recall--f1-score)
   - [Đánh đổi Precision/Recall & Ngưỡng quyết định](#đánh-đổi-precisionrecall--ngưỡng-quyết-định)
   - [Đường cong ROC & Chỉ số AUC](#đường-cong-roc--chỉ-số-auc)
4. [3.4 Bài toán Phân lớp Đa lớp (Multiclass Classification)](#34-bài-toán-phân-lớp-đa-lớp-multiclass-classification)
   - [Chiến lược OvR (One-vs-Rest) và OvO (One-vs-One)](#chiến-lược-ovr-one-vs-rest-và-ovo-one-vs-one)
5. [3.5 Bài toán Phân lớp Đa nhãn (Multilabel Classification)](#35-bài-toán-phân-lớp-đa-nhãn-multilabel-classification)
6. [3.6 Bài toán Phân lớp Đa đầu vào (Multioutput Classification)](#36-bài-toán-phân-lớp-đa-đầu-vào-multioutput-classification)
7. [3.7 Thực hành tổng hợp với Scikit-Learn](#37-thực-hành-tổng-hợp-với-scikit-learn)

---

## 3.1 Bộ dữ liệu MNIST
* Được coi là bài toán "Hello World" của Máy học.
* Gồm 70.000 ảnh xám kích thước $28 \times 28$ pixel biểu diễn chữ số viết tay từ 0 đến 9 của học sinh phổ thông và nhân viên Cục điều tra dân số Mỹ.
* Được phân chia sẵn: **60.000 ảnh huấn luyện** và **10.000 ảnh kiểm thử**.
* Mỗi ảnh được biểu diễn bằng 784 đặc trưng (mỗi đặc trưng ứng với độ sáng một pixel từ 0 đến 255).

---

## 3.2 Bài toán Phân lớp Nhị phân (Binary Classification)

Bài toán chỉ có **2 lớp đầu ra**: Positive (Dương tính / True) và Negative (Âm tính / False).
* *Ví dụ 1:* Nhận dạng chữ số 5 (True: "là số 5", False: "không phải số 5").
* *Ví dụ 2:* Thử nghiệm nCoV (True: "dương tính", False: "âm tính").
* *Thuật toán phổ biến:* SGD (Stochastic Gradient Descent Classifier), Logistic Regression, Binary SVM.

---

## 3.3 Đánh giá hiệu quả Phân lớp

### Ma trận nhầm lẫn (Confusion Matrix)
Ma trận thể hiện số lượng điểm dữ liệu thuộc lớp thực tế (dòng) được dự đoán vào từng lớp (cột).

| Thực tế \ Dự đoán | Dự đoán Negative (0) | Dự đoán Positive (1) |
| :--- | :---: | :---: |
| **Thực tế Negative (0)** | **TN** (True Negative) | **FP** (False Positive) *(Lỗi Loại I)* |
| **Thực tế Positive (1)** | **FN** (False Negative) *(Lỗi Loại II)* | **TP** (True Positive) |

### Độ chính xác (Accuracy) & Vấn đề dữ liệu lệch (Imbalanced Data)
* **Công thức Accuracy:**
  $$\text{Accuracy} = \frac{\text{TP} + \text{TN}}{\text{TP} + \text{TN} + \text{FP} + \text{FN}}$$
* **Hạn chế:** Accuracy **KHÔNG** phải là thước đo tốt khi tập dữ liệu bị lệch (imbalanced/skewed dataset).  
  *Ví dụ:* Trong tập dữ liệu có 90% mẫu là "Non-5" và 10% là "5", một mô hình ngu ngốc luôn dự đoán mọi mẫu là "Non-5" vẫn đạt **Accuracy = 90%**, nhưng mô hình này hoàn toàn vô dụng.

### Precision, Recall & F1-Score

1. **Precision (Độ chính xác dự đoán dương tính):**  
   $$\text{Precision} = \frac{\text{TP}}{\text{TP} + \text{FP}}$$  
   *Ý nghĩa:* Trong số những mẫu mô hình dự đoán là Positive, có bao nhiêu phần trăm là Positive thật sự?
   
2. **Recall (Độ phủ / Độ nhạy - Sensitivity / True Positive Rate):**  
   $$\text{Recall} = \frac{\text{TP}}{\text{TP} + \text{FN}}$$  
   *Ý nghĩa:* Trong số những mẫu Positive thực tế, mô hình đã bắt được bao nhiêu phần trăm?

3. **F1-Score (Trung bình điều hòa giữa Precision và Recall):**  
   $$\text{F1} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}} = \frac{\text{TP}}{\text{TP} + \frac{\text{FP} + \text{FN}}{2}}$$  
   *Dùng khi:* Cần một chỉ số kết hợp cả Precision và Recall có vai trò ngang nhau.

### Đánh đổi Precision/Recall & Ngưỡng quyết định (Decision Threshold)
* Không thể vừa tối ưu Precision vừa tối ưu Recall (tăng Precision thì Recall giảm và ngược lại).
* **Ứng dụng thực tế theo yêu cầu bài toán:**
  - *Ưu tiên Precision cao:* Bài toán lọc video an toàn cho trẻ em (thà bỏ sót video an toàn chứ không được duyệt nhầm video độc hại).
  - *Ưu tiên Recall cao:* Bài toán phát hiện bệnh ung thư, phát hiện trộm cắp siêu thị (thà cảnh báo nhầm chứ nhất quyết không được bỏ sót người bệnh/kẻ trộm).

### Đường cong ROC & Chỉ số AUC
* **Đường cong ROC (Receiver Operating Characteristic):** Biểu diễn mối quan hệ giữa **TPR (Recall)** và **FPR (False Positive Rate)** trên nhiều ngưỡng quyết định khác nhau.
  $$\text{FPR} = \frac{\text{FP}}{\text{FP} + \text{TN}} = 1 - \text{Specificity}$$
* **Chỉ số AUC (Area Under the Curve):** Diện tích nằm dưới đường cong ROC.
  - $\text{AUC} = 1.0$: Bộ phân lớp lý tưởng (hoàn hảo).
  - $\text{AUC} = 0.5$: Bộ phân lớp ngẫu nhiên (đường gạch đứt).
  - So sánh AUC là phương pháp tiêu chuẩn để so sánh hiệu năng giữa các bộ phân lớp khác nhau (ví dụ: SGD vs Random Forest).

---

## 3.4 Bài toán Phân lớp Đa lớp (Multiclass Classification)

Phân loại điểm dữ liệu vào **nhiều hơn 2 lớp** (ví dụ: nhận dạng 10 chữ số từ 0 đến 9).

### Chiến lược chuyển đổi từ mô hình Phân lớp Nhị phân:
1. **One-vs-Rest (OvR) / One-vs-All:**
   - Xây dựng $N$ bộ phân lớp nhị phân (mỗi bộ cho 1 lớp vs tất cả các lớp còn lại).
   - Khi dự đoán, chọn lớp có điểm số quyết định cao nhất.
   - *Ưu điểm:* Dễ triển khai, được ưu tiên cho đa số thuật toán.
2. **One-vs-One (OvO):**
   - Xây dựng $\frac{N(N-1)}{2}$ bộ phân lớp nhị phân cho từng cặp lớp (ví dụ MNIST 10 lớp cần $45$ bộ phân lớp).
   - Khi dự đoán, chọn lớp chiến thắng nhiều cuộc bình chọn nhất.
   - *Ưu điểm:* Mỗi bộ phân lớp chỉ cần huấn luyện trên tập dữ liệu con nhỏ chứa 2 lớp đó → Rất thích hợp cho các thuật toán huấn luyện chậm trên dữ liệu lớn như **SVM**.

---

## 3.5 Bài toán Phân lớp Đa nhãn (Multilabel Classification)

Mỗi mẫu dữ liệu có thể được gán **nhiều nhãn đầu ra nhị phân cùng lúc**.
* *Ví dụ:* Nhận dạng chữ số MNIST với 2 đầu ra:
  - Nhãn 1: Chữ số có lớn hơn hoặc bằng 7 không? (True/False)
  - Nhãn 2: Chữ số có phải số lẻ không? (True/False)
  *Nhập vào ảnh số 9 → Đầu ra: `[True, True]`.*
* **Đánh giá:** Tính F1-score riêng cho từng nhãn rồi lấy trung bình (Macro/Weighted F1-score).

---

## 3.6 Bài toán Phân lớp Đa đầu vào (Multioutput Classification)

Là trường hợp tổng quát của Phân lớp đa nhãn, trong đó **mỗi nhãn đầu ra có thể nhận nhiều hơn 2 giá trị**.
* *Ví dụ điển hình:* Bài toán **Khử nhiễu ảnh (Image Denoising)**.
  - **Đầu vào:** Ảnh chữ số viết tay bị nhiễu.
  - **Đầu ra:** Ảnh sạch đã khử nhiễu gồm 784 pixel, mỗi pixel là một đầu ra nhận giá trị độ sáng từ $0$ đến $255$.

---

## 3.7 Thực hành tổng hợp với Scikit-Learn

### Các hàm & Lớp quan trọng cần nhớ trong Scikit-Learn:
```python
# 1. Tải bộ dữ liệu
from sklearn.datasets import fetch_openml
mnist = fetch_openml('mnist_784', version=1)

# 2. Xử lý chuẩn hóa & Chia tập dữ liệu
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)

# 3. Huấn luyện mô hình
from sklearn.linear_model import SGDClassifier
from sklearn.ensemble import RandomForestClassifier
sgd_clf = SGDClassifier(random_state=42)
sgd_clf.fit(X_train, y_train_5)

# 4. Thẩm định chéo & Ma trận nhầm lẫn
from sklearn.model_selection import cross_val_score, cross_val_predict
from sklearn.metrics import confusion_matrix, precision_score, recall_score, f1_score
y_train_pred = cross_val_predict(sgd_clf, X_train, y_train_5, cv=3)
cm = confusion_matrix(y_train_5, y_train_pred)

# 5. Đường cong Precision-Recall & ROC/AUC
from sklearn.metrics import precision_recall_curve, roc_curve, roc_auc_score
fpr, tpr, thresholds = roc_curve(y_train_5, y_scores)
auc_score = roc_auc_score(y_train_5, y_scores)

# 6. Chiến lược OvO / OvR cho Phân lớp Đa lớp
from sklearn.multiclass import OneVsOneClassifier, OneVsRestClassifier
ovo_clf = OneVsOneClassifier(SGDClassifier(random_state=42))
```

---

> **Tài liệu tham khảo:** *Hands-on Machine Learning with Scikit-Learn, Keras & TensorFlow (2nd Edition)* – Aurélien Géron.
