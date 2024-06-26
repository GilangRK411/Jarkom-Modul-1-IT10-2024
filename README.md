# Anggota Kelompok
| Nama | NRP |
| ---------------------- | ---------- |
| Khansa Adia Rahma      | 5027221071 |
| Gilang Raya Kurnaiwan   | 5027221045 |

## 1. Soal Praktikum Jarkom Nomer 1 (creds)

Attacker menyadari jika dia bisa membuat clone ftp server dari target, temukan kredensialn dari server ftp yang dibuat oleh attacker

Dikerjakan dengan memasukan *nc 10.15.40.20 10007* di terminal linux

## Pengerjaan
1. Cari file / jaringan yang mencurigakan dari soal yang diberikan yaitu *evidience.pcap*
   
2. Cari dengan menggunakan **filter protocal FTP**, Cari yang mencurigakan / beda (disini saya menemunkan dari info) USER h3ngk3rTzy dan PASS S!l3ncE

<img src="https://i.ibb.co/9GspYbS/Screenshot-2024-04-03-132108.png" alt="Screenshot-2024-04-03-132108" border="0">

3. masuk dari salah satu jaringan tadi misal **dari IP 10.30.3.1 dengan info USER h3ngk3rTzy** dengan klik kanan lalu **kilk follow TCP stream**

<img src="https://i.ibb.co/BL1X0XM/Screenshot-2024-04-04-092903.png" alt="Screenshot-2024-04-04-092903" border="0">

4. Coba masukan USER dan PASS yang ada di dalam jaringan tersebut ke Soal *nc 10.15.40.20 10007* dengan **format USER:username dan PASS:password**

<img src="https://i.ibb.co/ncJd660/Screenshot-2024-04-03-132434.png" alt="Screenshot-2024-04-03-132434" border="0">

5. FLAG CTF (JARKOM2024{s3curE_uR_FtP_xTfkXcpfQAVHRA9})

## 2. Soal Praktikum Jarkom Nomer 2 (ATM or ATP or FTP ?)

Pradityo mencoba mengembangkan server ftp, tetapi seseorang mencoba melakukan bruteforce login, bisakah Anda menganalisis apa yang terjadi?

Dikerjakan Dengan memasukan *nc 10.15.40.20 10004* di terminal linux

### Pengerjaan

1. Cari dengan filter protocol FTP
   
2. Temukan kata kata **yang paling mencurigakan / paling beda sendiri** misal di **Nomer 2** ini adalah *PASS m4y_th3_Kn!fe_ch1p_&_sh4tter* yang di dapat dari protocal FTP dan IP 10.30.3.4

<img src="https://i.ibb.co/5TPGp6c/Screenshot-275.png" alt="Screenshot-275" border="0">

Ketika di buka dengan **klik kanan lalu klik follow TCP Stream**

<img src="https://i.ibb.co/Z8pZFpv/Screenshot-276.png" alt="Screenshot-276" border="0">

3. Masukkan pass Bruteforce yang sudah didapat tadi ke soal *nc 10.15.40.20 10004* kalau benar maka akan muncul flag CTF nya seperti gambar di bawah

   <img src="https://i.ibb.co/p2MRV1z/Screenshot-2024-04-03-133336.png" alt="Screenshot-2024-04-03-133336" border="0">

## 3. Soal Praktikum Jarkom Nomer 3 (malwleowleo) 

Dapatkah kamu menemukan file malware yang dikirim oleh attacker melalui ftp?

Dikerjakan Dengan memasukan *nc 10.15.40.20 10008* di terminal linux

### Pengerjaan

1. Mirip-mirip dengan soal nomer 1 tadi bedanya ini didapat dari *IP Addres 10.30.3.1* dengan filter pencarian *tcp.stream. eq 2*

<img src="https://i.ibb.co/LSyVT30/Screenshot-2024-04-03-140243.png" alt="Screenshot-2024-04-03-140243" border="0">

Buka jaringan tersebut seperti biasanya dengan follow TCP Stream

<img src="https://i.ibb.co/gjT4p7k/Screenshot-2024-04-03-140252.png" alt="Screenshot-2024-04-03-140252" border="0">

Lihat yang di bawah akan ditemukan nama yang mencurigakan yaitu STOR m4L1c10us_W4re.c

<img src="https://i.ibb.co/tm6ddCW/Screenshot-2024-04-03-140259.png" alt="Screenshot-2024-04-03-140259" border="0">

2. Masukkan nama file yang mencurigakan tadi ke soal *nc 10.15.40.20 10008* lalu FLAG akan muncul dengan format nama JARKOM2024{beC4refUl_0f_m4lwAr3_96wRXOxyi6ko8At}

<img src="https://i.ibb.co/7Kwp2Cs/Screenshot-2024-04-03-140643.png" alt="Screenshot-2024-04-03-140643" border="0">

## 4. Soal Praktikum Jarkom Nomor 4 (How Many Packets?) 

Berapa kali attempt login yang dilakukan oleh hacker?

Dikerjakan Dengan memasukan *nc 10.15.40.20 10005* di terminal linux

### Pengerjaan

1. Untuk mencari informasi percobaan login yang dilakukan melalui FTP oleh hacker bisa dengan memfilter dengan command berikut:
   `````````````````````````````````
   ftp && frame contains " Login "
   `````````````````````````````````
   Sehingga akan, memunculkan jumlah attemp yang dilakukan oleh hacker pada bagian paling bawah yaitu **Displayed:**, pada soal ini terlihat bahwa terdapat 934 percobaan login yang dilakukan oleh hacker.
   <img width="1101" alt="image" src="https://github.com/GilangRK411/Jarkom-Modul-1-IT10-2024/assets/130457714/71e08937-191a-4ae4-abcc-907b4df85a09">

3. Selanjutnya, pada terminal masukkan jawaban untuk membuktikan kebenarannya dan mendapatkan flag.
   <img width="668" alt="image" src="https://github.com/GilangRK411/Jarkom-Modul-1-IT10-2024/assets/130457714/6a679ea7-af46-4265-8ea0-10cc14f9d04f">

## 5. Soal Praktikum Jarkom Nomor 5 (trace him) 

Selain menghitung jumlah packet, coba lacak juga ip penyerang tersebut!

Dikerjakan Dengan memasukan *nc 10.15.40.20 10006* di terminal linux

### Pengerjaan

1. Untuk melacak alamat IP hacker, dengan melihat kembali soal ATM or ATP or FTP pada nomor 2. Pada soal tersebut kita sudah berhasil menjawab untuk password yang digunakan oleh attacker yaitu: *m4y_th3_Kn!fe_ch1p_&_sh4tter*.
2. Selanjutnya, gunakan command berikut
   ``````````````
   ftp.request.command == "USER" || ftp.request.command == "PASS"
   ``````````````

   Lalu cari bagian yang memiliki PASS: *m4y_th3_Kn!fe_ch1p_&_sh4tter* dan lihat kembali **IP** atau **source** yang digunakan. Pada soal ini penyerang menggunakan IP **10.30.3.4** sebagai berikut:
   <img width="1101" alt="image" src="https://github.com/GilangRK411/Jarkom-Modul-1-IT10-2024/assets/130457714/5506bf77-b818-4215-b731-0ec72e04c82b">

3. Selanjutnya, pada terminal masukkan jawaban untuk membuktikan kebenarannya dan mendapatkan flag.
<img width="668" alt="image" src="https://github.com/GilangRK411/Jarkom-Modul-1-IT10-2024/assets/130457714/24eb4fe6-9e03-4d48-b66a-9fbffac97d2e">

## 6. Soal Praktikum Jarkom Nomer 6 (whoami) 

Dapatkah kamu menemukan siapa identitas attacker?

Dikerjakan Dengan memasukan *nc 10.15.40.20 10009* di terminal linux

### Pengerjaan

1. Cari Jawaban dengan menggunakan FIlter FTP-DATA di wireshark
   
3. Temukan file/jaringsan yang menurut kalian paling mencurigakan disini saya menggunakan fila berdata sebagai berikut
  ``````````````
1544	391.142970	10.30.3.1	10.15.40.20	FTP-DATA	260	FTP Data: 188 bytes (PASV) (STOR m4L1c10us_W4re.c)
  ``````````````

<img src="https://i.ibb.co/sCB66LP/Screenshot-2024-04-04-092958.png" alt="Screenshot-2024-04-04-092958" border="0">

3. masuk ke jaringan tersebut dengan menggunakan **follow TCP Stream**, Didalamya akan ada **text yang sudah di code dengan format base64** coba decode kode tersebut ke text aslinya

<img src="https://i.ibb.co/8X3SS6T/Screenshot-2024-04-03-184942.png" alt="Screenshot-2024-04-03-184942" border="0">

4. Hapus **tanda // dari code tersebut dari //SGVsbG8gbXkgbmFtZSBpcyBQYXVsIEF0cmVpZGVzCg== menjadi SGVsbG8gbXkgbmFtZSBpcyBQYXVsIEF0cmVpZGVzCg==** maka code tersebut akan menjadi text normal yang bertuliskan **Hello my name is Paul Atreides**

<img src="https://i.ibb.co/MR33dk6/Screenshot-2024-04-04-093144.png" alt="Screenshot-2024-04-04-093144" border="0">

5. Masuk ke soal *nc 10.15.40.20 10009* lewat OS linux anda masukkan jawaban ke soal Paul_Atreides maka FLAG CTF akan muncul **JARKOM2024{Duk3_0f_4rak!s_LISAN AL GHAIB!_9hrCY7xygAFoC8q}**

<img src="https://i.ibb.co/hsL5CzQ/Screenshot-2024-04-03-185948.png" alt="Screenshot-2024-04-03-185948" border="0">

# **Revisi**

## 7. Soal Praktikum Jarkom Nomer 7 (evidence) 

Perusahaan nanomate baru saja kebobolan. Mereka menyewamu untuk mencari tahu bagaimana caranya pelaku bisa masuk.

Dikerjakan Dengan memasukan *nc 10.15.40.20 10002* di terminal linux

### Pengerjaan

1. Buka WIreshark dan, Masukkan di terminal wireshark filter *tcp/http*

<img src="https://i.ibb.co/5YpRhNB/Screenshot-2024-04-04-091229.png" alt="Screenshot-2024-04-04-091229" border="0">

Jika masih belum menemukan yang kalian cari ganti dengan filter baru misal *tcp contains "login"*

<img src="https://i.ibb.co/m0SZBLK/Screenshot-2024-04-04-091318.png" alt="Screenshot-2024-04-04-091318" border="0">

2. buka sebuah jaringan yang menurut anda berisi data tentang Domain, Server dan hal lain yang di butuhkan di soal 7 ini

<img src="https://i.ibb.co/hMBT4pR/Screenshot-2024-04-04-091343.png" alt="Screenshot-2024-04-04-091343" border="0">

DIsini anda akan kekurangan data yaitu data tengang email yang berhasil login, clue nya adalah **lihat data yang anda buka kalau ada tulisan Invalid Username or Password, berati pasti ada data yang Login successful.** Data yang benar Tersebut didapat dari memasukan filter *tcp.stream eq 1240* di terminal wireshark

<img src="https://i.ibb.co/WHs8M27/Screenshot-2024-04-04-091413.png" alt="Screenshot-2024-04-04-091413" border="0">

3.  Masukkan Jawaban - jawaban yang sudah ditemukan ke soal *nc 10.15.40.20 10009*

<img src="https://i.ibb.co/WpjPHSJ/Screenshot-2024-04-04-091530.png" alt="Screenshot-2024-04-04-091530" border="0">

4.  Flag Ditemukan dengan format nama

<img src="https://i.ibb.co/34qbBQF/Screenshot-2024-04-04-091535.png" alt="Screenshot-2024-04-04-091535" border="0">
   
