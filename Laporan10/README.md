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

4. Buat user dan buat directory maildir untuk semua user sebagai tempat mailbox email
![restart_postfix](https://img001.prntscr.com/file/img001/u5Pd6W-pTjG-jRD9tdRq-A.jpeg)
Pada command maildirmake, adalah untuk membuat directory maildir pada home directory masing-masing user, lalu membuat baru dengan nama user1 dan user2. Terlihat bahwa secara otomatis ketika ada user baru, terdapat directory maildir di home directory setiap user

5. Lalu restart service postfix dan courier-imapnya
![restart_postfix](https://img001.prntscr.com/file/img001/G5yNlQSXQ6G0CYeo6LDmgg.jpeg)

6. Kemudian tambah CNAME untuk email pada file db-forward

![tambah CNAME](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/le5012f6s5rgzv6j9joj.png)

## Membuat Contoh Mail
7. Testing kirim email ke user2
![restart_postfix](https://img001.prntscr.com/file/img001/lUjkc23dQMaerAhdXqPHpw.jpeg)
Kali ini akan ada percobaan mengirim email ke user via telnet
