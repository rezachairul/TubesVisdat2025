# 🌳 Analisis Deforestasi Indonesia

Proyek ini bertujuan untuk menganalisis data deforestasi di Indonesia berdasarkan dataset tahunan per provinsi dan kategori lahan. Analisis dilakukan menggunakan Python dan divisualisasikan melalui berbagai jenis grafik agar dapat memberikan gambaran tren dan distribusi deforestasi nasional dari tahun ke tahun.

## ⚙️ Tools & Library

Proyek ini dikembangkan menggunakan bahasa pemrograman Python dengan library berikut:

- `pandas` — untuk manipulasi dan pembersihan data
- `numpy` — untuk operasi numerik
- `matplotlib.pyplot` — untuk membuat visualisasi dasar
- `seaborn` — untuk membuat visualisasi statistik yang lebih menarik
- `jupyter notebook` — untuk mengembangkan dan mendokumentasikan analisis

## Teknik Preprocessing dengan Agregation

Setelah data dibersihkan, dilakukan agregasi menggunakan teknik:
- `groupby()` pada kolom `Tahun`, `Provinsi`, dan `Kategori`
- Fungsi agregasi utama: `.sum()` untuk mendapatkan total deforestasi atau luasan lahan per kategori
- Hasil agregasi digunakan untuk membuat visualisasi seperti line chart, bar chart, pie chart, dan heatmap

## 🧹 Data Preprocessing

Langkah-langkah pembersihan dan transformasi data:
1. **Gabungkan Header**  
   Dataset memiliki dua baris header (Tahun dan Kategori) yang digabung menjadi format `Tahun - Kategori`.

2. **Ubah ke Long Format**  
   Menggunakan `pandas.melt()` untuk mengubah data menjadi long format dengan kolom:
   - `Provinsi`
   - `Tahun`
   - `Kategori`
   - `Nilai`

3. **Pisahkan Kolom**  
   Kolom gabungan `Tahun - Kategori` dipecah menjadi dua kolom terpisah: `Tahun` dan `Kategori`.

4. **Filter Nilai Valid**  
   Hanya data numerik yang valid yang dipertahankan. Nilai yang mengandung deskripsi diabaikan.

5. **Konversi Tipe Data**  
   Nilai diformat ulang (hapus koma, titik) dan dikonversi ke `float` agar bisa dihitung dan divisualisasikan.

## 📈 Visualisasi

Berikut adalah visualisasi yang dihasilkan dari dataset:

### 1. Tren Total Deforestasi Nasional per Tahun
Visualisasi: **Line Chart**  
Menampilkan jumlah total deforestasi di seluruh Indonesia dari tahun ke tahun.

### 2. Perbandingan Kawasan Hutan vs APL per Tahun
Visualisasi: **Stacked Bar Chart**  
Membandingkan penggunaan lahan antara Kawasan Hutan dan APL (Area Penggunaan Lain) dari tahun ke tahun.

### 3. Deforestasi Terbesar per Provinsi (Akumulatif)
Visualisasi: **Pie Chart**  
Menampilkan 10 provinsi dengan akumulasi deforestasi terbesar sepanjang tahun pengamatan.

### 4. Heatmap Deforestasi per Provinsi dan Tahun
Visualisasi: **Heatmap**  
Menampilkan sebaran intensitas deforestasi berdasarkan provinsi dan tahun. Membantu mengidentifikasi pola spasial dan temporal.

---
