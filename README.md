# 🐶🐱 Klasifikasi Wajah Hewan dengan Deep Learning

Proyek ini bertujuan untuk membangun model klasifikasi wajah hewan menggunakan deep learning. Dataset terdiri dari gambar berbagai spesies hewan, dan model diekspor dalam beberapa format seperti TensorFlow SavedModel, TFLite, dan TensorFlow.js agar mudah di-deploy ke berbagai platform (web, mobile, dan embedded systems).

---

## 📊 Insight Dataset

Dataset yang digunakan adalah **AFHQ (Animal Faces HQ)**, terdiri dari gambar wajah hewan dalam tiga kategori utama:

| Kelas     | Deskripsi                           | Jumlah Gambar (perkiraan) |
|-----------|-------------------------------------|----------------------------|
| 🐶 Dog    | Gambar wajah anjing berbagai ras    | ~5000                     |
| 🐱 Cat    | Gambar wajah kucing                 | ~5000                     |
| 🐯 Wild   | Hewan liar (seperti harimau, rubah) | ~5000                     |

## 🧠 Model & Arsitektur

Model CNN dibangun dengan TensorFlow/Keras. Proses pelatihan meliputi:
- Augmentasi gambar
- Transfer learning (opsional, tergantung implementasi)
- Evaluasi akurasi & loss
- Konversi model ke TFLite dan TF.js

---

## 🚀 Ekspor Model

Model ini telah diekspor dalam berbagai format:
- **SavedModel** → Untuk digunakan langsung di TensorFlow.
- **TFLite (.tflite)** → Untuk perangkat mobile dan embedded systems.
- **TensorFlow.js (.json & .bin)** → Untuk deployment di aplikasi web.

---

## 📈 Hasil Pelatihan

- Akurasi training dan validasi dicatat dalam notebook.
- Visualisasi metrik pelatihan (akurasi & loss) tersedia.

---

## 💾 Cara Menjalankan Notebook

1. Buka Google Colab.
2. Unggah `klasifikasi_wajah_hewan.ipynb` dan semua folder terkait.
3. Jalankan sel notebook secara berurutan.
4. Model akan disimpan otomatis ke direktori `saved_model`, `tflite`, dan `tfjs_model`.

---

## 📥 Sumber Dataset

Dataset yang digunakan: [Animal Faces HQ (AFHQ)](https://www.kaggle.com/datasets/splcher/animefacedataset)

Gunakan `kaggle.json` untuk mengunduh dataset secara otomatis melalui API Kaggle di notebook.

---

## 🛠️ Dependencies

- Python 3.x
- TensorFlow
- Keras
- TensorFlow Lite Converter
- TensorFlow.js Converter
- OpenCV (opsional, untuk preprocessing)

Install semua dependensi di Colab dengan:

```bash
!pip install tensorflow tensorflowjs
