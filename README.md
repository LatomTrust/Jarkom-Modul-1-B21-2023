# Jarkom-Modul-1-B21-2023

| **No** | **Nama**                         | **NRP**    |
| ------ | -------------------------------- | ---------- |
| 1      |Anneu Tsabita Putri               | 5025211026 |
| 2      | Cavel Ferrari                    | 5025211198 |


--------------------------------

## Soal 1

User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

<ol type="a">
<li>
    Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 
</li>

<li>
    Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?
</li>

<li>
    Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
</li>

<li>
    Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
</li>

</ol>



## Jawaban Soal 1 :

- 

--------------------------------

## Soal 2 :

Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

## Jawaban Soal 2 :


--------------------------------
## Soal 3 :

Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

<ol type="a">
<li>
    Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
</li>

- 21

<li>
    Protokol layer transport apa yang digunakan?
</li>

- UDP

</ol>


## Jawaban Soal 3 :
Untuk menjawab soal nomor 3 kita melakukan search pada display filter:
```
ip.addr == 239.255.255.250 && udp.port == 3702
```
Tujuan dari filter diatas adalah untuk menyaring paket berdasarkan alamat IP sumber atau tujuan dengan  ip.addr == 239.255.255.250, dan mencari port == 3702


![messageImage_1695380751811](https://github.com/LatomTrust/Jarkom-Modul-1-B21-2023/assets/91776952/9c265725-d3e7-4399-b02a-f78aa66a946b)


Untuk menjawab soal no `3a` yaitu mengetahui banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702 yaitu dengan cara melihat dibagian bawah tampilan file pcap pada wireshark terdapat keterangan bahwa displayed = 21. Maka dapat disimpulkan bahwa paket yang tercapture pada filter tersebut sebanyak 21. 

Untuk menjawab soal `3b` yaitu protokol layer transport apa yang digunakan, kita dapat melihat pada tampilan hasil filter seperti pada gambar diatas, terdapat keterangan di kolom protocol itu menggunakan UDP.

--------------------------------
## Soal 4 :

Berapa nilai checksum yang didapat dari header pada paket nomor 130?

## Jawaban Soal 4 :
 - Cari Packet nomor 130 pada aplikasi Wireshark, lalu  pada sisi kiri bawah klik panel `User Data Protocol..` dapat-lah jawaban nilai cheksum.

   
![messageImage_1695381118011](https://github.com/LatomTrust/Jarkom-Modul-1-B21-2023/assets/91776952/96b6cbbe-55cd-4f8e-8e02-dd102e8c13d1)


--------------------------------
## Soal 5 :

Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.

Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

> 60

Port berapakah pada server yang digunakan untuk service SMTP?

> 25

Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

> 74.53.140.153

## Jawaban Soal 5 :

Untuk menjawab soal ini, kita perlu terlebih dahulu mencari password untuk bisa membuka file connect pada file zip yang diberikan. Berikut langkah-langkah untuk menemukan password nya :
> Menganalisis isi paket dari pcap5
> Mencari protokol smtp untuk pengiriman email



> Mendapatkan body dari email yang berisikan password dari zip file.

![messageImage_1695381344832](https://github.com/LatomTrust/Jarkom-Modul-1-B21-2023/assets/91776952/4023c99c-aca0-4176-be97-f473c8f7c6cd)

<img width="484" alt="image" src="https://github.com/LatomTrust/Jarkom-Modul-1-B21-2023/assets/91776952/bb8f632c-4f0f-42ab-b72e-2cef0700af3f">

> Password yang didapat perlu di decode terlebih dahulu dengan base64decode lalu mendapatkan hasil decode adalah 5implePas5word.


<img width="603" alt="image" src="https://github.com/LatomTrust/Jarkom-Modul-1-B21-2023/assets/91776952/e0f096a8-5a1c-4154-8eec-aa36a98824fb">

> Lalu gunakan password untuk membuka file connect

<img width="342" alt="image" src="https://github.com/LatomTrust/Jarkom-Modul-1-B21-2023/assets/91776952/1f9370be-3069-4ec3-b8da-3805d93aee73">

Untuk menjawab soal no `5a` yaitu mengetahui banyak paket yang tercapture dari file pcap tersebut yaitu dengan melihat dibagian bawah tampilan file pcap pada wireshark terdapat keterangan bahwa displayed = 60.


Untuk menjawab soal `5b` yaitu mengetahu port berapakah pada server yang digunakan untuk service SMTP. Kita dapat melihat dibagian Transmission Control Protocol terdapat keterangan bahwa destination port nya adalah 25.


Untuk menjawab soal `5c` kita dapat menganalisis IP yang merupakan public IP. Maka didapatkan yang termasuk public IP adalah 74.53.140.153


--------------------------------
## Soal 6 :

Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan <b>"server SOURCE ADDRESS 7812 is invalid".</b> ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

## Jawaban Soal 6 :

Untuk menjawab soal nomor 6, kita perlu mencari dulu file dengan nomor 7812 pada file pcap yang diberikan.

<img width="761" alt="image" src="https://github.com/LatomTrust/Jarkom-Modul-1-B21-2023/assets/91776952/76103672-cf67-40c3-8fc8-4bcfc4cb6f0f">

Setelah, itu salin source address pada file nomor 7812 lalu decrypt menggunakan generate online. Hasilnya dapat dilihat pada file dibawah ini dan ditemukan yang sesuai dengan soal adalah `JDRNJA`

<img width="760" alt="image" src="https://github.com/LatomTrust/Jarkom-Modul-1-B21-2023/assets/91776952/adf9038a-0be2-4a4c-8cf2-7eda011a354d">


--------------------------------

## Soal 7 :

Berapa jumlah packet yang menuju IP 184.87.193.88?

## Jawaban Soal 7 :
- 
- 
- 
--------------------------------
## Soal 8 :

Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)
## Jawaban Soal 8 :

-

--------------------------------

## Soal 9 :
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

## Jawaban Soal 9 :

Untuk menjawab soal nomor 9, kita membuat kueri filter sebagai berikut:
```
ip.src == 10.51.40.1 && ip.dst != 10.39.55.34
```
Penjelasan queri diatas adalah:
- `ip.src == 10.51.40.1`: Bagian ini berarti Anda ingin mencari paket-paket yang memiliki alamat IP sumber (source IP) sebesar 10.51.40.1. Dengan kata lain, Anda mencari paket-paket yang berasal dari alamat IP ini.
- `&&`: Ini adalah operator logika "dan" yang digunakan untuk menggabungkan dua kondisi. 
- `ip.dst != 10.39.55.34`: Bagian ini berarti Anda ingin mencari paket-paket yang memiliki alamat IP tujuan (destination IP) yang tidak sama dengan 10.39.55.34.
  
<img width="760" alt="image" src="https://github.com/LatomTrust/Jarkom-Modul-1-B21-2023/assets/91776952/4c4e5377-6c9e-42af-868d-b9daf91d63c8">

--------------------------------

## Soal 10 :

Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

## Jawaban Soal 10 :
-
