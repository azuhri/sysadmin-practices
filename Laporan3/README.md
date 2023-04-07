## Kelompok 8
1. M. Roy Farchan
2. Azis Zuhri Pratomo
3. Habibi Fatahillah

### 1. Reset Configuration Router - 2
Reset Konfigurasi dilakukan dengan menggunakan software Winbox 

Akses fitur di bagian sidebar pada menu System -> pilih Reset Configuration -> centang No Default Configuration -> klik Reset Configuration.
 
Setelah itu akan otomatis melakukan rebooting pada router dan aplikasi akan melakukan reconnecting.


### 2. Config IP Local & Public
Setelah rebooting akses fitur di sidebar pada menu IP -> Addresses -> klik tombol "**+**" ->
**ETHER 1**
 - Address = 10.252.108.18/24
 - Network = 10.252.108.0
 - Interface = ETHER 1

 **ETHER 2**
 - Address = 192.168.8.1/24
 - Network = 192.168.8.1/24
 - Interface = ETHER 2


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/e27lqlmly86aohvbi1b3.png)


### 3. Config Default Route
Akses fitur di sidebar pada menu New Terminal
#### Configurasi Default Route
```console
ip route add dst-address=0.0.0.0/0 gateway=10.252.108.1
ip ro pr
```

### 3. Configurasi DNS
Akses fitur di sidebar pada menu IP -> DNS -> masukkan IP Server=202.9.85.3

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/00ygsanobl8tx9qyp1vj.png)



### 4. Config Internet Client
 - Berikut konfigurasi lengkapnya

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kydmgqi1tljcnikvp0pa.png)



### 5. Menambah IP Routes
Ketikkan pada New Terminal Winbox
```console
ip ro add gateway 10.252.108.11 dst 192.168.1.0/24
ip ro add gateway 10.252.108.12 dst 192.168.2.0/24
ip ro add gateway 10.252.108.13 dst 192.168.3.0/24
ip ro add gateway 10.252.108.14 dst 192.168.4.0/24
ip ro add gateway 10.252.108.15 dst 192.168.5.0/24
ip ro add gateway 10.252.108.16 dst 192.168.6.0/24
ip ro add gateway 10.252.108.17 dst 192.168.7.0/24
ip ro add gateway 10.252.108.19 dst 192.168.9.0/24
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gehvsvqqz29dc6l5qqo5.png)



### 6. Tes ping antar client

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/d96v1a4ayagqa9yl5yl8.png)


### 7. Export Config
Akses fitur di sidebar pada menu New Terminal, lalu ketikkan :

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/khzinz1j7eew6a633gnx.png)


dan file sudah berhasil di download ke komputer

