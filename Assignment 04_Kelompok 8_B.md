# Assignment 04

**Anggota Kelompok**
- Anjas Geofany Diamare_10231016  (Soal 1)
- Dzakwan Fatih Fadhilah_10231034  (Soal 2)
- Meiske Handayani_10231052  (Soal 3)
- Nilam Ayu NandaStari Romdoni_10231070  (Soal 4)
- Tiya Mitra Ayu Purwanti_10231088  (Soal 5)

## Soal 1
Dalam suatu acara makan bersama, terdapat 3 meja bundar yang dapat diisi
oleh 4 orang. Total tamu yang data sebanyak 15 orang. 
Ada berapa banyak cara menyusun lokasi tempat duduk tamu-tamu tersebut?

### Jawaban
$
C(n, r)  = \frac{n!}{r!(n-r)!}
$

$C(15, 4)$
x
$ C(11, 4)$
x
$ C(7, 4) $

$ = \frac{15!}{4!(15-4)!}$
x
$ \frac{11!}{4!(11-4)!}$
x
$\frac{7!}{4!(7-4)!}$

$= 1365 $
x
$ 330 $
x
$35$

$=16,072,250$

Jadi, terdapat 16,072,250 cara untuk menyusun lokasi tempat duduk tamu-tamu tersebut.

## Soal 2
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

### Jawaban
1. Graf pertama termasuk <B>Bipartite</B> karena kita dapat membagi simpul - simpulnya menjadi dua himpunan yang saling ekslusif: himpunan {<i>V</i><sub>1</sub>, <i>V</i><sub>2</sub>, <i>V</i><sub>4</sub> , <i>V</i><sub>5</sub>} dan himpunan {<i>V</i><sub>3</sub>}. Setiap sisi dalam graf ini menghubungkan simpul dari himpunan satu ke himpunan - himpunan lainnya.

2. Graf kedua bukan termasuk <B>Bipartite</B> karena kita tidak bisa membagi simpul - simpulnya menjadi dua himpunan yang saling ekslusif. Di sini {<i>V</i><sub>1</sub>, <i>V</i><sub>2</sub>, <i>V</i><sub>3</sub> , <i>V</i><sub>4</sub>, <i>V</i><sub>5</sub>} membentuk siklus, yang membuatnya tidak bisa dibagi simpulnya menjadi 2 himpunan.

3. Graf ketiga termasuk <B>Bipartite</B> karena kita dapat membagi simpul- simpulnya menjadi 2 himpunan yang saling ekslusif: himpunan <i>V</i><sub>1</sub> = { <i>V</i><sub>1</sub>, <i>V</i><sub>6</sub>, <i>V</i><sub>5</sub> }, { <i>V</i><sub>1</sub>, <i>V</i><sub>3</sub>, <i>V</i><sub>5</sub> } dan <i>V</i><sub>2</sub> = { <i>V</i><sub>2</sub>, <i>V</i><sub>6</sub>, <i>V</i><sub>4</sub> }, { <i>V</i><sub>2</sub>, <i>V</i><sub>3</sub>, <i>V</i><sub>4</sub> }.


## Soal 3
Tentukan dan jelaskan apakah mungkin melalui semua busur hanya sekali
di graf di bawah ini

<img src="../figures/euler-path-Q1.png" width=100>

### Jawaban
Jawabannya tidak bisa. Karena lintasan ini menggunakan lintasan euler, yang dimana akan ada satu lintasan yang hanya bisa dilewati dua kali, tidak bisa satu kali. Lintasan tersebut adalah lintasan yang berada di tengah, yang berbentuk lingkaran, kita harus memutar agar bisa melewati jalur tersebut.

## Soal 4
Lakukan pewarnaan pada setiap simpul graf di bawah ini sedemikian rupa
sehingga tidak ada dua simpul yang terhubung oleh suatu busur memiliki
warna yang sama. Himpunan warna yang dapat dipakai:
(Merah, Jingga, Kuning, Hijau, Biru, Ungu, dst.)

<img src="../figures/graph-coloring-Q1.png" width=300>

Ada berapa jumlah warna paling sedikit yang digunakan untuk mewarnai
graf diatas?

### Jawaban
|   Simpul   |  V2  |   V5   |  V6  |   V1   |   V4  |   V7  |   V3  |   V8  |   V9   |
|------------|------|--------|------|--------|-------|-------|-------|-------|--------|
|    Busur   |   6  |    6   |   5  |    4   |   4   |   4   |   3   |   3   |    3   |
|            | e1, e2, e3, e4, e5, e6 | e2, e7, e8, e9, e10, e11 | e8, e12, e13, e14, e15 | e5, e13, e16, e17 | e6, e7, e14, e16 | e3, e11, e12, e18 | e1, e10, e17 | e9, e15, e19 | e4, e18, e19 |
|    Warna   | Biru | Jingga | Biru | Jingga | Merah | Merah | Merah | Merah | Jingga |

Jadi, jumlah warna yang digunakan paling sedikit untuk mewarnai graf tersebut adalah 3 Warna. Untuk gambar graf nya :
[Colour Graf](https://drive.google.com/drive/folders/10i6RDCx2869O-X8HEGA5He565TT9TnZy?usp=drive_link)

## Soal 5
Berikut adalah papan dari _ultimate Tic-Tac-Toe_ berukuran 2x2.

<img src="../figures/ultimate-tix-tac-toe-2x2-Q1.drawio.png" width=300>

Jika pemain pertama memulai dengan simbol X. Tentukan dan gambarkan 
diagram tree untuk kemungkinan dua langkah pertama dimulai dari papan kosong.
_Petunjuk_: Gunakan drawio untuk menggambar langkah papan lebih cepat.

### Jawaban
[Diagram Tree](https://drive.google.com/drive/folders/10i6RDCx2869O-X8HEGA5He565TT9TnZy?usp=drive_link)