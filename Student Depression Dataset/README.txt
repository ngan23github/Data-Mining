===========================================================
  KHAI PHÁ DỮ LIỆU SỨC KHỎE TÂM THẦN SINH VIÊN - Student Depression Dataset
===========================================================

MÔ TẢ CẤU TRÚC THƯ MỤC
----------------------------------------------------------

data/
  Student_Depression_Dataset.csv
      Bộ dữ liệu gốc được tải từ Kaggle, gồm 27.901 dòng và 18 cột, chứa thông tin về nhân khẩu học, thói quen
      sinh hoạt, mức độ áp lực và tình trạng trầm cảm của sinh viên. Đây là đầu vào chính cho toàn bộ quá trình
      phân tích và mô hình hóa trong dự án.

eda.ipynb
      Jupyter Notebook thực hiện bước Phân tích Khám phá Dữ liệu (Exploratory Data Analysis — EDA), bao gồm:
        - Phân tích đơn biến (phân bố biến mục tiêu, các thuộc tính số và phân loại)
        - Phân tích hai biến (tỷ lệ trầm cảm theo từng yếu tố như áp lực học tập, giờ ngủ, chế độ ăn,...)
        - Phân tích đa biến (heatmap kết hợp, ma trận tương quan)
      Chạy file này trước để nắm tổng quan dữ liệu.

classification.ipynb
      Jupyter Notebook giải quyết bài toán Phân loại — dự đoán một sinh viên có nguy cơ trầm cảm hay không. Nội
      dung bao gồm:
        - Tiền xử lý, mã hóa và chuẩn hóa dữ liệu
        - Huấn luyện và so sánh 3 mô hình: Logistic Regression, Random Forest, XGBoost
        - Đánh giá theo Accuracy, Precision, Recall, F1-score và AUC

clustering.ipynb
      Jupyter Notebook giải quyết bài toán Phân cụm — nhóm sinh viên theo mức độ nguy cơ sức khỏe tâm thần. Nội
      dung bao gồm:
        - Tạo các đặc trưng tổng hợp (Mental_Risk_Score, Stress_Index, Lifestyle_Index,...)
        - Xác định số cụm bằng Elbow Method và Dendrogram
        - So sánh K-Means và Hierarchical Clustering
        - Đánh giá theo Silhouette Score, Davies-Bouldin Index, Dunn's Index

requirements.txt
      Danh sách tất cả các thư viện Python cần thiết để chạy dự án, kèm phiên bản tương ứng. Để cài đặt
      toàn bộ, chạy lệnh: pip install -r requirements.txt

===========================================================
HƯỚNG DẪN CHẠY DỰ ÁN
----------------------------------------------------------
1. Cài đặt môi trường:
     pip install -r requirements.txt

2. Chạy các notebook theo thứ tự:
     Bước 1 — eda.ipynb            (phân tích khám phá)
     Bước 2 — classification.ipynb (mô hình phân loại)
     Bước 3 — clustering.ipynb     (mô hình phân cụm)

3. Dữ liệu đầu vào đặt tại: data/Student_Depression_Dataset.csv

===========================================================
THÔNG TIN NHÓM
----------------------------------------------------------
Nhóm       : 03
Thành viên : Lâm Tú Nhi       — MSSV: 3123410250
             Lê Đoàn Kim Ngân — MSSV: 3123410231
===========================================================