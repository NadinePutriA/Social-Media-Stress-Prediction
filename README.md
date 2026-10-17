# Social-Media-Stress-Prediction
Prediksi stres pada pengguna media sosial menggunakan Logistic Regression dan Random Forest berdasarkan fitur linguistik dan sosial dengan Python.


# Prediksi Stres pada Pengguna Media Sosial

## Deskripsi Proyek

Proyek ini membahas penerapan Artificial Intelligence (AI) menggunakan algoritma machine learning untuk memprediksi tingkat stres pengguna media sosial berdasarkan fitur linguistik dan sosial. Proyek ini disusun sebagai tugas akhir mata kuliah Artificial Intelligence pada Program Studi S1 Sains Data, Universitas Negeri Surabaya.

Penelitian menggunakan dataset *Stress Analysis* dari Kaggle yang berisi fitur numerik hasil ekstraksi karakteristik bahasa dan aktivitas sosial pengguna Reddit. Model yang digunakan adalah Logistic Regression dan Random Forest untuk mengklasifikasikan pengguna ke dalam dua kategori, yaitu stres dan tidak stres.

Selain membandingkan performa model, penelitian ini juga menganalisis fitur yang berkontribusi terhadap prediksi menggunakan feature importance.

## Tujuan

- Menganalisis hubungan fitur linguistik dengan label tingkat stres.
- Mengidentifikasi kontribusi fitur sosial dalam prediksi tingkat stres.
- Membandingkan performa Logistic Regression dengan dan tanpa Robust Scaler serta Random Forest.
- Mengidentifikasi fitur yang paling berpengaruh berdasarkan feature importance.

## Dataset

Dataset yang digunakan adalah **Stress Analysis Dataset** dari Kaggle, yang disusun oleh Shuvojit Das dan berasal dari unggahan pengguna Reddit.

Dataset memiliki sekitar 2.838 entri dengan label target:
- `0`: Tidak stres
- `1`: Stres

Fitur dikelompokkan menjadi:

- **Fitur linguistik:** karakteristik emosional, kognitif, dan struktur bahasa, seperti `tone`, `negemo`, `iword`, dan `anxiety`.
- **Fitur sosial:** karakteristik interaksi pengguna di media sosial, termasuk karma, komentar, dan rasio upvote.

Penelitian menggunakan fitur numerik yang telah tersedia pada dataset, bukan melakukan ekstraksi fitur langsung dari teks mentah.

## Metodologi

### 1. Data Cleaning
- Memeriksa missing values dan data duplikat.
- Menghapus kolom identitas dan atribut yang tidak relevan.
- Menyesuaikan nama kolom untuk mempermudah analisis.

### 2. Exploratory Data Analysis (EDA)
- Statistik deskriptif fitur numerik.
- Analisis distribusi label stres dan tidak stres.
- Deteksi outlier menggunakan metode Interquartile Range (IQR).
- Analisis korelasi fitur terhadap label.

### 3. Feature Selection
Random Forest digunakan untuk menghitung feature importance dan memilih 50 fitur teratas sebagai input pemodelan.

### 4. Preprocessing dan Pemodelan
Data dibagi menjadi data latih dan data uji menggunakan rasio 80:20 dengan stratifikasi label.

Tiga pendekatan yang dibandingkan:
1. Logistic Regression tanpa scaling.
2. Logistic Regression dengan Robust Scaler.
3. Random Forest Classifier.

Robust Scaler digunakan untuk mengevaluasi pengaruh penskalaan fitur terhadap performa Logistic Regression.

### 5. Evaluasi Model
Performa model dievaluasi menggunakan:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

Hasil evaluasi digunakan untuk membandingkan kemampuan setiap model dalam mengklasifikasikan pengguna stres dan tidak stres.

## Hasil dan Evaluasi

Berdasarkan hasil pengujian, diperoleh perbandingan performa berikut:

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression (Unscaled) | 77,1% | 77,3% | 77,1% | 77,1% |
| Logistic Regression (Robust Scaled) | 77,1% | 77,4% | 77,1% | 77,1% |
| Random Forest | 77,8% | 77,8% | 77,8% | 77,8% |

Random Forest memperoleh performa terbaik berdasarkan metrik evaluasi yang digunakan, dengan accuracy sebesar **77,8%**. Model ini juga menghasilkan nilai precision, recall, dan F1-score sebesar 77,8%.

Hasil feature importance menunjukkan bahwa fitur seperti `tone`, `negemo`, `iword`, dan `clout` termasuk fitur yang memiliki kontribusi tinggi dalam prediksi. Temuan ini menunjukkan bahwa karakteristik emosional, pilihan kata, dan aspek sosial dapat memberikan informasi dalam proses klasifikasi.

## Konteks Akademik

Program Studi S1 Sains Data  
Universitas Negeri Surabaya

Mata Kuliah: Artificial Intelligence

## Catatan

Proyek ini merupakan analisis akademik berbasis dataset dan model machine learning. Hasil prediksi tidak dimaksudkan sebagai diagnosis atau pengganti evaluasi profesional terkait kesehatan mental.
