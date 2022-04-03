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

## 2. DATA MANIPULATION
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

