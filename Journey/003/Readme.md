![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/1226d6ae-7fe6-4360-838f-190e4e0f9cf0)


# Task 1 - Explore the Users dan Groups

  AWS Identity and Access Management (IAM) adalah layanan web yang memungkinkan pelanggaran Amazon Web Service (AWS) mengelola pengguna dan izin pengguna dia AWS. Dengan IAM kita dapat mengelola pengguna, kredensial keamanan dan izin mengontrol secara terpusat.

## Apa saja yang kita lakukan?

- Mengakses AWS Management Console
- Menjelajahi Pengguna dan Grup
- Skenario Bisnis - Menambahkan Pengguna ke Grup
- Masuk dan Menguji Users
- Bereksperimen dengan kebijakan akses layanan.

## Mengakses AWS Management Console

1. cari lab 1 pada bagian chapter 4. klik lab 1 lalu pada bagian atas instruksi pilih **mulai lab** untuk memulai lab, tunggu proses berjalan sampai lab status berubah menjadi **ready**, seperti gambar dibawah ini:  
 ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/bd027378-ff33-4915-a6b1-e9fa457321ac)

2. Klik tanda panah pada bagian start lab, lalu kita akan melihat ada tulisan AWS. Klik AWS maka kita akan mendapatkan Lab dibagian jendela baru web browse kita.
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/5a7b7e9f-9889-4a86-80e1-e61d16a1f77d)

 
## Menjelajahi Pengguna dan Group 

1. jika kita telah selesai menyalakan Lab selanjutnya, kita masuk pada lab yang telah terbuka di jendela baru. buka Lab yang berada dijendela baru dan klik buka Lab yang berada dijendela baru dan klik icon **search** disebelah service, ketikkan **IAM** lalu pilih juga service IAM pada bagian bawah.
 ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/bf349251-ee5a-4b65-9619-aa500b181e21)

2. pada panel navigasi, kita pilih **Users**. Akan ada beberapa Pengguna yang telah disediakan oleh AWS. kita akan pilih User-1:
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/1373be7a-ef8d-4ee0-8c7b-46a6aeb143c3)

3. setelah kita klik user-1 maka kita harus memastikan bahwa User-1 tidak memiliki permissions, tidak masuk kedalam group apapun. untuk security credential User-1 memiliki kata sandi yang telah diberikan oleh console, seperti gambar dibawah:
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/f1a8abfc-759c-4023-aa4f-13066380c597)

4. kita beralih pada panel navigasi disebelah kiri, lalu kita pilih User Group, pada tab user group terdapat 3 Gruop sesuai dengan fungsi gruop tersebut, kita pilih EC2-Support:
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/1c2f0477-a00c-435e-81ac-fd16776ad5fd)

5. setelah terpilih EC2-Support dapat dilihat pada bagian bawah terdapat beberapa pilihan tab, kita pilih saja permition, dan kita lihat pada policy name terdapat **AmazonEC2ReadOnlyAccess** yang merupakan kebijakan yang telah diatur oleh AWS untuk group ini.
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/8bdab6b6-e6d4-4a84-8fb1-648e1ca05077)

6. sama seperti EC2-Support pada S3-Support juga memiliki kebijakan **AmazonS3ReadOnlyAccess** seperti yang tercantum dalam foto berikut ini:
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/8f384192-db96-4ddf-bc3f-c7bd9c95038e)

7. untuk EC2-Admin kebijakan yang dimilikinya sedikit berbeda, pada Policy name berisikan EC2-Admin-Policy.
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/c614fb9c-2a84-4347-91f4-a164eee2d99f)


## Skenario Bisnis - Menambahkan Pengguna ke Grup
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/29b8bcfd-da45-4c7e-864e-394a7e10df71)

kita akan membuat konfigurasi seperti diatas dengan lab ini, kita akan menambahkan User-1 ke Group S3-Support, User-2 ke Grup EC2-Support, dan User-3 ke Grup EC2-Admin.

**A. Menambahkan user-1 ke Grup S3-Support**

1. kita beralih pada panel navigasi disebelah kiri, dan kita pilih Users Group.
2. Selanjutnya kita pilih S3-Support kita scroll pada bagian bawah dan pilih pada bagian user
   ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/836eaade-3dbf-493a-ace1-68aa8e39ddc7)
3. kita pilih saja User-1 lali klik Add users
   ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/1a1a6cd6-b4a6-4e86-ab09-09ae439a7dcf)

**B. Menambahkan User-2 ke Grup EC2-Support**

1. sama seperti tadi kita masuk pada tab navigasi Users Group.
2. Kita pilih EC2-Support lalu pilih Users dan kita pilih User-2 yang akan kita masukkan pada EC2-Support.
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/dbe9d850-a582-4512-9ec4-d03bddbd89b2)
 3. selanjutnya kita klik Add Users
    ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/53e3d69a-acaf-47a5-8c3b-1730398d5933)

**C. Menambahkan User-3 ke Grup EC2-Admin**

1. untuk menambahkan user-3 ini sama seperti sebelumnya. kita akan masuk pada menu Users Group, lalu kita pilih EC2-Admin.
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/16d98d82-c7be-48c1-8d36-3a8a28dd894b)

2. kita pilih User lalu kita klik Add user, selanjutnya kita akan pilih user-3 untuk dimasukkan pada EC2-Admin
    ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/e8f2cfcb-dbc3-4012-8546-9cafc56ae986)

## Masuk dan Menguji Users
  disini kita akan mencoba untuk login dengan Users yang sudah kita masukkan pada group sesuai dengan fungsinya, saya akan memberikan contoh untuk User-1 saja. pertama kita lihat pada navigasi di sebelah kiri. kita pilih dashboard dan kita liat disana terdapat tulisan sebagai berikut:
  
  ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/4c3199f8-57ce-484d-835f-c5435e12eff9)

kita salin URL tersebut lalu kita buka jendela baru dengan mode penyamaran. kita salin kesana lalu enter. Selanjutnya, kita akan masuk sebagai user-1, yang telah direkrut sebagai staf dukungan penyimpanan Amazon S3 Anda. lalu Masuk dengan:
- Nama pengguna IAM: user-1
- Kata sandi: Lab-Password1
  ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/03d9f93c-479f-4771-b7b4-d42625977b4e)

  kita klik sign in. selanjutnya kita akan masuk dalam lab dengan nama user-1, kita masuk pada S3 dan kita akan membuat bucket pada S3. Seperti gambar berikut:
  ![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/dc60bbac-cfa6-42e1-9f82-695ebc7ea4d1)

isikan nama untuk bucket kita terserah, sesuai dengan keinginan kalian atau ikuti instruksi dari gambar dibawah: 
![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/e916eac0-b715-451d-8611-bb002cffdc55)

setelah kita buat lalu kita simpan dengan mengeklik Choose bucket, setelah kita save seharusnya kita tidak dapat membuat bucket tersebut karena pada User-1 hanya memiliki akses **ReadOnly** di group S3-Support.


[link drive nya kaka](https://docs.google.com/document/d/1axsQ0lNZzaFj-FNlDvIcr2ZmF42cJQ6MLlSoc3l62BE/edit)
