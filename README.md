# Analisis Sentimen Ulasan Pengguna Aplikasi MyTelkomsel Menggunakan Naïve Bayes

## 📖 Deskripsi

Proyek ini bertujuan untuk menganalisis sentimen ulasan pengguna aplikasi **MyTelkomsel** yang diperoleh dari **Google Play Store**. Analisis dilakukan menggunakan algoritma **Naïve Bayes** untuk mengklasifikasikan ulasan ke dalam kategori **positif** dan **negatif**.

Penelitian ini menerapkan tahapan text mining mulai dari pengumpulan data, preprocessing teks, pelabelan sentimen, pembentukan model klasifikasi, hingga evaluasi performa model menggunakan metrik klasifikasi.

## 🎯 Tujuan Penelitian

* Mengidentifikasi sentimen pengguna terhadap aplikasi MyTelkomsel.
* Mengklasifikasikan ulasan pengguna ke dalam sentimen positif dan negatif.
* Mengukur performa algoritma Naïve Bayes dalam tugas klasifikasi sentimen.
* Memberikan gambaran tingkat kepuasan pengguna berdasarkan ulasan yang diberikan.

## 🗂 Dataset

Dataset berasal dari ulasan pengguna aplikasi **MyTelkomsel** yang diambil dari Google Play Store.

Karakteristik dataset:

* Sumber: Google Play Store
* Objek: Aplikasi MyTelkomsel
* Bahasa: Indonesia
* Jenis Data: Ulasan pengguna
* Kategori Sentimen: Positif dan Negatif

## 🔄 Tahapan Penelitian

### 1. Pengumpulan Data

Mengumpulkan ulasan pengguna aplikasi MyTelkomsel dari Google Play Store.

### 2. Preprocessing Data

Tahapan pembersihan dan normalisasi teks meliputi:

* Case Folding
* Cleaning Text
* Tokenizing
* Stopword Removal
* Stemming

### 3. Pelabelan Sentimen

Memberikan label sentimen pada setiap ulasan sebagai:

* Positif
* Negatif

### 4. Pembagian Dataset

Dataset dibagi menjadi data pelatihan (*training set*) dan data pengujian (*testing set*).

### 5. Klasifikasi Naïve Bayes

Membangun model klasifikasi menggunakan algoritma Naïve Bayes.

### 6. Evaluasi Model

Evaluasi dilakukan menggunakan:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

## 🛠 Teknologi yang Digunakan

* Python
* Google Colab / Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Sastrawi
* Matplotlib
* Seaborn

## 📁 Struktur Repository

```text
.
├── dataset/
│   ├── raw_data.csv
│   └── processed_data.csv
│
├── notebook/
│   └── project_sentiment_analysis_MyTelkomsel.ipynb
│
├── results/
│   ├── confusion_matrix.png
│   └── evaluation_metrics.png
│
├── requirements.txt
└── README.md
```

## 📊 Hasil Evaluasi Model

Proyek ini menggunakan algoritma klasifikasi **Multinomial Naive Bayes** dengan pembagian data *training* sebesar 80% dan data *testing* sebesar 20%.

Berdasarkan pengujian terhadap 371 data uji, model menghasilkan **Akurasi sebesar 92.45%**. 

Berikut adalah rincian metrik evaluasi model (Classification Report):

| Kelas | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| **Negatif** | 0.92 | 1.00 | 0.96 | 343 |
| **Positif** | 0.00 | 0.00 | 0.00 | 28 |
| | | | | |
| **Accuracy** | | | **0.92** | 371 |
| **Macro Avg** | 0.46 | 0.50 | 0.48 | 371 |
| **Weighted Avg** | 0.85 | 0.92 | 0.89 | 371 |

**Confusion Matrix:**
* **True Negative (TN):** 343
* **False Positive (FP):** 0
* **False Negative (FN):** 28
* **True Positive (TP):** 0

### 💡 Kesimpulan & Insight
<div align="justify">
  <ul>
    <li><strong>Performa pada Kelas Dominan:</strong> Model sangat luar biasa dalam mendeteksi dan mengklasifikasikan ulasan bersentimen <strong>Negatif</strong> (Recall 100% dan Precision 92%). Hal ini menunjukkan bahwa sistem sangat sensitif terhadap keluhan atau masalah teknis pengguna pada aplikasi MyTelkomsel.</li>
    <li><strong>Tantangan Ketidakseimbangan Data (Class Imbalance):</strong> Model gagal memprediksi sentimen <strong>Positif</strong> (nilai Precision dan Recall 0.00). Kendala ini sangat wajar terjadi karena data hasil <em>scraping</em> didominasi oleh ulasan bintang 1 (Negatif), yang terbukti dari total data uji di mana 343 data adalah negatif dan hanya 28 data yang positif.</li>
    <li><strong>Pengembangan Selanjutnya:</strong> Untuk proyek mendatang, disarankan menggunakan teknik <em>resampling</em> seperti <em>Oversampling</em> (misal: SMOTE) atau <em>Undersampling</em> untuk menyeimbangkan jumlah kelas Positif dan Negatif sebelum model dilatih, sehingga model dapat mengenali kedua sentimen dengan sama baiknya.</li>
  </ul>
</div>

## 🚀 Cara Menjalankan Proyek

### Clone Repository

```bash
git clone https://github.com/Ahmds20/Analisis-sentimen-aplikasi-My-Telkomsel.git
```

### Masuk ke Folder Proyek

```bash
cd Analisis-Sentimen-Aplikasi-MyTelkomsel
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Jalankan Notebook

```bash
jupyter notebook
```

Kemudian buka file:

```text
project_sentiment_analysis_MyTelkomsel.ipynb
```

## 👨‍🎓 Penulis

**Ahmad Jazil Faiz**

Program Studi Informatika

## 📄 Lisensi

Proyek ini dibuat untuk keperluan penelitian akademik, pembelajaran, dan pengembangan ilmu pengetahuan.
