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
- Cari nilai checksum pada detail paket dan didapatkan checksum: 0x18e5. <br>
- Hasil <br>
## **Soal Nomor 5**
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut. <br>
a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut? <br>
b. Port berapakah pada server yang digunakan untuk service SMTP? <br>
c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP? <br>
## **Penyelesaian Soal Nomor 5**
- Cari paket yang menggunakan protocol SMTP lalu lakukan follow. <br>
- Ditemukan passwordnya. <br>
- Decode menggunakan base64, didapatkan password “5implePas5word”. <br>
- Gunakan password untuk membuka file zip. <br>
- Connect ke address untuk menjawab soal. <br>
a.	Banyak paket yang dicapture dapat dilihat pada list paket yaitu 60 paket. <br>
b.	Port service SMTP ditemukan pada bagian detail paket yaitu 25. <br>
c.	Public IP dicari address yang diawali selain IP 10 yaitu IP 74.53.140.153. <br>
- Hasil <br>
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
