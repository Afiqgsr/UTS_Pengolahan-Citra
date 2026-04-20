# Deteksi Penggunaan Alat Pelindung Diri (APD) Menggunakan YOLOv8 dan CNN

## Deskripsi

Proyek ini bertujuan untuk mendeteksi penggunaan Alat Pelindung Diri (APD) pada pekerja konstruksi menggunakan pendekatan Computer Vision dan Deep Learning.

Sistem dikembangkan menggunakan pendekatan **Two-Stage Pipeline**, yaitu:

* **YOLOv8** untuk deteksi lokasi objek (bounding box)
* **CNN (ResNet18)** untuk klasifikasi detail atribut APD

---

## Tujuan

* Mendeteksi penggunaan APD secara otomatis dari citra
* Mengimplementasikan YOLOv8 untuk deteksi objek
* Menggunakan CNN (ResNet18) untuk klasifikasi APD
* Menghitung Safety Score

---

## Dataset

Dataset yang digunakan berasal dari Kaggle:

👉 https://www.kaggle.com/datasets/ketakichalke/ppe-kit-detection-construction-site-workers

Dataset berisi anotasi APD seperti:

* Helmet
* Gloves
* Vest
* Boots
* Goggles
* dan pelanggaran (no_helmet, dll)

---

## Metodologi

### 1. Preprocessing

* Cropping objek dari bounding box YOLO
* Resize gambar (224x224)
* Normalisasi citra

### 2. Deteksi Objek (YOLOv8)

* Digunakan untuk menemukan lokasi objek pada gambar

### 3. Klasifikasi (CNN - ResNet18)

* Mengklasifikasikan atribut APD dari hasil cropping

### 4. Two-Stage Pipeline

1. YOLO → deteksi lokasi
2. Crop → ekstraksi objek
3. CNN → klasifikasi

---

## Safety Score

Safety Score dihitung dengan rumus:

Safety Score = (APD Aman / Total APD) × 100%

Kategori:

* ≥ 80% → Sangat Aman
* 50–79% → Perlu Perhatian
* < 50% → Bahaya

---

## Hasil

* Deteksi bounding box objek pekerja
* Klasifikasi APD
* Confidence score
* Safety Score

---

## Teknologi

* Python
* OpenCV
* PyTorch
* YOLOv8 (Ultralytics)

---

## Anggota

* Adam Mahabayu Muhibbulloh
* Afiq Galuh Setya Ramadhani

---

## Catatan

Dataset tidak diupload ke GitHub karena ukuran besar. Silakan download melalui link Kaggle.
