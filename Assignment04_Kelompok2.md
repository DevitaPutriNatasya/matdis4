
# Assignment 04

**Group members**
- Raditya Yudianto NIM 10231076  $(Problem 5)$
- Ade Ayu Kholifah Putri NIM 10231004  $(Problem 1)$
- Az-Zahra Atikah Nurhaliza NIM 10231022  $(Problem 2)$
- Muhammad Ariel Rayhan NIM 10231058  $(Problem  3)$
- Hita Higueta Pancaro NIM 10231040  $(Problem  3)$
- Zahwa Hanna Dwi Putri NIM 10231092 $(Problem  4)$

## Problem 1 (Combinatorial)
Dalam suatu acara makan bersama, terdapat 3 meja bundar yang dapat diisi
oleh 4 orang. Total tamu yang data sebanyak 15 orang. 
Ada berapa banyak cara menyusun lokasi tempat duduk tamu-tamu tersebut?

### Answer
Untuk menghitung jumlah cara menyusun lokasi tempat duduk tamu-tamu tersebut, kita dapat menggunakan rumus untuk mendistribusikan objek yang tidak dapat dibedakan ke dalam kotak yang dapat dibedakan. Rumusnya diberikan oleh:

$[\binom{n+r-1}{r-1}]$

di mana $(n)$ adalah jumlah objek (tamu) dan $(r)$ adalah jumlah kotak (meja). Dalam hal ini, terdapat 15 tamu dan 3 meja, sehingga rumusnya menjadi:

$[\binom{15+3-1}{3-1} = \binom{17}{2} = \frac{17!}{2!15!} = 136
]$

Oleh karena itu, terdapat 136 cara untuk menyusun tamu-tamu tersebut di 3 meja bundar.

## Problem 2 (Graph 1a)
Suatu graf dikatakan graf _bipartite_ jika kita dapat memisahkan 
himpunan simpul-simpulnya (_vertices_), $V$ menjadi dua himpunan simpul $V_1$ 
dan $V_2$ yang mana tidak ada busur (_edge_) sama sekali yang menghubungkan
dua simpul di dalam satu himpunan yang sama.

Sebagai contoh:
<table>
  <tr>
    <td><b>Graf</b></td>
    <td><b>Penjelasan</b></td>
  </tr>
  <tr>
    <td><img src="../figures/bipartite-ex-01.png" width=800></td>
    <td> <b>Bipartite</b> karena kita dapat memisahkan simpul-simpulnya menjadi dua himpunan 
    <i>V</i><sub>1</sub> = {
      <i>v</i><sub>1</sub>, 
      <i>v</i><sub>3</sub>, 
      <i>v</i><sub>5</sub> } dan 
    <i>V</i><sub>2</sub> = {
      <i>v</i><sub>2</sub>, 
      <i>v</i><sub>4</sub>, 
      <i>v</i><sub>6</sub> } yang mana dimasing-masing himpunan 
    <i>V</i></sub>1</sub>  dan <i>V</i><sub>2</sub> tidak ada busur penghubung dan setiap anggota <i>V</i><sub>1</sub> dan <i>V</i><sub>2</sub> memiliki setidaknya satu busur penghubung.</td>
  </tr>
  <tr>
    <td><img src="../figures/bipartite-ex-02.png" width=800></td> 
    <td>Bukan bipartite, karena bagaimanapun kita memisahkan simpul-simpulnya, selalu ada penghubung antara simpul dalam satu himpunan yang sama. Misal kita buat <i>V</i><sub>1</sub> = { <i>v</i><sub>1</sub> } dan 
    <i>V</i><sub>2</sub> = { <i>v</i><sub>2</sub>, <i>v</i><sub>3</sub> }. 
    Maka sangatlah jelas <i>v</i><sub>2</sub> dan <i>v</i><sub>3</sub> masih terhubung oleh busur dan tidak sesuai dengan definisi bipartite.</td>
  </tr>
</table>
Dari penjelasan di atas tentukan dan jelaskan apakah graf dibawah ini bipartite atau bukan:

1. <img src="../figures/bipartite-Q1.png" width=200 style="vertical-align:top">

2. <img src="../figures/bipartite-Q2.png" width=250 style="vertical-align:top">

3. <img src="../figures/bipartite-Q3.png" width=300 style="vertical-align:top">


### Answer

1.<b>Bukan Bipartite</b>,Karena <i>v</i><sub>3</sub> merupakan titik tengah dari semua simpul dan setiap simpul tidak memiliki sudut penghubung sehingga tidak memenuhi syarat graf <b>Bipartite</b>.

2.<b>Bukan Bipartite</b>,Karena jika kita memisahakan simpulnya.Misal <i>V</i><sub>1</sub> = { <i>v</i><sub>1</sub>,<i>v</i><sub>2</sub>,<i>v</i><sub>5</sub> } dan <i>V</i><sub>2</sub> = { <i>v</i><sub>3</sub>,<i>v</i><sub>4</sub>,}.Maka <i>v</i><sub>1</sub> dan <i>v</i><sub>3</sub> masih terhubung dengan busur

3.<b>Bipartite</b>,Jika memisahkan simpulnya <i>V</i><sub>1</sub> = { <i>v</i><sub>1</sub>,<i>v</i><sub>6</sub>,<i>v</i><sub>5</sub> },dan <i>V</i><sub>2</sub> = { <i>v</i><sub>2</sub>,<i>v</i><sub>3</sub>,<i>v</i><sub>4</sub> } tiap himpunan tidak memiliki busur penghubung dan tiap simpul memiliki satu busur penghubung

## Problem 3 (Graph 1b)
Tentukan dan jelaskan apakah mungkin melalui semua busur hanya sekali
di graf di bawah ini

<img src="../figures/euler-path-Q1.png" width=100>

### Answer
tidak, dikarenakan graf yang ditaunjukan di atas tidak termasuk lintasan euler. Suatu graf dapat dikategorikan sebagai lintasan euler bila titik dengan derajat ganjil banyaknya kurang dari tiga, sedangkan derjat ganjil yang ditunjukan pada graf diatas menampilkan 4 titik yang memiliki derajat ganjil

## Problem 4 (Graph coloring)

Lakukan pewarnaan pada setiap simpul graf di bawah ini sedemikian rupa
sehingga tidak ada dua simpul yang terhubung oleh suatu busur memiliki
warna yang sama. Himpunan warna yang dapat dipakai:
(Merah, Jingga, Kuning, Hijau, Biru, Ungu, dst.)

<img src="../figures/graph-coloring-Q1.png" width=300>

Ada berapa jumlah warna paling sedikit yang digunakan untuk mewarnai
graf diatas?

### Answer
## Problem 4 (Graph coloring)

Lakukan pewarnaan pada setiap simpul graf di bawah ini sedemikian rupa
sehingga tidak ada dua simpul yang terhubung oleh suatu busur memiliki
warna yang sama. Himpunan warna yang dapat dipakai:
(Merah, Jingga, Kuning, Hijau, Biru, Ungu, dst.)

<img src="../figures/graph-coloring-Q1.png" width=300>

Ada berapa jumlah warna paling sedikit yang digunakan untuk mewarnai
graf diatas?

### Answer

| vertex, $v_i$  |  deg ($v_i$) |  
|---|---|
| $v_1$ |4|  
| $v_2$ |3| 
| $v_3$ |6|
| $v_4$ |4|
| $v_5$ |3|
| $v_6$ |3|
| $v_7$ |5|
| $v_8$ |4|
| $v_9$ |6|

|$v_3$|$v_9$|$v_7$|$v_1$|$v_4$|$v_8$|$v_2$|$v_5$| $v_6$|
|---|---|---|---|---|---|---|---|---|
|$C_1$|$C_2$|$C_2$|$C_1$|$C_3$|$C_3$|$C_3$|$C_1$|$C_3$|

[img]
https://drive.google.com/file/d/1_CEoDNg3LO1N8tqlkHt6WUUV3tM0IJOc/view?usp=drivesdk

Jumlah warna paling sedikit yang digunakan untuk memberikan warna pada graf adalah 3 warna.

## Problem 5 (Tree)

Berikut adalah papan dari _ultimate Tic-Tac-Toe_ berukuran 2x2.

<img src="../figures/ultimate-tix-tac-toe-2x2-Q1.drawio.png" width=300>

Jika pemain pertama memulai dengan simbol X. Tentukan dan gambarkan 
diagram tree untuk 
kemungkinan dua langkah pertama dimulai dari papan kosong.
_Petunjuk_: Gunakan drawio untuk menggambar langkah papan lebih cepat.

### Answer

link jawaban dalam diagram pohon tertera pada link berikut :

https://drive.google.com/file/d/1_BMdV3T3JY67We6Rur8Xw8OFEtfJnCaX/view?usp=drivesdk