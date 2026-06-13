# Klasifikasi Citra Garpu, Sandal, dan Speaker Menggunakan Pengolahan Citra Digital

Proyek ini merupakan implementasi **pengolahan citra digital** dan **machine learning** untuk melakukan klasifikasi gambar objek ke dalam beberapa kelas, yaitu **Garpu**, **Sandal**, dan **Speaker**. Proyek ini dibuat dalam bentuk notebook Python/Jupyter dengan proses ekstraksi fitur citra, pembuatan dataset fitur, pelatihan model klasifikasi, prediksi, evaluasi akurasi, serta visualisasi confusion matrix.

Proyek ini cocok digunakan sebagai bahan pembelajaran untuk memahami bagaimana citra digital dapat diubah menjadi data numerik, lalu digunakan sebagai input model machine learning untuk klasifikasi objek sederhana.

---

## Identitas Proyek

**Mata Kuliah:** Pengolahan Citra Digital  
**Jenis Proyek:** Klasifikasi Gambar / Image Classification  
**Metode Utama:** Ekstraksi fitur citra + Machine Learning  
**Notebook:** `code.ipynb`

**Kelompok 3:**

- Jeni Kasturi
- Aidil Farhan Rares
- Muhammad Zacky Desh Putra

---

## Tujuan Proyek

Tujuan utama dari proyek ini adalah membangun pipeline sederhana untuk mengolah citra digital dan melakukan klasifikasi objek berdasarkan fitur numerik yang diekstrak dari gambar.

Secara umum, proyek ini memiliki tujuan sebagai berikut:

1. Membaca dataset gambar dari beberapa kategori objek.
2. Mengubah gambar berwarna menjadi citra grayscale.
3. Mengekstrak fitur statistik dari citra.
4. Menyimpan hasil ekstraksi fitur ke dalam file Excel.
5. Menggabungkan data fitur dengan label kelas.
6. Melatih model machine learning untuk klasifikasi.
7. Melakukan prediksi terhadap data testing.
8. Mengevaluasi performa model menggunakan akurasi dan confusion matrix.

---

## Dataset

Dataset yang digunakan terdiri dari gambar objek dengan beberapa kelas:

| Kelas | Jumlah Data |
|---|---:|
| Garpu | 50 gambar |
| Sandal | 50 gambar |
| Speaker | 50 gambar |

Total data pada file label gabungan adalah sekitar **150 data gambar**.

File dataset fitur yang digunakan dalam proyek:

```text
Fitur Garpu.xlsx
Fitur Sandal.xlsx
Fitur Speaker.xlsx
LABEL.xlsx
```

---

## Fitur yang Diekstrak

Setiap gambar diproses menjadi citra grayscale, kemudian dihitung beberapa fitur statistik berikut:

| Fitur | Keterangan |
|---|---|
| `rata` | Nilai rata-rata intensitas piksel gambar |
| `standar` | Standar deviasi intensitas piksel |
| `varian` | Variansi intensitas piksel |
| `skewness` | Tingkat kemencengan distribusi nilai piksel |
| `label` | Kelas objek gambar |

Fitur-fitur ini digunakan sebagai input untuk model klasifikasi.

---

## Teknologi yang Digunakan

Proyek ini dibuat menggunakan beberapa library Python berikut:

- Python
- Google Colab / Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- OpenCV
- Pillow
- SciPy
- Scikit-learn
- TensorFlow / Keras
- TQDM

---

## Alur Kerja Proyek

Alur kerja utama pada notebook adalah sebagai berikut:

```text
Dataset Gambar
      ↓
Membaca gambar menggunakan OpenCV
      ↓
Konversi RGB ke Grayscale
      ↓
Ekstraksi fitur statistik citra
      ↓
Menyimpan fitur ke Excel
      ↓
Membaca dataset gabungan berlabel
      ↓
Split data training dan testing
      ↓
Training model klasifikasi
      ↓
Prediksi data testing
      ↓
Evaluasi akurasi dan confusion matrix
```

---

## Model yang Digunakan

Notebook ini menyiapkan beberapa library model machine learning dan deep learning, seperti:

- Bernoulli Naive Bayes
- Gaussian Naive Bayes
- Categorical Naive Bayes
- Multinomial Naive Bayes
- Complement Naive Bayes
- Logistic Regression
- Random Forest
- K-Nearest Neighbors
- Neural Network / CNN

Pada implementasi utama di notebook, model yang dijalankan untuk klasifikasi adalah:

```text
Bernoulli Naive Bayes
```

Model dilatih menggunakan data training, kemudian diuji menggunakan data testing untuk melihat hasil prediksi dan performa klasifikasi.

---

## Evaluasi Model

Evaluasi model dilakukan menggunakan:

- Akurasi model
- Hasil prediksi data testing
- Confusion matrix
- Visualisasi heatmap confusion matrix

Pada hasil notebook, model menghasilkan akurasi sekitar:

```text
0.60 atau 60%
```

Nilai akurasi dapat berubah apabila dataset, pembagian data training-testing, preprocessing, atau model yang digunakan diperbarui.

---

## Struktur File

Struktur file yang disarankan untuk repository GitHub:

```text
Klasifikasi-Citra-Garpu-Sandal-Speaker/
│
├── code.ipynb
├── Fitur Garpu.xlsx
├── Fitur Sandal.xlsx
├── Fitur Speaker.xlsx
├── LABEL.xlsx
├── README.md
└── outputs/
    ├── data_xtes.xlsx
    ├── data_ytes.xlsx
    └── hasil_prediksi.xlsx
```

Keterangan:

| File | Keterangan |
|---|---|
| `code.ipynb` | Notebook utama untuk proses pengolahan citra dan klasifikasi |
| `Fitur Garpu.xlsx` | Hasil ekstraksi fitur dari gambar garpu |
| `Fitur Sandal.xlsx` | Hasil ekstraksi fitur dari gambar sandal |
| `Fitur Speaker.xlsx` | Hasil ekstraksi fitur dari gambar speaker |
| `LABEL.xlsx` | Dataset gabungan berisi fitur dan label kelas |
| `data_xtes.xlsx` | Data fitur testing yang diekspor dari notebook |
| `data_ytes.xlsx` | Label asli data testing |
| `hasil_prediksi.xlsx` | Hasil prediksi model |

---

## Cara Menjalankan Proyek

### 1. Clone repository

```bash
git clone https://github.com/username/Klasifikasi-Citra-Garpu-Sandal-Speaker.git
cd Klasifikasi-Citra-Garpu-Sandal-Speaker
```

### 2. Install library yang dibutuhkan

```bash
pip install numpy pandas matplotlib seaborn opencv-python pillow scipy scikit-learn tensorflow tqdm openpyxl
```

### 3. Buka notebook

Buka file berikut menggunakan Jupyter Notebook, JupyterLab, VS Code, atau Google Colab:

```text
code.ipynb
```

### 4. Sesuaikan path dataset

Jika menjalankan di Google Colab, pastikan path Google Drive pada notebook sudah sesuai dengan lokasi dataset gambar.

Contoh path pada notebook:

```text
/content/drive/MyDrive/DatasetKelompok3/
```

Jika menjalankan secara lokal, ubah path dataset sesuai lokasi folder di komputer.

### 5. Jalankan semua cell

Jalankan notebook dari awal sampai akhir untuk melakukan:

- Import library
- Membaca dataset gambar
- Ekstraksi fitur citra
- Membuat file Excel fitur
- Membaca dataset berlabel
- Training model
- Prediksi
- Evaluasi model
- Menyimpan hasil prediksi

---

## Hasil Output

Output utama dari proyek ini adalah:

1. File fitur citra dalam format Excel.
2. Hasil prediksi model klasifikasi.
3. Nilai akurasi model.
4. Confusion matrix.
5. Visualisasi heatmap confusion matrix.

---

## Manfaat Proyek

Proyek ini bermanfaat untuk:

- Memahami dasar pengolahan citra digital.
- Mempelajari cara mengubah gambar menjadi fitur numerik.
- Menerapkan machine learning untuk klasifikasi gambar sederhana.
- Melatih pemahaman preprocessing, training, testing, dan evaluasi model.
- Menjadi contoh portfolio dasar di bidang Computer Vision dan Machine Learning.

---

## Pengembangan Selanjutnya

Beberapa pengembangan yang dapat dilakukan pada proyek ini:

- Menambahkan jumlah dataset agar model lebih akurat.
- Menggunakan data augmentation untuk memperkaya variasi gambar.
- Menerapkan model CNN secara penuh untuk klasifikasi berbasis gambar langsung.
- Membandingkan beberapa algoritma seperti Logistic Regression, Random Forest, KNN, dan Naive Bayes.
- Menambahkan classification report berupa precision, recall, dan F1-score.
- Membuat aplikasi sederhana berbasis web untuk upload gambar dan prediksi kelas objek.

---

## Kesimpulan

Proyek ini menunjukkan bahwa gambar dapat diproses menjadi data numerik melalui ekstraksi fitur statistik, kemudian digunakan untuk membangun model klasifikasi objek. Dengan menggunakan fitur seperti rata-rata, standar deviasi, varian, dan skewness, model machine learning dapat mempelajari pola dari setiap kelas gambar dan menghasilkan prediksi terhadap data testing.

Meskipun akurasi awal masih dapat ditingkatkan, proyek ini sudah mencakup pipeline dasar pengolahan citra digital dan machine learning, mulai dari preprocessing citra, ekstraksi fitur, training model, prediksi, hingga evaluasi hasil.

---

## Author

**Aidil Farhan Rares**

