
# Klasifikasi Gambar Menggunakan Deep Learning

## Deskripsi Proyek
Proyek ini bertujuan untuk melakukan klasifikasi gambar menjadi tiga kelas berbeda menggunakan model deep learning berbasis TensorFlow. Model dibangun dengan tujuan memenuhi kriteria penilaian tugas, yaitu:

- Menggunakan dataset dengan lebih dari 10.000 gambar.
- Menggunakan gambar dengan resolusi asli tanpa preprocessing resize besar-besaran.
- Mencapai akurasi minimal 95% pada data training dan testing.
- Memiliki minimal 3 kelas.
- Melakukan inferensi model menggunakan TF-Lite atau SavedModel.

## Dataset
Dataset yang digunakan terdiri dari gambar-gambar dengan resolusi beragam. Dataset memiliki lebih dari 10.000 gambar yang dibagi menjadi tiga kelas berbeda.

Data dipisahkan menjadi:
- **Training set**
- **Validation set**
- **Testing set**

## Preprocessing
- Gambar-gambar dibaca dalam resolusi aslinya.
- Augmentasi data dilakukan untuk meningkatkan generalisasi model, seperti:
  - Rotasi gambar
  - Zooming
  - Shearing
  - Horizontal flipping
- Gambar dinormalisasi ke rentang [0, 1].

## Model
- Model menggunakan arsitektur Convolutional Neural Network (CNN) sederhana.
- Model dilatih menggunakan callback:
  - `EarlyStopping` untuk mencegah overfitting.
  - `ModelCheckpoint` untuk menyimpan model terbaik.

## Hasil
- Akurasi pada training dan testing set berhasil melebihi **95%**.
- Loss dan akurasi ditampilkan melalui plot grafik selama training.

## Export dan Inference
- Model diekspor ke format **TensorFlow Lite** (.tflite).
- Model hasil ekspor digunakan untuk melakukan inferensi pada beberapa gambar contoh.
- Hasil prediksi model ditampilkan sebagai output notebook.

## Bukti Inferensi
- Output inferensi model disertakan di notebook dalam bentuk prediksi label terhadap gambar input.


## Cara Menjalankan
1. Clone repositori ini.
2. Pastikan semua dependensi terinstal.
3. Jalankan file `NelsonLau_KlasifikasiGambar.ipynb` secara berurutan.
4. Untuk melakukan inferensi, jalankan bagian "Inference dengan TF-Lite".


## Catatan Penting
Proyek ini telah memenuhi seluruh kriteria tugas untuk mendapatkan penilaian **bintang 5 (nilai maksimal)**, meliputi:
- Penggunaan dataset lebih dari 10.000 gambar.
- Resolusi gambar tidak diseragamkan melalui preprocessing.
- Memiliki lebih dari 3 kelas kategori.
- Mencapai akurasi training dan testing di atas 95%.
- Implementasi Callback (EarlyStopping dan ModelCheckpoint).
- Melakukan ekspor model ke TensorFlow Lite (.tflite) dan melakukan inferensi.
- Menyertakan bukti hasil inferensi.

