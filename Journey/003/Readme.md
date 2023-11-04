![image](https://github.com/dianarahmatulk/100DaysOfCloud/assets/140806099/1226d6ae-7fe6-4360-838f-190e4e0f9cf0)


# Task 1 - Explore the Users dan Groups

  AWS Identity and Access Management (IAM) adalah layanan web yang memungkinkan pelanggaran Amazon Web Service (AWS) mengelola pengguna dan izin pengguna dia AWS. Dengan IAM kita dapat mengelola pengguna, kredensial keamanan dan izin mengontrol secara terpusat.

## Apa saja yang kita lakukan?

- Mengakses AWS Management Console
- Menjelajahi Pengguna dan Grup
- Skenario Bisnis - Menambahkan Pengguna ke Grup
- Menemukan dan Menggunakan URL masuk IAM
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
2. pilih Users dan kita pilih           
## Try yourself

✍️ Add a mini tutorial to encourage the reader to get started learning something new about the cloud.

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
