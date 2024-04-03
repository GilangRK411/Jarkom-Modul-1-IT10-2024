# Anggota Kelompok
| Nama | NRP |
| ---------------------- | ---------- |
| Khansa | 5027221035 |
| Gilang Raya Kurniwan | 5027221045 |

# 1. Soal Praktikum Jarkom Nomer 1

Attacker menyadari jika dia bisa membuat clone ftp server dari target, temukan kredensialn dari server ftp yang dibuat oleh attacker

Dikerjakan dengan *nc 10.15.40.20 10007*

## pengerjaan
1. Cari file / jaringan yang mencurigakan dari soal yang diberikan yaitu evidience.pcap
2. Cari dengan menggunakan **filter protocal FTP**, Cari yang mencurigakan / beda (disini saya menemunkan dari info) USER h3ngk3rTzy dan PASS S!l3ncE

<img src="https://i.ibb.co/9GspYbS/Screenshot-2024-04-03-132108.png" alt="Screenshot-2024-04-03-132108" border="0">

3. Caba masuk dari salah satu jaringan tadi misal **dari IP 10.30.3.1 dengan info USER h3ngk3rTzy** dengan klik kanan lalu **kilk follow TCP stream**

<img src="https://i.ibb.co/dpj16M6/Screenshot-2024-04-03-132211.png" alt="Screenshot-2024-04-03-132211" border="0">

4. Coba masukan USER dan PASS yang ada di dalam jaringan tersebut ke Soal *nc 10.15.40.20 10007* dengan **format USER:username dan PASS:password**

<img src="https://i.ibb.co/ncJd660/Screenshot-2024-04-03-132434.png" alt="Screenshot-2024-04-03-132434" border="0">

5. Jika benar maka soal akan memberikan kunci jawaban dari CTF tersebut (JARKOM2024{s3curE_uR_FtP_xTfkXcpfQAVHRA9})


# 2. Soal Praktikum Jarkom Nomer 2

Pradityo mencoba mengembangkan server ftp, tetapi seseorang mencoba melakukan bruteforce login, bisakah Anda menganalisis apa yang terjadi?

Dikerjakan Dengan *nc 10.15.40.20 10004*

## Pengerjaan

1. Cari dengan filter protocol FTP
2. Temukan kata kata **yang paling mencurigakan / paling beda sendiri** misal di **Nomer 2** ini adalah *PASS m4y_th3_Kn!fe_ch1p_&_sh4tter* yang di dapat dari protocal FTP dan IP 10.30.3.4

<img src="https://i.ibb.co/5TPGp6c/Screenshot-275.png" alt="Screenshot-275" border="0">

Ketika di buka dengan **klik kanan lalu klik follow TCP Stream**

<img src="https://i.ibb.co/Z8pZFpv/Screenshot-276.png" alt="Screenshot-276" border="0">
