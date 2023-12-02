# Assignment 04

**Group members**
- Riqqah Khalda Karina (10231082) (Problem 3)
- Alfiani Dwiyuniarti (10231010) (Problem 2 dan 4)
- David Ramadhani Pangestu (10231028) (Problem )
- Muhammad Irvany Saputra (10231064) (Problem 1)
- Irwan Maulana (10231046) (Problem 5)

## Problem 1 (Combinatorial)
Dalam suatu acara makan bersama, terdapat 3 meja bundar yang dapat diisi
oleh 4 orang. Total tamu yang data sebanyak 15 orang. 
Ada berapa banyak cara menyusun lokasi tempat duduk tamu-tamu tersebut?

### Answer
1. Pilih 4 tamu dari 15 untuk meja pertama:
   \[ C(15,4) = \frac{15!}{4!(15-4)!} \]

2. Pilih 4 tamu dari 11 untuk meja kedua:
   \[ C(11,4) = \frac{11!}{4!(11-4)!} \]

3. Pilih 4 tamu dari 7 untuk meja ketiga:
   \[ C(7,4) = \frac{7!}{4!(7-4)!} \]

Setelah itu menentukan meja untuk masing masing tamu: 

\[ 4! \]

Jumlah total cara untuk menyusun lokasi tempat duduk tamu-tamu tersebut adalah:

\[ C(15,4) \times C(11,4) \times C(7,4) \times 4! \]  \[= 10,359,600 \]

Jadi, ada 10,359,600 cara yang mungkin untuk menyusun lokasi tempat duduk tamu-tamu tersebut.

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

3.<b>Bipartite</b>,Jika memisahkan simpulnya <i>V</i><sub>1</sub> = { <i>v</i><sub>1</sub>,<i>v</i><sub>6</sub>,<i>v</i><sub>5</sub> },dan <i>V</i><sub>2</sub> = { <i>v</i><sub>2</sub>,<i>v</i><sub>3</sub>,<i>v</i><sub>4</sub> } tiap himpunan tidak memiliki busur penghubung dan tiap simpul memiliki satu busur penghubung

## Problem 3 (Graph 1b)
Tentukan dan jelaskan apakah mungkin melalui semua busur hanya sekali
di graf di bawah ini

<img src="../figures/euler-path-Q1.png" width=100>

### Answer
tidak bisa, untuk melewati graf tersebut harus melewati titik yang melingkar(ditengah) 2 kali agar dapat sampai di titik akhir. lintasan yang digunakan adalah lintasan euler, dimana terdapat 1 lintasan yang bisa dilewati 2 kali

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

Jadi, Jumlah warna yang digunakan untuk mewarnai graf tersebut adalah 3 Warna

## Problem 5 (Tree)

Berikut adalah papan dari _ultimate Tic-Tac-Toe_ berukuran 2x2.

<img src="../figures/ultimate-tix-tac-toe-2x2-Q1.drawio.png" width=300>

Jika pemain pertama memulai dengan simbol X. Tentukan dan gambarkan 
diagram tree untuk 
kemungkinan dua langkah pertama dimulai dari papan kosong.
_Petunjuk_: Gunakan drawio untuk menggambar langkah papan lebih cepat.

### Answer
![assignment5](Assignmentno5.drawio.png)