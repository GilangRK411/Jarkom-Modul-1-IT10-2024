# Anggota Kelompok
| Nama | NRP |
| ---------------------- | ---------- |
| Khansa | 5027221071  |
| Gilang Raya Kurniwan | 5027221045 |

# 1. Soal Praktikum Jarkom Nomer 1 (creds)

Attacker menyadari jika dia bisa membuat clone ftp server dari target, temukan kredensialn dari server ftp yang dibuat oleh attacker

Dikerjakan dengan memasukan *nc 10.15.40.20 10007* di terminal linux

## pengerjaan
1. Cari file / jaringan yang mencurigakan dari soal yang diberikan yaitu *evidience.pcap*
   
2. Cari dengan menggunakan **filter protocal FTP**, Cari yang mencurigakan / beda (disini saya menemunkan dari info) USER h3ngk3rTzy dan PASS S!l3ncE

<img src="https://i.ibb.co/9GspYbS/Screenshot-2024-04-03-132108.png" alt="Screenshot-2024-04-03-132108" border="0">

3. Caba masuk dari salah satu jaringan tadi misal **dari IP 10.30.3.1 dengan info USER h3ngk3rTzy** dengan klik kanan lalu **kilk follow TCP stream**

<img src="https://i.ibb.co/dpj16M6/Screenshot-2024-04-03-132211.png" alt="Screenshot-2024-04-03-132211" border="0">

4. Coba masukan USER dan PASS yang ada di dalam jaringan tersebut ke Soal *nc 10.15.40.20 10007* dengan **format USER:username dan PASS:password**

<img src="https://i.ibb.co/ncJd660/Screenshot-2024-04-03-132434.png" alt="Screenshot-2024-04-03-132434" border="0">

5. FLAG CTF (JARKOM2024{s3curE_uR_FtP_xTfkXcpfQAVHRA9})


# 2. Soal Praktikum Jarkom Nomer 2 (ATM or ATP or FTP ?)

Pradityo mencoba mengembangkan server ftp, tetapi seseorang mencoba melakukan bruteforce login, bisakah Anda menganalisis apa yang terjadi?

Dikerjakan Dengan memasukan *nc 10.15.40.20 10004* di terminal linux

## Pengerjaan

1. Cari dengan filter protocol FTP
   
2. Temukan kata kata **yang paling mencurigakan / paling beda sendiri** misal di **Nomer 2** ini adalah *PASS m4y_th3_Kn!fe_ch1p_&_sh4tter* yang di dapat dari protocal FTP dan IP 10.30.3.4

<img src="https://i.ibb.co/5TPGp6c/Screenshot-275.png" alt="Screenshot-275" border="0">

Ketika di buka dengan **klik kanan lalu klik follow TCP Stream**

<img src="https://i.ibb.co/Z8pZFpv/Screenshot-276.png" alt="Screenshot-276" border="0">

3. Masukkan pass Bruteforce yang sudah didapat tadi ke soal *nc 10.15.40.20 10004* kalau benar maka akan muncul flag CTF nya seperti gambar di bawah

   <img src="https://i.ibb.co/p2MRV1z/Screenshot-2024-04-03-133336.png" alt="Screenshot-2024-04-03-133336" border="0">

# 3. Soal Praktikum Jarkom Nomer 3 (malwleowleo) 

Dapatkah kamu menemukan file malware yang dikirim oleh attacker melalui ftp?

Dikerjakan Dengan memasukan *nc 10.15.40.20 10008* di terminal linux


## Pengerjaan

1. Mirip-mirip dengan soal nomer 1 tadi bedanya ini didapat dari *IP Addres 10.30.3.1* dengan filter pencarian *tcp.stream. eq 2*

<img src="https://i.ibb.co/LSyVT30/Screenshot-2024-04-03-140243.png" alt="Screenshot-2024-04-03-140243" border="0">

Buka jaringan tersebut seperti biasanya dengan follow TCP Stream

<img src="https://i.ibb.co/gjT4p7k/Screenshot-2024-04-03-140252.png" alt="Screenshot-2024-04-03-140252" border="0">

Lihat yang di bawah akan ditemukan nama yang mencurigakan yaitu STOR m4L1c10us_W4re.c

<img src="https://i.ibb.co/tm6ddCW/Screenshot-2024-04-03-140259.png" alt="Screenshot-2024-04-03-140259" border="0">

2. Masukkan nama file yang mencurigakan tadi ke soal *nc 10.15.40.20 10008* lalu FLAG akan muncul dengan format nama JARKOM2024{beC4refUl_0f_m4lwAr3_96wRXOxyi6ko8At}

<img src="https://i.ibb.co/7Kwp2Cs/Screenshot-2024-04-03-140643.png" alt="Screenshot-2024-04-03-140643" border="0">

# 6. Soal Praktikum Jarkom Nomer 6 (whoami) 

Dapatkah kamu menemukan siapa identitas attacker?

Dikerjakan Dengan memasukan *nc 10.15.40.20 10009* di terminal linux

## Pengerjaan

1. Cari Jawaban dengan menggunakan FIlter FTP-DATA
2. Temukan file/jaringsan yang menurut kalian paling mencurigakan disini saya menggunakan fila berdata sebagai berikut *1544	391.142970	10.30.3.1	10.15.40.20	FTP-DATA	260	FTP Data: 188 bytes (PASV) (STOR m4L1c10us_W4re.c)*

<img src="https://i.ibb.co/mt88HSF/Screenshot-2024-04-03-184934.png" alt="Screenshot-2024-04-03-184934" border="0">

3. Coba masuk ke jaringan tersebut dengan menggunakan **follow TCP Stream**, Didalamya akan ada **text yang sudah di code dengan format base64** coba decode kode tersebut ke text aslinya

<img src="https://i.ibb.co/8X3SS6T/Screenshot-2024-04-03-184942.png" alt="Screenshot-2024-04-03-184942" border="0">

4. Hapus **tanda // dari code tersebut dari //SGVsbG8gbXkgbmFtZSBpcyBQYXVsIEF0cmVpZGVzCg== menjadi SGVsbG8gbXkgbmFtZSBpcyBQYXVsIEF0cmVpZGVzCg==** maka code tersebut akan menjadi text normal yang bertuliskan **Hello my name is Paul Atreides**

<img src="https://i.ibb.co/1GMQb4L/Screenshot-2024-04-03-185150.png" alt="Screenshot-2024-04-03-185150" border="0">

5. Masuk ke soal *nc 10.15.40.20 10009* lewat OS linux anda masukkan jawaban ke soal Paul_Atreides maka FLAG CTF akan muncul **JARKOM2024{Duk3_0f_4rak!s_LISAN AL GHAIB!_9hrCY7xygAFoC8q}**

<img src="https://i.ibb.co/hsL5CzQ/Screenshot-2024-04-03-185948.png" alt="Screenshot-2024-04-03-185948" border="0">

