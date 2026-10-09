# 🚀 CHƯƠNG 2: 8 BƯỚC LÀM DỰ ÁN MÁY HỌC (PHƯƠNG PHÁP FEYNMAN)

> 💡 **Dành cho học sinh cấp 2:** Làm một dự án Máy học giống hệt như việc **nấu một món ăn ngon** cho cuộc thi Vua Đầu Bếp (MasterChef). Hãy cùng trải qua 8 chặng chơi game này nhé!

---

## 🎮 HÀNH TRÌNH 8 CHẶNG LÀM DỰ ÁN MÁY HỌC

```
Chặng 1: Đọc đề bài ➔ Chặng 2: Đi chợ mua nguyên liệu ➔ Chặng 3: Nếm thử nguyên liệu (EDA)
                                                                       │
Chặng 6: Nêm nếm gia vị ◄─ Chặng 5: Nấu thử mô hình ◄─ Chặng 4: Sơ chế làm sạch dữ liệu
       │
       ▼
Chặng 7: Dọn món thuyết trình ➔ Chặng 8: Mở nhà hàng & Theo dõi chất lượng
```

---

### 🧩 Chặng 1: Xác định bối cảnh - "Đề bài yêu cầu nấu món gì?"
* Trước khi lao vào máy tính gõ code, hãy tự hỏi:
  - Chúng ta làm robot này để làm gì? (Ví dụ: Dự đoán giá nhà ở California để giúp người nghèo mua nhà).
  - Kết quả đo bằng thước đo gì? (Đo bằng độ lệch trung bình RMSE - giống như đo độ mặn của nước dùng).

---

### 🛒 Chặng 2: Thu thập dữ liệu - "Đi chợ nhặt nguyên liệu"
* Robot không thể thông minh nếu không có dữ liệu.
* Bạn sẽ lên các "chợ dữ liệu miễn phí" nổi tiếng như:
  - **Kaggle Datasets** (Kho dữ liệu lớn nhất thế giới của dân Data).
  - **UCI Machine Learning Repository** (Kho dữ liệu học tập kinh điển).

---

### 🔍 Chặng 3: Khám phá dữ liệu (EDA) - "Nắm rõ từng nguyên liệu"
* Nhìn ngắm bảng dữ liệu: Cột này là số phòng ngủ, cột kia là thu nhập trung bình, cột nọ là giá nhà.
* Vẽ biểu đồ hình ảnh (Histogram, Scatter Plot) để xem: *"Có nhà nào giá cao bất thường như 100 tỷ không?"* hay *"Khu vực gần biển giá nhà có đắt hơn không?"*.

---

### 🧹 Chặng 4: Chuẩn bị dữ liệu - "Rửa rau, gọt vỏ, thái thịt"
Đây là bước tốn nhiều thời gian nhất của nhà khoa học dữ liệu!
* **Nhặt rác / Điền chỗ trống:** Có những ngôi nhà bị thiếu thông tin số phòng $\rightarrow$ Phải điền số trung bình vào (`SimpleImputer`).
* **Biến chữ thành số:** Máy tính chỉ hiểu số, không hiểu chữ!
  - Chữ "Gần biển", "Trong đất liền" $\rightarrow$ Phải đổi thành mã số nhị phân `[1, 0, 0]` bằng kỹ thuật **One-Hot Encoding**.
* **Đưa về cùng kích thước (Scaling):**
  - Tuổi nhà từ $1$ đến $50$ năm.
  - Thu nhập từ $10.000\$ $ đến $1.000.000\$ $.
  - Nếu để nguyên, số tiền to quá sẽ đè bẹp số tuổi! Ta phải chuẩn hóa (`StandardScaler`) đưa tất cả về cùng một thước đo.

---

### 🍳 Chặng 5: Huấn luyện mô hình - "Cho robot học nấu ăn"
* Thử cho robot học bằng nhiều thuật toán khác nhau: Hồi quy tuyến tính (Linear Regression), Cây quyết định (Decision Tree), Rừng ngẫu nhiên (Random Forest).
* **Thi thử K-Fold Cross Validation:** Chia dữ liệu làm 5 phần. Cho máy học 4 phần rồi thi thử trên 1 phần còn lại. Lặp lại 5 lần để xem robot đạt bao nhiêu điểm trung bình!

---

### 🎛️ Chặng 6: Tinh chỉnh siêu tham số - "Nêm nếm gia vị tối ưu"
* Mỗi thuật toán có các "nút vặn" (Siêu tham số - Hyperparameters).
* **Grid Search:** Thử từng nút vặn một cách kiên nhẫn.
* **Randomized Search:** Vặn ngẫu nhiên các nút để tìm ra vị ngon nhất nhanh hơn.
* **Ensemble Methods:** Kết hợp 5 robot nhỏ lại thành 1 siêu robot (ví dụ: Random Forest kết hợp hàng trăm Decision Tree).

---

### 📢 Chặng 7: Trình bày giải pháp - "Khoe món ăn với ban giám khảo"
* Viết báo cáo giải thích: *"Mô hình của em giúp dự đoán chính xác giá nhà 92%, yếu tố ảnh hưởng lớn nhất là Thu Nhập của người dân!"*.

---

### 🏬 Chặng 8: Vận hành & Theo dõi (MLOps) - "Mở nhà hàng thực tế"
* Đóng gói mô hình thành một Web Service hoặc ứng dụng điện thoại.
* **Bảo trì liên tục:** Theo thời gian, giá nhà năm 2026 sẽ khác năm 1990. Nếu không cập nhật dữ liệu mới liên tục, mô hình sẽ bị "lạc hậu" (Concept Drift).

---

## 🎯 BÀI TẬP THỬ THÁCH FEYNMAN

1. Tại sao nếu không làm bước **Standardization (Chuẩn hóa đặc trưng)** ở Chặng 4 thì mô hình máy học sẽ bị "dẫn dắt" bởi những con số lớn?
2. Hãy tưởng tượng bạn làm một ứng dụng dự đoán giá Trà Sữa. Bạn sẽ thu thập những cột thông tin (đặc trưng) nào?
