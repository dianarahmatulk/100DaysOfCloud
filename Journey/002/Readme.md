**Modul 2 dan Modul 3:**
# Modul 2 - Ekonomi dan pembayaran cloud

## Bagian 1 - Dasar-dasar Harga

**A. Pendorong dasar**

  pada AWS tersedia berbagai komputasi yang tentunya tidak gratis kan, ketika kita telah menggunakan sebuah instance kita perlu juga mengeluarkan uang untuk hal tersebut. Nah untuk sistem pembayaran dalam AWS inipun cukup beragam, jadi terdapat 3 model pembayaran dengan mengacu pada 3 pendorong dasar yaitu:

**- Komputasi**
  Jika kita menggunakan Komputasi sebagai pendorong kita akan membayar biaya perjam/detik sesuai dengan instance yang kita pakai.
  
**- Penyimpanan**
  lain dengan Komputasi untuk model penyimpanan ini AWS akan menghiung biaya yang anda melalui banyaknya biaya yang anda gunakan, hal ini dihitung per-GB.
  
**- Transfer data**
  Data yang keluar akan diberikan biaya, untuk biaya masuk tidak diberikan biaya (dengan beberapa pengecualian.). untuk pendorong dasar ini kita juga dikenai biaya per-GB.

**B. Cara Pembayaran AWS**

  Setelah memngetahui pendorong dasar dari pembayaran, kita bisa berfikir jika kita akan membayar layanan komputasi sesuai dengan apa yang kita gunakan. metode pembayaran AWS dibagi menjadi 3 juga:
  - Bayar sesuai yang anda gunakan
    
    pengguna bisa membayar layanan yang dikonsumsi/ digunakan oleh pengguna saja, tanpa biaya dimuka yang besar
    
  - Bayar lebih sedikit ketika anda melakukan pemesanan
    
      ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/38717f60-feae-43b8-bd0d-38a65402e24e)

  - bayar lebih sedikit ketika anda lebih banyak seiring berkembangnya AWS
    
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/c2c63182-9319-44bb-ba68-41727e5bb50e)

  - AWS Tingkat Gratis
      AWS juga menyediakan untuk pengguna yang ingin mendapatkan pengalaman menggunkan AWS secara gratis dengan instans mikro amazon EC2 T2 selama 1 tahun. 

    

## Bagian 2 - Total Biaya Kepemilikan
  **On-premise VS Cloud**

  On-premise versus cloud adalah pernyataan bagaimana mereka di-deploy. Infrastucture ini diinstall pada komputer server milik perusahaan. ada biaya yang disebut dengan biaya  modal, yang berkaitan dengan insfrastuctur tradisional. pada Infrastuctur cloud dibeli dari penyedia layanan yang membangun dan memelihara semua fasilitas. pelanggan akan membayar sesuai yang digunakan.

  **Total Biaya Kepemilikan (TCO)**

TCO adalah perkiraan keuangan untuk membantu mengidentifikasikan biaya langsung dan tidak langsung dari suatu sistem.  Jadi mengapa menggunakan TCO? 
    Untuk membandingkan biaya menjalankan seluruh lingkungan infrastuktur atau beban kerja spesifik On-premise versus di AWS. Total biaya kepemilikan adalah Alat yang dapat digunakan untuk membandingkan, TCO meliputi biaya layanan dan biaya terkait kepemilikan layanan. Perbandingan ini dilakukan dengan tujuan untuk membuat anggaran dan membangun kasus bisnis untuk berpindah ke cloud, beberapa management pusat data meliputi:
- biaya server untuk perangkat keras dan perangkatlunak, serta biaya fasilitas untuk menyimpan peralatan.
- Biaya penyimpanan untuk perangkat keras, administrasi, dan fasilitas.
- Biaya jaringan untuk perangkat keras, administrasi, dan fasilitas.
- Selain itu, biaya tenaga kerja IT yang diperlukan untuk mengelola seluruh solusi

  Pertimbangan TCO, Beberapa biaya terkait manajement pusat data meliputi:
biaya server untuk perangkat keras dan perangkat lunak, serta biaya fasilitas untuk menyimpan peralatan.
 
**Dashbor Penagihan AWS**

Dasbor penagihan ini memungkinkan pengguna melihat status pengeluaran AWS bulan ini sampai saat ini. dan mengidentifikasi layanan yang berkontribusi terhadap sebagian besar pengeluaran keseluruhan dan memahami tren biaya dengan baik. 

Dukungan teknis
Menyedikan kombinasi alat dan keahlian yang unik:
- AWS Support
- Paket AWS Support
Dukungan disediakan untuk:
- Bereksperimen dengan AWS
- Pengguna produksi AWS
- Penggunaan AWS untuk bisnis penting
Paduan proaktif
- Manajer akun teknis (MAT)
Praktik terbaik:
- AWS Trusted Advisor
Bantuan Akun:
- AWS Support Concierge

![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/29059bd0-183c-418f-b927-84c48600d678)


# Bagian 3 - AWS Organization
  AWS Organizations adalah layanan manajemen akun yang memungkinkan Anda menggabungkan beberapa akun AWS ke sebuahorganisasiyang Anda buat dan kelola secara terpusat. AWS Organizations meliputi tagihan terkonsolidasi dan kemampuan manajemen akun yang membantu Anda memenuhi anggaran, keamanan, dan kebutuhan kepatuhan bisnis Anda dengan lebih baik.
  
  Manfaat utama AWS Organizations adalah:
  - Mengelola kebijakan akses secara terpusat di beberapa akun AWS.
  - Mengontrol akses ke layanan AWS.
  - Mengautomasi pembuatan dan pengelolaan akun AWS.
  - Tagihan terkonsolidasi di beberapa akun AWS.

  Fitur utama dan manfaat memungkinkan anda untuk membuat service control policies (SCP) untuk mengontrol pengguna layanan AWS di beberapa akun AWS secara terpusat, dapat membuat grup akun dan kemudian melampirkan kebijakan ke dalam gruop untuk memastikan kebijakan yang benar. dan masih banyak yang lainya.
  Keamanan dengan AWS Organizations. tidak menggantikan kebijakan AWS Identity dan Access Management, terkait pengguna, grup dan peran dalam akun AWS.
  Dengan kebijakan IAM, kita dapat mengizinkan atau menolak akses ke layanan AWS. Sebaliknya, di Organization kita perlu menggunakan service Control Policies (SCP) untuk membuat sebuah kebijakan.
 
  **Penyimpanan Organisasi**

  proses ini mengasumsikan bahwa Anda memiliki akses ke dua akun AWS yang ada, dan Anda dapat masuk ke setiap akun sebagai administrator.
  Tinjau langkah-langkah ini untuk menyiapkan AWS Organizations:
  •Langkah 1 adalah membuat organisasi Anda dengan akun AWS Anda saat ini sebagai akun master. Anda juga mengundang satu akun AWS untuk bergabung dengan organisasi Anda dan membuat akun lain sebagai akun anggota.
  •Langkah 2 adalah membuat dua unit organisasi dalam organisasi baru Anda dan menempatkan akun anggota di OU tersebut.
  •Langkah 3 adalah membuat service control policies yang memungkinkan Anda menerapkan batasan tindakan apa yang dapat didelegasikan kepada pengguna dan peran dalam akun anggota. Kebijakan kontrol layanan adalah jenis kebijakan kontrol organisasi.
  •Langkah 4 adalah menguji kebijakan organisasi Anda. Masuk sebagai pengguna untuk masing-masing peran (seperti OU1 atau OU2) dan lihat bagaimana service control policies ini memengaruhi akses akun. Atau, Anda dapat menggunakan simulator kebijakan IAM untuk menguji dan memecahkan masalah IAM dan kebijakan berbasis sumber daya yang melekat pada pengguna, grup, atau IAM role di akun AWS Anda

# Modul 3 - AWS Global Infrastructure
  
  Amazon Web Services (AWS) memiliki infrastruktur global yang sangat luas dan kompleks yang didesain untuk menyediakan layanan cloud kepada pelanggan di seluruh dunia. Infrastruktur global AWS mencakup sejumlah wilayah geografis, zona availabilitas, dan pusat data yang terhubung untuk menyediakan layanan cloud yang andal, cepat, dan aman. Berikut adalah beberapa komponen utama dari infrastruktur global AWS:

**Wilayah (Region):**

AWS terdiri dari beberapa wilayah di seluruh dunia, yang masing-masing adalah lokasi fisik yang terpisah dan independen. Setiap wilayah memiliki beberapa zona availabilitas.
Setiap wilayah dilengkapi dengan pusat data, jaringan, dan infrastruktur yang dikelola secara independen. Ini memungkinkan pelanggan untuk mendekati layanan AWS dari wilayah yang paling cocok dengan lokasi geografis mereka.

**Zona Availabilitas (Availability Zone):**

Setiap wilayah terdiri dari satu atau lebih zona availabilitas, yang adalah lokasi fisik terpisah dengan listrik, pendingin, dan jaringan yang terpisah.
Zona availabilitas adalah elemen penting dalam strategi AWS untuk meningkatkan ketersediaan dan ketahanan. Pelanggan dapat mendistribusikan aplikasi mereka di zona availabilitas yang berbeda untuk menjaga ketersediaan jika ada gangguan pada satu zona.

**Edge Location:**

Edge locations adalah titik distribusi global yang digunakan untuk caching dan menyajikan konten statis, seperti gambar dan video, kepada pengguna akhir.
Mereka terutama terkonsentrasi di seluruh dunia untuk mengurangi latensi dan mempercepat pengiriman konten. Edge locations juga digunakan oleh layanan AWS seperti Amazon CloudFront (Content Delivery Network).

**Global Network Backbone:**

AWS memiliki jaringan global yang sangat cepat dan andal yang menghubungkan seluruh wilayah, zona availabilitas, dan edge location mereka.
Jaringan global AWS membantu dalam mendistribusikan data dengan cepat dan aman, serta memastikan ketersediaan tinggi layanan.

**AWS Direct Connect:**

AWS Direct Connect adalah layanan yang memungkinkan pelanggan untuk menghubungkan jaringan pribadi mereka langsung ke jaringan AWS, sehingga data dapat mengalir langsung antara lokasi pelanggan dan wilayah AWS tanpa melalui internet umum.

**AWS Global Accelerator:**

AWS Global Accelerator adalah layanan yang memungkinkan pelanggan untuk mengalokasikan alamat IP anycast yang dikelola oleh AWS ke aplikasi mereka di berbagai wilayah, sehingga memungkinkan pengalihan lalu lintas global yang sangat cepat dan andal.
Infrastruktur global AWS dirancang untuk memberikan fleksibilitas, ketersediaan, dan kinerja terbaik untuk pelanggan mereka di seluruh dunia. Pelanggan dapat memilih wilayah dan zona availabilitas yang sesuai dengan kebutuhan mereka, dan AWS menyediakan alat dan layanan untuk 
mengelola aplikasi mereka dengan efisien di seluruh infrastruktur global mereka.

![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/5d92f56b-61e6-43ef-91e4-b4a3f4ba259b)


[diambil dari sini](https://chat.openai.com/c/9f3f412a-567c-4403-8772-d528490fa855)
[dan dari sini juga](https://awsacademy.instructure.com/courses/61312/modules/items/5410054)
