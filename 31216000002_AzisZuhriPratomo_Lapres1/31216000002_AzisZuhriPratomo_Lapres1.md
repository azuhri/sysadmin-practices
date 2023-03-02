Kamis, 2 Maret 2023

LAPORAN TUGAS

WORKSHOP ADMISTRASI JARINGAN






![](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.001.png)

#Dr. Ferry Astika Saputra ST, M.Sc.






Nama	: Azis Zuhri Pratomo 

NRP 	: 3121600002

Kelas	: 2  D4 IT A



**Laporan Materi Pendahuluan Ubuntu Server**

**1**. **Identifikasi kernel**
**

Kernel pada linux adalah inti dari turunan sistem operasi berbasis UNIX seperti system distro linux. Kernel menghubungkan hardware dengan sistem operasi, mengatur akses sumber daya, dan menjalankan semua proses pada sistem operasi.
`	`Sebagai inti sistem operasi, kernel Linux bertanggung jawab atas pengelolaan sumber daya seperti memori, prosesor, jaringan, dan input/output.
**

uname -a untuk menampilkan semua informasi tentang sistem seperti :
- nama host 
- versi kernel 
- arsitektur sistem 
- platform sistem operasi 
- tanggal 
- waktu kompilasi kernel
- dll. 

Command uname -a pada Ubuntu Server saya

![](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.002.png)

Saya menggunakan ubuntu versi 20 dengan versi kernel 5.4.0-109. Versi kernel ini adalah 5.19.0.35, di mana:

- 5 adalah nomor utama kernel

- 4 adalah nomor minor kernel, yang menunjukkan bahwa ini adalah kernel seri 4 dari seri 5.

- 0 adalah nomor revisi kernel, yang menunjukkan bahwa ini adalah revisi pertama dari kernel seri 19.

- 109 adalah nomor pembangunan kernel, yang menunjukkan bahwa ini adalah build ke-109 dari revisi pertama dari kernel seri 4.


##2. Identifikasi directory structure**

Struktur directory dari ubuntu server 20 milik saya :
![](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.003.png)
- /usr :
menyimpan program dan data yang terkait dengan pengguna. 
- /bin :
berisi execute table file user biasa
- /sbin :
execute table file untuk super user
- /root :
menyimpan file konfigurasi, skrip shell, dan data lainnya yang berkaitan dengan pengguna root.
- /home :
     menyimpan semua file dan data pribadi pengguna, seperti file dokumen, gambar, musik, dan 
   video.
- /var : 
untuk data data folatil berubah rubah seperti log sistem
- /temp :
penyimpanan sementara (seperti variable)
- /etc :
   untuk file-file konfigurasi dari suatu services
- /opt :
   untuk aplikasi aplikasi optional (tambahan)

- /mnt :
   digunakan untuk memuat sistem file dari file sistem lain.







**3. identifikasi perbedaan sudo dan su**

command **su** (switch user) digunakan untuk mengubah/perpindah menjadi user lain.
sementara **sudo** (superuser do) digunakan untuk menjalankan command tertentu sebagai akun superuser atau akun lain tanpa perlu masuk ke dalam akun superuser secara langsung.

Saat menggunakan command su, pengguna harus memasukkan password untuk akun superuser atau akun lain yang dituju. Namun, saat menggunakan perintah "sudo", pengguna diminta untuk memasukkan kata sandi mereka sendiri untuk memverifikasi identitas mereka sebelum menjalankan perintah.

Penggunaan **sudo** lebih aman dari pada menggunakan **su** karena dengan menggunakan sudo kita tidak perlu masuk sebagai superuser (root) untuk menggunakan akses superuser

Ganti user ke user root

![Text Description automatically generated](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.004.png)

Mencoba install package ssh dengan menggunakan super user

![Text Description automatically generated](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.005.png)

Exit, untuk menggunakan user biasa kembali dan saya mencoba install ssh tanpa menggunakan sudo dan terjadi error, dan setelah menggunakan sudo saya bisa menginstall ssh![Text Description automatically generated](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.006.png)


Pada saat membuat user baru , kita harus mendaftar kan user baru tersebut ke grup sudo.
Jika tidak maka user baru itu tidak akan bisa menggunakan command sudo 

- Membuat  user baru bernama  ajis 
  ![Text Description automatically generated](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.007.png)**
- Mengganti user menggunakan user ajis
  ![](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.008.png)
- Mencoba menggunakan command sudo dengan user ajis 
  ![](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.009.png)

Terlihat terjadi error, ketika user ajis menggunakan command sudo, ini terjadi karena user ajis belum di masukan ke group sudo 

- Memasukan user **ajis** ke group sudo

![Text Description automatically generated](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.010.png)

Ketika telah menjadi anggota dari group sudo, maka user ajis bisa menggunakan command sudo



**4. identifikasi jenis repository**
Ini adalah file sources.list Ubuntu yang berisi beberapa jenis repository. Berikut adalah identifikasi jenis repository berdasarkan baris yang dimulai dengan "deb" :

**deb cdrom**: 
`  `Ini adalah repository dari CD/DVD instalasi Ubuntu.

**deb <http://id.archive.ubuntu.com/ubuntu/> kinetic main restricted**  :
`     `adalah repository utama (main) Ubuntu, yang berisi paket-paket utama untuk sistem operasi 
`   `Ubuntu.

**deb <http://id.archive.ubuntu.com/ubuntu/> kinetic-updates main restricted** :
`   `Ini adalah repository Ubuntu untuk pembaruan (updates) dari paket-paket di repository utama.

**deb <http://id.archive.ubuntu.com/ubuntu/> kinetic universe** :
`   `adalah repository Ubuntu untuk paket-paket yang tidak disupport secara resmi oleh Ubuntu, namun 
`   `tetap terbuka untuk diakses oleh pengguna.

**deb <http://security.ubuntu.com/ubuntu> kinetic-security multiverse** :
`   `adalah repository Ubuntu untuk pembaruan keamanan (security) dari paket-paket di repository 
`   `multiverse.

**deb <http://security.ubuntu.com/ubuntu> kinetic-security universe** :
`   `Ini adalah repository Ubuntu untuk pembaruan keamanan (security) dari paket-paket di repository   
` `universe.
**deb <http://security.ubuntu.com/ubuntu> kinetic-security main restricted** :
`    `Ini adalah repository Ubuntu untuk pembaruan keamanan (security) dari paket-paket di repository utama.





- isi file dari /etc/apt/sources.list

![](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.011.png)

**5. identifikasi perintah apt**




` `apt install : Menginstall sebuah package.

apt update : Memperbarui daftar paket dan index  metadata atau yang tersedia di repository.

apt upgrade : Menginstall paket-paket baru yang tersedia dan mengupgrade paket yang sudah terinstall.

apt remove : Menghapus paket yang sudah terinstall.

apt autoremove : Menghapus paket-paket yang tidak lagi dibutuhkan oleh sistem.

apt search : Mencari paket yang tersedia pada repository.

apt show : Menampilkan informasi detail tentang paket yang tersedia di repository.

apt list : Menampilkan daftar paket-paket yang sudah terinstall.

apt full-upgrade : Menginstall paket-paket baru dan mengupgrade paket-paket yang sudah terinstall dengan menyelesaikan semua ketergantungan (dependencies) yang dibutuhkan.

Instruksi penggunaan command apt :

![Text Description automatically generated](Aspose.Words.7be61356-e8b0-4fb9-8875-629857f7f869.012.png)

