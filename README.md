# BBCA STOCK PREDICTION

![_3d8508af-d3f5-44e2-88bd-d37d5d450ecd](https://github.com/Yahya08/BBC-Stock-Predictions/blob/main/public/PNG/download.png)

## Background

Pasar saham merupakan arena yang dinamis di mana 
investor berusaha untuk memperoleh keuntungan melalui 
perdagangan saham perusahaan publik. Salah satu perusahaan 
publik yang menjadi fokus perhatian investor di pasar saham 
Indonesia adalah PT Bank Central Asia (BBCA), sebuah 
lembaga keuangan terkemuka di Indonesia. BBCA telah 
menjadi sorotan pasar dikarenakan harga sahamnya terus 
menguat, yang dapat dilihat dari volume transaksi yang 
semakin tinggi (Vina C. Nugroho et al., 2021). Kinerja yang 
konsisten dan reputasi yang kuat telah membuat saham BBCA 
menjadi primadona bagi investor yang mencari stabilitas dan 
potensi keuntungan dalam investasi saham.


Harga saham BBCA dari tahun ke tahun terus meningkat 
karena kinerja saham BCA terus memberikan performa terbaik 
dalam industri perbankan di Indonesia (Vina C. Nugroho et al., 
2021). Meskipun sempat terjadi penurunan tren di masa 
pandemi pada tahun 2020-2021, laba perusahaan dan harga 
saham tetap cukup baik. Pada awal pandemi Covid-19, harga 
saham BBCA terkoreksi besar-besaran, mencapai harga 
terendah di kisaran Rp21.000, namun segera naik kembali ke 
harga Rp35.000 pada kuartal IV tahun 2020 (Pratiwi 
Sabdowati et al., 2020; Putu Tirta Aditya, et al., 2023).
Namun, pergerakan harga saham sangat sulit diprediksi 
(Sakhare & Sagar Imambi, 2019; Zhang et al., 2022). Kenaikan 
dan penurunan harga saham biasanya dipengaruhi banyak 
faktor, salah satunya adalah ekspektasi dan preferensi 
masyarakat dalam berbelanja secara online serta kemudahan 
sistem pembayaran digital (Putu Tirta Aditya, et al., 2023). 
Oleh karena itu, meramal pergerakan harga saham secara 
akurat merupakan tantangan menarik yang perlu dipelajari 
lebih lanjut.


Prediksi harga saham dapat menggunakan kecerdasan 
buatan seperti machine learning untuk menghasilkan prediksi 
yang akurat (Saini & Sharma, 2022). Peramalan nilai saham 
dengan metode machine learning dapat menggunakan 
informasi dari transaksi harian, termasuk data tentang harga 
penutupan (close), harga tertinggi (high), harga terendah (low), 
harga pembukaan (open), serta volume transaksi.

## Preprocesing
![_3d8508af-d3f5-44e2-88bd-d37d5d450ecd](https://github.com/Yahya08/BBC-Stock-Predictions/blob/main/public/PNG/Diagram%20Tanpa%20Judul.drawio%20(1).png)

1. Pengambilan Dataseet

Kami menggunakan dataset Bank Central Asia Stock 
Historical Price dari BBCA yang diupdate 1 hari lalu dari tahun 
2019. (https://www.kaggle.com/datasets/caesarmario/bank-centralasia-stock-historical-price?select=BBCA.JK_monthly.csv.) 
Datasheet tersebut memiliki 7 feature
• Date : Kolom ini berisi informasi tentang tanggal 
transaksi.
• Open : harga awal (harga pembukaan) dari saham.
• High : harga tertinggi yang dicapai oleh saham selama 
periode perdagangan.
• Low : harga terendah yang dicapai oleh saham selama 
periode perdagangan.
• Close : harga penutupan dari saham pada hari 
perdagangan.
• Adj Close : harga penutupan yang telah disesuaikan 
untuk memperhitungkan semua perubahan yang terjadi 
dalam saham tersebut
• Volume : jumlah saham yang diperdagangkan selama 
periode waktu tertentu.


2. Pre-processing 

Data pre-processing merupakan langkah yang 
dilakukan guna mempersiapkan data agar dapat digunakan 
pada tahap pemodelan. Tujuan dari preprocesing ialah 
membersihkan data, mempersiapkan data Dan menormalkan 
data sebelum dilakukannya pemodelan tanpa merubah 
validitas isi yang terkandung dalam dataseet [1].
1) Pengecekan Missing Values
Missing Values atau nilai yang hilang 
merujuk pada nilai yang absen atau tidak ada dalam 
data, meskipun seharusnya ada atau diharapkan 
ada[2]. Ini bisa terjadi karena berbagai alasan seperti 
kesalahan pengumpulan data, kegagalan perangkat 
lunak, atau kesalahan manusia. Kehadiran nilai yang 
hilang dapat mempengaruhi analisis data dan 
interpretasi hasil, sehingga penting untuk mengelola 
nilai yang hilang dengan benar dalam analisis data.
2) Seleksi Fitur
Seleksi fitur adalah proses dalam analisis 
data dan pembelajaran mesin di mana subset fitur dari 
data yang tersedia dipilih untuk digunakan dalam 
model atau analisis lebih lanjut. Tujuannya adalah 
untuk mengurangi dimensi data dengan 
mempertahankan hanya fitur-fitur yang paling 
relevan atau yang paling berkontribusi terhadap 
prediksi atau analisis yang dilakukan[3]. Pendekatan 
seleksi fitur membantu mengurangi overfitting, 
mempercepat waktu komputasi, dan meningkatkan 
interpretabilitas model. Metode yang umum 
digunakan dalam seleksi fitur meliputi teknik statistik 
seperti uji kepentingan fitur, pemilihan berdasarkan
model, dan metode berbasis pengurangan dimensi 
seperti Principal Component Analysis (PCA). 
3) Deteksi dan Penghapusan Outlier
Deteksi dan penghapusan outlier adalah proses 
dalam analisis data yang bertujuan untuk 
mengidentifikasi dan mengatasi titik data yang tidak 
biasa atau ekstrim di dalam dataset. Outlier adalah 
nilai yang jauh berbeda dari sebagian besar data 
lainnya dalam kumpulan data [4]. Penyebab outlier 
bisa bermacam-macam, seperti kesalahan 
pengukuran, gangguan pada pengumpulan data, atau 
sifat alami dari fenomena yang diamati.
4) Konversi Format Tanggal dan Pengurutan Data
Konversi format tanggal adalah proses mengubah 
representasi data tanggal dari satu format ke format 
lain yang lebih sesuai untuk analisis atau 
penyimpanan data. Misalnya, seringkali dalam data 
mentah, tanggal dapat direpresentasikan dalam 
berbagai format seperti "YYYY-MM-DD" atau 
"DD/MM/YYYY". Dalam analisis data, seringkali 
lebih efektif untuk mengonversi semua tanggal ke 
format yang konsisten, misalnya menjadi objek 
tanggal Python atau menggunakan format tertentu 
seperti "YYYY-MM-DD". Proses ini mempermudah 
pengurutan data berdasarkan tanggal dan penggunaan 
tanggal dalam analisis waktu.
Pengurutan data adalah proses menyusun data 
dalam urutan tertentu, biasanya berdasarkan nilai dari 
satu atau lebih kolom dalam dataset. Ketika datanya 
terkait dengan waktu atau tanggal, penting untuk 
mengurutkannya berdasarkan kolom tanggal secara 
kronologis atau urutan waktu lainnya.


3. Normalisasi data

Data historis saham dan indikator teknikal perlu 
dinormalisasi. Teknik normalisasi data yang digunakan 
dalam penelitian ini adalah Teknik min-max. Normalisasi 
min-max mengubah nilai-nilai dalam dataset ke dalam 
rentang nilai tertentu, misalnya [0, 1]. Teknik ini 
memetakan setiap nilai dalam dataset ke dalam rentang 
tersebut menggunakan Persamaan berikut, [5].
Xnorm = X−Xmin
Xmax−Xmin
(1)
Xnorm adalah nilai yang telah dinormalisasi dari nilai 
asli X, Xmin adalah nilai terkecil dalam dataset, Dan Xmax
adalah nilai terbesar dalam dataset. Dengan menggunakan 
normalisasi min-max, semua nilai dalam dataset dikonversi 
ke dalam rentang [0, 1]. Nilai terkecil dalam dataset akan 
menjadi 0, sedangkan nilai terbesar akan menjadi 1. Nilainilai lainnya akan terdistribusi di antara 0 dan 1 sesuai 
dengan proporsinya dalam dataset.


4. Spliting Data

Splitting data merupakan proses pembagian data 
menjadi dua atau lebih bagian yang mengandung banyak
data[6]. Pada tahap ini, dilakukan pemisahan data yang 
berfungsi untuk memisahkan variabel independen dari 
variabel dependen. Selain itu, pada tahap ini juga 
dilakukan pemisahan data untuk pelatihan (training) dan 
pengujian (testing) model. Pembagian data antara 
pelatihan dan pengujian digunakan untuk melatih model 
dan mengevaluasi kualitas metode yang digunakan.

4. Modeling
- Linear Regresion
Linear regresion digunakan untuk menganalisis 
hubungan antara variabel independen dan dependen. 
Regresi ini terdiri dari dua model dasar: regresi linear 
sederhana dan regresi linear berganda. Regresi linear 
sederhana digunakan untuk memprediksi hubungan antara 
dua variabel, sementara regresi linear berganda 
melibatkan dua atau lebih variabel independen[7].
![_3d8508af-d3f5-44e2-88bd-d37d5d450ecd](https://github.com/Yahya08/BBC-Stock-Predictions/blob/main/public/PNG/download%20(1).png)


- Random Forest Regresion
Random Forest Regresion adalah metode 
ensemble learning yang terdiri dari beberapa pohon 
keputusan yang dilatih pada subset yang berbeda dari data 
pelatihan dan hasil prediksi dari semua pohon ini 
digabungkan untuk memberikan prediksi akhir[10].
Random Forest Regression menggabungkan 
konsep-konsep dari beberapa pohon keputusan yang secara 
acak dibangun selama proses pelatihan. Setiap pohon 
dalam Random Forest dihasilkan secara independen dan 
memiliki prediksi sendiri. Prediksi akhir dari Random 
Forest adalah rata-rata (untuk regresi) dari prediksiprediksi yang dihasilkan oleh setiap pohon individu.
Berikut adalah persamaan umum dari Random 
Forest Regression [11].
𝑦̂ =
1
𝑁𝑡𝑟𝑒𝑒
∑ 𝑓𝑖(𝑥)
𝑁𝑡𝑟𝑒𝑒
𝑖=1
(4)
𝑦̂ ∶ 𝑃𝑟𝑒𝑑𝑖𝑘𝑠𝑖 𝑎𝑘ℎ𝑖𝑟 𝑢𝑛𝑡𝑢𝑘 𝑣𝑎𝑟𝑖𝑎𝑏𝑒𝑙 𝑑𝑒𝑝𝑒𝑛𝑑𝑒𝑛
𝑁𝑡𝑟𝑒𝑒:𝐽𝑢𝑚𝑙𝑎ℎ 𝑝𝑜ℎ𝑜𝑛
𝑓𝑖
(𝑥): 𝑝𝑟𝑒𝑑𝑖𝑘𝑠𝑖 𝑑𝑎𝑟𝑖 𝑝𝑜ℎ𝑜𝑛 𝑘𝑒𝑝𝑢𝑡𝑢𝑠𝑎𝑛
![_3d8508af-d3f5-44e2-88bd-d37d5d450ecd](https://github.com/Yahya08/BBC-Stock-Predictions/blob/main/public/PNG/download%20(2).png)

- Support Vector Regresion
Support Vector Regresion adalah varian dari SVM 
yang digunakan untuk tugas regresi. Alih-alih mencoba 
memisahkan data menggunakan hyperplane seperti pada 
SVM untuk klasifikasi, SVR mencoba menyesuaikan data 
dalam sebuah margin yang ditentukan, yang dikenal
sebagai epsilon-tube [12].
Support Vector Regression (SVR) bekerja dengan 
mencoba membangun sebuah hyperplane (bidang pemisah) 
dalam ruang fitur yang memiliki margin maksimal terhadap 
titik data. Hyperplane ini digunakan untuk memprediksi 
nilai variabel dependen berdasarkan variabel independen.
Berikut adalah bentuk umum dari persamaan SVR [13]:
𝑦 = 𝑊𝑇
. 𝑥 + 𝑏 (5)
𝑥 ∶ 𝑣𝑒𝑘𝑡𝑜𝑟 𝑖𝑛𝑝𝑢𝑡 𝑦𝑎𝑛𝑔 𝑚𝑒𝑤𝑎𝑘𝑖𝑙𝑖 𝑓𝑖𝑡𝑢𝑟 − 𝑓𝑖𝑡𝑢𝑟
𝑊: 𝑣𝑒𝑐𝑡𝑜𝑟 𝑏𝑜𝑏𝑜𝑡
𝑏 ∶ 𝑛𝑖𝑙𝑎𝑖 𝑏𝑖𝑎𝑠 (𝑜𝑓𝑓𝑠𝑒𝑒𝑡)
![_3d8508af-d3f5-44e2-88bd-d37d5d450ecd](https://github.com/Yahya08/BBC-Stock-Predictions/blob/main/public/PNG/download%20(3).png)

## Evaluation
Evaluasi model adalah proses menilai kinerja 
suatu model pembelajaran mesin berdasarkan berbagai 
metrik untuk menentukan seberapa baik model tersebut 
memprediksi data yang belum pernah dilihat sebelumnya 
(data pengujian). Evaluasi model sangat penting untuk 
memastikan bahwa model yang dibangun tidak hanya 
bekerja dengan baik pada data pelatihan tetapi juga mampu 
menggeneralisasi dengan baik pada data baru.

![_3d8508af-d3f5-44e2-88bd-d37d5d450ecd](https://github.com/Yahya08/BBC-Stock-Predictions/blob/main/public/PNG/download%20(4).png)
![_3d8508af-d3f5-44e2-88bd-d37d5d450ecd](https://github.com/Yahya08/BBC-Stock-Predictions/blob/main/public/PNG/download%20(5).png)
![_3d8508af-d3f5-44e2-88bd-d37d5d450ecd](https://github.com/Yahya08/BBC-Stock-Predictions/blob/main/public/PNG/newplot%20(1).png)
