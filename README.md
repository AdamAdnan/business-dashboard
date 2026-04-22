# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding
Perusahaan Jaya Jaya Maju merupakan perusahaan multinasional dengan lebih dari 1000 karyawan yang tersebar di berbagai wilayah. Seiring dengan pertumbuhan perusahaan, kompleksitas dalam pengelolaan sumber daya manusia juga semakin meningkat.

Dalam kondisi tersebut, perusahaan perlu memiliki sistem dan pendekatan yang efektif dalam mengelola karyawan, termasuk dalam memahami dinamika tenaga kerja serta menjaga stabilitas organisasi. Pemanfaatan data menjadi salah satu pendekatan yang penting untuk membantu perusahaan dalam mengambil keputusan yang lebih tepat dan berbasis bukti.

### Permasalahan Bisnis

Perusahaan Jaya Jaya Maju saat ini menghadapi permasalahan tingginya tingkat attrition karyawan, yang telah melampaui ambang batas normal (>10%). Kondisi ini menunjukkan adanya ketidakstabilan dalam pengelolaan sumber daya manusia yang berpotensi mengganggu keberlangsungan operasional perusahaan.

Tingginya attrition tidak hanya berdampak pada kehilangan tenaga kerja, tetapi juga menimbulkan konsekuensi bisnis yang signifikan, seperti meningkatnya biaya rekrutmen dan pelatihan karyawan baru, menurunnya produktivitas tim akibat proses adaptasi, serta hilangnya pengetahuan dan pengalaman yang telah dimiliki oleh karyawan sebelumnya.

Selain itu, ketidakmampuan perusahaan dalam mengidentifikasi faktor-faktor utama penyebab attrition—baik yang berkaitan dengan kompensasi, beban kerja, jabatan, maupun keseimbangan kerja—dapat menyebabkan permasalahan ini terus berulang tanpa solusi yang tepat.

Apabila kondisi ini tidak segera ditangani, maka dalam jangka panjang perusahaan berisiko mengalami penurunan kinerja organisasi, meningkatnya turnover secara berkelanjutan, serta melemahnya daya saing perusahaan di industri.

Oleh karena itu, diperlukan analisis berbasis data untuk memahami faktor-faktor penyebab attrition serta merumuskan strategi yang efektif dalam meningkatkan retensi karyawan.

### Cakupan Proyek
Untuk menjawab permasalahan bisnis yang telah diidentifikasi, proyek ini berfokus pada penerapan pendekatan berbasis data melalui analisis dan pemodelan machine learning untuk memahami serta memprediksi attrition karyawan.

Proyek ini mencakup beberapa tahapan utama, yaitu Exploratory Data Analysis (EDA) untuk memahami karakteristik data dan mengidentifikasi pola yang berkaitan dengan attrition, serta pembangunan model klasifikasi untuk memprediksi kemungkinan seorang karyawan akan keluar dari perusahaan. Dalam proses pemodelan, digunakan Logistic Regression sebagai model baseline yang mudah diinterpretasikan dan Random Forest sebagai model utama yang mampu menangani kompleksitas data serta memberikan informasi mengenai pentingnya fitur.

Selain itu, proyek ini juga mencakup pembuatan dashboard visualisasi data yang digunakan untuk menyajikan insight secara interaktif dan membantu pihak manajemen dalam memahami faktor-faktor yang mempengaruhi attrition. Dashboard ini berfungsi sebagai alat pendukung pengambilan keputusan berbasis data.

Sebagai output akhir, proyek ini menghasilkan:

- Model machine learning untuk memprediksi attrition karyawan
- Dashboard visualisasi data untuk analisis faktor-faktor attrition
- Script prediksi yang dapat digunakan untuk melakukan evaluasi terhadap data karyawan baru

Adapun batasan dalam proyek ini meliputi penggunaan data historis karyawan yang tersedia tanpa mempertimbangkan faktor eksternal di luar dataset, serta model yang dibangun difokuskan pada prediksi attrition tanpa membahas strategi implementasi sistem secara real-time.

Dalam pelaksanaannya, proyek ini menggunakan beberapa resource dan tools, antara lain:

- Data karyawan perusahaan Jaya Jaya Maju
- Bahasa pemrograman Python sebagai tool utama
- Library pendukung untuk pengolahan data, visualisasi, serta pembangunan model klasifikasi

### Persiapan

Sumber data: [Jaya Jaya Maju](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee)

#### Struktur Folder
```
employee-attrition-analytics/
│
├── model.pkl
├── features.pkl
├── notebook.ipynb
├── prediction.py
├── README.md
├── insight_dt_dicoding-dashboard.jpg
├── insight_dt_dicoding-video
├── metabase.db.mv.db
└── requirements.txt
```
#### Setup Environment - Anaconda
```
conda create --name employee-dashboard python=3.12
conda activate employee-dashboard
D: 
cd employee-attrition-analytics
pip install -r requirements.txt
```
#### Cara Menjalankan Script Python (.py)
1. Pastikan sudah membuat dan mengaktifkan environment terlebih dahulu menggunakan perintah diatas
2. Kemudian masuk ke Folder Project
   ```
   D:
   cd employee-attrition-analytics
   ```
4. Jalankan Script
   ```
   python prediction.py
   ```
6. Contoh Input:
```
Umur: 25
Gaji Bulanan: 3000
Jarak dari Rumah: 15
Total Working Years: 3
Years at Company: 1
Jumlah Perusahaan Sebelumnya: 1
Overtime (yes/no): yes
Department (sales/hr/rnd): sales
```
## Business Dashboard

Dashboard ini dikembangkan untuk membantu perusahaan dalam memahami faktor-faktor yang mempengaruhi attrition karyawan secara visual dan interaktif. Dashboard menyajikan berbagai metrik utama serta analisis berdasarkan beberapa dimensi penting yang telah diidentifikasi melalui proses Exploratory Data Analysis (EDA) dan pemodelan machine learning.

Pada bagian atas dashboard ditampilkan Key Performance Indicators (KPI) yang memberikan gambaran umum mengenai kondisi perusahaan, seperti tingkat attrition, total karyawan, dan jumlah karyawan yang keluar. Informasi ini berfungsi sebagai indikator awal untuk menilai tingkat permasalahan yang dihadapi.

Selanjutnya, dashboard menampilkan beberapa visualisasi utama yang berfokus pada faktor-faktor yang terbukti berpengaruh terhadap attrition, antara lain:
- Attrition berdasarkan overtime untuk melihat pengaruh beban kerja
- Attrition berdasarkan tingkat pendapatan untuk memahami peran kompensasi
- Attrition berdasarkan masa kerja untuk mengidentifikasi fase kritis karyawan
- Attrition berdasarkan job level untuk melihat perbedaan risiko antar level jabatan
- Attrition berdasarkan departemen dan job role untuk mengetahui area dengan risiko tertinggi
- Attrition berdasarkan usia dan work-life balance untuk memahami faktor demografis dan kesejahteraan karyawan

Visualisasi yang ditampilkan pada dashboard telah disesuaikan dengan hasil analisis pada notebook, sehingga setiap grafik memiliki keterkaitan langsung dengan kesimpulan yang diambil.

Dengan adanya dashboard ini, pihak manajemen dapat dengan mudah mengidentifikasi kelompok karyawan yang berisiko tinggi mengalami attrition serta memahami faktor-faktor penyebabnya. Hal ini memungkinkan perusahaan untuk mengambil keputusan yang lebih tepat dan berbasis data dalam upaya meningkatkan retensi karyawan.

### Akses Dashboard Metabase
Dashboard pada proyek ini dibuat menggunakan Metabase dan dapat diakses secara lokal menggunakan file database yang telah disertakan.

#### Informasi Akses
- **Metabase Version**: 0.59.5.1
- **Database File**: `metabase.db.mv.db`
- **Username**: adnan100701@gmail.com
- **Password**: Adam070103

#### Cara Menjalankan
1. Pastikan Docker sudah terinstall pada perangkat Anda.
2. Jalankan Metabase menggunakan perintah berikut:
   ```
   docker run -d -p 3000:3000 -v D:\employee-attrition-analytics:/metabase.db --name metabase metabase/metabase
   ```
4. Buka browser dan akses:
   ```
   http://localhost:3000
   ```
5. Login menggunakan username dan password yang telah disediakan.
6. Setelah berhasil masuk, pada halaman utama pilih menu **Our analytics**.
7. Masuk ke dalam koleksi tersebut, lalu scroll ke bawah hingga menemukan dashboard bernama **HR Attrition Analytics Dashboard**.
8. Klik pada dashboard tersebut.
9. Setelah itu, dashboard akan terbuka dan menampilkan seluruh visualisasi analisis HR Attrition.


## Conclusion

Berdasarkan hasil analisis data melalui Exploratory Data Analysis (EDA) dan pemodelan menggunakan Random Forest, dapat disimpulkan bahwa attrition karyawan dipengaruhi oleh kombinasi faktor kompensasi, beban kerja, serta pengalaman kerja.

Faktor utama yang terbukti paling berpengaruh meliputi pendapatan (MonthlyIncome), overtime, usia, serta masa kerja (YearsAtCompany dan TotalWorkingYears). Karyawan dengan usia lebih muda, masa kerja yang lebih pendek, pendapatan rendah, serta beban kerja tinggi cenderung memiliki risiko attrition yang lebih tinggi.

Selain itu, faktor tambahan seperti jarak tempat tinggal dan struktur pendapatan juga turut berkontribusi dalam meningkatkan kemungkinan karyawan keluar. Temuan ini menunjukkan bahwa attrition tidak disebabkan oleh satu faktor tunggal, melainkan oleh kombinasi berbagai aspek yang berkaitan dengan kondisi kerja dan karakteristik karyawan.

Dengan demikian, pendekatan berbasis data yang menggabungkan analisis dan model prediktif dapat membantu perusahaan dalam mengidentifikasi risiko attrition secara lebih akurat serta mendukung pengambilan keputusan strategis dalam pengelolaan sumber daya manusia.

### Rekomendasi Action Items 

Berikut adalah rekomendasi tindakan yang perlu dilakukan perusahaan untuk mengatasi permasalahan yang ada.

- Evaluasi Beban Kerja dan Kebijakan Overtime
  
  Perusahaan perlu mengevaluasi kebijakan jam kerja lembur, karena karyawan yang sering melakukan overtime memiliki risiko attrition yang jauh lebih tinggi. Pengaturan beban kerja yang lebih seimbang serta monitoring intensitas lembur dapat membantu mengurangi tekanan kerja dan meningkatkan retensi karyawan.
- Perkuat Strategi Retensi untuk Karyawan Baru dan Level Awal

  Perusahaan disarankan untuk memperkuat program onboarding dan engagement pada karyawan dengan masa kerja awal serta level jabatan rendah, karena kelompok ini memiliki risiko attrition paling tinggi. Program mentoring, pengembangan karier, serta evaluasi kompensasi awal dapat membantu meningkatkan loyalitas dan keterikatan karyawan.
