# Laporan Proyek Machine Learning - Mizanul Ridho Aohana

## Project Overview

<br>
<div><img src="https://github.com/mizanulridhoaohana/Proyek-Akhir-Machine-Learning-Terapan/assets/112617513/f2b1f44c-35f2-4699-aab0-577c29567d9a" width="1000"/></div>
Gambar 1. Logo Spotify
<br>


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

![correlation](https://github.com/mizanulridhoaohana/Proyek-Akhir-Machine-Learning-Terapan/assets/112617513/88d32b80-666f-4fe8-83c7-d6ee8bb41023)

Gambar 2. Visualisasi Korelasi Dataset

![pairplot](https://github.com/mizanulridhoaohana/Proyek-Akhir-Machine-Learning-Terapan/assets/112617513/1dbcc853-51dc-406d-81d7-953dce04c825)

Gambar 3. Visualisasi Sebaran dan Korelasi Keseluruhan data

Dalam Exploratory Data Analysis (EDA), Gambar 2 dan Gambar 3 akan melakukan visualisasi hubungan antara setiap pasangan variabel numerik dalam dataset. Setiap sel dalam matriks berisi sebuah scatter plot yang menunjukkan bagaimana dua variabel numerik berinteraksi. Selain itu, diagonal matriks berisi histogram dari masing-masing variabel, yang dapat membantu untuk mempermudah dalam memahami distribusi data. Palet warna yang digunakan oleh Seaborn dapat membantu mengidentifikasi kategori dalam variabel, sehingga memungkinkan untuk melihat hubungan antar variabel numerik dalam konteks kategori. Fungsi ini memberikan pandangan keseluruhan tentang data, dapat membantu dalam menemukan pola, korelasi, atau outlier yang mungkin tidak terlihat dalam statistik deskriptif biasa.

![distribution](https://github.com/mizanulridhoaohana/Proyek-Akhir-Machine-Learning-Terapan/assets/112617513/ec2e5395-4535-4d50-804c-f60aa7ab49cf)

Gambar 4. Visualisasi Distribusi Popularitas berdasarkan Density

Dari 

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
Metrik evaluasi yang digunakan pada proyek ini [Accuracy](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html). $R^2$ (R-_squared_), juga dikenal sebagai koefisien determinasi, adalah metrik evaluasi yang digunakan dalam statistik dan analisis regresi untuk mengukur sejauh mana model regresi cocok dengan data yang diamati. $R^2 Score$ mengukur seberapa baik variabilitas dalam data independen (variabel prediktor) menjelaskan variabilitas dalam data dependen (variabel target). $R^2 Score$ berkisar antara 0 hingga 1, di mana 1 mengindikasikan bahwa model mampu menjelaskan semua variasi dalam data dengan sempurna, sementara 0 menunjukkan bahwa model tidak menjelaskan variasi apa pun dan hasilnya sama dengan prediksi rata-rata. 

Oleh karena itu, penggunaan $R^2 Score$ dalam  proyek ini adalah untuk mengukur sejauh mana model mampu menjelaskan variasi dalam harga mobil sport berdasarkan atribut-atribut yang ada. Dengan cara membandingkan kinerja model dengan prediksi rata-rata, R2 Score memberikan gambaran tentang tingkat akurasi prediksi, yang penting dalam menentukan prediksi harga mobil. Berikut formula $R^2 Score$ :

<br>
<div><img src="https://github.com/mizanulridhoaohana/machine-learning-terapan/assets/112617513/06c7a544-80f8-4d61-8746-3076900587a5" width="600" align="center"/></div>
<br>


Dalam rumus ini:
- $\( R^2 \)$ adalah $R^2 Score$.
- $SSRES$ adalah jumlah kuadrat dari sisa kesalahan.
- $SSTOT$ adalah jumlah total kesalahan.
- $\( y_i \)$ adalah nilai sebenarnya dari data.
- $\( \hat{y}_i \)$ adalah nilai yang diprediksi oleh model.
- $\( \bar{y} \)$ adalah rata-rata dari nilai sebenarnya.

Contoh Interpretasi perhitungan $R^2 Score$ :
Asumsikan $R^2$ = 0,68
Dapat dikatakan bahwa 68% variabilitas atribut keluaran dependen dapat dijelaskan oleh model, sedangkan 32% sisanya masih belum dapat dijelaskan.
$R^2$ menunjukkan proporsi titik data yang terletak di dalam garis yang dibuat oleh persamaan regresi. Nilai $R^2$ yang lebih tinggi diinginkan karena menunjukkan hasil yang lebih baik.


**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.
