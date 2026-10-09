# CHƯƠNG 2: QUY TRÌNH THỰC HIỆN DỰ ÁN MÁY HỌC

> **Tài liệu học tập & Tổng hợp chi tiết từ Giáo trình Máy học**  
> **Chủ đề:** Quy trình 8 bước chuẩn xây dựng dự án Machine Learning từ bài toán thực tế.

---

## MỤC LỤC
1. [2.1 Sơ đồ quy trình 8 bước chuẩn](#21-sơ-đồ-quy-trình-8-bước-chuẩn)
2. [2.2 Chi tiết 8 bước thực hiện dự án](#22-chi-tiết-8-bước-thực-hiện-dự-án)
   - [Bước 1: Xác định bối cảnh & Yêu cầu bài toán](#bước-1-xác-định-bối-cảnh--yêu-cầu-bài-toán)
   - [Bước 2: Thu thập dữ liệu](#bước-2-thu-thập-dữ-liệu)
   - [Bước 3: Khám phá dữ liệu (EDA)](#bước-3-khám-phá-dữ-liệu-eda)
   - [Bước 4: Chuẩn bị dữ liệu (Data Preprocessing)](#bước-4-chuẩn-bị-dữ-liệu-data-preprocessing)
   - [Bước 5: Huấn luyện mô hình](#bước-5-huấn-luyện-mô-hình)
   - [Bước 6: Tinh chỉnh mô hình (Model Tuning)](#bước-6-tinh-chỉnh-mô-hình-model-tuning)
   - [Bước 7: Trình bày giải pháp](#bước-7-trình-bày-giải-pháp)
   - [Bước 8: Vận hành, theo dõi và bảo trì (MLOps/Deployment)](#bước-8-vận-hành-theo-dõi-và-bảo-trì-mlopsdeployment)

---

## 2.1 Sơ đồ quy trình 8 bước chuẩn

Một dự án Máy học trong thực tế được thực hiện qua **8 bước quy chuẩn**:

```
[1. Bối cảnh & Yêu cầu] ➔ [2. Thu thập Dữ liệu] ➔ [3. Khám phá Dữ liệu (EDA)]
                                                            │
[6. Tinh chỉnh Mô hình] ◄─ [5. Huấn luyện Mô hình] ◄─ [4. Chuẩn bị Dữ liệu]
          │
          ▼
[7. Trình bày Giải pháp] ➔ [8. Vận hành, Theo dõi & Bảo trì (MLOps)]
```

---

## 2.2 Chi tiết 8 bước thực hiện dự án

### Bước 1: Xác định bối cảnh & Yêu cầu bài toán
* Hiểu rõ mục tiêu kinh doanh (Business Objective) và cách giải pháp máy học sẽ được sử dụng.
* Xác định hệ thống hiện tại đang hoạt động như thế nào.
* Lựa chọn loại bài toán (Supervised/Unsupervised, Binary/Multiclass, Online/Batch).
* Chọn thước đo hiệu năng (Performance Metrics):
  - *Hồi quy:* RMSE (Root Mean Squared Error), MAE (Mean Absolute Error).
  - *Phân loại:* Accuracy, Precision, Recall, F1-Score, AUC.

### Bước 2: Thu thập dữ liệu
* Tìm kiếm và tổng hợp nguồn dữ liệu.
* Dữ liệu thực hành ví dụ: *California Housing Prices Dataset* (Dữ liệu giá nhà ở California năm 1990).
* Một số kho dữ liệu mở phổ biến:
  - UCI Machine Learning Repository
  - Kaggle Datasets
  - Amazon AWS Open Datasets
  - Data Portals, OpenDataMonitor, Quandl...

### Bước 3: Khám phá dữ liệu (EDA - Exploratory Data Analysis)
* Nghiên cứu cấu trúc dữ liệu: Số lượng dòng/cột, kiểu dữ liệu (`info()`, `describe()`).
* Trực quan hóa dữ liệu (Matplotlib, Seaborn): Vẽ biểu đồ phân bố (Histogram), biểu đồ phân tán (Scatter Plot).
* Kiểm tra mối tương quan giữa các thuộc tính (Ma trận tương quan Pearson).
* Thử nghiệm kết hợp các thuộc tính để tạo thuộc tính mới tiềm năng.

### Bước 4: Chuẩn bị dữ liệu (Data Preprocessing)
* **Xử lý thiếu dữ liệu (Missing Values):** Bỏ dòng, bỏ cột, hoặc điền giá trị (Imputation: trung bình, trung vị, tần suất). Dùng `SimpleImputer`.
* **Xử lý thuộc tính dạng phân loại (Categorical Attributes):**
  - *Ordinal Encoding:* Chuyển thành số có thứ tự (`OrdinalEncoder`).
  - *One-Hot Encoding:* Biến đổi thành vector nhị phân (`OneHotEncoder`).
* **Chuẩn hóa đặc trưng (Feature Scaling):**
  - *Min-Max Scaling (Normalization):* Đưa giá trị về đoạn $[0, 1]$.
  - *Standardization:* Trừ giá trị trung bình $\mu$ và chia cho độ lệch chuẩn $\sigma$ (đưa về phân bố có trung bình 0, phương sai 1). Dùng `StandardScaler`.
* **Xây dựng Pipeline:** Tự động hóa toàn bộ bước biến đổi dữ liệu bằng `Pipeline` và `ColumnTransformer` của Scikit-Learn.

### Bước 5: Huấn luyện mô hình
* Huấn luyện các mô hình cơ bản (Baseline Models): Linear Regression, Decision Tree, Random Forest, SVM...
* Đánh giá hiệu năng ban đầu bằng phương pháp **Thẩm định chéo (K-Fold Cross Validation)**: Chia dữ liệu huấn luyện thành $K$ phần, dùng $K-1$ phần để học và 1 phần để kiểm tra, lặp lại $K$ lần và lấy trung bình.
* Phát hiện các vấn đề Underfitting hoặc Overfitting ban đầu.

### Bước 6: Tinh chỉnh mô hình (Model Tuning)
* **Grid Search (`GridSearchCV`):** Thử toàn bộ các tổ hợp siêu tham số được định sẵn. Phù hợp khi số lượng tổ hợp nhỏ.
* **Randomized Search (`RandomizedSearchCV`):** Chọn ngẫu nhiên bộ giá trị trong không gian tìm kiếm qua mỗi vòng lặp. Thích hợp cho không gian tìm kiếm lớn, giúp tiết kiệm tài nguyên.
* **Ensemble Methods:** Kết hợp nhiều mô hình thành phần để nâng cao độ chính xác (ví dụ: Random Forest kết hợp nhiều Decision Tree).
* **Phân tích lỗi (Error Analysis):** Đánh giá mức độ quan trọng của các thuộc tính (`feature_importances_`), soi kỹ các trường hợp mô hình dự đoán sai để cải tiến bước chuẩn bị dữ liệu.
* **Đánh giá cuối cùng trên tập Test:** Chạy pipeline hoàn chỉnh để đo đạc kết quả trên tập kiểm thử (không được tinh chỉnh thêm sau bước này).

### Bước 7: Trình bày giải pháp
* Viết báo cáo rõ ràng: Nêu bật các phát hiện, giải pháp hiệu quả và không hiệu quả, giả định đã dùng, hạn chế của hệ thống.
* Trực quan hóa kết quả và tạo tài liệu hướng dẫn vận hành.

### Bước 8: Vận hành, theo dõi và bảo trì (MLOps / Deployment)
* **Triển khai (Deploy):** Lưu mô hình và pipeline bằng `joblib` hoặc `pickle`. Đóng gói thành Web Service (REST API / FastAPI / Flask) hoặc deploy lên Cloud (Google Cloud AI Platform, AWS SageMaker).
* **Theo dõi (Monitoring):** Theo dõi hiệu năng theo thời gian (Downstream metrics).
* **Bảo trì:** Định kỳ thu thập dữ liệu mới, gán nhãn và huấn luyện lại mô hình để tránh hiện tượng suy giảm chất lượng (*Concept Drift / Data Drift*).

---

> **Tài liệu tham khảo:** *Hands-on Machine Learning with Scikit-Learn, Keras & TensorFlow (2nd Edition)* – Aurélien Géron.
