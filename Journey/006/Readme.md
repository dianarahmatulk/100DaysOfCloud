
# Modul 5 - Jaringandan penyampaian konten
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
Jaringan VPC ini berisika

## Keamanan VPC



## Amazon Route 53



## Amazon CloudFron



[link](link)
