# 🧠 KHAI PHÁ DỮ LIỆU SỨC KHỎE TÂM THẦN SINH VIÊN
### Student Depression Dataset

---

## 📁 Mô tả cấu trúc thư mục

```
📦 project/
├── 📂 data/
│   └── Student_Depression_Dataset.csv
├── 📓 eda.ipynb
├── 📓 classification.ipynb
├── 📓 clustering.ipynb
├── 📄 README.md
└── 📄 requirements.txt
```

---

### `data/Student_Depression_Dataset.csv`
Bộ dữ liệu gốc được tải từ [Kaggle](https://www.kaggle.com/datasets/hopesb/student-depression-dataset/data), gồm **27.901 dòng** và **18 cột**, chứa thông tin về nhân khẩu học, thói quen sinh hoạt, mức độ áp lực và tình trạng trầm cảm của sinh viên. Đây là đầu vào chính cho toàn bộ quá trình phân tích và mô hình hóa trong dự án.

---

### `eda.ipynb`
Jupyter Notebook thực hiện bước **Phân tích Khám phá Dữ liệu** (Exploratory Data Analysis — EDA), bao gồm:
- **Phân tích đơn biến** — phân bố biến mục tiêu, các thuộc tính số và phân loại
- **Phân tích hai biến** — tỷ lệ trầm cảm theo từng yếu tố như áp lực học tập, giờ ngủ, chế độ ăn,...
- **Phân tích đa biến** — heatmap kết hợp, ma trận tương quan

> ⚠️ Chạy file này **trước tiên** để nắm tổng quan dữ liệu.

---

### `classification.ipynb`
Jupyter Notebook giải quyết **bài toán Phân loại** — dự đoán một sinh viên có nguy cơ trầm cảm hay không. Nội dung bao gồm:
- Tiền xử lý, mã hóa và chuẩn hóa dữ liệu
- Huấn luyện và so sánh 3 mô hình: **Logistic Regression**, **Random Forest**, **XGBoost**
- Đánh giá theo Accuracy, Precision, Recall, F1-score và AUC

---

### `clustering.ipynb`
Jupyter Notebook giải quyết **bài toán Phân cụm** — nhóm sinh viên theo mức độ nguy cơ sức khỏe tâm thần. Nội dung bao gồm:
- Tạo các đặc trưng tổng hợp (`Mental_Risk_Score`, `Stress_Index`, `Lifestyle_Index`,...)
- Xác định số cụm bằng **Elbow Method** và **Dendrogram**
- So sánh **K-Means** và **Hierarchical Clustering**
- Đánh giá theo Silhouette Score, Davies-Bouldin Index, Dunn's Index

---

## 🚀 Hướng dẫn chạy dự án

**Bước 1 — Cài đặt môi trường:**
```bash
pip install -r requirements.txt
```

**Bước 2 — Chạy các notebook theo thứ tự:**

| Thứ tự | File | Mục đích |
|:---:|---|---|
| 1 | `eda.ipynb` | Phân tích khám phá dữ liệu |
| 2 | `classification.ipynb` | Mô hình phân loại |
| 3 | `clustering.ipynb` | Mô hình phân cụm |

**Bước 3 — Dữ liệu đầu vào:**
```
data/Student_Depression_Dataset.csv
```

---

## 👥 Thông tin nhóm

| | |
|---|---|
| **Nhóm** | 03 |
| **Thành viên** | Lâm Tú Nhi — MSSV: 3123410250 |
| | Lê Đoàn Kim Ngân — MSSV: 3123410231 |