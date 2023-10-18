# Mini Project 4 : Predict Customer Clicked Ads Classification by Using Machine Learning
## Background
Sebuah perusahaan di Indonesia ingin mengevaluasi efektivitas sebuah iklan yang mereka tayangkan, hal ini sangat penting untuk memahami sejauh mana iklan mereka mencapai target pasar dan menarik perhatian pelanggan. Dengan menganalisis data historical advertisement dan mengidentifikasi wawasan serta pola-pola yang terjadi, proyek ini membantu perusahaan menentukan target pemasaran yang tepat. Fokus utamanya adalah membuat model klasifikasi machine learning untuk mengidentifikasi pelanggan target yang tepat.
## Objective
Membuat model machine learning classification untuk memudahkan perusahaan dalam mengambil keputusan dalam menentukan target marketing.
## Tools
Proyek ini menggunakan Python sebagai bahasa pemrograman, Jupyter notebook / Google collab, serta beberapa pustaka seperti pandas, numpy, sklearn untuk pre-processing dan pembelajaran mesin, dan kombinasi matplotlib dan seaborn untuk visualisasi data.
## Content
### Data Cleaning dan Data Preprocessing
Tahap ini meliputi beberapa proses, seperti penanganan missing value. Fitur numerik dengan nilai yang hilang diisi dengan nilai median masing-masing fitur. Penggunaan nilai median dipilih karena distribusi data cenderung condong. Untuk fitur kategorikal, nilai yang hilang diisi dengan nilai modus dari fitur tersebut, dan dataset tidak mengandung nilai duplikat. Proses ini melibatkan ekstraksi tanggal dan waktu, memisahkan fitur data dan target, kemudian membagi data menjadi 70% untuk training dan 30% untuk testing. Encoding fitur dilakukan menggunakan teknik Label Encoding dan One Hot Encoding.
### Data Modeling
Pemodelan data dilakukan baik tanpa maupun dengan normalisasi. Setelah proses normalisasi, terlihat beberapa perubahan dalam hasil model. Akurasi meningkat untuk semua model, terutama untuk KNN dan Regresi Logistik, menunjukkan peningkatan yang signifikan dibandingkan dengan hasil sebelumnya. Hal ini menunjukkan bahwa penanganan normalisasi data dapat meningkatkan kinerja model, termasuk skor akurasi, recall, dan presisi.
### Confusion Matrix
Model menghasilkan hasil yang sangat baik, dengan meminimalkan jumlah False Positif (Iklan diprediksi diklik tetapi sebenarnya tidak) hingga 3%. Hal ini menghasilkan skor True Positive yang tinggi (Iklan diprediksi dan benar-benar diklik) sebesar 46,5%, yang berpotensi memberikan keuntungan lebih tinggi.
### Feature Important
- Fitur `Daily Time Spent on Site` dan `Daily Internet Usage` menunjukkan korelasi tertinggi dalam memprediksi iklan yang diklik oleh pelanggan. Hal ini didukung oleh analisis EDA sebelumnya, yang mengindikasikan bahwa pelanggan dengan penggunaan internet harian dan waktu yang dihabiskan di situs yang lebih rendah cenderung lebih sering mengklik iklan. 
- Fitur `Age` dan `Area Income` juga penting, menunjukkan bahwa pelanggan dengan usia lebih muda dan pendapatan lebih tinggi cenderung kurang mengklik iklan.
### Rekomendasi Bisnis
- Untuk pelanggan yang menghabiskan waktu sekitar 40-45 menit harian di situs, pertimbangkan iklan yang lebih interaktif atau konten yang singkat dan jelas.
- Fokuskan upaya pemasaran pada pelanggan dengan penggunaan internet harian sekitar 100-150. Sesuaikan iklan dengan minat mereka.
- Sasar kelompok usia yang lebih tua secara khusus. Buat iklan yang relevan dengan preferensi dan kebutuhan mereka.
- Gunakan data usia dan pendapatan daerah untuk mengidentifikasi dan menargetkan kelompok pelanggan dengan potensi tinggi untuk mengklik iklan, sehingga alokasi anggaran pemasaran dapat dilakukan dengan lebih efisien.
## Simulasi Menggunakan Model Machine Learning
Berdasarkan confusion metrix, kita dapat mengelompokkan pelanggan berdasarkan prediksi siapa yang mengklik iklan (145 pelanggan) dan siapa yang tidak mengklik iklan (155 pelanggan).
- Marketing cost = 145 customers X Rp 10.000 = Rp 1.450.000
- Conversion rate = 140/145 * 100% = 96,5%
- Revenue = 140 customers X Rp 15.000 = Rp 2.100.000
- Profit = Revenue - Cost = Rp 650.000
Berdasarkan simulasi disamping, besarnya keuntungan sebesar **Rp 650.000** dengan tingkat keuntungan **44,8%**.
## Kesimpulan
Implementasi model machine learning untuk memprediksi klik iklan pelanggan sangat berharga dalam dunia industri, mencegah potensi kerugian dan menghasilkan potensi keuntungan yang lebih tinggi.
