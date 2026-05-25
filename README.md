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
<img width="616" height="489" alt="image" src="https://github.com/user-attachments/assets/59786814-9858-4515-9922-66ec6657f78f" />
