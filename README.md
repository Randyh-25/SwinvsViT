# Perbandingan Vision Transformer (ViT) vs. Swin Transformer untuk Klasifikasi Jenis Kulit

Repositori ini berisi notebook Jupyter yang melakukan analisis perbandingan antara arsitektur Vision Transformer (ViT) dan Swin Transformer pada dataset "Oily, Dry and Normal Skin Types" dari Kaggle.

## Abstrak

Eksperimen ini bertujuan untuk membandingkan kinerja dua model Vision Transformer yang populer untuk tugas klasifikasi gambar. Prosesnya mencakup:
- Pra-pemrosesan data dan augmentasi.
- Pelatihan model ViT dan Swin Transformer.
- Evaluasi menggunakan metrik akurasi, F1-score, presisi, dan recall.
- Pembuatan confusion matrix untuk analisis kesalahan.
- Pengukuran kecepatan inferensi untuk membandingkan efisiensi.
- Visualisasi kurva pembelajaran dan contoh prediksi.

## Dataset

Dataset yang digunakan adalah **[Oily, Dry and Normal Skin Types Dataset](https://www.kaggle.com/datasets/shakyadissanayake/oily-dry-and-normal-skin-types-dataset)** dari Kaggle. Dataset ini berisi gambar-gambar wajah yang diklasifikasikan ke dalam tiga kategori: kulit berminyak (oily), kering (dry), dan normal.

## Model yang Digunakan

1.  **Vision Transformer (ViT)**: `vit_base_patch16_224`
2.  **Swin Transformer**: `swin_tiny_patch4_window7_224`

Kedua model diinisialisasi dengan bobot pra-terlatih dari `timm` dan disesuaikan untuk tugas klasifikasi 3 kelas.

## Cara Menjalankan

1.  **Unduh Notebook**: Kloning repositori ini atau unduh file `Skin_ViT_Comparison_enhanced (1).ipynb`.
2.  **Setup Lingkungan**: Buka notebook di lingkungan yang mendukung Jupyter (seperti Google Colab atau VS Code).
3.  **Kaggle API**: Pastikan Anda memiliki file `kaggle.json` di lokasi yang benar (notebook ini mengasumsikan `/content/drive/MyDrive/kaggle/kaggle.json` di Google Colab). Sesuaikan path jika perlu.
4.  **Jalankan Sel**: Jalankan semua sel secara berurutan untuk mengunduh dataset, melatih model, dan melihat hasilnya.

## Hasil

Notebook ini menghasilkan beberapa tabel dan visualisasi untuk membandingkan model:
- **Tabel Jumlah Parameter**: Membandingkan kompleksitas model.
- **Tabel Metrik Evaluasi**: Menampilkan Akurasi, Presisi, Recall, dan F1-score.
- **Tabel Waktu Inferensi**: Mengukur kecepatan prediksi pada set pengujian.
- **Kurva Pembelajaran**: Memvisualisasikan akurasi pelatihan dan validasi per epoch.
- **Confusion Matrices**: Menunjukkan kinerja per kelas.
- **Contoh Prediksi**: Menampilkan hasil prediksi pada gambar uji.

Analisis akhir memberikan ringkasan tentang model mana yang terbaik berdasarkan akurasi, efisiensi (jumlah parameter), dan kecepatan.
