# Konfigurasi SMTP Server

**SMTP** merupakan singkatan dari Simple Mail Transfer Protokol berfungsi sebagai protokol yang memfasilitasi dalam hal transfer <u>e-mail</u>. 

SMTP menggunakan 3 port, Port 25 digunakan untuk non SSL, port 587 untuk TLS dan 465 untuk SSL. Namun oleh sebagian ISP, port 25 telah ditutup karena dianggap berbahaya dengan tidak adanya encryption module yang digunakan.

Berikut cara konfigurasi SMTP Server pada Sistem Operasi Linux:
1. Menginstall package Postfix 


![Install Package](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/oxjf71hkqcoptznokxx5.png)

2. Mengisi nama email sistem

Fase ini akan dijalankan secara otomatis sehingga user akan diminta mengisi email system name.

![System Email Name](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ihhbu984f8e5p9u27zoh.png)

3. Lalu konfigurasi file **main.cf** seperti berikut ini

![main.cf](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zyiwl4oumm836dxfxfy7.png)

Setelah melakukan konfigurasi simpan perubahan, lalu restart konfigurasi postfix nya

![dpkg](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/45w2hvw0vou72dlhbjof.png)

4. Kemudian tambah CNAME untuk email pada file db-forward

![tambah CNAME](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/le5012f6s5rgzv6j9joj.png)


## Membuat Contoh Mail

Semua package telah terinstall selanjutnya konfigurasi pada apache2 nya.

Kami mencoba membuat webmail nya, kami menggunakan webmail opensource dari netflix

![wget webmail](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/r6q05of0m42gfekfj64q.png)

Kemudian tambahkan juga konfigurasi apache 2 di site-availables, 


![konfigutasi apache](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fd55u40bfiibavnymn45.png)

Terakhir **restart** service apache2 agar bisa menggunakan Web Mail. 
