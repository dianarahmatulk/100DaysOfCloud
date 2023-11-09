# Modul 4 - Keamanan AWS Cloud

## Daftar Isi

- model tanggung jawab bersama AWS
- AWS Identity and access management (IAM)
- Mengamankan akun AWS baru
- Mengamankan Akun
- Mengamankan data di AWS
- Berupaya memastikan kepatuhan

## Bagian 1 - Model tanggung jawab bersama AWS

Model tanggung jawab bersama ini dirancang untuk membantu meringankan beban operasional pengguna. Namun pelanggan juga tetap bertanggung jawab untuk beberapa aspek keamanan secara keseluruhan. Nah mari pelajari perbedaan siapa yang bertanggung jawab atas apa yang sering disebut sebagai "keamanan dari cloud" vs "keamanan di cloud"

AWS mengoprasikan, mengontrol dan mengelola komponen dari virtualisasi perangkat lunak ke keamanan fisik. **AWS bertanggung jawab** melindungi infrastruktur yang menjalankan semua layanan yang ditawarkan di cloud.

**Pengguna bertanggung jawab** atas enkripsi data saat istirahat dan data dalam transit, memastikan bahwa jaringan dikonfigurasi untuk keamanan dan kredensial keamanan dan login deelola dengan aman. selain itu **Pengguna bertangggung jawab** atas konfigurasi grub keamanan, sistem operasi yang berjalan pada instans.

**Tanggung jawab AWS: Keamanan dari cloud**

Setelah mmebaca hal diatas kita bisa menyimpulkan jika AWS juga berperan untuk menjaga keamanan, hal ini merupakan tanggung jawab dari AWS sendiri. AWS bertanggung jawab melindungi infrastruktur global yang menjalankan semua layanan yang ditawarkan di AWS Cloud. Infrastruktur global ini termasuk Wilayah AWS, Availability Zone, dan edge location. Berikut yang termasuk dlam tanggung jawab atas keamanan dari cloud:

- Keamanan fisik pusat data
- Infrastuktur perangkat keras
- Infratruktur perangkat lunak
- infrastuktur jaringan.

**Tanggung jawab Pengguna: Keamanan di cloud**

meskipun Infrastuktur cloud sudah dijamin dan dikelola oleh AWS, pengguna juga bertanggung jawab untuk keamanan semua yang mereka masukkan ke dalam cloud. Pengguna bertanggung jawab atas apa yang dilaksanankan dengan menggunakan layanan AWS san untuk aplikasi yang terhubung ke AWS. Ketika pelanggan menggunakan layanan AWS, mereka tetap memiliki kontrol penuh atas konten mereka. pelanggan bertanggung jawab mengelola persyaratan keamanan konten sensitif, termasuk:

- Konten yang pelanggan pilih untuk disimpan di AWS
- Layanan AWS yang digunakan bersama konten
- Dinegara mana konten tersebut disimpan
- Format dan struktur dari konten tersebut
- Pelanggan yang memiliki akses ke konten tersebut. 

**Karakteristik Layanan dan tanggung jawab keamanan**

- Infrastructure as a service (IaaS)
- Platform as a service (PaaS)
- Software as a service (SaaS)
    - AWS Trusted Advisor
    - AWS Shield
    - Amazon Chime
      
## Bagian 2 - AWS Identity dan Access Management (IAM)

IAM adalah alat yang secara terpusat mengelola akses untuk meluncurkan, mengkonfigurasi, mengelola serta mengakhiri sumber daya akun AWS anda. Memungkinkan anda untuk mengontrol akses ke komputasi, penyimpanan, basis data dan layanan aplikasi di AWS Cloud. IAM sendiri digunakan untuk mengelola sumber daya yang dapat diakses oleh siapa dan bagaimana sumber daya ini dapat diakses.

**IAM merupakan komponen penting**

untuk memahami cara menggunakan IAM sebagai alat keamanan akun AWS, penting untuk memahami peran dan fungsi dari masing masing dari empat komponen IAM berikut:

- pengguna IAM: Orang atau aplikasi yang ditentukan dalam akun AWS dan harus membuat panggilan API ke produk.

- Grub IAM: Merupakan kumpulan pengguna IAM, kita dapat menggunakan grub IAM untuk menyederhanakan penentuan dan pengelolaan izin untuk beberapa pengguna.
  
- Kebijakan IAM: Berisi dokumen yang menetapkan izin untuk menentukan apa yang dapat dilakukan pengguna di akun AWS.
  
- IAM role: Alat yang digunakan sebagai akses sementara ke sumber daya AWS tertentu dalam akun AWS.

**Autentikasi sebagai pengguna IAM untuk mendapat akses**
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/d998440d-8f2a-4020-8adc-04c3a1c883c5)

Autentikasi merupakan konsep keamanan komputer dasar yang berarti pengguna harus membuktikan identitas mereka. Untuk menentukan pengguna IAM, kita bisa memilih jenis akses apa yang diizinkan bagi pengguna untuk mengakses sumber daya AWS. Kita bisa menetapkan dua jenis akses kepada pengguna yaitu:

- Akses Program: pengguna akan diminta untuk menunjukkan access key ID dan secret access key, ketika mereka melakukan panggilan API AWS dengan memnggunakan AWS CLI, AWS SDK, atau beberapa alat pengembangan lainya.
  
- AWS Manangement console: pengguna IAM akan diminta untuk mengisi bidang yang muncul di jendela masuk browser. pengguna akan dimintai 12 digit ID. Pengguna juga harus memasukkan nama pengguna dan kata sandi IAM. Mereka juga dimintai kode autentikasi.

**IAM MFA**

MFA memeberikan keamanan tingkat lanjut, dengan MFA Pengguna dan system harus memberikan token MFA. Pilihan untuk membuat token autentikasi MFA mencakup aplikasi yang kompatible dengan MFA Virtual.

**Otoritasi: Tindakan yang diizinkan**

Otoritasi merupakan proses menentukan izin yang harus diberikan untuk pengguna, layanan maupn aplikasi. Untuk menetapkan izin kepada pengguna, grub, atau peran. pengguna harus membuat kebijakan IAM arena tidak ada izin default. Prinsip **hak istimewa terendah** adalah konsep penting dalam keamanan komputer. ini akan memberikan hak istimewa pengguna minimal yang diperlukan untuk pengguna, berdasarkan kebutuhan pengguna nantinya. 

**Kebijakan IAM**

Kebijakan IAM adalah pernyataan resmi izin yang akan diberkan kepada entitas. kebijakan dapat dilampirkan ke setiap Pengguna, grub, peran, atau sumber daya. kita dapat melampirka kebijakan untuk sumber daya AWS uang akan memblokir semua permintaan yang tidak berasal dari kisaran alamat internet protocol(IP) disetujui.
Terdapat dua jenis kebijakan IAM 
1. Kebijakan berbasis identitas: kebijakan ijin yang dapat kita lampirkan pada pelaku atau identitas, seperti pengguna peran, atau grup IAM. kebijakan ini dikategorikan lebih lanjut sebagai:
   - kebijakan terkelola
   - kebijakan inline 
3. Kebijakan berbasis sumber daya: merupakan kebijakan JSON yang kita lampirkan pada sumber daya, sepert bucket amazon S3.

## Bagian 3 - Mengamankan akun AWS baru

**Akses pengguna root akun AWS versus akses IAM**

Ketika kita membuat akun AWS, kita pasti memulai dengan identitas masuk tunggal yang memiliki akses lengkap ke semua layanan dan sumber daya AWS di akun tersebut. Identitas yang kita buat ini disebut sebagai **pengguna root akun AWS** pengguna root akun AWS ini memiliki kendali penuh atas segala sumber daya di akun. oeh karena itu pengguna root ini tidak boleh dipakai untuk interaksi sehari-hari
Maka disini AWS merekomendasikan agar kita menggunakan IAM untuk membuat user tambahan, kita bisa membuat pengguna sesuai dengan apa yang kita telah berikan. kita bisa membuat grub administratif yang nantiya akan berisi hal-hal yang dapat diakukan user tersebut. 

**Mengamankan akun AWS baru**
ada banyak macam yang perlu kita amankan di dalam AWS, beberapa hal itu akan dijelaskan dibawah ini:
1. Pengguna root akun
   Berikut cara untuk mengamankan akun pengguna root adalah. behenti menggunakan root sesegera mungkin, cara berhenti menggunakan root sebagai berikut;
       - login dengan root, buatlah pengguna IAM untuk kita sendiri, simpan access key.
       - buat grup IAM, Beri izin administrator penuh, tambahkan pengguna IAM ke grub.
       - nonaktifkan dan hapus access key pengguna root akun, jika ada.
       - aktifkan sandi untuk pengguna.
       - masuk dengan kredensial pengguna IAM yang telah anda buat.
       - simpan kredensial pengguna root akun anda ditempat yang aman.
   
2. MFA
   Mengaktifkan otentikasi multifaktor (MFA), Memerlukan MFA untuk semua pengguna IAM, kita juga dapa menggunakan MFA untuk mengontrol akes ke API layanan AWS. berikut adalah pilihan API untuk mengambil token MFA:
    - Aplikasi yang kompaible dengan MFA virtual:
      - Google Authenticator
      - Aunty Authenticator (Aplikasi Windows Phone)
    - Perangkat kunci keamanan U2F
      - Yubikey
    - Opsi MFA perangkat keras
      - key fob oleh Gemalto
        
3. AWS CloudTrail
   Gunakan AWS CloudTrail untuk melacak aktivitas pengguna di akun anda, Berikut ini cara untuk mengakses CloudTrail:
       - masuk ke AWS manangement console dan pilih layanan CloudTrail
       - klik riwayat peristiwa.
   
4. Laporan tagihan
   laporan tagihan ini seperi laporan penggunaan dan Biaya pada AWS, Laporan tagihan memberikan informasi tentang penggunaan sumber daya AWS dan perkiraan biaya untuk pengguna itu. 


## Bagian 4 - Mengamankan data di AWS
**Enkripsi data saat istirahat**

Enkripsi data adalah alat penting untuk digunakan ketika tujuan Anda untuk melindungi data digital. Enkripsi data mengambil data yang dapat dibaca dan mengodekannya sehingga tidak dapat dibaca oleh siapa pun yang tidak memiliki akses ke kunci rahasia yang dapat digunakan untuk memecahkan kode itu. Data saat istirahat mengacu pada data yang tersimpan secara fisik pada disk atau pita.

**Enkripsi data dalam transit**

Data dalam transit mengacu pada data yang bergerak di seluruh jaringan. Enkripsi data dalam transit dilakukan dengan menggunakan Transport Layer Security (TLS) 1.2 dengan cipher AES-256 standar terbuka. 

**Mengamankan bucket dan objek amazon S3**

Secara default, semua bucket Amazon S3 bersifat pribadi dan dapat diakses hanyaoleh pengguna yang secara eksplisit diberikan akses. 
AWS menyediakan banyak alat dan pilihan untuk mengendalikan akses ke bucket S3 atau objek, termasuk:
- Menggunakan Blokir Akses Publik Amazon S3. Pengaturan ini menimpa kebijakan lain atau izin objek. Aktifkan Blokir Akses Publik untuk semua bucket yang tidak ingin diakses publik.
  
- Penulisan kebijakan IAM yang menentukan pengguna atau peran yang dapat mengakses bucket dan objek tertentu.
  
- Penulisan kebijakan bucketyang menentukan akses ke bucket atau objek tertentu.  Opsi ini biasanya digunakan ketika pengguna atau sistem tidak dapat mengautentikasi menggunakan IAM. 

## Bagian 5 - Bekerja untuk memastikan kepatuhan
**Program kepatuhan AWS**

AWS juga menyediakan fitur keamanan dan perjanjian hukum yang dirancang untuk membantu mendukung pelanggan dengan peraturan umum dan hukum. Salah satu contohnya adalah peraturan Health Insurance Portability and Accountability Act (HIPAA). AWS terlibat dengan badan penyertifikasi eksternal dan auditor independen untuk memberi pelanggan informasi yang memadai tentang kebijakan, proses, dan kontrol yang ditetapkan dan dioperasikan oleh AWS.

**AWS Config**

AWS Config adalah layanan yang memungkinkan Anda mengakses, mengaudit, dan mengevaluasi konfigurasi sumber daya AWS Anda. AWS Config terus memantau dan mencatat konfigurasi sumber daya AWS Anda dan memungkinkan Anda mengautomasi evaluasi konfigurasi tercatat terhadap konfigurasi yang diinginkan.

**AWS Artifact**

AWS Artifact menyediakan pengunduhan dokumen keamanan dan kepatuhan AWS sesuai permintaan, seperti sertifikasi ISO AWS, Payment Card Industry (PCI), dan laporan Service Organization Control (SOC). Anda dapat mengirimkan dokumen keamanan dan kepatuhan (juga dikenal sebagaiartefak audit) kepada auditor atau regulator Anda untuk menunjukkan keamanan dan kepatuhan infrastruktur dan layanan AWS yang Anda gunakan. 

## Bagian 6 - Layanan keamanan dan sumber daya tambahan
**AWS Service catalog**

AWS Service Catalog memungkinkan organisasi membuat dan mengelola katalog layanan IT yang disetujui untuk digunakan (misalnya, bagi karyawan Anda untuk menggunakan) pada AWS. Hal ini memungkinkan pengguna Anda dengan cepat men-deploy layanan IT yang mereka butuhkan, dan dirancang agar pengguna hanya men-deploy konfigurasi yang disetujui. AWS Service Catalog dapat mendukung upaya Anda untuk mengelola layanan IT yang di-deploy, dan dapat membantu Anda mencapai tata kelola yang konsisten dan memenuhi persyaratan kepatuhan.

**layanan keamanan tambahan yang dipilih**

**Amazon Macie** adalah layanan keamanan yang menggunakan machine learning untuk secara otomatis menemukan, mengklasifikasikan, dan melindungi data sensitif di AWS. 
**Amazon Inspector** adalah layanan penilaian keamanan otomatis yang membantu memperbaiki keamanan dan kepatuhan aplikasi yang di-deploy di AWS. Amazon Inspector secara otomatis menilai aplikasi untuk eksposur, kerentanan, dan penyimpangan dari praktik terbaik. 
**Amazon GuardDutymerupakan** layanan deteksi ancaman yang secara berkelanjutan memantau aktivitas mencurigakan dan perilaku tidak bertanggung jawab untuk melindungi akun dan beban kerja AWS Anda.

[g ada](link)
