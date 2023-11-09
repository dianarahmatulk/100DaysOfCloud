## Skenario
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/f1517eca-3c5a-4606-a7e4-b8b8da609b8d)

# LAB 2 - Membangun VPC dan Server Web

Di lab ini, Anda akan menggunakan Amazon Virtual Private Cloud (VPC) untuk membuat VPC Anda sendiri dan menambahkan komponen tambahan untuk menghasilkan jaringan yang dikustomisasi. Kemudian, Anda akan membuat security group. Kemudian Anda akan mengonfigurasikan dan mengkustomisasi instans EC2 untuk menjalankan server web dan Anda akan meluncurkannya agar berjalan di subnet di dalam VPC.

## Introduction

Amazon Virtual Private Cloud (Amazon VPC) memungkinkan Anda meluncurkan sumber daya Amazon Web Services (AWS) ke dalam jaringan virtual yang ditetapkan. Jaringan virtual ini sangat mirip dengan jaringan tradisional yang akan dioperasikan di pusat data Anda sendiri, tetapi dengan manfaat yang sama seperti saat menggunakan infrastruktur AWS yang dapat diskalakan. Anda dapat membuat VPC yang mencakup beberapa Availability Zone.

## Yang akan kita dapatkan

- Membuat VPC.
- Membuat subnet.
- Mengonfigurasi security group.
- Meluncurkan instans EC2 ke VPC.

## Mengakses AWS Management Console

1. kita klik Start lab untuk membuka lab
2. tunggu hingga status lab siap
3. pada bagian navigasi kita pilih AWS
   
## Task 1 : Membuat VPC

1. Di kotak pencarian di sebelah kanan Services (Layanan), cari dan pilih VPC untuk membuka konsol VPC
2. Mulai membuat VPC.
   - Di sebelah kanan atas layar, pastikan wilayah yang dipilih adalah N. Virginia (us-east-1).
   - Pilih tautan dasbor VPC yang juga menuju ke sisi kiri atas konsol. Lalu klik tulisan create VPC
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/93e6b452-ecd3-49fb-b330-e1dba2b8aa5f)
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/640dde35-7fff-41c5-b8ef-932ce0a25a2c)
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/b3cad8f0-cd6c-4541-926b-42270d7196b7)
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/167d02cc-ec2c-4b10-8e9d-d186d448bb54)
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/cafee14f-631d-46be-92b4-7069099aa0c2)
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/7e1bef34-a618-4074-a670-255082946c69)
3. Setelah melakukan hal seperti diatas kita akan klik create VPS, lalu kita akan beralih ke tab loading/ pembuatan VPC resources seperti berikut ini:
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/072745b7-4589-471c-94be-0460476f7da7)
4. lalu kita bisa melihat jika VPS sudah dibuat di sini
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/7adaad41-bced-4231-a0fd-6d290e4ce248)

5. dan berikut ini adalah VPS yang saya buat
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/2d12f02a-cb30-450b-94a4-28f32947fc66)



## TASK 2 - Membuat Subnet Tambahan

Setelah membuat VPC, Kita akan menambahkan lebih banyak Subnet. berikut caranya

1. Di panel navigasi kiri, pilih Subnet. Pertama, Anda akan membuat subnet publik kedua. 
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/6658f141-1034-4ee1-9433-711011c9812f)


2. Pilih Buat subnet, lalu konfigurasikan:
- ID VPC:  lab-vpc (pilih dari menu).
- Nama subnet: lab-subnet-public2
- Availability Zone: Pilih Availability Zone kedua (misalnya, us-east-1b)
- Blok CIDR IPv4: 10.0.2.0/24
- Subnet akan berisi semua alamat IP yang dimulai dengan 10.0.2.x.

![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/c78c1496-9e09-41ad-b40b-2d309ad4d600)
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/df5a2433-e0c8-4bf0-972c-4f5f086f3781)
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/def421a5-0939-4ee1-8461-0c9de21f454f)

3. lakukan hal yang sama untuk subnet private kita dan hasilnya akan seperti berikut ini
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/a5e36c71-191c-400f-88cf-1e1ff5baf918)

4. 



### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 3 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

## ☁️ Cloud Outcome

✍️ (Result) Describe your personal outcome, and lessons learned.

## Next Steps

✍️ Describe what you think you think you want to do next.

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
