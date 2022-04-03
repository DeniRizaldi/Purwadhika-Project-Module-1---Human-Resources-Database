# Purwadhika-Project-Module-2---Human-Resources-Database

Pada Project ini akan membahas Data Analysis yang bersumber dari SQL Human-Resources, [link] (https://drive.google.com/drive/folders/1G9Q2sohMFVes7NCHaUHcuAAjlOybBYJG).

Secara garis besar, Project ini berisikan :
1. Data Understanding
2. Database
3. Data Manipulation
4. Data Visualization & Statistics

Diberikan juga pertanyaan-pertanyaan pada file _Capstone Project 2 - List Question.pdf_ pertanyaan yang telah dibuat melalui analisis data, membuat cerita dan visualisasi, serta mempresentasikan insight dari analisis.

## 1. DATA UNDERSTANDING
  Berisikan beberapa sub-bab yang dibahas, yaitu
### a. Context :
Prolog dari sebuah Database Human Resource, dan insight yang akan dibahas
### b. Database Information
Sumber-sumber database, tabel database, dan penjelasan singkat mengenai tabel database. Terdapat ERD juga yang memberi tahu hubungan antar tabel di dalam database Human Resource.

## 2. DATABASE
Bagian ini merupakan langkah awal untuk mulai melakukan proses analisis data. 
### a. Connecting to Database
Menggunakan library sqlalchemy dan hanya import create_engine, untuk koneksi ke MySQL
### b. Data Detail
Data ini merupakan gabungan dari 5 tabel, yaitu tabel Countries, Locations, Departments, Employees dan Jobs. Masing-masing dari setiap tabel tersebut diambil beberapa kolomnya dan tidak diambil secara keseluruhan.
Terdapat pula query yang dicantumkan untuk mengambil isi dari database.

## 3. DATA MANIPULATION
Sebelum melakukan analisis lebih lanjut, hal yang harus dilakukan adalah mengecek informasi serta anomali pada data. Pada bagian ini, data akan _dibersihkan_, sehingga output akhir yang diharapkan adalah terdapat sebuah dataset yang bersih yang dapat dianalisis lebih lanjut dengan menampilkan visualisasi, serta melihat statistics-nya.
### a. Data Anomalies
Melihat anomali-anomali pada detail data dari tampilan non-null dan tipe datanya.
### b. Melihat Data Sekilas dari General Info
Ada dua kesimpulan yang diambil, yaitu Kesimpulan pertama adalah bahwa terdapat missing value yang harus ditanggulangi. Kesimpulan keduanya adalah terdapat features yang memiliki tipe data yang salah dan harus diubah sesuai dengan tipe data seharusnya.
### c. Missing Values
Yang paling jadi sorotan adalah COUNTRY_ID dan COUNTRY_NAME yang memiliki total missing value yang lebih dari 30%.
### d. Handling Anomalies
Pertama, ditemukan COUNTRY_ID yang seharusnya _UK_, namun berisi _OX_, dengan penanggulangannya adalah mengganti value dari COUNTRY_ID tersebut.
Kedua, ada 1 missing value yang relatif sama di setiap kolom, dengan penanggulangannya adalah menghapus missing value tersebut.
### e. Recheck Missing Value Information
Memastikan bahwa semua feature tidak ada miising value.
### f. Mengubah Tipe Data yang Salah
Merubah LOCATION_ID, DEPARTMENT_ID, EMPLOYEE_ID dari tipe data float menjadi tipe data integer.
### g. Recheck Data Information
Memastikan tipe data 3 feature diatas sudah berubah ke integer.
### h. Data Duplicate
Melihat data yang duplikat, namun setelah melihat dataframe, tidak ditemukan adanya data duplikat.
### i. Preview Cleaned Data
Memastikan Data sudah bersih
### j. General Info Cleaned Data
Resume dari seluruh data, terkait tipe data, jumlah data, jumlah missing value, persentase missing value, jumlah unik, dan contoh unik.
### k. Salary Berdasarkan Department Name
Grouping Data Department Name berdasarkan Salary. Slicing yang hanya berisikan UK, US, Finance, Purchasing, Sales dan Shipping.
### l. Data Outlier
Melihat Outlier dari data Slicing.

## 4. DATA VISUALIZATION & STATISTICS
Melakukan visualisasi data untuk mendapatkan beberapa insight yang kemudian dapat menjadi landasan dalam pengambilan keputusan.
Menggunakan beberapa library seperti plotly.express, matplotlib.pyplot dan seaborn.
### a. Department dengan rata-rata Salary terbesar
Diurutkan Department name dari yang terbesar sampai yang terkecil berdasarkan rata-rata Salary, yaitu Sales, Finance, Purchasing dan Shipping.
### b. Job Title dengan rata-rata Salary terbesar
Diurutkan Job title dari yang terbesar sampai yang terkecil berdasarkan rata-rata Salary, yaitu Sales Manager, Finance Manager, Purchasing Manager, Sales Representative, Accountant, Stock Manager, Shipping Clerk, Stock Clerk dan Purchasing Clerk.
### c. Perbandingan rata-rata Salary UK dan US
Secara Umum, rata-rata keseluruhan Salary UK lebih besar dibandingkan dengan rata-rata keseluruhan Salary US.
### d. Uji Perbandingan Salary UK & US
Uji Perbandingan rata-rata Salary UK terhadap rata-rata Salary US menggunakan Independent Samples T-Test. Hasil yang didapat adalah Gagal Tolak H0 Karena P-Value (0.5453186935419745 > 5%) karena Data terdistribusi Normal.
