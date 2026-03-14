# Bank Transaction Profiling and Classification Pipeline 🏦🤖

Proyek ini merupakan Submission Akhir untuk kelas "Belajar Machine Learning untuk Pemula" dari program **Coding Camp 2026 Powered By DBS Foundation x Dicoding**.

## 📌 Deskripsi Proyek
Proyek ini mengimplementasikan pendekatan hibrida *Machine Learning* menggunakan algoritma **Unsupervised Learning** (Clustering) dan **Supervised Learning** (Classification) pada dataset transaksi bank. Tujuannya adalah untuk mengelompokkan nasabah berdasarkan perilaku transaksi mereka (customer profiling) dan membangun model yang dapat memprediksi profil nasabah baru secara akurat.

## 🛠️ Alur Kerja (Workflow)
1. **Data Preprocessing:** - Penanganan *missing values*, penghapusan duplikat, dan *handling outliers*.
   - *Feature Scaling* (StandardScaler) dan *Feature Encoding* (LabelEncoder & One-Hot Encoding).
2. **Unsupervised Learning (Clustering):**
   - Menemukan jumlah klaster optimal menggunakan **Elbow Method** (Silhouette Score).
   - Mengelompokkan data menggunakan **K-Means Clustering**.
   - Reduksi dimensi dan visualisasi klaster menggunakan **PCA (Principal Component Analysis)**.
   - *Inverse transform* untuk interpretasi karakteristik bisnis dari masing-masing klaster.
3. **Supervised Learning (Classification):**
   - Menggunakan hasil klasterisasi sebagai variabel Target (`y`).
   - Melatih model dasar menggunakan **Decision Tree Classifier**.
   - Melatih model pembanding menggunakan **Random Forest Classifier**.
   - Meningkatkan performa model melalui **Hyperparameter Tuning** dengan `GridSearchCV`.

## 💻 Tech Stack
- **Bahasa:** Python
- **Library Utama:** Pandas, NumPy, Scikit-Learn, Seaborn, Matplotlib, Yellowbrick.

## 🚀 Hasil dan Kesimpulan
Model berhasil mengidentifikasi 4 profil utama nasabah berdasarkan perilaku transaksi dan daya beli. Model *Random Forest* yang telah melalui proses *Hyperparameter Tuning* menunjukkan metrik evaluasi (Accuracy, Precision, Recall, F1-Score) terbaik dalam memprediksi kelas target pada *testing set*.
