# Laporan Proyek Machine Learning - Mizanul Ridho Aohana

## Project Overview

Pada bagian ini, Kamu perlu menuliskan latar belakang yang relevan dengan proyek yang diangkat.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Jelaskan mengapa proyek ini penting untuk diselesaikan.
- Menyertakan hasil riset terkait atau referensi. Referensi yang diberikan harus berasal dari sumber yang kredibel dan author yang jelas.
  
  Format Referensi: [Judul Referensi](https://scholar.google.com/) 

## Business Understanding

Proyek ini dibangun untuk perusahaan dengan karakteristik bisnis sebagai berikut :
+ Perusahaan yang aktif mengembangkan aplikasi lagu untuk kepentingan komersial.
+ Perusahaan yang aktif melakukan pembaruan untuk meningkatkan kenyamanan pengguna.

### Problem Statements

Berikut beberapa permasalahan yang diperoleh:
- Informasi apa saja yang dapat diperoleh dari dataset ini, terutama mengenai hubungan antara fitur-fitur tertentu yang memengaruhi popularitas musik?
- Dengan informasi yang ada pada dataset, bagaimana cara menghasilkan algoritma yang optimal dalam memberikan rekomendasi lagu kepada pengguna?
- Bagaimana penggunaan algoritma dapat meningkatkan ketertarikan pengguna?

### Goals

Tujuan dalam proyek ini adalah:
- Menentukan variabel yang paling berpengaruh terhadap popularitas musik, dan mengidentifikasi korelasi antara variabel-variabel tersebut.
- Meningkatkan jumlah pemutaran lagu baru dan efisiensi dalam memberikan rekomendasi lagu baru berdasarkan peningkatan pemahaman tentang faktor-faktor yang dipengaruhi.
- Mengembangkan model machine learning yang mampu memberikan rekomendasi lagu baru dengan tingkat akurasi yang tinggi berdasarkan karakteristik tertentu, sehingga memungkinkan perusahaan untuk menyesuaikan strategi produksi dan iklan.

### Solution statements

- Melakukan analisis mendalam pada dataset yang ada, proses ini seperti exploratory data analytics (EDA). Analisis ini akan membantu dalam mengidentifikasi hubungan antar fitur dan mendeteksi outlier yang mungkin memengaruhi rekomendasi dan hasil prediksi yang diberikan.
- Selanjutnya, perlu dilakukan persiapan data agar sesuai untuk pelatihan model machine learning. Ini termasuk pemrosesan data, penanganan nilai-nilai yang hilang, dan pemilihan fitur yang relevan.
- Dalam penyelesaian masalah ini, akan digunakan algoritma machine learning seperti Scholastic Gradient Descent (SGD) dan Decision Tree.

## Data Understanding
Dataset yang digunakan dalam proyek ini merupakan dataset dari spotify yang terdiri dari 18 fitur. Dataset ini diperoleh dari [Github : Rashi Bhansali](https://github.com/rashi-bhansali/Song-Recommender-cosine-similarity-and-KNN-/blob/main/data.csv).

Berikut informasi pada dataset :

+ Dataset memiliki format CSV (_Comma-Seperated Values_).
+ Dataset memiliki 8585 sample dengan 18 fitur.
+ Dataset memiliki 5 fitur bertipe stobject, 3 fitur bertipe _Integer_ dan 10 fitur bertipe _Float_.
+ Terdapat beberapa missing value dan data yang tidak perlu digunakan dalam dataset.


### Variabel pada dataset

Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- id: memberikan data unique key dalam setiap key.
- name: memberikan data nama dari lagu
- album: memberikan data nama dari album
- artist: memberikan data nama artist
- release_date: memberikan data tanggal rilis dari lagu tersebut
- duration_ms: Semakin tinggi nilainya, semakin lama durasi lagu tersebut.
- popularity: Semakin tinggi nilainya, semakin populer lagu tersebut.
- danceability: Semakin tinggi nilainya, semakin mudah untuk menari mengikuti lagu ini
- acousticness: Semakin tinggi nilainya, semakin akustik lagu tersebut
- danceability.1: Semakin tinggi nilainya, semakin mudah untuk menari mengikuti lagu ini
- energy: Energi sebuah lagu - semakin tinggi nilainya, semakin energik. lagu
- instrumentalness: Nilai-nilai mendekati 1 menunjukkan lagu yang cenderung instrumental, nilai mendekati 0 menunjukkan lagu dengan vokal yang lebih dominan.
- liveness: Atribut ini mencerminkan apakah ada unsur pertunjukan langsung dalam lagu, seperti respon penonton atau nuansa pertunjukan langsung.   
- loudness: Semakin tinggi nilainya, semakin keras lagunya.   
- speechiness: Semakin tinggi nilainya, semakin banyak kata-kata yang diucapkan dalam lagu tersebut
- tempo: Tempo adalah atribut yang mengukur kecepatan atau laju sebuah lagu. Ini diukur dalam ketukan per menit (beats per minute atau BPM).
- year: Atribut "year" adalah tahun di mana lagu tersebut dirilis atau direkam.

### Exploratory Data Analytics

Pada proses EDA, banyak digunakan analisis sebaran dan korelasi yang bisa dilihat langsung pada code yang sudah dilampirkan. Penggunaan visualisasi juga menjadi faktor penting dalam mempermudah memahami karakteristik dataset. Hal ini memberikan _insight_ lanjutan untuk memproses data sebelum dilakukan proses prediksi.


## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model sisten rekomendasi yang Anda buat untuk menyelesaikan permasalahan. Sajikan top-N recommendation sebagai output.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menyajikan dua solusi rekomendasi dengan algoritma yang berbeda.
- Menjelaskan kelebihan dan kekurangan dari solusi/pendekatan yang dipilih.

## Evaluation
Pada bagian ini Anda perlu menyebutkan metrik evaluasi yang digunakan. Kemudian, jelaskan hasil proyek berdasarkan metrik evaluasi tersebut.

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.