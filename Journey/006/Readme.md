**Add a cover photo like:**
![placeholder image](https://via.placeholder.com/1200x600)

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

Jaringan komputer adalah dua mesin klien atau lebih yang terhubung bersama-sama untuk berbagi sumber daya. Sebuah jaringan dapat secara logis dipartisi menjadi subnet. Jaringan memerlukan perangkat jaringan (seperti perute atau switch) untuk menghubungkan semua klien bersama-sama dan memungkinkan komunikasi antarklien.AWS Training and CertificationModul 5: Jaringan dan Penyampaian Konten© 2021 Amazon Web Services, Inc. atau afiliasinya. Hak cipta dilindungi undang-undang.8

**2. Alamat IP**

Setiap mesin klien dalam jaringan memiliki alamat Internet Protocol (IP) yang unik yang mengidentifikasinya. Alamat IP adalah label numerik dalam format desimal. Mesin mengonversi angka desimal ke format biner.

Dalam contoh ini, alamat IP adalah 192.0.2.0. Masing-masing dari angka alamat IP yang dipisahkan empat titik (.) mewakili 8 bit dalam format angka oktal. Itu berarti, masing-masing dari empat angka bisa angka berapa pun dari 0 sampai 255. Total gabungan dari empat angka untuk sebuah alamat IP adalah 32 bit dalam format biner.AWS Training and CertificationModul 5: Jaringan dan Penyampaian Konten© 2021 Amazon Web Services, Inc. atau afiliasinya. Hak cipta dilindungi undang-undang.9


**3. Alamat IPv4 dan IPv6**

Alamat IPv6 terdiri dari delapan grup empat huruf dan angka yang dipisahkan oleh titik dua (:). Dalam contoh ini, alamat IPv6 adalah 2600:1f18:22ba:8c00:ba86:a05e:a5ba:00FF. Masing-masing dari delapan grup alamat IPv6 yang dipisahkan titik dua mewakili 16 bit dalam format angka heksadesimal. Itu berarti masing-masing dari delapan grup tersebut bisa apa saja dari 0 sampai FFFF. Total gabungan dari delapan grup untuk alamat IPv6 adalah 128 bit dalam format biner.

**4. Classless Inter-Domain Routing (CIDR)**

Bit yang tidak tetap diperbolehkan untuk berubah. CIDR adalah cara untuk mengekspresikan grup alamat IP yang berturut-turut satu sama lain.

Dalam contoh ini, alamat CIDR adalah 192.0.2.0/24. Angka terakhir (24) memberitahu Anda bahwa 24 bit pertama harus ditetapkan. 8 bit terakhir bersifat fleksibel, yang artinya 28(atau 256) alamat IP tersedia untuk jaringan, dengan rentang antara 192.0.2.0 hingga 192.0.2.255 Angka desimal keempat diperbolehkan untuk berubah dari 0 hingga 255.

Jika CIDR adalah 192.0.2.0/16, angka terakhir (16) memberitahu Anda bahwa 16 bit pertama harus ditetapkan. 16 bit terakhir bersifat fleksibel, yang berarti bahwa 216(atau 65.536) alamat IP tersedia untuk jaringan dengan rentang 192.0.0.0 hingga 192.0.255.255. Angka desimal ketiga dan keempat masing-masing dapat berubah dari 0 hingga 255.AWS Training and CertificationModul 5: Jaringan dan Penyampaian Konten© 2021 Amazon Web Services, Inc. atau afiliasinya. Hak cipta dilindungi undang-undang.11

**5. Model Open Systems Interconnection (OSI)**

Model Open Systems Interconnection (OSI) adalah model konseptual yang digunakanuntuk menjelaskan bagaimana data melalui jaringan. Model ini terdiri dari tujuh lapis dan menunjukkan protokol umum dan alamat yang digunakan untuk mengirim data pada setiap lapis. Misalnya, hub dan switch bekerja pada lapis 2 (lapis tautan data). Perute bekerja pada lapis 3 (lapis jaringan). Model OSI juga dapat digunakan untuk memahami bagaimana komunikasi berlangsung di virtual private cloud (VPC), yang akan Anda pelajari di bagian berikutnya.AWS Training and CertificationModul 5: Jaringan dan Penyampaian Konten© 2021 Amazon Web Services, Inc. atau afiliasinya. Hak cipta dilindungi undang-undang.13

## Amazon Virtual Private Cloud (Amazon VPC)



## Jaringan VPC


## Keamanan VPC



## Amazon Route 53



## Amazon CloudFron



[link](link)
