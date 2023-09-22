# Jarkom-Modul-1-E30-2023
# **Praktikum 1 Jaringan Komputer**
<div align=justify>

Berikut repository dari Kelompok E30 Praktikum Modul 1 Jaringan Komputer.

# **Anggota Kelompok**

| Nama                      | NRP        | Kelas                |
| ------------------------- | ---------- | ----------------     |
| Hana Maheswari            | 5025211182 | Jaringan Komputer E  |
| Meyroja Jovancha Firoos   | 5025211204 | Jaringan Komputer E  |

# **Dokumentasi dan Penjelasan Soal**
<div align=justify>

Berikut adalah dokumentasi yang berisi source code dari tiap soal dan penjelasan terkait perintah yang digunakan. 

## **Soal Nomor 1**
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 

b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 

c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
## **Penyelesaian Soal Nomor 1**
## **Soal Nomor 2**
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
## **Penyelesaian Soal Nomor 2**
## **Soal Nomor 3**
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

b. Protokol layer transport apa yang digunakan?
## **Penyelesaian Soal Nomor 3**
## **Soal Nomor 4**
Berapa nilai checksum yang didapat dari header pada paket nomor 130?
## **Penyelesaian Soal Nomor 4**
- Dicari paket nomor 130. <br>
![4 1](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/e6c7871a-0dc3-43bf-9c9b-6683ec828103)
- Cari nilai checksum pada detail paket dan didapatkan checksum: 0x18e5. <br>
![4 2](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/efd7f48e-b6b4-47d1-849b-d5e4097d4a2b)
- Hasil <br>
![4 3](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/d8f85eaf-5a82-4e0a-8d93-d8cb26b711c6)
## **Soal Nomor 5**
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut. <br>
a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut? <br>
b. Port berapakah pada server yang digunakan untuk service SMTP? <br>
c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP? <br>
## **Penyelesaian Soal Nomor 5**
- Cari paket yang menggunakan protocol SMTP lalu lakukan follow. <br>
![5 1](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/df1524e0-ee67-4420-8820-a6c83a5196e0)
- Ditemukan passwordnya. <br>
![5 2](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/283728a5-cd5a-441c-a856-ac028c8a30fe)
- Decode menggunakan base64, didapatkan password “5implePas5word”. <br>
![5 3](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/4407edde-0cb4-4a6c-903e-74c143038485)
- Gunakan password untuk membuka file zip. <br>
![5 4](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/eaed2fd9-298c-4305-860f-676a08761a95)
- Connect ke address untuk menjawab soal. <br>
a.	Banyak paket yang dicapture dapat dilihat pada list paket yaitu 60 paket. <br>
![5 5](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/1e33f4ae-27da-4f11-9b4c-f32e096f473b)
b.	Port service SMTP ditemukan pada bagian detail paket yaitu 25. <br>
![5 6](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/3ce5804b-2712-470c-83d4-d515343a6af3)
c.	Public IP dicari address yang diawali selain IP 10 yaitu IP 74.53.140.153. <br>
![5 7](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/4401bd2e-88fe-45e2-a4a3-446b5707d3bd)
- Hasil <br>
![5 8](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/e82b1808-4935-47f1-8d31-52a0cd495e16)
## **Soal Nomor 6**
Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.
## **Penyelesaian Soal Nomor 6**
## **Soal Nomor 7**
Berapa jumlah packet yang menuju IP 184.87.193.88?
## **Penyelesaian Soal Nomor 7**
- Dilakukan filter paket menggunakan ip.dst == 184.87.193.88, ditemukan 6 paket. <br>
- Hasil <br>
## **Soal Nomor 8**
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)
## **Penyelesaian Soal Nomor 8**
- Filter dilakukan menggunakan logical OR menjadi tcp.dstport == 80 || udp.dstport == 80. <br>
- Hasil <br>
## **Soal Nomor 9**
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
## **Penyelesaian Soal Nomor 9**
- Filter dilakukan dengan menggunakan logical AND menjadi ip.src == 10.51.40.1 && ip.dst != 10.39.55.34. <br>
- Hasil <br>
## **Soal Nomor 10**
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet
## **Penyelesaian Soal Nomor 10**
