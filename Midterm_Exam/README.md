# Midterm Exam - Jaringan Syaraf Tiruan

Direktori ini berisi pengerjaan Ujian Tengah Periode (UTP) mata kuliah Jaringan Syaraf Tiruan (JST). Terdapat dua ujian yang mencakup implementasi berbagai arsitektur jaringan saraf tiruan untuk studi kasus yang berbeda.

## Daftar Ujian

### UTP 1 - Multilayer Perceptron (MLP) tanpa Backpropagation

**Studi Kasus:** Klasifikasi kondisi tangki reaktor menggunakan sensor suhu dan tekanan (masalah XOR-like)

**Arsitektur:**
- 2 input (suhu, tekanan) → hidden layer (sigmoid) → 1 output (linear)
- Bobot input→hidden dibekukan (random initialization, tidak dilatih)
- Hanya bobot hidden→output yang dilatih menggunakan aturan delta (Widrow-Hoff)

**Fitur Utama:**
- Implementasi manual tanpa library jaringan saraf (Keras, PyTorch, sklearn)
- Pra-pemrosesan dengan standarisasi z-score
- Grid search untuk hyperparameter tuning (hidden_size, learning_rate, max_epoch)
- Analisis pengaruh standarisasi, learning rate, dan threshold
- Evaluasi dengan train/validation/test split (64%/16%/20%)

**Hasil Utama:**
- Konfigurasi terbaik: hidden_size=32, learning_rate=0.01, max_epoch=200
- Akurasi train: 94.79%, validasi: 96.1%, test: 95.83%
- Analisis mengapa hidden layer diperlukan untuk masalah non-linear (XOR)
- Pembahasan batas stabilitas learning rate berdasarkan norma vektor input

**File:** `UTP1_MLP_245150207111073_RUSDIANSYAH ALIEF PRASETYA.ipynb`

---

### UTP 2 - MADALINE (MRI) untuk Klasifikasi Citra Digit

**Studi Kasus:** Klasifikasi digit tulisan tangan 8x8 piksel menjadi dua kelompok
- Kelompok A (+1): digit berlengkung (2, 3, 5, 8)
- Kelompok B (-1): digit bergaris lurus (1, 4, 7, 9)

**Arsitektur:**
- Banyak ADALINE (hidden layer) → unit OR (output layer)
- Aturan pelatihan MRI (Many ADALINE) untuk update bobot
- Binarisasi piksel dengan threshold yang dapat disesuaikan

**Fitur Utama:**
- Implementasi manual MADALINE dengan aturan MRI
- Binarisasi citra dengan threshold variabel (0, 4, 8, 12)
- Output layer OR dengan bobot tetap (v=0.5, b_out dinamis)
- Evaluasi pada data bersih dan data noisy (salt-and-pepper 10%)
- Visualisasi bobot hidden layer dan analisis per digit

**Hasil Utama:**
- Konfigurasi terbaik: threshold=8, n_hidden=8
- Akurasi train: 100%, validasi: 92.08%, test bersih: 90.05%, test noisy: 82.41%
- Analisis perbandingan aturan MRI vs implementasi sebelumnya
- Interpretasi bobot hidden: setiap unit berspesialisasi pada digit tertentu
- Analisis robustness terhadap derau dan perbaikan yang mungkin

**File:** `UTP2_MADALINE_245150207111073_RUSDIANSYAH ALIEF PRASETYA.ipynb`

---

## Penilaian

Kedua UTP dinilai berdasarkan:
- Implementasi kode (fungsi-fungsi yang diminta)
- Eksperimen dan grid search
- Analisis mendalam dengan merujuk pada hasil output notebook
- Pemahaman konsep teoritis (standarisasi, learning rate, arsitektur, dll)

## Author

**Rusdiansyah Alief Prasetya**  
NIM: 245150207111073  
Mata Kuliah: Jaringan Syaraf Tiruan (JST)
