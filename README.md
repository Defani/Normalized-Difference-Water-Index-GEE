# 🌊 NDWI Analysis using Google Earth Engine (Sentinel-2)

Analisis **Normalized Difference Water Index (NDWI)** berbasis **Google Earth Engine (GEE)** menggunakan citra **Sentinel-2 Surface Reflectance** untuk **monitoring badan air** dan **perhitungan luas perairan** secara otomatis.

---

## 📌 Deskripsi Singkat
NDWI (*Normalized Difference Water Index*) adalah indeks spektral yang dikembangkan oleh **McFeeters (1996)** untuk mendelineasi badan air terbuka dengan memanfaatkan reflektansi **band hijau (Green)** dan **near-infrared (NIR)**.  
Metode ini efektif untuk:
- 🔍 Ekstraksi badan air
- ☁️ Reduksi pengaruh vegetasi dan tanah
- 📐 Perhitungan luas perairan (hektar)
- 🗺️ Konversi raster ke vektor

---

## 🧮 Formula NDWI
\[
NDWI = \frac{Green - NIR}{Green + NIR}
\]

Pada Sentinel-2:
- **Green** : Band 3 (B3)  
- **NIR** : Band 8 (B8)

---

## 🛰️ Data & Platform
- **Data** : Sentinel-2 SR Harmonized  
- **Resolusi** : 10 meter  
- **Platform** : Google Earth Engine  
- **Bahasa** : JavaScript  

---

## ⚙️ Alur Analisis
1. ☁️ Cloud masking menggunakan **Scene Classification Layer (SCL)**
2. 📆 Filter waktu dan persentase awan
3. 🧩 Komposit citra (median)
4. 🌊 Perhitungan NDWI
5. 🎚️ Thresholding NDWI (> 0.009)
6. 📏 Perhitungan luas badan air (hektar)
7. 🧱 Konversi raster → vektor (polygon)

---

## 🎨 Visualisasi
- Komposit Sentinel-2 **11-8-2**
- NDWI dengan palet warna gradasi
- Masking area air
- Layer vektor badan air

---

## 📊 Output
- 🗺️ Peta NDWI
- 💧 Mask area badan air
- 📐 Luas badan air (hektar)
- 🧩 Vektor polygon badan air

---

## 🚀 Cara Menggunakan
1. Buka **Google Earth Engine Code Editor**
2. Salin seluruh script dari repository ini
3. Pastikan variabel **`geometry`** sudah didefinisikan
4. Jalankan script ▶️
5. Cek hasil visualisasi dan output luas di **Console**

---

## 🧑‍💻 Author
**Defani Arman Alfitriansyah**  
🎓 Fakultas Kehutanan dan Lingkungan – Universitas Kuningan  
📧 Email: 20220710063@uniku.ac.id  

---

## 📚 Referensi
- McFeeters, S.K. (1996). *The use of the Normalized Difference Water Index (NDWI) in the delineation of open water features*.  
- Gao, B. (1996). *NDWI—A normalized difference water index for remote sensing of vegetation liquid water*.  
- Cardille et al. (2024). *Cloud-Based Remote Sensing with Google Earth Engine*. Springer.

---

✨ Feel free to fork, modify, and use this script for research or learning purposes.
