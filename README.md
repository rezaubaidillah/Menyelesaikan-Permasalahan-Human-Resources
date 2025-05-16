# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

### Latar Belakang Bisnis
Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000. Perusahaan ini memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. Walaupun telah menjadi perusahaan yang cukup besar, Jaya Jaya Maju masih menghadapi kesulitan dalam mengelola karyawan. Hal ini berdampak pada tingginya *attrition rate* (rasio jumlah karyawan yang keluar dibandingkan total karyawan keseluruhan) yang mencapai lebih dari 10%. Untuk mencegah situasi ini semakin memburuk, manajer departemen HR meminta bantuan untuk mengidentifikasi berbagai faktor yang mempengaruhi tingginya *attrition rate* tersebut.

### Permasalahan Bisnis
Permasalahan bisnis utama yang akan diselesaikan dalam proyek ini adalah:  
- Mengidentifikasi faktor-faktor utama yang memengaruhi tingginya *attrition rate* di Jaya Jaya Maju.

### Cakupan Proyek
Proyek ini mencakup:  
- Melakukan analisis data untuk memahami pola dan tren yang berkaitan dengan *attrition*.  
- Membangun model *machine learning* untuk menentukan fitur-fitur penting yang dapat membantu mencegah *attrition* karyawan.

### Persiapan
- **Sumber Data**: Data karyawan diperoleh dari [repositori GitHub Dicoding](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee).  Dataset ini adalah Dataset Karyawan Jaya Jaya Maju sesuai dengan instruksi dari submission proyek ini.
- **Setup Environment**:  
  - Menjalankan `notebook.ipynb`
   - Pastikan dependensi, packages, library yang dibutuhkan sudah tersedia (lihat file `requirements.txt` untuk melihat dependensi yang dibutuhkan).
   - Jalankan seluruh isi file `notebook.ipynb` menggunakan Google Colab/Jupyter Notebook untuk melihat hasil analisis data, temuan, dan insight yang diperoleh.
  - **Menjalankan Dashboard**:
   Untuk melihat isi dashboard secara langsung, dapat menggunakan **metabase** dengan bantuan Docker (pastikan Docker sudah terinstall).
   - Jalankan perintah berikut:
      ```
      docker pull metabase/metabase:v0.46.4
      ```
   - Jalankan container Metabase menggunakan perintah:
      ```
      docker run -p 3000:3000 --name metabase metabase/metabase
      ```
   - Login ke Metabase menggunakan username dan password berikut:
      ```
      username: root@mail.com
      password: root123
      ```
## Business Dashboard
Hasil analisis data divisualisasikan dalam bentuk *dashboard* untuk membantu tim HR memantau dan memahami *attrition*. Elemen-elemen yang disertakan dalam *dashboard* meliputi:  
- Rasio *attrition*.  
- Jumlah total karyawan yang tidak keluar dan yang keluar.  
- **Koefisien Negatif** (menunjukkan fitur yang mengurangi kemungkinan *attrition*):  
  - *JobLevel*: -0.74  
  - *EnvironmentSatisfaction*: -0.65  
  - *StockOptionLevel*: -0.64  
  - Semakin besar nilai absolutnya, semakin kuat efeknya dalam mencegah *attrition*.  
- **Koefisien Positif** (menunjukkan fitur yang meningkatkan kemungkinan *attrition*):  
  - *OverTime*: 1.27  
  - *YearsSinceLastPromotion*: 0.55  
  - *YearsAtCompany*: 0.52  
  - Semakin besar nilainya, semakin kuat pengaruhnya terhadap *attrition*.  
- Visualisasi *attrition* berdasarkan *OverTime*, *JobLevel*, *EnvironmentSatisfaction*, dan *StockOptionLevel*.  

## Conclusion
Berdasarkan analisis yang dilakukan, fitur-fitur seperti *OverTime*, *JobLevel*, *EnvironmentSatisfaction*, dan *StockOptionLevel* memiliki pengaruh yang signifikan terhadap keputusan karyawan untuk keluar dari perusahaan. Fitur dengan koefisien positif seperti *OverTime* meningkatkan risiko *attrition*, sedangkan fitur dengan koefisien negatif seperti *JobLevel* dan *EnvironmentSatisfaction* dapat membantu mengurangi risiko tersebut.

### Rekomendasi Action Items
Berikut adalah beberapa rekomendasi tindakan yang dapat dilakukan perusahaan untuk mengurangi *attrition rate*:  
- **Action Item 1**: Mengurangi beban kerja lembur (*OverTime*) dengan mengatur jadwal kerja yang lebih seimbang atau menambah tenaga kerja.  
- **Action Item 2**: Meningkatkan kepuasan lingkungan kerja (*EnvironmentSatisfaction*) melalui perbaikan fasilitas dan menciptakan suasana kerja yang lebih nyaman.  
- **Action Item 3**: Menawarkan lebih banyak opsi saham (*StockOptionLevel*) kepada karyawan untuk meningkatkan loyalitas mereka terhadap perusahaan.