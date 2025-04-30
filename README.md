# 🌳 Analisis Deforestasi di Indonesia (Data Aggregation & Visualization)

Project ini berfokus pada pembersihan dan analisis data deforestasi di Indonesia berdasarkan dataset multi-level (tahun dan kategori), dengan teknik **data aggregation** dan visualisasi interaktif menggunakan `pandas`, `matplotlib`, dan `seaborn`.

## 📁 Struktur Dataset

Dataset mentah berupa file CSV dengan struktur multi-header pada baris pertama dan kedua. Proses cleaning dilakukan agar data siap dianalisis.

Kolom hasil cleaning:

- `Provinsi`: Nama provinsi
- `Tahun`: Tahun pengamatan
- `Kategori`: Jenis data (misalnya "Deforestasi Kawasan Hutan", "APL", dll.)
- `Nilai`: Nilai numerik (dalam hektar)

---

## 🧼 Data Cleaning

Data dibersihkan dengan langkah-langkah berikut:

1. Gabungkan dua baris header menjadi satu nama kolom (format: `Tahun - Kategori`)
2. Ubah dari format wide ke long menggunakan `melt()`
3. Pisahkan kolom gabungan menjadi `Tahun` dan `Kategori`
4. Filter hanya nilai numerik
5. Hapus koma dan ubah ke float

File hasil cleaning disimpan sebagai: `dataset/datasetTubes_cleaned.csv`

---

## 📊 Analisis & Visualisasi

Berikut beberapa hasil visualisasi yang dibuat:

### 1. Tren Total Deforestasi Nasional per Tahun
Menampilkan perubahan total deforestasi nasional dari waktu ke waktu (Line Chart).

### 2. Perbandingan Kawasan Hutan vs APL per Tahun
Menunjukkan bagaimana proporsi antara kawasan hutan dan area penggunaan lain (APL) tiap tahun (Stacked Bar Chart).

### 3. Deforestasi Terbesar per Provinsi (Akumulatif)
Visualisasi provinsi-provinsi dengan total deforestasi tertinggi (Pie Chart).

### 4. Heatmap Deforestasi per Provinsi dan Tahun
Visualisasi intensitas deforestasi berdasarkan wilayah dan tahun (Heatmap).

---

## 🛠️ Tools & Library

- Python 3
- pandas
- matplotlib
- seaborn
- jupyter notebook / VS Code

---

## 🚀 Menjalankan Proyek

1. Clone repositori:
   ```bash
   git clone https://github.com/username/nama-repo.git
   cd nama-repo
    ```
