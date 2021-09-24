# Jarkom-Modul-1-D01-2021

## Soal 1


## Soal 11
Diminta untuk menfilter sehingga wireshark hanya mengambil paket yang berasal dari "port 80!".<br><br>
Step : Ketik `src port 80` pada filter di wireshark.
<img src="Img/11_1.PNG">
<img src="Img/11_2.PNG">

Untuk hasil dari `port 80` yaitu kosong dikarenakan pada port tersebut tidak terjadinya protokol `http` yang berjalan.

## Soal 12
Diminta untuk menfilter sehingga wireshark hanya mengambil paket yang mengandung "port 21!".<br><br>
Step : Ketik `port 21` pada filter di wireshark.
<img src="Img/12_1.PNG">
<img src="Img/12_2.PNG">

## Soal 13
Diminta untuk menfilter sehingga wireshark hanya menampilkan paket yang menuju "port 443!".<br><br>
Step : Ketik `dst port 443` pada filter di wireshark.
<img src="Img/13_1.PNG">
<img src="Img/13_2.PNG">

## Soal 14
Diminta untuk menfilter sehingga wireshark hanya mengambil paket yang tujuannya ke "kemenag.go.id!".<br><br>
Step : Ketik `dst host kemenag.go.id` pada filter di wireshark.
<img src="Img/14_1.PNG">
<img src="Img/14_2.PNG">

Catatan : untuk menjalankan filter `dst host kemenag.go.id`, jangan lupa untuk membuka juga website dari "kemenag.go.id". Jika tidak,
maka program tidak berjalan atau paket yang akan diambil masih berupa kosongan.

## Soal 15
Diminta untuk menfilter sehingga wireshark hanya mengambil paket yang berasal dari "ip kalian!"
Step :
1. Buka "Command Prompt" dan ketik `ipconfig`
<img src="Img/15_1.PNG">
<img src="Img/15_2.PNG">
2. Copy ip address pada `IPv4 Address : 192.168.0.113` pada `ipconfig`, dan paste ke filter expression pada wireshark dengan command `src host 192.168.0.113`.
<img src="Img/15_3.PNG">
<img src="Img/15_4.PNG">
