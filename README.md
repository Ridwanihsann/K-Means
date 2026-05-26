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

### Analisis Hasil Clustering
Berdasarkan visualisasi *scatter plot* antara kecepatan (*speed*) dan jarak (*distance*), algoritma K-Means membagi data perjalanan menjadi 3 kelompok utama:
* **Cluster 1 (Jarak Pendek - Kecepatan Rendah):** Titik data yang terkonsentrasi di area sudut kiri bawah. Kelompok ini merepresentasikan rute perjalanan pendek dengan kecepatan lambat, yang sangat mungkin berupa aktivitas berjalan kaki, bersepeda, atau berkendara di area padat lalu lintas.
* **Cluster 2 (Jarak Menengah - Kecepatan Sedang):** Kelompok data yang berada di tengah. Merepresentasikan pola mobilitas urban (perkotaan) yang normal dengan jarak tempuh dan kecepatan yang cukup stabil.
* **Cluster 3 (Jarak Jauh - Kecepatan Tinggi):** Titik data yang lebih menyebar ke arah kanan dan atas. Kelompok ini mengindikasikan perjalanan melalui jalur cepat, jalan tol, atau perjalanan antar-kota dengan durasi dan rute yang panjang.

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

### Analisis Hasil Clustering
Berdasarkan visualisasi *scatter plot* antara saldo (*balance*) dan jumlah pembelian (*purchases*), K-Means berhasil memisahkan nasabah ke dalam 4 segmen perilaku utama:
* **Cluster 1 (Low Balance, Low Purchases):** Nasabah pasif. Ini adalah kelompok dominan yang menjaga saldo kredit mereka tetap rendah dan jarang melakukan transaksi pembelian dalam jumlah besar.
* **Cluster 2 (High Balance, Low Purchases):** Nasabah tipe "penabung" (*savers*). Mereka membiarkan banyak dana/saldo mengendap di dalam akun mereka, tetapi sangat membatasi diri dalam melakukan transaksi perbelanjaan.
* **Cluster 3 (Low Balance, High Purchases):** Nasabah aktif/konsumtif. Kelompok ini sangat sering menggunakan kartu kredit untuk transaksi pembelian yang cukup besar, sehingga saldo mengendap mereka cenderung rendah atau selalu diputarkan.
* **Cluster 4 (High Balance, High Purchases):** Nasabah premium (*high-rollers*). Segmen eksklusif yang memiliki saldo tersimpan dalam jumlah sangat tinggi dan secara bersamaan rutin melakukan transaksi belanja bernilai fantastis.
