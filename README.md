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

**Soal a dan b**
menggunakan filter 
```
ftp.request.command == STOR
```


<img width="1121" alt="Screenshot 2023-09-22 at 18 20 53" src="https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/145383781/747fac54-ef8c-4b4d-8d9f-fab82941aa7f">


- Lalu cari packet yang berisi Request : STOR (namafile) (karena aktivitasnya berupa mengunggah suatu file)
- Sehingga, sequence number (raw) dan acknowledge number (raw) dapat diketahui
a. sequence number (raw) : 258040667
b. acknowledge number (raw) : 104486103925


**Soal c dan d**
menggunakan filter
```
ftp
```


<img width="1123" alt="Screenshot 2023-09-22 at 18 38 04" src="https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/145383781/07c645a6-14d5-40e3-9ac2-59865b1ffc08">


- Lalu cari packet yang berisi Response : 150 ... (namafile)
- Sehingga, sequence number (raw) dan acknowledge number (raw) dapat diketahui
a. sequence number (raw) : 1044861039
b. acknowledge number (raw) : 258040696

## **Soal Nomor 2**
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
## **Penyelesaian Soal Nomor 2**

menggunakan filter
```
tcp contains "10.21.78.111"
```


<img width="1121" alt="Screenshot 2023-09-22 at 18 52 31" src="https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/145383781/1f701c65-b274-480c-a7b5-7f25e6a121c2">


- Pilih salah satu paket
- Klik kanan pada paket tersebut
- Pilih follow -> TCP STREAM
- Sehingga, web server yang digunakan dapat terlihat yaitu **gunicorn**

## **Soal Nomor 3**
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

b. Protokol layer transport apa yang digunakan?
## **Penyelesaian Soal Nomor 3**
menggunakan filter
```
ip.addr == 239.255.255.250 && (tcp.port == 3702 || udp.port == 3702)
```


<img width="1118" alt="Screenshot 2023-09-22 at 19 03 46" src="https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/145383781/6180fb35-8d9c-47ea-93a5-e96d0d91a96b">


- Lalu, dapat kita hitung paket yang tercapture yaitu sebanyak **21** paket
- protocol layer yang digunakan adalah **UDP**
  
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
![5 6](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/58a5734b-2b50-4cb0-897c-c687fcad55c5)
c.	Public IP dicari address yang diawali selain IP 10 yaitu IP 74.53.140.153. <br>
![5 7](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/3cf1a3d3-5f6c-4bb6-8184-3a2c4ced2bb6)
- Hasil <br>
![5 8](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/34ac3908-f482-41c4-8e67-07fefffe1c02)
## **Soal Nomor 6**
Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.
## **Penyelesaian Soal Nomor 6**
## **Soal Nomor 7**
Berapa jumlah packet yang menuju IP 184.87.193.88?
## **Penyelesaian Soal Nomor 7**
- Dilakukan filter paket menggunakan ip.dst == 184.87.193.88, ditemukan 6 paket. <br>
![7 1](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/dc114eb8-adc5-4854-aa44-dfb2fcaae817)
- Hasil <br>
![7 2](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/6f5d3a9b-76da-437b-9fcd-a25e5d95b966)
## **Soal Nomor 8**
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)
## **Penyelesaian Soal Nomor 8**
- Filter dilakukan menggunakan logical OR menjadi tcp.dstport == 80 || udp.dstport == 80. <br>
![8 1](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/606f02b2-c113-4cf3-9a49-d9f1d5f0e8eb)
- Hasil <br>
![8 2](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/db3d9c43-d6de-4559-960e-ef29119d657d)
## **Soal Nomor 9**
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
## **Penyelesaian Soal Nomor 9**
- Filter dilakukan dengan menggunakan logical AND menjadi ip.src == 10.51.40.1 && ip.dst != 10.39.55.34. <br>
![9 1](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/5083af8d-8e06-495b-b847-ec7871ba0912)
- Hasil <br>
![9 2](https://github.com/hanamahes78/Jarkom-Modul-1-E30-2023/assets/108173681/2af52f62-8c59-498f-9bab-fdbdd2b3d9df)
## **Soal Nomor 10**
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet
## **Penyelesaian Soal Nomor 10**
