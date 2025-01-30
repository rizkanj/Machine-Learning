# Machine Learning - Breast Cancer Classification

## Deskripsi Proyek
Proyek ini bertujuan untuk membangun model Machine Learning yang dapat mengklasifikasikan diagnosis kanker payudara berdasarkan dataset Wisconsin Breast Cancer Dataset. Model yang digunakan dalam proyek ini meliputi **Random Forest, Decision Tree, dan K-Nearest Neighbors (KNN), dengan optimasi hyperparameter dan evaluasi model.

## Dataset
Dataset yang digunakan adalah wdbc.data dari Wisconsin Diagnostic Breast Cancer (WDBC), yang berisi fitur dari sel kanker dan label diagnosis. Fitur mencakup berbagai metrik seperti **radius, tekstur, perimeter, area, smoothness, compactness, concavity, dan lainnya.

## Instalasi
Pastikan Anda memiliki Python 3.x dan pustaka berikut terinstal:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn joblib
```

## Struktur Kode
1. Import Library - Memuat pustaka yang diperlukan.
2. Load Dataset - Membaca dataset dan memberi nama pada kolom.
3. Preprocessing Data
   - Menghapus kolom ID.
   - Mengecek nilai yang hilang.
   - Mengubah label diagnosis menjadi numerik menggunakan LabelEncoder.
4. Eksplorasi Data
   - Menampilkan statistik dataset.
   - Memvisualisasikan distribusi diagnosis.
   - Analisis korelasi antar fitur dengan heatmap.
5. Feature Selection
   - Mengidentifikasi fitur dengan korelasi tinggi terhadap target.
6. Training dan Evaluasi Model
   - Random Forest, Decision Tree, KNN
   - Evaluasi dengan Confusion Matrix, Accuracy, Precision-Recall Curve, dan Classification Report.
7. Hyperparameter Tuning
   - Menggunakan GridSearchCV untuk optimasi parameter terbaik pada setiap model.
8. Cross Validation & Feature Importance
   - Menggunakan cross\_val\_score untuk validasi kinerja model.
   - Menampilkan 10 fitur paling penting untuk model Random Forest.
9. ROC Curve & Precision-Recall Curve
   - Membandingkan performa model dengan AUC-ROC Curve dan Precision-Recall Curve.
10. Simpan Model Terbaik
    - Model terbaik dari setiap algoritma disimpan menggunakan joblib.

## Cara Menjalankan
1. Jalankan semua cell kode dalam urutan yang benar.
2. Dataset akan diproses dan model akan dilatih.
3. Hasil evaluasi model akan ditampilkan, termasuk accurasy, confusion matrix, dan grafik evaluasi.
4. Model terbaik akan disimpan dalam file .pkl.

## Hasil Evaluasi
- Random Forest memberikan hasil terbaik dengan akurasi yang lebih tinggi dibandingkan model lainnya.
- Decision Tree memiliki performa yang cukup baik tetapi lebih rentan terhadap overfitting.
- KNN menunjukkan performa yang lebih bervariasi tergantung pada parameter jumlah tetangga (k).
- Feature Importance menunjukkan fitur yang paling berpengaruh dalam prediksi diagnosis.

## Kesimpulan
Model Random Forest menjadi pilihan terbaik berdasarkan akurasi dan kestabilan. Evaluasi model dilakukan dengan Confusion Matrix, ROC Curve, dan Precision-Recall Curve untuk memahami performa lebih lanjut.
