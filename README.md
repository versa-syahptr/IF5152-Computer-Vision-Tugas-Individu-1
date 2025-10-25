# Tugas Individu IF5152 - Computer Vision  
**Nama:** Versa Syahputra Santo  
**NIM:** 23525041

---

## 📘 Deskripsi Umum  
Repositori ini berisi implementasi **pipeline Computer Vision terintegrasi** yang mencakup empat tahap utama:  
1. **Image Filtering**  
2. **Edge Detection & Sampling**  
3. **Feature / Interest Points**  
4. **Camera Geometry & Calibration**  

Setiap tahap diimplementasikan pada direktori terpisah menggunakan **Jupyter Notebook (.ipynb)** agar mudah melakukan eksplorasi parameter dan visualisasi hasil.  
Dataset yang digunakan adalah **gambar standar dari library `skimage.data`** serta **gambar tambahan pribadi** untuk analisis mandiri.

---

## ⚙️ Struktur Folder  
```
Versa Syahputra Santo_23525041_IF5152_TugasIndividuCV/
├── 01_filtering
│   └── filtering.ipynb
├── 02_edge
│   └── edge.ipynb
├── 03_featurepoints
│   └── feature.ipynb
├── 04_geometry
│   └── geometry.ipynb
├── pexels-snapsbyclark-12981881.jpg
├── README.md
└── requirements.txt
```


---

## 🔄 Alur Aplikasi (Workflow Pipeline)

Aplikasi ini terdiri dari empat tahap utama: **Filtering**, **Edge Detection**, **Feature Points**, dan **Geometry/Calibration**.  
Masing-masing tahap diimplementasikan dalam notebook terpisah, namun secara konseptual tetap membentuk alur pipeline *computer vision* yang berkelanjutan.

### 🔹 Tahap 1 – Filtering
Melakukan *noise reduction* menggunakan **Gaussian filter** dan eksplorasi filter non-linear seperti **Median**.  
Hasil citra yang lebih halus dapat digunakan sebagai *pra-proses* untuk tahap edge detection.

### 🔹 Tahap 2 – Edge Detection
Menggunakan **Sobel** dan **Canny** untuk mendeteksi tepi objek.  
Citra masukan dapat berupa hasil filtering atau citra asli, tergantung eksperimen parameter.

### 🔹 Tahap 3 – Feature Points Detection
Mendeteksi titik-titik fitur penting menggunakan **Harris Corner** dan **FAST**.  
Tahap ini dapat dijalankan langsung dari citra asli atau edge map sebelumnya untuk eksplorasi tambahan.

### 🔹 Tahap 4 – Geometry / Calibration
Melakukan estimasi transformasi geometrik menggunakan pola **checkerboard**.  
Hasil berupa overlay transformasi dan matriks parameter estimasi.

> Desain modular ini memastikan setiap konsep dapat diuji secara mandiri, sekaligus merepresentasikan pipeline *computer vision* yang utuh.
---

## 🚀 Cara Menjalankan
**1. Instalasi Dependensi**

```bash
pip install -r requirements.txt
```

**2. Menjalankan Notebook**

Jalankan notebook sesuai urutan pipeline:
```bash
jupyter notebook 01_filtering/filtering.ipynb
jupyter notebook 02_edge/edge_detection.ipynb
jupyter notebook 03_featurepoints/feature_points.ipynb
jupyter notebook 04_geometry/camera_geometry.ipynb
```
