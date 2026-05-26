# Implementasi K-Means Clustering: GPS Trajectories

## Deskripsi Proyek
Proyek ini bertujuan untuk mengelompokkan data perjalanan berdasarkan jarak (*distance*) dan kecepatan (*speed*) menggunakan metode *Unsupervised Learning*, yaitu K-Means Clustering. 

## Informasi Dataset
Data yang digunakan adalah dataset **GPS Trajectories** yang dikumpulkan dari aplikasi Android Go!Track.
* **Sumber Daya:** [UCI Machine Learning Repository - GPS Trajectories](https://archive.ics.uci.edu/dataset/354/gps+trajectories)

## Persyaratan (Dependencies)
Untuk menjalankan notebook ini, pastikan Anda telah menginstal *library* berikut:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`

## Langkah Pengerjaan
1. **Memuat Data:** Membaca file `go_track_tracks.csv` menggunakan Pandas.
2. **Pembersihan Data:** Menghapus kolom `linha` yang tidak relevan untuk proses *clustering*.
3. **Eksplorasi Data:** Memvisualisasikan persebaran awal data `speed` terhadap `distance` menggunakan *scatter plot*.
4. **Penskalaan (Normalisasi):** Mengubah skala data menggunakan `MinMaxScaler` agar tidak ada dominasi nilai fitur yang terlalu besar.
5. **Pemodelan K-Means:** Melatih model K-Means dengan menentukan jumlah kluster (K) sebanyak 3.
6. **Evaluasi:** Mengukur kualitas kluster menggunakan Silhouette Score.
7. **Visualisasi Hasil:** Menampilkan *scatter plot* dari hasil kluster beserta letak titik pusat (*centroid*) masing-masing kluster.

## Hasil Visualisasi
<img width="695" height="547" alt="image" src="https://github.com/user-attachments/assets/653903a3-6c16-4fb5-a858-f24807a3e531" />


# Implementasi K-Means Clustering: Credit Card Dataset

## Deskripsi Proyek
Proyek ini bertujuan untuk mengelompokkan data perilaku nasabah kartu kredit berdasarkan saldo (*balance*) dan total pembelian (*purchases*) menggunakan metode *Unsupervised Learning*, yaitu K-Means Clustering. 

## Informasi Dataset
Data yang digunakan adalah dataset **Credit Card Dataset for Clustering** yang merangkum riwayat transaksi dan perilaku pemegang kartu kredit.
* **Sumber Daya:** [Kaggle - Credit Card Dataset for Clustering](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)

## Dataset
Dataset berisi ringkasan aktivitas nasabah kartu kredit. Fitur utama yang digunakan untuk clustering adalah:

| Kolom | Deskripsi |
|---|---|
| `BALANCE` | Saldo yang tersisa di akun kartu kredit nasabah |
| `PURCHASES` | Total nilai pembelian yang dilakukan oleh nasabah |

## Persyaratan (Dependencies)
Untuk menjalankan notebook ini, pastikan Anda telah menginstal *library* berikut:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`

## Langkah Pengerjaan
1. **Memuat Data:** Membaca file `CC GENERAL.csv` menggunakan Pandas.
2. **Pembersihan Data:** Menghapus kolom `CUST_ID` yang tidak relevan dan mengisi nilai kosong (*missing values*) dengan nilai median.
3. **Eksplorasi Data:** Memvisualisasikan persebaran awal data `PURCHASES` terhadap `BALANCE` menggunakan *scatter plot*.
4. **Penskalaan (Normalisasi):** Mengubah skala data menggunakan `MinMaxScaler` agar tidak ada dominasi nilai fitur yang terlalu besar dari nominal transaksi.
5. **Pemodelan K-Means:** Melatih model K-Means dengan menentukan jumlah kluster (K) sebanyak 4.
6. **Evaluasi:** Mengukur kualitas kluster menggunakan Silhouette Score.
7. **Visualisasi Hasil:** Menampilkan *scatter plot* dari hasil kluster beserta letak titik pusat (*centroid*) masing-masing kluster.

## Hasil Visualisasi
<img width="868" height="547" alt="image" src="https://github.com/user-attachments/assets/27142777-a8ca-4c22-b1fe-a9552a62099c" />
