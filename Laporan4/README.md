Kelompok 8:
- M. Roy Farchan
- Azis Zuhri Pratomo
- Habibie Fatahillah
# Setting lokal NTP linux

Pertama dilakukan adalah menginstall **ntp** nya seperti pada gambar dibawah ini

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/54trq4pric1ifwab4fs1.png)

Setelah menginstall masuk ke konfigurasi, edit file konfigurasi 

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/v17nhgvh0egdirvem525.png)

dan komen line 4 pool dibawah ini:

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/n5586923x1o6kjsh68ie.png)

Setelah itu, pada baris paling bawah tambahkan kode yang menunjukan netword ID dari komputer dan netmask nya juga.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vp1pbysr62of00i88r89.png)

Restart service dari ntp, dan saya melakukan pengecekan status untuk memastikan ntp berjalan dengan baik.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zo852altymozna9b1ecq.png)

lakukan command dibawah untuk mengecek apakah server ntp sudah ditambahkan, dan hasilnya seperti pada gambar dibawah ini.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/bxfiub4t3t3p95biqose.png)





