# Jarkom-Modul-1-D01-2021

## Soal 1



## Soal 6
Diminta untuk mencari username dan password ketika melakukan login ke FTP Server <br>
Maka filternya adalah
```
ftp.request.command == "USER" || ftp.request.command == "PASS"
```
seperti berikut
<img src="Img/6_1.png">

Dan didapatkan username serta password sebagai berikut
```
Username : secretuser
```
```
Password : aku.pengen.pw.aja
```

## Soal 7
Ada 500 file zip yang disimpan ke FTP Server. Diminta untuk menyimpan dan membuka file pdf.(Hint = nama pdf-nya "Real.pdf") <br>
Adapun step nya adalah sebagai berikut <br>
1. Masukkan filter 
```
ftp-data contains “Real.pdf”
```
<img src="Img/7_1.png">

<br>
2. Lalu klik kanan pada hasil yang paling atas setelah itu klik Follow lalu TCP Scream <br>
<img src="Img/7_2.png">
<br>
3. Lalu ubah Show Data As menjadi Raw
<img src="Img/7_3.png">
<br>
4. Lalu klik save as Real.pdf
<img src="Img/7_4.png">
<br>
Berikut ini merupakan isi dari Real.pdf<br>
<img src="Img/7_5.png">


## Soal 8
Diminta untuk mencari paket yang menunjukkan pengambilan dari file FTP tersebut. <br>
Karena perintahnya merupakan pengambilan maka memakai filter **RETR** <br>
Berikut ini adalah filternya
```
  ftp contains “RETR”
```
<img src="Img/8.png">

## Soal 9
Dari paket-paket yang menuju FTP terdapat indikasi penyimpanan beberapa file. <br>
Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". <br>
Simpan dan buka file tersebut!

 1. Maka kita memerlukan filter untuk menemukan file secret.zip tersebut dengan memasukkan filter sebagai berikut
```
 ftp-data.command == "STOR secret.zip"
```
<img src="Img/9_1.png">

  2.Lalu klik kanan menuju `Follow lalu TCP Scream`
 <img src="Img/9_2.png"> 
  3. Setelah itu ubah Show Data > Raw
  <img src="Img/9_3.png"> 
  <br>
  4. Lalu simpan file tersebut dengan nama "secret.zip" <br>
    <img width="439" alt="9_4" src="https://user-images.githubusercontent.com/73489643/134729811-f47e1b48-0176-40e5-83a3-5fb30ddf8681.png">
  <br>
  5. Maka berikut, ini merupakan tampilan isi dari file "secret.zip" yang memerlukan password untuk membukanya <br>
 <img width="605" alt="9_5" src="https://user-images.githubusercontent.com/73489643/134730508-b533295f-4235-4347-9d0c-a0017f09ace3.png">

## Soal 10
Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! <br>
Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"! <br>
1.
  Maka untuk membuka dan mencari password tersebut, maka digunakan filter sebagai berikut
 ```
   ftp-data.command == "STOR history.txt"
 ```
  <img src="Img/10_1.png">
<br>
2.
  Lalu pada history bash dari history.txt terdapat file `bukanapaapa.txt` yang menunjukkan bahwa file tersebut merupakan passwordnya. <br>
  Untuk mendapatkan file tersebut maka filternya adalah :
 ```
   ftp-data.command == "STOR bukanapaapa.txt"
 ```
  <img width="825" alt="10_2" src="https://user-images.githubusercontent.com/73489643/134732098-2733e1b2-5a05-4f49-a8e7-b736c792f926.png">
 <br>
3.
  Lalu klik kanan menuju `Follow lalu TCP Scream`
  <img src="Img/10_3.png">

 4.
  Setelah itu ubah Show Data > Raw <br>
  <img width="546" alt="10_4" src="https://user-images.githubusercontent.com/73489643/134731579-c9d50d57-ebff-462a-90f9-c195fd4c1136.png">
 
5. Setelah itu simpan file bernama history.txt
<img width="403" alt="10_5" src="https://user-images.githubusercontent.com/73489643/134732249-c0691fea-d09d-4907-b209-6092f17d43e6.png">

6. Berikut ini merupakan isi dari history.txt, yang merupakan password untuk membuka file secret.zip.
<img width="258" alt="10_6" src="https://user-images.githubusercontent.com/73489643/134732319-6bb6be04-2894-4ab4-bd1a-66543f7c37b3.png">

7. Berikut ini merupakan isi dari file Wanted.pdf
<img src="Img/10_7.png">
  
  
  
## Soal 11
Diminta untuk menfilter sehingga wireshark hanya mengambil paket yang berasal dari "port 80!".<br><br>
Step : Ketik `src port 80` pada filter di wireshark.
<img src="Img/11_1.PNG">
<img src="Img/11_2.PNG">

Catatan : untuk hasil dari `port 80` yaitu berupa kosongan dikarenakan pada port tersebut tidak terjadinya protokol `http` yang berjalan.

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
Diminta untuk menfilter sehingga wireshark hanya mengambil paket yang berasal dari "ip kalian!".<br><br>
Step :
1. Buka "Command Prompt" dan ketik `ipconfig`
<img src="Img/15_1.PNG">
<img src="Img/15_2.PNG">

2. Copy "ip address" pada `IPv4 Address : 192.168.0.113` pada `ipconfig`, dan paste ke filter expression pada wireshark dengan command `src host 192.168.0.113`.
<img src="Img/15_3.PNG">
<img src="Img/15_4.PNG">

Catatan : Untuk pengambilan "ip address" disesuaikan dengan "ip address" sendiri.
