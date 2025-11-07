# Xử lý dữ liệu và Xây dựng mô hình dự đoán bệnh

## 1. Giới thiệu
Dự án này nhằm mục tiêu **xây dựng mô hình dự đoán khả năng mắc bệnh của bệnh nhân** dựa trên các đặc trưng y học có sẵn. Quá trình thực hiện bao gồm các bước xử lý dữ liệu, khám phá đặc trưng, và huấn luyện mô hình học máy (Machine Learning).

---

## 2. Dữ liệu
- **Nguồn dữ liệu:** Bộ dữ liệu gồm thông tin cá nhân và chỉ số sức khỏe của bệnh nhân.  
- **Các cột chính:** Tuổi, giới tính, huyết áp, đường huyết, cholesterol, v.v.  
- **Cột mục tiêu (Target):** Biến nhị phân cho biết bệnh nhân có mắc bệnh hay không.  
- **Cột không liên quan:** `id` (đã bị loại bỏ vì không mang thông tin dự đoán).

---

## 3. Xử lý dữ liệu
- **Làm sạch dữ liệu:**
  - Xóa cột `id` không liên quan.  
  - Kiểm tra và xử lý giá trị thiếu (missing values).  
  - Mã hóa các biến phân loại bằng **One-Hot Encoding**. 
  - v.v 

- **Phát hiện và xử lý ngoại lai (Outliers):**
  - Dùng phương pháp **IQR (Interquartile Range)** để phát hiện giá trị bất thường.  
  - Sử dụng `np.clip()` để thay thế các giá trị vượt ngoài ngưỡng bằng **giới hạn hợp lý (lower_bound / upper_bound)**.  

- **Chuẩn hóa dữ liệu:**  
  Giúp đảm bảo mô hình học ổn định và tránh ảnh hưởng của thang đo khác nhau giữa các biến.

---

## 4. Xây dựng mô hình
- **Mục tiêu:** Dự đoán khả năng mắc bệnh của bệnh nhân.  
- **Các bước chính:**
  1. Chia dữ liệu thành tập huấn luyện và kiểm tra.  
  2. Huấn luyện mô hình (ví dụ: Logistic Regression, Random Forest,...).  
  3. Đánh giá mô hình bằng các chỉ số: Accuracy, Precision, Recall, F1-score.  

---

## 5. Kết luận
Dự án giúp rèn luyện kỹ năng **tiền xử lý dữ liệu, phát hiện ngoại lai, và xây dựng mô hình dự đoán** — các bước quan trọng trong quy trình **Data Science**.  
Kết quả mô hình có thể được sử dụng để **hỗ trợ chẩn đoán sớm và ra quyết định y tế chính xác hơn**.

---
