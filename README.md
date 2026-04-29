# 📊 Data Mining — Project Cuối Kỳ

> **Môn:** Khám Phá Dữ Liệu  
> **Đề tài chính:** Dự đoán trầm cảm sinh viên dựa trên áp lực học tập, giờ ngủ, stress tài chính và lối sống

---

## 📁 Cấu trúc thư mục

```
project/
│
├── 📓 student_depression.ipynb                ← Notebook chính (ĐỀ TÀI MỚI — chạy file này)
├── 📓 mobile_addiction.ipynb                  ← Notebook đề tài cũ (mobile addiction)
├── 📂 charts/ 
│   ├── 📊 Student_Depression_Dataset.csv
│   └── 📊 mobile_addiction_data.csv
│
├── 📦 requirements.txt                        ← Danh sách thư viện cần cài
├── 📖 README.md                               ← File mô tả cơ bản
│
└── 📂 charts/                                 ← Thư mục chứa biểu đồ (tự tạo khi chạy notebook)
    ├── 01_target_distribution.png
    ├── 02_feature_distributions.png
    └── ...
```

---

## 📋 Mô tả chi tiết các file

### 🔵 File chính

| File | Mô tả | Trạng thái |
|---|---|---|
| `student_depression.ipynb` | Notebook đầy đủ: EDA → tiền xử lý → 4 mô hình (LR, DT, RF, XGBoost) → đánh giá → kết luận | ✅ **Chạy file này** |
| `Student_Depression_Dataset.csv` | 27,901 sinh viên × 18 cột. Dữ liệu thực. Nhãn: `Depression` (0/1) | ✅ Tải từ Kaggle |
| `requirements.txt` | Danh sách toàn bộ thư viện Python cần thiết | ✅ Dùng để cài |

### 🟡 File tham khảo / đề tài cũ

| File | Mô tả | Ghi chú |
|---|---|---|
| `mobile_addiction.ipynb` | Notebook đề tài cũ: phân loại mức độ nghiện điện thoại | ⚠️ Dataset synthetic — accuracy ~25% |
| `mobile_addiction_data.csv` | 3,000 mẫu × 34 cột. **Synthetic data** — nhãn gán ngẫu nhiên | ⚠️ Không dùng cho đề tài mới |
| `BaoCao_PhanLoai_NghienDienThoai.docx` | Báo cáo Word hoàn chỉnh đề tài cũ (6 chương, có biểu đồ) | 📄 Tham khảo |
| `MauBaoCao.docx` | Template mẫu cấu trúc báo cáo từ giảng viên | 📄 Template |
| `Yêu_cầu_project_cuối_kì` | Đề bài, danh sách thuật toán, yêu cầu đánh giá | 📋 Đề bài |

### 🟢 Dataset chính — Student Depression Dataset

| Thông tin | Chi tiết |
|---|---|
| **Nguồn** | [Kaggle — adilshamim8](https://www.kaggle.com/datasets/adilshamim8/student-depression-dataset) |
| **Số mẫu** | 27,901 sinh viên |
| **Số cột** | 18 thuộc tính |
| **Target** | `Depression` (0 = không trầm cảm, 1 = có trầm cảm) |
| **Loại dữ liệu** | Dữ liệu khảo sát thực tế |
| **Accuracy kỳ vọng** | 83–85% (AUC ~0.91) |

**Các cột quan trọng:**

| Cột | Kiểu | Mô tả |
|---|---|---|
| `Academic Pressure` | Float (0–5) | Mức độ áp lực học tập |
| `Financial Stress` | Float (0–5) | Mức độ stress tài chính |
| `Sleep Duration` | Categorical | Thời gian ngủ mỗi ngày |
| `Dietary Habits` | Categorical | Chế độ ăn uống |
| `Have you ever had suicidal thoughts ?` | Yes/No | Tiền sử suy nghĩ tự tử |
| `Family History of Mental Illness` | Yes/No | Tiền sử bệnh tâm thần trong gia đình |
| `CGPA` | Float | Điểm trung bình tích lũy |
| `Work/Study Hours` | Float | Số giờ học/làm mỗi ngày |
| `Depression` | 0/1 | **Biến mục tiêu** |

---

## ⚙️ Hướng dẫn cài đặt & Chạy

### Bước 1 — Tạo môi trường ảo

#### `venv` (built-in, không cần cài thêm) — Khuyến nghị

Chạy trong Git Bash:

```bash
# Tạo môi trường
python -m venv venv

# Kích hoạt
source venv/Scripts/activate
```

```bash
# Thoát môi trường
deactivate

# Xóa môi trường khi không cần
rmdir /s /q venv            # Windows
rm -rf venv                 # macOS / Linux
```

---

### Bước 2 — Cài đặt thư viện

Sau khi kích hoạt môi trường ảo:

```bash
pip install -r requirements.txt
```

---

## 📈 Kết quả kỳ vọng

| Mô hình | Accuracy | AUC | Ghi chú |
|---|---|---|---|
| Logistic Regression | ~80% | ~0.87 | Baseline tốt, dễ giải thích |
| Decision Tree | ~82% | ~0.88 | Có thể visualize cây |
| **Random Forest** | **~84%** | **~0.91** | Ổn định, ít overfitting |
| **XGBoost** | **~85%** | **~0.92** | Tốt nhất, nhanh |

> Kết quả thực tế có thể dao động nhẹ tùy phiên bản thư viện và random seed.

---

## 📚 Tài liệu tham khảo

- [Student Depression Dataset — Kaggle](https://www.kaggle.com/datasets/adilshamim8/student-depression-dataset)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [XGBoost Documentation](https://xgboost.readthedocs.io/)
- Noviandy, T.R., et al. (2025). *An Explainable ML Study of Behavioral and Psychological Determinants of Depression*. Journal of Educational Management and Learning, 3(1).
- WHO. (2023). *Depressive disorder (depression)*. WHO Fact Sheet.

---

*README — Data Mining Project Cuối Kỳ 2026*
