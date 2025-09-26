# 🚦 Traffic Sign Recognition System  
> **Course Project – Introduction to Machine Learning**  
> Nhóm 14 – Lớp CNTT 17-03 – Khoa CNTT – Đại học Đại Nam  

[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)  
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.2-orange.svg)](https://scikit-learn.org/)  
[![OpenCV](https://img.shields.io/badge/opencv-4.8-green.svg)](https://opencv.org/)  

---

## 📑 Mục lục
- [Giới thiệu](#-giới-thiệu)
- [Mô hình đề xuất](#-mô-hình-đề-xuất)
- [Cấu trúc dữ liệu](#-cấu-trúc-dữ-liệu)
- [Cài đặt & Yêu cầu](#️-cài-đặt--yêu-cầu)
- [Cách chạy](#-cách-chạy)
- [Kết quả](#-kết-quả)
- [Thành viên nhóm](#-thành-viên-nhóm)
- [Tài liệu tham khảo](#-tài-liệu-tham-khảo)

---

## 📖 Giới thiệu
Bài toán **nhận dạng biển báo giao thông** là một ứng dụng quan trọng trong các hệ thống hỗ trợ lái xe và xe tự hành.  

Trong đồ án này, chúng tôi xây dựng một hệ thống phân loại ảnh biển báo dựa trên:  
- **Trích xuất đặc trưng bằng HOG (Histogram of Oriented Gradients)**  
- **Phân loại bằng KNN (K-Nearest Neighbors)**  

**Ưu điểm:**  
- Dễ triển khai, trực quan.  
- Hiệu quả đối với dữ liệu có hình dạng và cạnh đặc trưng rõ ràng như biển báo giao thông.  

---

## 🧠 Mô hình đề xuất
1. **Tiền xử lý dữ liệu**: Resize ảnh, chuyển về thang xám, chuẩn hóa.  
2. **Trích xuất đặc trưng (HOG)**: Mỗi ảnh được biểu diễn thành vector gradient theo hướng.  
3. **Huấn luyện & Dự đoán (KNN)**:  
   - Tính khoảng cách giữa vector đặc trưng ảnh mới với tập huấn luyện.  
   - Chọn ra *k* láng giềng gần nhất.  
   - Dự đoán nhãn theo luật đa số.  

Sơ đồ pipeline:  
Ảnh gốc → Tiền xử lý → Vector HOG → KNN → Nhãn biển báo
## 📂 Cấu trúc dữ liệu
Sử dụng dataset **[GTSRB – German Traffic Sign Recognition Benchmark](https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign)**


## ⚙️ Cài đặt & Yêu cầu
Cài đặt môi trường:  
```bash
pip install -r requirements.txt
```
##Cách chạy

Clone repo
```bash
git clone https://github.com/username/Traffic-Sign-Recognition-System.git
cd Traffic-Sign-Recognition-System
```
##Chuẩn bị dữ liệu

##Tải dataset GTSRB và giải nén vào thư mục gtsrb/.
## Chạy huấn luyện và đánh giá
```bash
python main.py
```
##Kết quả sẽ hiển thị:
Accuracy trên tập test.
##Báo cáo chi tiết (Precision, Recall, F1-score).
Confusion Matrix trực quan bằng heatmap.
##Kết quả
Độ chính xác (Accuracy): ~96%
Bảng phân loại:

              precision    recall  f1-score   support

           0       0.97      0.96      0.97       250
           1       0.95      0.95      0.95       240
           ...
