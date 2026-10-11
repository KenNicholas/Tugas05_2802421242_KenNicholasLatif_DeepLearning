# Tugas05_2802421242_KenNicholasLatif_DeepLearning

Repositori ini berisi implementasi eksperimen (CNN) menggunakan PyTorch. Proyek ini membandingkan kinerja model pelatihan dari awal (from scratch) dengan  *Transfer Learning (feature extraction dan progressive fine-tuning) pada kondisi dataset yang terbatas.

## Deskripsi Eksperimen
Eksperimen ini berfokus pada analisis pergeseran representasi visual, mitigasi *catastrophic forgetting*, dan efektivitas *data augmentation* menggunakan dataset **Oxford-IIIT Pet** (subset 10 kelas hewan peliharaan).

### Skenario Pengujian (B1 - B5)
- **B1**: Baseline from Scratch (ResNet-18)
- **B2**: Feature Extraction (ResNet-18)
- **B3**: Progressive Fine-Tuning (ResNet-18 dengan *differential learning rates*)
- **B4**: Uji Kontrol Data Augmentation (Tanpa vs Dengan Augmentasi)
- **B5**: Arsitektur Pembanding (Feature Extraction menggunakan EfficientNet-B0)

## Struktur Repositori
- `notebook_eksperimen.ipynb`: Kode utama yang mencakup seluruh alur kerja (persiapan data, pelatihan, evaluasi metrik, dan visualisasi *feature map*).
- `training_logs.json`: Bukti log hasil eksekusi eksperimen untuk setiap skenario pelatihan.
- `requirements.txt`: Daftar pustaka Python yang dibutuhkan untuk mereproduksi eksperimen.

## Parameter Utama
- **Resolusi Input**: 224x224 piksel
- **Fungsi Loss**: CrossEntropyLoss
- **Optimizer**: AdamW
- **Kriteria Berhenti**: *Early stopping* berbasis *validation loss*
