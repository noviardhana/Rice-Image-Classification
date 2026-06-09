# 🌾 Klasifikasi Citra Jenis Beras (Rice Image Classification)

## 📌 Deskripsi Proyek
Model *Deep Learning* berbasis **Convolutional Neural Network (CNN)** yang dirancang untuk mengklasifikasikan 5 varietas beras secara otomatis dengan akurasi tinggi: **Arborio, Basmati, Ipsala, Jasmine, dan Karacadag**.

---

## 📊 Statistik & Pembagian Dataset
Pemisahan data dilakukan secara ketat untuk menjaga integritas model dan mencegah *data leakage*.

| Set | Proporsi | Karakteristik |
| :--- | :--- | :--- |
| **Training** | 70% | Citra asli + Augmentasi (variasi pola) |
| **Validation** | 10% | 100% murni, pantau *overfitting* & *Early Stopping* |
| **Test** | 20% | 100% murni, pengujian performa akhir |

> **Input Dimensi:** 224x224 piksel (RGB)



[Image of Convolutional Neural Network architecture diagram]


---

## 🚀 Format Deployment
Model telah dikonversi ke dalam berbagai format untuk mendukung fleksibilitas penggunaan lintas *platform*:

* **`saved_model/`** Format standar **TensorFlow/Keras** untuk *backend* server yang membutuhkan akurasi penuh.
* **`tflite/`** Format terkompresi yang dioptimalkan untuk performa tinggi pada **perangkat mobile** (Android/iOS) dan IoT.
* **`tfjs_model/`** Format JSON & Binari untuk integrasi langsung ke **aplikasi Web**, memungkinkan inferensi berjalan di sisi *client* (browser).