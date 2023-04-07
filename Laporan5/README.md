# Konfigurasi DNS Server pada Linux
Artikel ini merupakan laporan dari Workshop Administrasi Jaringan kelas 2 D4 IT A tahun 2023 Teknik Informatika, Politeknik Elektronika Negeri Surabaya

Dosen pengampu: Dr. Ferry Astika Saputra. S.T, M.Sc.

Anggota Kelompok 8:
1. M. Roy Farchan
2. Azis Zuhri Pratomo
3. Habibie Fatahillah

## Macam-Macam DNS
Informasi yang diminta user dalam sistem DNS disebut dengan DNS record. Ada beberapa jenis informasi yang bisa diminta dalam sistem DNS. Berikut adalah 10 DNS record yang paling sering dijumpai:

- A Record atau Address record ─ menyimpan informasi soal hostname, time to live (TTL), dan IPv4 Address.
- AAA Record ─ menyimpan informasi hostname dan hubungannya dengan IPv6 address.
- MX Record ─ merekam server SMTP yang khusus digunakan untuk saling berkirim email di suatu domain.
- CNAME Record ─ digunakan untuk me-redirect domain atau subdomain ke sebuah IP Address. Lewat fungsi satu ini, Anda tak perlu memperbarui DNS record.
- NS Record ─ merujuk subdomain pada authoritative name server yang diinginkan. Record ini berguna jika subdomain Anda di web hosting berbeda dengan domain.
- PTR Record ─ memberikan izin pada DNS resolver untuk menyediakan informasi soal IP Address dan menampilkan hostname (reverse DNS lookup).
- CERT Record ─ menyimpan sertifikat enkripsi atau sertifikat keamanan.
- SRV Record ─ menyimpan informasi terkait lokasi komunikasi, semacam Priority, Name, Weight, Port, Points, dan TTL
- TXT Record ─ membawa dan menyalurkan data yang hanya bisa dibaca oleh mesin.
- SOA Record ─ bagian yang muncul di awal dokumen DNS zone. Bagian yang sama juga merujuk pada Authoritative Name Server serta informasi lengkap sebuah domain.


## Langkah - Langkah

1. Melakukan update dan upgarde pada linux
Hal ini dilakukan agar 
```
> sudo apt-get update
> sudo apt-get upgrade
```

2. Menginstall package **bind9** & **bind9utils**
```
> sudo apt-get install bind9 bind9utils
```


3. Melakukan konfigurasi di

Buka file named-conf, disini kami menggunakan software nano untuk mengeditnya

![Buka File named-conf](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jqooab0k1gqws5bqq5eh.png)

Mengganti konfigurasi dns server
 
![konfigurasi named-conf](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/dsbqebi8hnvl4saapfwx.png)

4. Konfigurasi file forward


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3g133sf1jklje6qrg6tv.png)



5. Konfigurasi file reverse

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/uhvz6fidk3np0gnwdd85.png)

6. Konfigurasi resolve

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/r7vg5iy6kwpjl8yb2ocg.png)

7. Melakukan pengujian

Cek record forward
![forward](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rtzn4wg15m6iqhwb9zmh.png)

Cek record reverse
![Reverse](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zrw8n0i4bsk67njsj4fm.png)


## Referensi
https://guru.smkn1pacitan.sch.id/sis/2022/03/29/instalasi-dan-konfigurasi-dns-server-pada-linux-debian-11/



