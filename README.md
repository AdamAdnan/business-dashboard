# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding
Perusahaan Jaya Jaya Maju adalah perusahaan multinasional dengan lebih dari 1000 karyawan yang tersebar di berbagai wilayah. Seiring pertumbuhan perusahaan, kompleksitas dalam pengelolaan sumber daya manusia juga meningkat.
Salah satu masalah utama yang dihadapi adalah tingginya tingkat attrition rate, yaitu rasio karyawan yang keluar dibandingkan total karyawan. Tingkat attrition yang melebihi 10% menunjukkan adanya potensi masalah serius dalam:
- Kepuasan kerja
- lingkungan kerja
- kompensasi
- maupun faktor manajerial lainnya.
  
Jika tidak ditangani, kondisi ini akan dapat berdampak pada:
- meningkatnya biaya rekrutmen dan pelatihan,
- menurunnya produktivitas tim
- hilangnya knowledge dan pengalaman karyawan.
  
Oleh karena itu, perusahaan membutuhkan pendekatan berbasis data untuk memahami penyebab utama attrition dan mengambil keputusan strategis.
### Permasalahan Bisnis

Berdasarkan kondisi tersebut
1. Faktor apa saja yang paling berpengaruh terhadap attrition karyawan?
2. Apakah faktor seperti gaji, lama bekerja, jabatan, atau work-life balance mempengaruhi keputusan karyawan untuk keluar?
3. Bagaimana karakteristik karyawan yang cenderung resign?
4. Apakah terdapat pola tertentu berdasarkan departemen, usia, atau lokasi kerja?

### Cakupan Proyek

Untuk menjawab permasalahan bisnis tersebut, proyek ini berfokus pada penerapan pendekatan classification untuk memprediksi attrition karyawan berdasarkan data yang tersedia. Dalam proses pengembangannya, digunakan dua metode utama, yaitu Logistic Regression sebagai model baseline yang mudah diinterpretasikan serta Random Forest sebagai model utama yang mampu menangani data kompleks dan memberikan informasi terkait pentingnya fitur.

Selain itu, proyek ini juga mencakup proses Exploratory Data Analysis (EDA) untuk memahami karakteristik data serta mengidentifikasi pola dan faktor-faktor yang berpengaruh terhadap attrition. Hasil dari analisis ini diharapkan dapat memberikan insight yang mendalam sekaligus mendukung proses pengambilan keputusan berbasis data.

Berdasarkan cakupan proyek tersebut, dibutuhkan beberapa resource dan tools berikut:
- Data karyawan perusahaan Jaya Jaya Maju
- Bahasa pemrograman Python sebagai tool utama dalam proyek ini
- Berbagai library pendukung untuk pengolahan data, visualisasi, serta pembangunan dan evaluasi model klasifikasi
### Persiapan

Sumber data: [Jaya Jaya Maju](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee)

Setup environment:

```
conda create --name bike-dashboard python=3.12
conda activate bike-dashboard
# Berali ke drive D tempat project disimpan
D:
cd bike-sharing-main
pip install -r requirements.txt
```

## Business Dashboard

Dashboard HR Attrition Analytics ini bertujuan untuk menganalisis tingkat attrition (karyawan keluar) di perusahaan serta mengidentifikasi faktor-faktor yang paling mempengaruhinya.

Dari total 1,058 karyawan, terdapat 179 karyawan yang keluar, dengan attrition rate sebesar ±17%. Angka ini menunjukkan bahwa perusahaan memiliki tingkat turnover yang cukup signifikan dan perlu perhatian khusus.

Analisis dilakukan dari berbagai perspektif, yaitu:

- Departemen → untuk melihat unit kerja dengan attrition tertinggi
- OverTime → untuk melihat pengaruh lembur terhadap keputusan resign
- Job Role & Job Level → untuk melihat posisi yang paling rentan
- Years at Company → untuk melihat fase kritis karyawan keluar
- Monthly Income → untuk melihat pengaruh kompensasi
- Age & Gender → untuk melihat karakteristik demografis
- Work-Life Balance → untuk melihat keseimbangan kerja dan dampaknya

## Conclusion

Berdasarkan hasil analisis dashboard, dapat disimpulkan bahwa attrition di perusahaan tidak terjadi secara acak, tetapi dipengaruhi oleh beberapa faktor utama.

Faktor yang paling berpengaruh terhadap attrition adalah:

- OverTime (lembur) → karyawan yang sering lembur cenderung lebih tinggi tingkat keluar
- Monthly Income → karyawan dengan pendapatan lebih rendah memiliki kecenderungan resign lebih besar
- Job Level & Job Role → posisi entry-level dan beberapa role tertentu lebih rentan
- Years at Company → tahun-tahun awal masa kerja merupakan periode paling kritis
- Work-Life Balance → keseimbangan kerja yang buruk meningkatkan risiko resign

Secara keseluruhan, attrition perusahaan lebih banyak dipengaruhi oleh kombinasi faktor beban kerja, kompensasi, dan pengalaman kerja awal, bukan hanya satu faktor tunggal.

### Rekomendasi Action Items 

Berikut adalah rekomendasi tindakan yang perlu dilakukan perusahaan untuk mengatasi permasalahan yang ada.

- Perusahaan perlu mengevaluasi kebijakan jam kerja lembur, karena karyawan yang sering melakukan overtime menunjukkan tingkat attrition yang lebih tinggi.
- Selain itu, tingkat attrition paling tinggi terjadi pada masa awal masa kerja, sehingga proses onboarding serta strategi engagement pada periode awal menjadi faktor yang sangat penting untuk ditingkatkan.
