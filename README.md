# Laporan Proyek Machine Learning - Mizanul Ridho Aohana

## Project Overview

<br>
<div><img src="https://github.com/mizanulridhoaohana/Proyek-Akhir-Machine-Learning-Terapan/assets/112617513/f2b1f44c-35f2-4699-aab0-577c29567d9a" width="1000"/></div>
Gambar 1. Logo Spotify
<br>

Musik adalah salah satu hal yang tidak bisa dilepaskan dalam kehidupan sehari-hari. Sebagian besar penduduk dunia hampir menggunakan musik dalam berbagai kegiatan, tujuan penggunaannya bermacam-macam, mulai dari hiburan, relaksasi, penyemangat, dll. Secara tidak langsung, hal ini berimplikasi kepada besarnya peluang industri musik untuk mengembangkan bisnis dan meraup keuntungan. Dengan adanya oportunitis ini, banyak bermunculan start up atau platform penyedia layanan musik yang mengakibatkan persaingan semakin ketat. Berikut adalah beberapa tren dan tantangan dalam industri musik:

+ Pasar yang Saturasi: Persaingan dalam industri musik semakin ketat dengan banyak artis dan label yang merilis lagu-lagu baru. Hal ini membuat sulit bagi artis untuk mendapatkan perhatian dan menonjol di tengah persaingan yang sengit.
+ Kebutuhan Personalisasi: Pengguna mengharapkan pengalaman mendengarkan yang lebih personal dan rekomendasi musik yang sesuai dengan preferensi mereka. Kebutuhan untuk memenuhi ekspektasi ini menjadi tantangan besar.
+ Volume Data yang Besar: Data musik dan perilaku mendengarkan pengguna terus berkembang secara eksponensial, yang memerlukan pendekatan yang cerdas untuk mengelola, menganalisis, dan memanfaatkannya.

Untuk mengatasi tren dan tantangan dalam persaingan industri musik, pemanfaatan machine learning adalah resolusi yang efektif. Dengan menggunakan machine learning, perusahaan musik dapat menghadirkan pengalaman mendengarkan yang lebih personal dan rekomendasi musik yang akurat kepada pengguna. Resolusi ini melibatkan pengembangan model rekomendasi musik yang mampu memahami preferensi pengguna dan memberikan rekomendasi yang sesuai.

Selain itu, machine learning dapat digunakan untuk memprediksi musik yang mirip dengan yang sering diputar pengguna. Ini membantu dalam meningkatkan eksplorasi musik pengguna dan memperkenalkan mereka pada lagu-lagu yang mungkin mereka nikmati. Dengan analisis data yang mendalam, machine learning dapat mengidentifikasi pola dalam perilaku mendengarkan pengguna dan menggunakan informasi ini untuk memberikan rekomendasi yang relevan.

Penggunaan machine learning juga dapat membantu dalam mengelola volume data yang besar dan menghasilkan wawasan berharga dari data musik. Dengan algoritma machine learning, perusahaan musik dapat memproses dan menganalisis data secara efisien, mengidentifikasi tren, dan membuat keputusan yang didasarkan pada data.

Dengan demikian, machine learning adalah resolusi yang kuat untuk menjawab tren dan tantangan dalam industri musik dengan memberikan pengalaman mendengarkan yang lebih personal, rekomendasi musik yang cermat, dan pemanfaatan data yang lebih efisien sehingga pengguna mendapatkan pengalaman yang lebih baik.

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

Dari Gambar 4. density dapat memberikan informasi tentang bagaimana popularitas terdistribusi di antara berbagai item. Density yang tinggi pada suatu titik di grafik berarti bahwa ada banyak item yang memiliki popularitas sekitar nilai tersebut, sementara density yang rendah menunjukkan bahwa hanya sedikit item yang memiliki popularitas pada tingkat tersebut. Pada Gambar 4. grafik menunjukkan bahwa dataset memiliki sebaran popularitas yang terkonsentrasi cukup merata. Kemudian jika dilihat lebih jauh, nilai density popularitas mulai menurun pada angka 50.

![image](https://github.com/mizanulridhoaohana/Proyek-Akhir-Machine-Learning-Terapan/assets/112617513/4d3f2c8e-0ba9-4ed8-8544-d0efa59acd95)

Gambar 5. Features Correlation wih dependent variable

Gambar 5 mendeskripsikan feature correlation setelah dilakukan pengolahan data. Jika dilihat pada gambar, data menunjukkan feature yang memiliki korelasi tertinngi adalah loudness, disusul dengan energy dan danceability.

![popularity](https://github.com/mizanulridhoaohana/Proyek-Akhir-Machine-Learning-Terapan/assets/112617513/0fb596ae-701e-47f0-9525-c5f640cd07c4)

Gambar 6. Sebaran Artis Populer

Pada Gambar 6. ditampilkan 15 artist dengan rating popularitas tertinggi. Rating tertinggi ada pada artis Various Artist, Various Artist ini artinya artist yang terdiri lebih dari 1 orang (duo dan group band).

## Data Preparation

Data preparation yang dilakukan pada dataset ini adalah sebagai berikut:
+ Encoding

  _Encoding_ adalah teknik mengubah data kategorik menjadi data numerik dimana setiap kategori menjadi kolom baru dengan nilai unik yang diberikan secara berurutan. Fitur yang akan diubah menjadi numerik pada proyek ini adalah _popularity_. Dengan mengubah data kategori numerik, perhitungan dalam data modeling dapat dipermudah dan disederhanakan.
  
+ Check Missing Value

  Proses ini akan melakukan pengecekan terhadap nilai _missing value_ dari dataset yang sudah ada. Hal ini dilakukan untuk mengantisipasi _overfit_ atau _underfit_ pada model yang akan dibangun dikarenakan oleh dataset yang belum dinormalisasi

+ Convert Data Type

  Pada proses ini, akan dilakukan penyeragaman tipe data pada setiap kolom numerik, sehingga seluruh kolom dapat terstandarisasi dengan baik.

+ Add Additional Variable

  Proses ini bertujuan untuk menambahkan variabel baru yang dapat memberikan _insight_ baru mengenai mobil yang sudah diproduksi. Variabel yang ditambahkan adalah _Age_, variabel ini merepresentasikan umur dari kendaraan sampai dengan saat ini.

+ Train Test Split

  _Train test split_ adalah proses membagi data menjadi data latih dan data uji. Data latih akan digunakan untuk membangun model, sedangkan data uji akan digunakan untuk menguji performa model. Pada proyek ini dataset sebesar 1007 dibagi menjadi komposisi 805 (80%) untuk data latih dan 202 (20%) untuk data uji. Komposisi pembagian ini digunakan karena jumlah dataset yang dimiliki cenderung sedikit, sehingga untuk mengoptimalkan pelatihan model, maka komposisi training yang digunakan adalah 80% dan testing 20%.
  

## Modeling
+ Algoritma
  Penelitian ini melakukan pemodelan dengan 3 algoritma, yaitu _Cosine Similarity_, _Scholastic Gradient Descent_, dan _Decision Tree_.
  + Cosine Similarity

    _Cosine similarity_ adalah sebuah metrik atau ukuran yang digunakan untuk mengukur sejauh mana dua vektor berada dalam arah yang sama dalam ruang berdimensi banyak. Ini adalah salah satu metode yang umum digunakan dalam pemrosesan teks, pengelompokan (clustering), sistem rekomendasi, dan berbagai bidang lainnya di mana perlu dilakukan perbandingan atau pengukuran kesamaan antara dua vektor atau dokumen.
    Cosine similarity mengukur kesamaan berdasarkan sudut antara dua vektor dalam ruang berdimensi banyak. Dua vektor yang benar-benar sejajar memiliki cosine similarity sebesar 1, sedangkan dua vektor yang tegak lurus memiliki cosine similarity sebesar 0, dan vektor yang berlawanan arah memiliki cosine similarity sebesar -1.
    Rumus dari cosine similarity antara dua vektor A dan B adalah sebagai berikut:

    $$\\text{Cosine Similarity}(A, B) = \frac{{A \cdot B}}{{\|A\| \cdot \|B\|}} \$$

    Di mana:
    - $\(A \cdot B\)$ adalah hasil perkalian titik (dot product) antara vektor A dan B.
    - $\(\|A\|\) dan \(\|B\|\)$ adalah panjang (magnitude) dari vektor A dan B, yang dapat dihitung sebagai akar kuadrat dari jumlah kuadrat elemen-elemen vektor.

    Cosine similarity sering digunakan dalam pemrosesan teks untuk mengukur sejauh mana dua dokumen serupa berdasarkan representasi vektor (misalnya, model ruang vektor Word2Vec atau TF-IDF). Semakin tinggi nilai cosine similarity antara dua dokumen, semakin mirip atau serupa kontennya. Ini memungkinkan perbandingan dan pengelompokan dokumen berdasarkan kesamaan mereka dalam representasi vektor.
    
  + Scholastic Gradient Descent (SGD)

    _Stochastic Gradient Descent_ (SGD) adalah sebuah algoritma optimisasi yang digunakan dalam machine learning untuk melatih model. Kerja algoritma ini adalah dengan memperbarui parameter-model secara iteratif untuk mengurangi kesalahan prediksi seiring dengan melihat satu data pelatihan atau sekelompok data pelatihan yang dipilih secara acak pada setiap iterasi.

    1. Inisialisasi parameter-model secara acak atau awal: θ(0)
    2. Untuk setiap iterasi t = 1, 2, 3, ...:
       
       a. Pilih satu data pelatihan atau sekelompok data pelatihan secara acak: $(xi, yi)$
       b. Hitung gradien dari fungsi biaya terhadap parameter-model:

       $$∇J(θ(t), xi, yi)$$
       
       c. Perbarui parameter-model:

       $$θ(t+1) = θ(t) - α * ∇J(θ(t), xi, yi)$$
       
       d. (Opsional) Periksa kriteria penghentian, seperti jumlah iterasi atau tingkat kesalahan yang dapat diterima.

       Di mana:
       - $θ(t)$ adalah parameter-model pada iterasi ke-t.
       - $(xi, yi)$ adalah data pelatihan yang dipilih pada iterasi ke-t, dengan xi sebagai fitur dan yi sebagai label.
       - $J(θ, xi, yi)$ adalah fungsi biaya yang digunakan untuk mengukur kesalahan prediksi model terhadap data pelatihan $(xi, yi)$.
       - $∇J(θ, xi, yi)$ adalah gradien dari fungsi biaya $J(θ, xi, yi)$ terhadap parameter-model θ.
       - $α$ adalah langkah pembaruan (learning rate) yang mengendalikan seberapa besar perubahan yang dilakukan pada setiap iterasi.

  + Decision Tree

    _Decision tree_ (pohon keputusan) adalah sebuah model prediktif dalam ilmu data dan pembelajaran mesin yang digunakan untuk mengambil keputusan berdasarkan aturan yang didefinisikan dalam bentuk struktur pohon. Model ini digunakan untuk masalah klasifikasi dan regresi, serta dapat digunakan untuk tugas pengambilan keputusan yang melibatkan berbagai variabel dan skenario. Algoritma _Decision Tree_ mengikuti serangkaian langkah untuk membangun model pemutusan keputusan. Langkah-langkah dari algoritma _Decision tree_ adalah sebagai berikut:
    1. Mulai dari simpul akar, misalkan sebagai S, yang berisi dataset lengkap.
    2. Ambil atribut terbaik dalam dataset menggunakan _Attribute Selection Measure_ (ASM). ASM yang bisa digunakan di antaranya _Information Gain_ dan Gini _Index_
    3. Pisahkan himpunan S menjadi himpunan bagian yang berisi kemungkinan nilai untuk atribut terbaik.
    4. Buat simpul _decision tree_ yang berisi atribut terbaik.
    5. Buat simpul _decision tree_ baru secara rekursif menggunakan himpunan bagian dari kumpulan data yang dibuat pada langkah 3. Lanjutkan proses ini sampai tahap terakhir di mana tidak dapat mengklasifikasikan simpul lebih lanjut. Simpul ini yang menjadi simpul akhir atau disebut sebagai simpul daun (_leaf node_).

    Dengan demikian, _Decision Tree_ membantu dalam memetakan kondisi atau atribut yang membimbing keputusan berdasarkan data yang ada, dan memungkinkan untuk melakukan klasifikasi atau prediksi. Dalam implementasinya digunakan [sklearn.tree.DecisionTreeClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html) dalam code.

  + Hyperparameter Tuning (Grid Search)
    
    _ Hyperparameter tuning_ adalah cara untuk mendapatkan parameter terbaik dari algoritma dalam membangun model. Salah satu teknik dalam _hyperparameter tuning_ yang digunakan dalam proyek ini adalah _grid search_. Langkah pertama dalam algoritma ini adalah mendefinisikan parameter yang akan diuji, seperti kedalaman pohon dalam Decision Tree atau laju pembelajaran dalam Scholastic Gradient Descent. Kemudian, akan dibuat "grid" parameter yang berisi semua kombinasi nilai yang akan diuji. Setelah itu, data akan dibagi menjadi set pelatihan dan set validasi silang. Untuk setiap kombinasi parameter dalam grid, model dilatih pada set pelatihan dan diuji pada set validasi silang. Hasilnya dievaluasi dengan metrik kinerja seperti akurasi. Setelah mengevaluasi semua kombinasi parameter, akan dipilih kombinasi yang memberikan kinerja terbaik. Parameter ini kemudian digunakan untuk melatih model pada seluruh data pelatihan. Pendekatan ini akan mempermudah dalam menemukan parameter yang optimal tanpa harus melakukan upaya uji coba dan kesalahan secara manual, dan memastikan bahwa model yang dibangun memiliki kinerja paling baik untuk tugas yang diberikan.


## Evaluation
Metrik evaluasi yang digunakan pada proyek ini adalah [Accuracy](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html). Metrik evaluasi $accuracy$ adalah salah satu metrik yang digunakan dalam machine learning untuk mengukur sejauh mana model klasifikasi berhasil dalam memprediksi kelas dari data uji. Metrik ini mengukur persentase dari prediksi yang benar (prediksi yang sesuai dengan kelas sebenarnya) dibandingkan dengan total jumlah prediksi.

Formula untuk menghitung metrik $accuracy$ adalah sebagai berikut:

$$\ \text{Accuracy} = \frac{\text{Jumlah Prediksi Benar}}{\text{Total Jumlah Prediksi}} \$$

Dalam formula ini:
- $Jumlah Prediksi Benar$ adalah jumlah prediksi yang benar atau prediksi yang sesuai dengan kelas sebenarnya.
- $Total Jumlah Prediksi$ adalah jumlah dari semua prediksi yang dilakukan oleh model.

Hasil akhir dari metrik "accuracy" dinyatakan dalam bentuk persentase. Semakin tinggi nilai "accuracy," semakin baik kinerja model dalam melakukan prediksi kelas.

### Hasil Evaluasi Proyek

Setelah mengimplementasikan algoritma _Logistic Linear Regression_ dan _Decision Tree_ diperoleh hasil evaluasi menggunakan $R^2 Score$. Berikut hasil evaluasi pada proyek ini :

  Tabel 1. Evaluasi kedekatan vector $cosine similarity$ untuk rekomendasi lagu
  | rekomendasi musik                | kedekatan |
  |----------------------------------|-----------|
  | Sooraj Ki Baahon Mein            | 0.963532  |
  | Nayan Tarse                      | 0.963530  |
  | Tamma Tamma Again                | 0.963530  |
  | Shades of Grey                   | 0.963527  |
  | Taaron Ke Shehar                 | 0.963526  |

  Jika dilihat pada Tabel 1. nilai _cosine similarity_ yang dihasilkan bisa dibilang sudah sangat baik karena mendekati nilai sempurna yaitu 1. Oleh karena itu, bisa dikatakan bahwa rekomendasi yang dihasilkan sudah benar.

  Selain menggunakan cosine similarity, untuk menjalankan prediksi digunakan algoritma Scholastic Gradient Descent (SGD) dan Decision Tree. Dalam penerapannya, kedua algoritma ini juga dikombinasikan dengan hypertuning parameter (grid search). Hasil akhir dari algoritma ini adalah sebagai berikut:
  
  Tabel 2. Evaluasi $accuracy$ pada proyek
  | model                       | accuracy |
  |-----------------------------|----------|
  | Scholastic Gradient Descent | 0.905521 |
  | Decision Tree               | 0.736810 |

  Tabel 3. Best Parameter pada _Hyper-Tuning_
  | model    | best_params                                                     |
  |----------|-----------------------------------------------------------------|
  | Scholastic Gradient Descent| {'alpha': 0.001}|
  | Decision Tree| {'max_depth': 5, 'max_features': 1.0, 'min_samples_leaf': 1, 'min_samples_split': 2}|
  
  Berdasarkan Tabel 2. dapat diketahui bahwa hasil yang diperoleh oleh _Scholastic Gradient Descent_ cenderung lebih tinggi jika dibandingkan dengan _Decision Tree_ dengan nilai $accuracy$ secara berturut-urut 0,90 dan 0,73. Hasil ini sudah cukup memuaskan karena _Scholastic Gradient Descent_ mampu untuk memprediksi label sesuai dengan label sebenarnya pada dataset dataset. Dalam konteks ini, mendekati 1 adalah hal yang baik karena model _Scholastic Gradient Descent_ yang telah di-_tune_ mampu memberikan hasil prediksi benar dengan baik berdasarkan fitur-fitur yang digunakan. Ini menunjukkan bahwa model mampu memberikan prediksi yang sangat baik dan akurat dalam memberikan rekomendasi musik sesuai preferensi musik yang disukai oleh pengguna.
  
  Tabel 3. berisi parameter terbaik (best parameters) yang dihasilkan dari proses hyperparameter tuning (penyetelan parameter) untuk masing-masing model. Parameter terbaik ini digunakan saat melatih model. Untuk dua model yang disebutkan, yaitu _Scholastic Gradient Descent_ dan _Decision Tree_, parameter terbaik adalah sebagai berikut:

+ Model "Scholastic Gradient Descent" memiliki parameter terbaik {'alpha': 0.001}. Ini menunjukkan bahwa parameter 'alpha' dengan nilai 0.001 memberikan kinerja terbaik untuk model SGD.
+ Model "Decision Tree" memiliki parameter terbaik {'max_depth': 5, 'max_features': 1.0, 'min_samples_leaf': 1, 'min_samples_split': 2}. Ini menunjukkan kombinasi parameter yang menghasilkan kinerja terbaik untuk model Decision Tree.

Tabel ini memberikan wawasan tentang parameter mana yang paling sesuai untuk digunakan dalam melatih model-model tersebut. Parameter terbaik ini dapat membantu meningkatkan kinerja model dalam memprediksi data.

### Implikasi Bisnis 

Hasil evaluasi dengan $accuracy$ yang mendekati 1 memiliki implikasi yang signifikan dalam konteks pengambilan keputusan bisnis. Dalam kasus ini, di mana model _Scholatic Gradient Descent (SGD)_ yang telah di-_tune_ memiliki $accuracy$ sebesar 0.97438, ini berarti bahwa model tersebut mampu melakukan prediksi benar pada setiap label berdasarkan fitur-fitur yang diberikan.

Implikasi ini dapat berdampak pada sejumlah keputusan bisnis:

1. Peningkatan Pengalaman Pengguna: Dengan menggunakan model rekomendasi yang optimal, Anda dapat meningkatkan pengalaman pengguna di platform musik Anda. Dengan memahami preferensi dan perilaku mendengarkan pengguna, Anda dapat menyajikan lagu-lagu yang sesuai dengan selera mereka, sehingga meningkatkan retensi pengguna dan mendorong lebih banyak interaksi dengan platform.

2. Peningkatan Retensi Pengguna: Model rekomendasi yang baik dapat membantu mempertahankan pengguna dalam jangka waktu yang lebih lama. Pengguna yang mendapatkan rekomendasi yang relevan dan sesuai dengan preferensi mereka lebih cenderung untuk terus menggunakan platform Anda, yang dapat menghasilkan pendapatan berkelanjutan.

3. Pengoptimalan Katalog Musik: Dengan memahami faktor-faktor yang memengaruhi popularitas musik, Anda dapat mengoptimalkan katalog musik Anda. Anda dapat menentukan lagu-lagu mana yang paling sesuai untuk promosi, dan mungkin mendapatkan wawasan tentang tren musik yang sedang berlangsung.

4. Monetisasi Lebih Lanjut: Dengan memahami perilaku pengguna dan preferensi mereka, Anda dapat mengarahkan pengguna ke konten berbayar atau menghasilkan pendapatan tambahan melalui rekomendasi yang cermat.

5. Analisis Sentimen dan Pemasaran: Data tentang popularitas musik dan preferensi pengguna dapat memberikan wawasan berharga tentang tren dan sentimen musik. Perusahaan dapat menggunakan data ini untuk merancang kampanye pemasaran yang lebih efektif dan mengidentifikasi peluang bisnis yang mungkin.

6. Kolaborasi dengan Artis dan Label Musik: Dengan pemahaman yang lebih baik tentang faktor-faktor yang memengaruhi popularitas musik, Anda dapat menjalin kemitraan dengan artis dan label musik untuk mempromosikan lagu-lagu yang mungkin mendapatkan popularitas lebih besar.

7. Pemahaman Audiens yang Lebih Baik: Analisis data yang lebih mendalam dapat membantu Anda memahami audiens Anda dengan lebih baik. Ini dapat membantu dalam pengembangan konten yang disesuaikan, rencana pemasaran yang lebih efisien, dan pertumbuhan bisnis yang berkelanjutan.

8. Pemantauan dan Evaluasi Kinerja: Model rekomendasi dapat membantu Anda dalam pemantauan dan evaluasi kinerja lagu-lagu, album, atau artis tertentu. Anda dapat mengidentifikasi kinerja yang kuat dan memahami faktor-faktor yang berkontribusi terhadap kesuksesan mereka.

