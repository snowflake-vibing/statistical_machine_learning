# 🎯 CHƯƠNG 3: BÍ MẬT CỦA BÀI TOÁN PHÂN LOẠI (PHƯƠNG PHÁP FEYNMAN)

> 💡 **Dành cho học sinh cấp 2:** Phân loại giống như việc bạn phân loại rác thải vào thùng nhựa / thùng giấy, hay thầy cô chấm bài kiểm tra ĐÚNG / SAI.

---

## ❓ CÂU HỎI 1: Bộ dữ liệu MNIST là gì mà ai học Máy học cũng phải biết?

* **MNIST** giống như bài tập *"Bảng cửu chương"* hay *"Hello World"* của dân Máy Học.
* Nó gồm **70.000 tấm ảnh nhỏ xíu** ($28 \times 28$ pixel) ghi lại chữ số viết tay từ $0$ đến $9$ của các bạn học sinh và nhân viên Mỹ.
* Nhiệm vụ của máy tính: Nhìn vào bức ảnh và đoán xem đó là số mấy!

---

## ❓ CÂU HỎI 2: Ma trận nhầm lẫn (Confusion Matrix) là gì?

Hãy tưởng tượng bạn chơi trò chơi nhận diện **"Con Chó hay Không Phải Con Chó"**. 
Ma trận nhầm lẫn giống như **Bảng ghi sổ nợ bài kiểm tra**:

| Thực tế \ Máy đoán | Máy đoán KHÔNG PHẢI CHÓ (0) | Máy đoán LÀ CON CHÓ (1) |
| :--- | :---: | :---: |
| **Thực tế KHÔNG PHẢI CHÓ** | **TN** *(Đoán đúng con mèo là không phải chó)* | **FP** *(Nhầm con mèo thành con chó - Lỗi báo động giả)* |
| **Thực tế LÀ CON CHÓ** | **FN** *(Bỏ sót con chó, bảo không phải)* | **TP** *(Đoán chuẩn xác con chó)* |

---

## ❓ CÂU HỎI 3: Tại sao đạt 90% Accuracy (Độ chính xác) vẫn có thể bị điểm F?

* **Bẫy dữ liệu lệch (Imbalanced Data):**
  - Tưởng tượng trong lớp có 90 bạn nữ và 10 bạn nam.
  - Một bạn học sinh nhắm mắt đoán bừa: *"Tất cả mọi người trong lớp đều là NỮ!"*.
  - Kết quả: Bạn ấy đoán đúng 90/100 bạn $\rightarrow$ **Accuracy = 90%**!
  - Nhưng bạn ấy có thực sự thông minh không? **Không hề!** Bạn ấy không nhận diện được bất kỳ bạn nam nào!

👉 Vì thế, chúng ta phải dùng 2 thước đo thông minh hơn: **Precision** và **Recall**.

---

## ❓ CÂU HỎI 4: Precision và Recall khác nhau thế nào? (Ví dụ siêu dễ nhớ)

### 👮 1. Precision (Độ chuẩn xác khi ra quyết định)
* **Câu chuyện Chú Công An:** Khi chú công an bắt nghi phạm: *"Đã bắt ai là phải đúng người đó, thà thả nhầm còn hơn bắt nhầm người tốt!"*.
* $\text{Precision} = \frac{\text{TP}}{\text{TP} + \text{FP}}$ (Số người bắt đúng / Tổng số người đã bị bắt).

### 🏥 2. Recall (Độ bao phủ / Không bỏ sót)
* **Câu chuyện Bác Sĩ Khám Bệnh Ung Thư:** Khi bác sĩ xét nghiệm bệnh nguy hiểm: *"Thà chẩn đoán nhầm 10 người khỏe mạnh để kiểm tra lại, chứ tuyệt đối KHÔNG ĐƯỢC BỎ SÓT 1 người bệnh nào!"*.
* $\text{Recall} = \frac{\text{TP}}{\text{TP} + \text{FN}}$ (Số bệnh nhân phát hiện được / Tổng số bệnh nhân thực tế).

### ⚖️ F1-Score: Sự hòa giải hoàn hảo
* $F1$-Score là trung bình điều hòa giữa Precision và Recall. Nếu 1 trong 2 cái bằng 0 thì F1 sẽ sụt giảm thảm hại!

---

## ❓ CÂU HỎI 5: Đấu 1-vs-Rest và 1-vs-1 là gì?

Khi phải phân loại 10 chữ số (từ 0 đến 9), các thuật toán nhị phân sẽ đấu thế nào?

1. **One-vs-Rest (OvR - Đấu với tất cả):**
   - Tạo 10 hiệp sĩ: Hiệp sĩ 0 (Đoán số 0 vs Không phải 0), Hiệp sĩ 1 (Số 1 vs Không phải 1)...
   - Hiệp sĩ nào hô to nhất (điểm cao nhất) thì chọn số đó!

2. **One-vs-One (OvO - Đấu vòng tròn từng cặp):**
   - Giống như giải bóng đá World Cup: Cho từng cặp đấu với nhau (Số 0 vs Số 1, Số 0 vs Số 2... tổng cộng 45 trận đấu).
   - Con số nào thắng nhiều trận nhất sẽ giành cúp vô địch!

---

## 🎯 BÀI TẬP THỬ THÁCH FEYNMAN

1. Trong bài toán **Phát hiện Email Lừa Đảo (Spam)**, bạn nên ưu tiên **Precision cao** hay **Recall cao**? Tại sao? (Gợi ý: Nếu lỡ chuyển thư quan trọng của sếp vào thùng rác thì sao?).
2. Trong bài toán **Phát hiện Trộm Cắp ở Siêu Thị**, bạn nên ưu tiên chỉ số nào?
