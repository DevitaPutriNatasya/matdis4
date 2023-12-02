# Assignment 04

**Group members**
- Indah Nur Fortuna (10231044) (Problem 1)
- Ahmad Daffa Alfattah (10231008) (Problem 2)
- Rayhan Iqbal (10231080) (Problem 3)
- Cintya Widhi Astuti(10231026) (Problem 4)
- Muhammad Dani (10231062) (Problem 5)

## Problem 1 (Combinatorial)
Dalam suatu acara makan bersama, terdapat 3 meja bundar yang dapat diisi
oleh 4 orang. Total tamu yang data sebanyak 15 orang. 
Ada berapa banyak cara menyusun lokasi tempat duduk tamu-tamu tersebut?

### Answer
$
C(n, r) = \frac{n!}{r!(n-r)!}
$

$C(15, 4)$
x
$C(11, 4)$
x
$C(7, 4)$

$ = \frac{15!}{4!(15-4)!}$
x
$ \frac{11!}{4!(11-4)!}$
x
$ \frac{7!}{4!(7-4)!}$

$ = \frac{15!}{4!x11!}$
x
$ \frac{11!}{4!x7!}$
x
$ \frac{7!}{4!x3!}$

$ = \frac{15!}{4!x4!x4!x3!}$

$ = \frac{15x14x13x12}{4x3x2x1}$
x
$ \frac{11x10x9x8}{4x3x2x1}$
x
$ \frac{7x6x5x4}{4x3x2x1}$


$ = 1365 $
x
$ 330 $
x
$ 35 $

$ = 16,072,250 $

Jadi, banyaknya cara untuk menyusun lokasi tempat duduk tamu - tamu tersebut adalah 16,072,250 cara.


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

### Menentukan Jalur Euler dalam Graf

Untuk menentukan apakah mungkin melalui semua busur hanya sekali di dalam suatu graf, kita dapat menggunakan konsep jalur Euler. Jalur Euler adalah jalur yang melalui semua busur (atau tepi) graf tepat satu kali tanpa mengangkat pensil dari kertas.

Untuk menentukan apakah suatu graf memiliki jalur Euler, kita dapat memeriksa derajat setiap simpul (node) di dalam graf. Derajat simpul adalah jumlah tepi yang terhubung ke simpul tersebut. Dalam konteks jalur Euler, aturan dasar adalah sebagai berikut:

1. Jika terdapat lebih dari dua simpul dengan derajat ganjil (jumlah tepi yang terhubung ke simpul tersebut adalah ganjil), maka graf tersebut tidak memiliki jalur Euler.

2. Jika semua simpul memiliki derajat genap, graf tersebut memiliki jalur Euler. Jalur Euler dapat dimulai dari dan berakhir di simpul mana pun.

3. Jika terdapat tepat dua simpul dengan derajat ganjil, maka graf tersebut memiliki jalur Euler. Jalur Euler harus dimulai dari salah satu simpul dengan derajat ganjil dan berakhir di simpul yang lain.

Mariku coba periksa graf pada gambar di atas. Asumsikan bahwa A, B, C, dan D mewakili simpul-simpul graf tersebut.

### Derajat setiap simpul:

- Derajat(A) = 2
- Derajat(B) = 3
- Derajat(C) = 2
- Derajat(D) = 3

Terdapat dua simpul dengan derajat ganjil (B dan D), sehingga graf tersebut memiliki jalur Euler. Oleh karena itu, mungkin untuk melalui semua busur hanya sekali di graf tersebut.

### Jalur Euler yang mungkin:

B - D - C - B - A - C

## Problem 4 (Graph coloring)

Lakukan pewarnaan pada setiap simpul graf di bawah ini sedemikian rupa
sehingga tidak ada dua simpul yang terhubung oleh suatu busur memiliki
warna yang sama. Himpunan warna yang dapat dipakai:
(Merah, Jingga, Kuning, Hijau, Biru, Ungu, dst.)

<img src="../figures/graph-coloring-Q1.png" width=300>

Ada berapa jumlah warna paling sedikit yang digunakan untuk mewarnai
graf diatas?

### Answer
| Simpul | V2 | V5 | V6 | V1 | V4 | V7 | V3 | V8 | V9 |
|----------|------|-----|-----|-----|-----|-----|-----|-----|-----|
|Busur   | 6 | 6 | 5 | 4 | 4 | 4 | 3 | 3 | 3 |
|Warna | Hijau | Biru | Hijau | Biru | Jingga  | Jingga | Jingga | Jingga | Ungu |

Jadi, Jumlah warna yang digunakan untuk mewarnai graf tersebut adalah 3 Warna


## Problem 5 (Tree)

Berikut adalah papan dari _ultimate Tic-Tac-Toe_ berukuran 2x2.

<img src="../figures/ultimate-tix-tac-toe-2x2-Q1.drawio.png" width=300>

Jika pemain pertama memulai dengan simbol X. Tentukan dan gambarkan 
diagram tree untuk 
kemungkinan dua langkah pertama dimulai dari papan kosong.
_Petunjuk_: Gunakan drawio untuk menggambar langkah papan lebih cepat.

### Answer
[Colour Graf](https://drive.google.com/file/d/1nxV4Gi2pPAEQKizUIK7l5VgefoOSIMnz/view?usp=sharing)

