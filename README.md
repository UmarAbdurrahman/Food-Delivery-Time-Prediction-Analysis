# 🍔 Food Delivery Time Prediction

## 📌 Project Description

Di era digital, layanan pesan-antar makanan semakin populer karena praktis dan cepat. Tantangan utamanya adalah **estimasi waktu pengiriman** yang akurat. Prediksi yang tidak tepat dapat menurunkan kepuasan pelanggan.

Project ini membangun **model Machine Learning** untuk memprediksi waktu pengiriman makanan berdasarkan faktor-faktor seperti:

* Jarak antara restoran dan pelanggan
* Tingkat kemacetan lalu lintas
* Waktu pemesanan (peak/off-peak)
* Jumlah item dalam pesanan
* Karakteristik kurir

Dengan model ini, layanan dapat memberikan estimasi yang lebih realistis dan meningkatkan pengalaman pelanggan.

---

## 🎯 Project Objectives

Tujuan utama project ini adalah:

1. Membantu perusahaan food delivery meningkatkan kepuasan pelanggan.
2. Memberikan estimasi waktu pengiriman yang lebih realistis.
3. Mengoptimalkan alur logistik perusahaan.

---

## 📊 Dataset

* Sumber: [Kaggle – Food Delivery Time Prediction](https://www.kaggle.com/datasets/denkuznetz/food-delivery-time-prediction/data)
* Jumlah data: **1000 baris × 9 kolom**
* Fitur utama:

  * `Order_ID`
  * `Distance_km`
  * `Weather`
  * `Traffic_Level`
  * `Time_of_Day`
  * `Vehicle_Type`
  * `Preparation_Time_min`
  * `Courier_Experience_yrs`
  * `Delivery_Time_min` (target variable)

---

## ⚙️ Data Preprocessing

* **Missing values**: Minor, dihapus untuk konsistensi.
* **Duplicate check**: Tidak ditemukan duplikasi.
* **Encoding**: Fitur kategorikal diubah ke numerik.

---

## 🔎 Exploratory Data Analysis (EDA)

* Distribusi waktu pengiriman: Mayoritas **45–55 menit**, outlier di atas **100 menit**.
* Korelasi:

  * `Distance_km` → faktor utama (0.78).
  * `Preparation_Time_min` → berpengaruh sedang (0.31).
  * `Courier_Experience_yrs` → pengaruh kecil (-0.09).

---

## 🤖 Machine Learning Models

* **Models used**:

  * Linear Regression
  * Random Forest

* **Feature Importance (Random Forest)**:

  * Distance: ~73%
  * Preparation Time: ~17%
  * Courier Experience: ~5%
  * Lainnya (<5%): Weather, Traffic, Time of Day, Vehicle Type

* **Performance**:

  * Akurat di range **20–90 menit**.
  * Kurang akurat untuk outlier (>100 menit).

---

## 💡 Business Recommendations

* **High Priority**:

  * Gunakan estimasi realistis (45–60 menit).
  * Optimalkan order jarak jauh dengan biaya dinamis/zona layanan.
  * Tingkatkan efisiensi persiapan restoran.

* **Mid Priority**:

  * Manfaatkan pengalaman kurir untuk pesanan peak hours/jarak jauh.
  * Monitoring & notifikasi untuk outlier (>100 menit).

* **Low Priority**:

  * Gunakan model untuk simulasi logistik (zona baru, jenis kendaraan, dll).

---

## ✅ Conclusion

* Model ML (Linear Regression & Random Forest) mampu memprediksi waktu pengiriman dengan cukup baik.
* Faktor terpenting: **Distance (~73%)**, diikuti **Preparation Time (~17%)**.
* Model membantu mengurangi keluhan pelanggan, serta mendukung efisiensi operasional.

---
