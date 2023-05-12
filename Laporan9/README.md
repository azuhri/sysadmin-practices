# Konfigurasi DNS pada Slave

Ini merupakan lanjutan dari konfigurasi DNS pada minggu sebelumnya.

1. Yang pertama dilakukan adalah menambah `allow-transfer` pada zone di file **named.conf.local**

![named.conf.local](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1u08dhu677y815r47fdy.png)

2. Kemudian tambahkan juga forwarder dari IP DNS di **/var/cache/bind9/**


![/var/cache/bind9/](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8bq7zzog6iaax0yz2e8k.png)

3. Langkah berikutnya restart service bind9


![Restart Bind9](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/40fams9vtp9kx55tapjt.png)

4. Konfigurasi pada apache agar bisa diakses 

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mch333ulxti3qxkdzmc9.png)


Berikut hasil akhirnya 

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6k5kkj08prncxreiehsh.png)
