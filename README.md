# 🧠 Sentiment Analysis dengan Naive Bayes & SVM

Proyek ini bertujuan untuk melakukan analisis sentimen terhadap data teks menggunakan dua algoritma pembelajaran mesin: **Multinomial Naive Bayes (MNB)** dan **Support Vector Machine (SVM)**. Analisis ini berguna untuk mengklasifikasikan opini pengguna (positif, negatif, atau netral) berdasarkan teks ulasan atau komentar yang mereka berikan.

---

## 🎯 Tujuan Proyek

- Mengklasifikasikan sentimen dari data teks (ulasan, komentar, opini).
- Membandingkan performa model Multinomial Naive Bayes dan SVM.
- Menyajikan hasil akurasi dan evaluasi dari kedua model.

---

## 🛠️ Teknologi dan Library

- Python 3.x
- Scikit-learn (`sklearn`)
- Pandas
- Numpy
- Matplotlib / Seaborn (visualisasi opsional)
- Jupyter Notebook (jika digunakan)

---

## 🔄 Alur Proyek

1. **Preprocessing Data Teks**
   - Lowercasing
   - Tokenisasi
   - Stopword removal
   - Stemming (opsional)
   - Vectorization dengan `CountVectorizer` atau `TfidfVectorizer`

2. **Training Model**
   - Multinomial Naive Bayes
   - Support Vector Machine (SVM)

3. **Evaluasi Model**
   - Akurasi
   - Precision, Recall, F1-Score
   - Confusion Matrix

4. **Prediksi**
   - Uji model terhadap data baru

---
## 📊 Hasil Evaluasi Model

Dua model machine learning digunakan untuk melakukan klasifikasi sentimen:

- **Multinomial Naive Bayes (MNB)**
- **Support Vector Machine (SVM)**

Keduanya diuji menggunakan data TF-IDF dengan split 80% data latih dan 20% data uji.

### 🔍 Akurasi Prediksi

| Model                     | Akurasi  |
|---------------------------|----------|
| Multinomial Naive Bayes   | 82.58%   |
| Support Vector Machine    | 80.43%   |

---

### 🧾 Laporan Klasifikasi 

#### 📌 Multinomial Naive Bayes (MNB)

| Label | Precision | Recall | F1-score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.93      | 0.86   | 0.89     | 2962    |
| 1     | 0.45      | 0.64   | 0.53     | 534     |

- **Accuracy**: 82.58%  
- **Macro Avg**: Precision 0.69, Recall 0.75, F1-score 0.71  
- **Weighted Avg**: Precision 0.86, Recall 0.83, F1-score 0.84

---

#### 📌 Support Vector Machine (SVM)

| Label | Precision | Recall | F1-score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.94      | 0.82   | 0.88     | 2962    |
| 1     | 0.42      | 0.73   | 0.53     | 534     |

- **Accuracy**: 80.43%  
- **Macro Avg**: Precision 0.68, Recall 0.77, F1-score 0.70  
- **Weighted Avg**: Precision 0.86, Recall 0.80, F1-score 0.82

---

### 📌 Insight:

- **Naive Bayes** sedikit lebih unggul dalam akurasi keseluruhan.
- **SVM** memiliki recall tinggi pada kelas minoritas (positif), tetapi precision-nya lebih rendah.
- Dataset menunjukkan ketidakseimbangan kelas (imbalanced), sehingga model cenderung bias terhadap label mayoritas (kelas 0).

📎 *Rekomendasi*:  
Untuk peningkatan performa pada kelas minoritas (positif), dapat diterapkan:
- Teknik **oversampling** seperti SMOTE
- Penyesuaian parameter `class_weight` di SVM
- Pembersihan atau augmentasi data teks
