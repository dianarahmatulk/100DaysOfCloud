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

Otoritasi merupakan proses menentukan izin yang harus diberikan 

## Bagian 3 - Mengamankan akun AWS baru


## Bagian 4 - Mengamankan data di AWS


## Bagian 5 - Bekerja untuk memastikan kepatuhan


## Bagian 6 - Layanan keamanan dan sumber daya tambahan


## ☁️ Cloud Outcome

✍️ (Result) Describe your personal outcome, and lessons learned.

## Next Steps

✍️ Describe what you think you think you want to do next.

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
