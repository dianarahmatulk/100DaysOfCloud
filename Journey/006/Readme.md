![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/ad921c92-7610-4fcd-a119-73d83e2c6179)

# Modul 5 - Jaringan dan penyampaian konten
Pada modul ini kita akan membahas 3 layanan dasar AWS untuk jaringan dan penyampaian konten.

## Modul ini membahas topik-topik berikut:

- Dasar-dasar jaringan
- Amazon Virtual Private Cloud (Amazon VPC)
- Jaringan VPC
- Keamanan VPC
- Amazon Route 53
- Amazon CloudFront

## Dasar-dasar jaringan

**1. Jaringan**

Jaringan komputer adalah dua mesin klien atau lebih yang terhubung bersama-sama untuk berbagi sumber daya. Sebuah jaringan dapat secara logis dipartisi menjadi subnet. Jaringan memerlukan perangkat jaringan (seperti perute atau switch) untuk menghubungkan semua klien bersama-sama dan memungkinkan komunikasi antar klien.

**2. Alamat IP**

Setiap mesin klien dalam jaringan memiliki alamat Internet Protocol (IP) yang unik yang mengidentifikasinya. Alamat IP adalah label numerik dalam format desimal. Mesin mengonversi angka desimal ke format biner.

Dalam contoh ini, alamat IP adalah 192.0.2.0. Masing-masing dari angka alamat IP yang dipisahkan empat titik (.) mewakili 8 bit dalam format angka oktal. Itu berarti, masing-masing dari empat angka bisa angka berapa pun dari 0 sampai 255. Total gabungan dari empat angka untuk sebuah alamat IP adalah 32 bit dalam format biner.


**3. Alamat IPv4 dan IPv6**

Alamat IPv6 terdiri dari delapan grup empat huruf dan angka yang dipisahkan oleh titik dua (:). Dalam contoh ini, alamat IPv6 adalah 2600:1f18:22ba:8c00:ba86:a05e:a5ba:00FF. Masing-masing dari delapan grup alamat IPv6 yang dipisahkan titik dua mewakili 16 bit dalam format angka heksadesimal. Itu berarti masing-masing dari delapan grup tersebut bisa apa saja dari 0 sampai FFFF. Total gabungan dari delapan grup untuk alamat IPv6 adalah 128 bit dalam format biner.

**4. Classless Inter-Domain Routing (CIDR)**

Bit yang tidak tetap diperbolehkan untuk berubah. CIDR adalah cara untuk mengekspresikan grup alamat IP yang berturut-turut satu sama lain.

Dalam contoh ini, alamat CIDR adalah 192.0.2.0/24. Angka terakhir (24) memberitahu Anda bahwa 24 bit pertama harus ditetapkan. 8 bit terakhir bersifat fleksibel, yang artinya 28(atau 256) alamat IP tersedia untuk jaringan, dengan rentang antara 192.0.2.0 hingga 192.0.2.255 Angka desimal keempat diperbolehkan untuk berubah dari 0 hingga 255.

Jika CIDR adalah 192.0.2.0/16, angka terakhir (16) memberitahu Anda bahwa 16 bit pertama harus ditetapkan. 16 bit terakhir bersifat fleksibel, yang berarti bahwa 216(atau 65.536) alamat IP tersedia untuk jaringan dengan rentang 192.0.0.0 hingga 192.0.255.255. Angka desimal ketiga dan keempat masing-masing dapat berubah dari 0 hingga 255.

**5. Model Open Systems Interconnection (OSI)**

Model Open Systems Interconnection (OSI) adalah model konseptual yang digunakanuntuk menjelaskan bagaimana data melalui jaringan. Model ini terdiri dari tujuh lapis dan menunjukkan protokol umum dan alamat yang digunakan untuk mengirim data pada setiap lapis. Misalnya, hub dan switch bekerja pada lapis 2 (lapis tautan data). Perute bekerja pada lapis 3 (lapis jaringan). Model OSI juga dapat digunakan untuk memahami bagaimana komunikasi berlangsung di virtual private cloud (VPC), yang akan Anda pelajari di bagian berikutnya.

## Amazon Virtual Private Cloud (Amazon VPC)

Amazon Virtual Private Cloud (Amazon VPC) adalah layanan yang memingkinkan anda menyediakan bagian yang terisolasi secara logis dari AWS cloud. VPC ini tempat kita untuk meluncurkan mesin virtual kita. Memberikan kita kontrol atas sumber daya jaringan virtual anda termasuk pilihan rentang alamat IP kita, pembuatan subnet dan konfigurasi table route, dan gateaway jaringan.  

**Hubungan VPC dengan Subnet**

Amazon VPC memungkinkan Anda menyediakan virtual private cloud (VPC). VPC adalah sebuah jaringan virtual yang terisolasi secara logis dari jaringan virtual lainnya di AWS Cloud.Sebuah VPC didedikasikan untuk akun Anda. VPC menjadi bagian dari satu Wilayah AWS dan dapat menjangkau beberapa Availability Zone.

Setelah membuat VPC, Anda dapat membaginya menjadi satu subnet atau lebih. Subnet adalah rentang alamat IP dalam VPC.Subnet menjadi bagian dari satu Availability Zone. Anda dapat membuat subnet di Availability Zone yang berbeda untuk ketersediaan tinggi. Subnet umumnya diklasifikasikan sebagai publik atau privat. Subnet publikmemiliki akses langsung ke internet, tetapi subnet privat tidak.

**Pemberian Alamat IP**
Alamat IP digunakan untuk berkomunikasi satu sama lain dengan sumber daya internet. ketika kita membuat VPC, Kita harus menetapkan blok CIDR IPv4 untuk VPC kita. kita dapat mengaitkan blok CIDR IPv6 dengan VPC dan subnet dan juga menetapkan alamat IPv6 dari block tersebut ke sumber daya dalam VPC kita. 
Saat kita membuat subnet kita memerlukan block CIDR-nya sendiri, untuk setiap blok CIDR yang kita tentukan AWS akan mencadangkan 6 alamat IP dalam block tersebut. AWS mencadangkan alamat IP ini untuk: 

- Alamat jaringan
- Perute local VPC (komunikasi internal)
- Resolusi DNS
- Penggunaan di masa mendatang
- Alamat siaran jaringan 

Setiap kita membuat VPC, maka pada masing-masing instans di VPC tersebut mendapatkan alamat IP pribadi secara otomatis. kita juga bisa meminta alamat IP publik untuk diterapkan saat membuat instans dengan mengubah alamat IP publik otomatis subnet.
maka alamat IP dibagi menjadi beberapa jenis yaitu. 

 - Alamat IPv4 Publik
     - Ditetapkan secara manual melalui alamat IP Elastis
     - Ditetapkan secara otomatis melalui pengaturan penetapan alamat IP Publik otomatis di              tingkat subnet.
 - Alamat IP Elastis
     - berkaitan dengan akun AWS
     - Dapat dialokasikan dan di petakan ulang kapan saja
     - biaya tambahan mungkin berlaku.

   untuk bagian IP kita juga akan bekenalan dengan antarmuka jaringan elastis, **Antarmuka Jaringan Elastis** adalah sebuah antarmuka jaringan virtual yang dapat kita lampirkan atau lepaskan dari instans dalam VPC.
   Lanjut kita berkenalan dengan Table route yang merupakan sekumpulan aturan(disebut rute) yang mengarahkan lalu lintas jaringan dari subnet kita, setiap route akan menetukantujuan target.
    
## Jaringan VPC
Jaringan VPC ini berisikan

## Keamanan VPC
Grup keamanan bertindak sebagai firewall virtual bagi instans, serta mengontrol lalu lintas masuk dan keluar.Grup keamanan bertindak pada tingkat instans, bukan tingkat subnet. Oleh karena itu, setiap instans di subnet di VPC Anda dapat ditetapkan ke rangkaian grup keamanan yang berbeda. 

Grup keamanan memiliki aturanyang mengontrol lalu lintas masuk dan keluar. Saat Anda membuat grup keamanan, grup tersebut tidak memiliki aturan masuk. Oleh karena itu, tidak ada lalu lintas masuk yang berasal dari host lainnya ke instans Anda yang diizinkan, hingga Anda menambahkan aturan masuk ke grup keamanan. Grup Keamanan default menolak semua lalu lintas masuk dan mengizinkan semua lalu lintas keluar. Grup keamanan bersifat stateful yang berarti bahwa informasi status disimpan bahkan setelah permintaan diproses.

Access control list jaringan (ACL jaringan)adalah lapis keamanan opsional untuk Amazon VPC Anda.Ini bertindak sebagai firewall untuk mengendalikan lalu lintas masuk dan keluar dari satu subnet atau lebih. Setiap subnet di VPC Anda harus dikaitkan dengan ACL jaringan. Jika Anda tidak mengaitkan subnet dengan ACL jaringan secara eksplisit, subnet dikaitkan dengan ACL jaringan default secara otomatis. 

- ACL jaringan memiliki aturan masuk dan keluar yang terpisah, dan setiap aturan dapat mengizin 


## Amazon Route 53

![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/0c30b308-dd69-4c1e-b8b7-e0935935fb3a)

Seperti sebagaimana fungsi dari Route 53 ini dirancang untuk merutekan pengguna akhir ke aplikasi internet dengan menerjemahkan nama jadi untuk pola dasar dari route 53 akan seperti diatas, jadi ketika pengguna mengajukan permintaan DNS. Resolver DNS memeriksa domain dengan route 53, mendapatkan IP lalu mengambalikan ke pengguna.

Amazon Route 53 mendukung bebrapa jenis kebijakan perutean yaitu:
 - Perutean sedrhana : menggunakan server tunggal dalam lingkungan.
 - perutean weighted round robin : Gunakan untuk merutekan lalu lintas ke beberapa sumber daya dalam proporsi yang Anda tentukan. Memungkinkan Anda menetapkan beban ke serangkaian catatan sumber daya untuk menentukan dengan frekuensi mana respons yang berbeda dilayani.
 - perutean latensi (LBR) : membantu meningkatkan aplikasi global kita
 - Perutean geolokasi–Gunakan saat Anda ingin merutekan lalu lintas berdasarkan lokasi pengguna.
 - Perutean kedekatan geografis–Gunakan saat Anda ingin merutekan lalu lintas berdasarkan lokasi sumber daya Anda dan, secara opsional, mengalihkan lalu lintas dari sumber daya di satu lokasi ke sumber daya di lokasi lain.
 - Perutean failover (failover DNS) —Gunakan saat Anda ingin mengonfigurasi failover aktif-pasif.
 - Perutean jawaban multinilai—Gunakan jika Anda ingin Route 53 merespons kueri DNS dengan hingga delapan catatan baik yang dipilih secara acak.

Deployment Multiwilayah merupakan kasus pengguna contoh untuk AWS route 53. Dengan Amazon Route 53, pengguna secara otomatis diarahkan ke load balancerElastic Load Balancing yang paling dekat dengan pengguna.


## Amazon CloudFront

Tujuan dari jaringan adalah untuk berbagi informasi antara sumber daya yang terhubung. Sejauh ini di dalam modul ini, Anda belajar tentang jaringan VPC dengan Amazon VPC. Anda belajar tentang berbagai opsi untuk menghubungkan VPC Anda ke internet, ke jaringan jarak jauh, ke VPC lain, dan ke layanan AWS.  

Sebuah jaringan penyampaian konten (CDN) adalah sistem server pembuatan cache yang didistribusikan secara global. CDN menyimpan salinan file yang biasa diminta dalam cache (konten statis, seperti Hypertext Markup Language, atau HTML; Cascading Style Sheet, atau CSS; JavaScript; dan file gambar) yang di-host di server asal aplikasi. CDN juga memberikan konten dinamis yang unik untuk pemohon dan tidak dapat disimpan di cache

Amazon CloudFront adalah layanan CDN cepat yang memberikan data, video, aplikasi, dan antarmuka pemrograman aplikasi (API) dengan aman kepada pelanggan secara global dengan latensi rendah dan kecepatan transfer yang tinggi. Hal Ini juga menyediakan lingkungan yang ramah developer. Amazon CloudFront berbeda dari solusi penyampaian konten tradisional karena memungkinkan Anda mendapatkan manfaat penyampaian konten kinerja tinggi dengan cepat tanpa kontrak negosiasi, harga tinggi, atau biaya minimum.

Biaya Amazon CloudFront ditagih berdasarkan penggunaan layanan aktual di empat area:
- Transfer Data Keluar : Dikenai biaya untuk volume data yang ditransfer keluar dari edge location Amozon CloudFront ke internet atau ke asal anda.
- Permintaan HTTP(S) : Dibebankan untuk jumlah permintaan HTTP(S)
- Permintaan Pembatalan Validasi : Tidak ada biaya tambahan untuk 1000 jalur pertama yang diminta untuk pembatalan validasi setiap bulan, Oleh karena itu 0,005 USD per jalur yang diminta untuk pembatalan validasi.
- SSL Kustom IP Khusus : 600 USD per bulan untuk setiap sertifikat SSL kustom yang diasosiasikan dengan satu atau lebih distribusi CloudFront menggunakan versi IP Khusus dari dukungan sertifikasi SSL.
  
[link](link)
