# Social-Media-Stress-Prediction
Prediksi stres pada pengguna media sosial menggunakan Logistic Regression dan Random Forest berdasarkan fitur linguistik dan sosial dengan Python.

**Prediksi Stres pada Pengguna Media Sosial**

Proyek Kecerdasan Artifisial untuk memprediksi stres pada pengguna media sosial berdasarkan fitur linguistik dan sosial menggunakan algoritma Logistic Regression dan Random Forest.

**Deskripsi Proyek**

Media sosial menjadi salah satu sarana bagi pengguna untuk mengekspresikan pikiran, perasaan, dan pengalaman sehari-hari. Melalui proyek ini, dilakukan analisis data dan penerapan machine learning untuk mempelajari pola yang berkaitan dengan stres berdasarkan data unggahan pengguna Reddit.

Beberapa model klasifikasi dibangun dan dibandingkan untuk mengetahui model yang memberikan hasil prediksi terbaik berdasarkan metrik evaluasi yang digunakan.

**Tujuan**
1. Melakukan eksplorasi dan analisis terhadap dataset.
2. Melakukan pembersihan dan persiapan data sebelum pemodelan.
3. Mengidentifikasi fitur yang relevan menggunakan feature importance.
4. Membangun model klasifikasi menggunakan Logistic Regression dan Random Forest.
5. Membandingkan kinerja model berdasarkan hasil evaluasi.

**Dataset**

Dataset yang digunakan adalah Stress Analysis dari Kaggle, yang berisi data unggahan Reddit dengan berbagai fitur linguistik dan sosial.

Informasi dataset:
- Jumlah data: 2.838 baris.
- Jumlah atribut: 111 kolom, termasuk label target.
- Label 0: Tidak stres.
- Label 1: Stres.
Dataset digunakan sebagai data eksperimen untuk membangun model klasifikasi.

**Metodologi**

Tahapan pengerjaan proyek meliputi:
1. Pembersihan Data
Memeriksa dan mempersiapkan data sebelum analisis dan pemodelan.
2. Analisis Data Eksploratif (EDA)
Melakukan statistik deskriptif, pemeriksaan pencilan menggunakan metode IQR, analisis distribusi label, dan pemeriksaan korelasi antarfitur.
3. Seleksi Fitur
Menggunakan feature importance dari Random Forest untuk memilih 50 fitur teratas.
4. Pembangunan Model
Membangun dan membandingkan tiga konfigurasi model:
- Logistic Regression tanpa scaling.
- Logistic Regression dengan RobustScaler.
- Random Forest.
5. Evaluasi Model
Menggunakan accuracy, precision, recall, F1-score, dan confusion matrix untuk mengevaluasi hasil klasifikasi.

**Catatan**

Proyek ini dibuat untuk keperluan akademik dalam penerapan machine learning pada klasifikasi data media sosial. Hasil prediksi model tidak dimaksudkan sebagai diagnosis atau penilaian pasti terhadap kondisi kesehatan mental seseorang.

**Konteks Akademik**

Mata Kuliah: Kecerdasan Artifisial
Universitas: Universitas Negeri Surabaya
