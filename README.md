# 📊 A/B Testing Performa Website E-Commerce

Proyek ini bertujuan untuk menganalisis performa sebuah website e-commerce berdasarkan metrik **konversi** dan **perilaku pengguna** (seperti time spent dan page views) menggunakan metode eksperimen **A/B Testing**. Dalam eksperimen ini, terdapat **5.000 data pengguna** yang dibagi menjadi dua grup:

- **Grup A**: tampilan website dengan _background_ putih
- **Grup B**: tampilan website dengan _background_ hitam

Tujuan utama dari eksperimen ini adalah untuk mengetahui apakah perubahan warna latar belakang memiliki pengaruh signifikan terhadap perilaku pengguna dan tingkat konversi.

## 📁 Dataset
Dataset terdiri dari informasi pengguna, termasuk:
- Group (A atau B)
- Device (mobile atau desktop)
- Lokasi geografis (England, Scotland, Wales, Northern Ireland)
- Time Spent (lama waktu pengguna berada di situs)
- Page Views (jumlah halaman yang dilihat)
- Conversion (Apakah pengguna melakukan konversi atau tidak)

## 📌 Metodologi

### 1. Eksplorasi Data
- Melihat distribusi tiap variabel
- Mengetahui proporsi masing-masing grup
- Menganalisis konversi berdasarkan device dan lokasi

### 2. Uji Asumsi Statistik
Dilakukan uji normalitas dan homogenitas sebelum menentukan metode statistik:
- **Time Spent & Page Views** → Tidak normal, homogen → uji non-parametrik
- **Conversion** → Data kategorik → uji proporsi dan chi-square

### 3. Uji Statistik
- **Z-Test & Chi-Square** → untuk konversi
- **Mann-Whitney U Test** → untuk time spent & page views

## 📈 Hasil dan Insight

### 1. **Tingkat Konversi**
- Grup B (background hitam) memiliki tingkat konversi **~14%**
- Grup A (background putih) hanya **~5%**
- Hasil uji statistik menunjukkan perbedaan signifikan:
  - Z-Test: p-value = 3.993e-25
  - Chi-Square: p-value = 6.572e-25
- 🔍 **Insight**: Background gelap berdampak positif pada konversi.

### 2. **Time Spent**
- Tidak ada perbedaan signifikan antara Grup A dan Grup B (p = 0.642)
- Distribusi tidak normal, uji menggunakan Mann-Whitney U Test

### 3. **Page Views**
- Tidak ada perbedaan signifikan antara Grup A dan Grup B (p = 0.4247)

### 4. **Analisis Tambahan (Lokasi & Device)**
- Grup B tetap menunjukkan konversi lebih tinggi di semua kombinasi device dan lokasi.
- Terdapat pola menarik dalam Grup B:
  - **England**: Desktop (15,82%) > Mobile (13,44%)
  - **Northern Ireland**: Mobile (12,01%) > Desktop (10,94%)
  - **Scotland**: Mobile (16,72%) > Desktop (13,64%) → perbedaan terbesar
  - **Wales**: Desktop ≈ Mobile (selisih sangat kecil)

## 🧠 Final Insight

Perubahan warna latar belakang situs dari putih ke hitam terbukti memiliki pengaruh signifikan terhadap peningkatan konversi, meskipun tidak memberikan dampak yang berarti terhadap lama waktu kunjungan atau jumlah halaman yang dibuka. Efek ini juga konsisten di seluruh lokasi dan perangkat pengguna, dengan beberapa variasi perilaku yang menarik untuk ditelusuri lebih lanjut.

## 💡 Rekomendasi Bisnis

- Implementasi tampilan dengan **background hitam** secara penuh dapat dipertimbangkan untuk meningkatkan tingkat konversi.
- Lakukan **eksperimen lanjutan** dengan elemen visual lainnya (warna tombol, layout, dll).
- Pertimbangkan segmentasi berdasarkan **lokasi dan perangkat** untuk personalisasi yang lebih tajam.
- Gunakan pendekatan **data-driven** dalam seluruh pengambilan keputusan desain dan UI/UX.

## ⚙️ Teknologi yang Digunakan

- Python (Pandas, NumPy, SciPy, Matplotlib, Seaborn)
- Google Colab
- Jupyter Notebook

## 📬 Kontak

Untuk pertanyaan lebih lanjut, silakan hubungi melalui GitHub issue atau email: **[email kamu di sini]**
