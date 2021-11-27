# LAPORAN RESMI PRAKTIKUM JARINGAN KOMPUTER MODUL 4 2021
```
Kelompok: E17
Prefix: 192.208.*.*
```
## Pembagian Subnet
Pada topologi, terdapat beberapa subnet, dan saya membaginya sebagai berikut dengan total 15 subnet.
![image](https://user-images.githubusercontent.com/49693862/143686642-53185c53-8850-4c63-8ecd-1176d8ef0259.png)

Selanjutnya, dilakukan pembuatan tabel total subnet pada topologi
![image](https://user-images.githubusercontent.com/49693862/143686731-d865f544-4bf5-479d-9718-1b472d94a6d2.png)

## VLSM
Untuk VLSM, setelah pembuatan tabel total subnet, gambar pohon vlsm agar mudah menentukan netmask yang akan dipakai. Karena total keperluan host ada 5843, maka digunakan netmask /19.
![image](https://user-images.githubusercontent.com/49693862/143686803-414335ab-54cf-479e-8c87-d38b29960d28.png)

Selanjutnya, setting pada cisco packet tracer sesuai dengan topologi yang kita buat dan jangan lupa untuk assign ip nya. Lengkapi juga routing pada router agar paket bisa terkirim.
![image](https://user-images.githubusercontent.com/49693862/143686863-5af2b3fc-8938-4d65-9c40-fa4d5f95ffa0.png)

## CIDR
Untuk CIDR, gabungkan dulu topologi seperti pada di modul.
![image](https://user-images.githubusercontent.com/49693862/143686921-54981d8d-74ab-4bd3-8c99-b8c03eaf4895.png)


Setelah digabungkan, bisa dilanjutkan dengan pembuatan pohon pembagian netmask.
![image](https://user-images.githubusercontent.com/49693862/143686966-56cedcb7-5810-4b2a-bb2a-0ceab2561517.png)

Pada CIDR, satu subnet diturunkan menjadi dua subnet sesuai dengan penggabungan subnet yang telah kita lakukan sebelumnya. Selanjutnya, buat topologi pada GNS3 dan lakukan setting IP. Jangan lupa atur aturan routing untuk topologi. Untuk CIDR, kita dapat membuat routing table yang efisien.
![image](https://user-images.githubusercontent.com/49693862/143687060-96f24276-33e0-4ba9-9be4-025907980d52.png)
Pada gambar diatas, bila kita ingin membuat route untuk tujuan ke A4, B4, B5, C4, dan C5, maka kita bisa menggunakan `192.208.0.0/16` sebagai aturan routenya. Agar terkoneksi dengan interent, lakukan pengaturan NAT di Foosha dengan sourcenya adalah root dari pohon CIDR yaitu, `192.208.0.0/15`. Tambahkan juga alamat DNS Server di masing-masing node agar dapat terhubung. Berikut adalah screenshot implementasi pada GNS3.
![image](https://user-images.githubusercontent.com/49693862/143687019-6198f087-4bb4-4787-af4a-6f3f01409685.png)

Setelah itu, bisa dilakukan uji coba ping.
