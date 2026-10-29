# Artificial Neuron Network - Running Model Neuron

Repository ini berisi seluruh pengerjaan mata kuliah Jaringan Syaraf Tiruan (JST) - Artificial Neuron Network. Terdapat berbagai implementasi model neuron dan algoritma pembelajaran yang dikerjakan selama semester.

## Struktur Repository

- **POST_6_Rusdiansyah_Alief_Prasetya_245150207111073.ipynb** - Post Test Bab 6: Self-Organizing Maps (SOM)
- **SOM/** - Direktori untuk laporan praktikum SOM (akan diisi dengan notebook Colab untuk laprak)
- **Midterm_Exam/** - Direktori berisi pengerjaan Ujian Tengah Periode (UTP 1 & 2)

## Post Test Bab 6 - Self-Organizing Maps

Post test ini berfokus pada implementasi algoritma **Self-Organizing Maps (SOM)** untuk klasterisasi data pengunjung perpustakaan. SOM adalah algoritma unsupervised learning yang digunakan untuk pemetaan topologi dan klasterisasi.

### Detail Post Test:
- **Dataset**: Pola_Kunjungan_Perpustakaan.csv (90 data pengunjung)
- **Fitur**: Kunjungan_per_Bulan dan Rata_Durasi_Menit
- **Parameter**: learning rate = 0.5, b = 0.5, max_epoch = 6
- **Jumlah Klaster**: 3 klaster (optimal berdasarkan silhouette score)

### Hasil:
- Silhouette Score tertinggi: 0.6859 (untuk 3 klaster)
- Klaster 1: Pengunjung jarang berkunjung (~5.25x/bulan) tapi durasi lama (~185 menit)
- Klaster 2: Pengunjung sangat aktif (~14.53x/bulan) dengan durasi sedang (~63 menit)
- Klaster 3: Pengunjung jarang berkunjung (~3x/bulan) dengan durasi singkat (~40 menit)

## Midterm Exam

Direktori `Midterm_Exam/` berisi pengerjaan Ujian Tengah Periode (UTP) yang mencakup implementasi berbagai arsitektur jaringan saraf tiruan:

### UTP 1 - Multilayer Perceptron (MLP)
- **Studi Kasus:** Klasifikasi kondisi tangki reaktor (masalah XOR-like dengan sensor suhu & tekanan)
- **Arsitektur:** 2 input → hidden layer (sigmoid, dibekukan) → 1 output (linear, dilatih dengan aturan delta)
- **Hasil:** Akurasi test 95.83% dengan hidden_size=32, learning_rate=0.01
- **Analisis:** Pengaruh standarisasi, learning rate stability, dan peran hidden layer untuk masalah non-linear

### UTP 2 - MADALINE (MRI)
- **Studi Kasus:** Klasifikasi digit tulisan tangan 8x8 piksel (digit berlengkung vs bergaris lurus)
- **Arsitektur:** Banyak ADALINE → unit OR dengan aturan MRI
- **Hasil:** Akurasi test bersih 90.05%, test noisy 82.41% dengan threshold=8, n_hidden=8
- **Analisis:** Interpretasi bobot hidden, robustness terhadap derau, dan perbandingan aturan MRI vs implementasi sebelumnya

Lihat detail lengkap di [README Midterm_Exam](Midterm_Exam/README.md).

## Author

**Rusdiansyah Alief Prasetya**  
NIM: 245150207111073  
Mata Kuliah: Jaringan Syaraf Tiruan (JST)
