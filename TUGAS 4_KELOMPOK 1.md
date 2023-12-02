# Assignment 04

**Group members**
- Achmad Zaki Zaidan (10231002) (Problem 2)
- Putri Rahmawati (10231074) (Problem 3)
- Arya Wijaya S (10231020) (Problem 4)
- Firni Fauziah Ramadhini (10231038) (Problem 1)
- Muhammad Alif Setiawan (10231056) (Problem 5)

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
Gambar diagram tree
https://drive.google.com/file/d/1X7Q-G961h6BNpeGvHKJ7dyacbE0YEgS4/view?usp=sharing

Kemungkinan dua langkahnya
_XOX, XOO, XOX, XOO, XOXO, XOXX, XOOO, XOOX, XOXO, XOXX, XOOX, XOOO_