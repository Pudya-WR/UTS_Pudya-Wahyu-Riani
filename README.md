**KONTEKS**

Dalam industri minuman beralkohol, khususnya produksi wine, kualitas merupakan faktor utama yang menentukan nilai jual dan reputasi suatu merek. Kualitas wine dapat dipengaruhi oleh berbagai faktor kimiawi seperti fixed acidity, volatile acidity , citric acid , dll. Penilaian kualitas biasanya dilakukan oleh panel ahli wine taster, yang tentunya membutuhkan waktu dan biaya yang cukup besar. Oleh karena itu, penting bagi produsen wine untuk memiliki metode otomatis yang mampu memprediksi kualitas wine berdasarkan karakteristik kimiawinya.

Dataset Wine Quality menyediakan data mengenai komposisi kimia dari wine merah (red wine) dan wine putih (white wine), beserta nilai kualitasnya yang diberikan oleh para ahli. Data ini membuka peluang untuk membangun model prediksi berbasis machine learning yang dapat membantu memperkirakan kualitas wine tanpa harus melakukan pengujian manual

**PROBLEM STATEMENT** 

Produsen wine menghadapi tantangan dalam menilai kualitas produk secara objektif dan efisien. Proses evaluasi manual tidak hanya memakan waktu, tetapi juga bergantung pada subjektivitas penilai. Dengan adanya dataset yang memuat berbagai variabel kimia seperti fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, sulphates, alcohol, dan variabel lainnya, diperlukan suatu pendekatan analitik untuk mengidentifikasi hubungan antara fitur-fitur kimiawi tersebut dengan tingkat kualitas wine. 

Oleh karena itu, analisis data ditugaskan untuk mengembangkan model prediksi yang mampu mengklasifikasikan tingkat kualitas wine berdasarkan fitur kimiawi, sekaligus mengetahui faktor-faktor utama yang paling berpengaruh terhadap peningkatan atau penurunan kualitas. Masalah ini penting karena kualitas merupakan indikator utama dalam menentukan nilai pasar dan kepuasan konsumen. Dengan memiliki model prediksi yang akurat, produsen dapat melakukan kontrol kualitas lebih awal dan menjaga konsistensi produk mereka di pasar.

**TUJUAN** 

Berdasarkan konteks dan permasalahan yang telah dijelaskan, tujuan dari proyek ini adalah untuk membangun model machine learning yang dapat memprediksi kualitas wine menggunakan data kimiawi dari wine merah dan wine putih. Dengan begitu, diharapkan dapat membantu produsen dalam mengoptimalkan proses produksi dan menjaga standar kualitas produk secara berkelanjutan.

**DATA SET**

Data yang digunakan pada analisis prediksi adalah dataset Wine Quality yang berisi fitur-fitur kimiawi dari anggur merah dan putih serta nilai kualitasnya. Setiap baris dalam dataset merepresentasikan satu sampel wine, sedangkan setiap kolom menggambarkan karakteristik atau atribut kimia yang berbeda. Adapun variabel-variabel yang terdapat dalam dataset ini adalah sebagai berikut:

**Fixed Acidity** : menunjukkan jumlah asam non-volatile yang tidak mudah menguap selama proses fermentasi, seperti asam tartarat.

**Volatile Acidity** : kadar asam yang mudah menguap, seperti asam asetat.

**Citric Acid** : salah satu asam alami yang menambah kesegaran dan kestabilan rasa wine.

**Residual Sugar** : jumlah gula yang tersisa setelah proses fermentasi selesai.

**Chlorides** : kandungan garam (natrium klorida) yang memengaruhi rasa dan kestabilan kimiawi wine.

**Free Sulfur Dioxide** : bentuk bebas dari sulfur dioksida yang berfungsi sebagai pengawet dan pelindung terhadap oksidasi.

**Total Sulfur Dioxide** : total kandungan sulfur dioksida dalam wine.

**Density** : tingkat kerapatan cairan wine, yang berhubungan erat dengan kadar alkohol dan gula.

**pH** : menunjukkan tingkat keasaman wine, yang memengaruhi rasa, warna, dan kestabilan produk.

**Sulphates** : senyawa yang berperan dalam pembentukan aroma serta meningkatkan efek pengawetan wine.

**Alcohol** : kadar alkohol dalam wine.

**Quality** : skor kualitas pada wine.

**Id** : identitas unik untuk setiap sampel wine.

Dataset ini mencakup berbagai fitur penting yang dapat digunakan untuk mempelajari hubungan antara komposisi kimia dan kualitas wine. Dengan memahami hubungan tersebut, dapat dilakukan proses analisis dan pemodelan untuk memperkirakan nilai kualitas dari wine berdasarkan karakteristik kimiawinya.

**PROSES CLEANING DATA**

Sebelum dilakukan proses pemodelan, tahap awal yang dilakukan adalah pembersihan data (data cleaning). Pada tahap ini, data diperiksa untuk memastikan tidak terdapat nilai yang hilang (missing values) atau nilai yang tidak diinginkan. Lalu setelah diketahui anomali yang terdapat pada data dilakukan penanganan pada data seperti melakukan proses normalisasi, drop row maupun standarisasi. 

**PEMBANTUKAN MODEL**

Setelah data dilakukan proses sleaning selanjutnyat data masuk kedalam proses pembentukan model dengan menggunakan data training yang telah disediakan. Terdapat 3 model yang digunakan yaitu Decision Tree, Naive Bayes, dan K-Nearest Neighbors (KNN).

**Decision Tree** : merupakan algoritma yang bekerja dengan membentuk struktur pohon keputusan untuk memetakan fitur terhadap label target.

**Naive Bayes** : merupakan metode probabilistik yang didasarkan pada Teorema Bayes dengan asumsi independensi antar variabel.

**K-Nearest Neighbors (KNN)** : merupakan metode yang bekerja dengan menghitung jarak antara satu sampel dengan sampel lainnya untuk menentukan kelas dari data baru berdasarkan kedekatannya dengan data pelatihan.

Setelah ketiga model dibuat maka akan dibandingkan hasil akurasi dari ketiga model tersebut.

**HASIL**

Setelah model telah dibuat, maka diperoleh hasil akurasi dari masing-masin gmode tersebut.Adapun nilai akurasi dari masing-masing model adalah sebagai berikut :

1. Model Decision Tree sebesar 0.59
2. Model Naive Bayes sebesar 0.51
3. Model K-Nearest Neighbors (KNN) sebesar 0.55

Dari hasil tersebut dapat disimpulkan bahwa Decision Tree memiliki performa terbaik di antara ketiga model yang digunakan.Nilai akurasi yang relatif rendah ini disebabkan oleh sifat dataset yang memiliki banyak kelas kualitas (*multiclass classification*), sehingga proses klasifikasi menjadi lebih kompleks.

Selain itu, hasil prediksi menunjukkan bahwa kelas kualitas yang terbentuk dari data wine berkisar antara 3 hingga 8, yang berarti terdapat enam kelas utama yaitu 3, 4, 5, 6, 7, dan 8. Hal ini menunjukkan variasi kualitas yang cukup luas di antara sampel yang ada, yang menjadi tantangan tersendiri dalam pemodelan dan prediksi kualitas wine.

