# Assignment 04

*Group members*
- Ariel Itsbat Nurhaq (10231018) (Problem #4)
- Noviansyah (10231072) (Problem #5)
- Muchlis Wahyu Saputra (10231054) (Problem #1)
- Eka Kusuma Yanti (10231036) (Problem #2)
- Verina Rahma Dinah (10231090) (Problem #3)

## Problem 1 (Combinatorial)
Dalam suatu acara makan bersama, terdapat 3 meja bundar yang dapat diisi
oleh 4 orang. Total tamu yang data sebanyak 15 orang. 
Ada berapa banyak cara menyusun lokasi tempat duduk tamu-tamu tersebut?

### Answer

# Penyelesaian Masalah Penempatan Tamu di Meja Bundar

Pertama-tama, kita harus memilih 4 orang dari 15 untuk duduk di meja pertama, lalu 4 dari 11 orang yang tersisa untuk meja kedua, dan 4 dari 7 orang yang tersisa untuk meja ketiga. Ini adalah kombinasi, yang dapat dihitung menggunakan rumus:

$$C(n, k) = \frac{n!}{k!(n-k)!}$$

di mana $$n$$ adalah jumlah total tamu dan $$k$$ adalah jumlah tamu per meja. Jadi, jumlah cara untuk menempatkan tamu di meja adalah:

$$C(15, 4) * C(11, 4) * C(7, 4)$$

Kemudian, untuk setiap meja, karena meja tersebut bundar, ada $$(k-1)!$$ cara untuk mengatur $$k$$ tamu di sekitar meja. Jadi, jumlah cara untuk mengatur tamu di sekitar meja adalah $$(4-1)!$$ untuk setiap meja.

Namun, kita masih memiliki 3 tamu yang belum ditempatkan. Tamu-tamu ini bisa duduk di salah satu dari 3 meja, jadi ada $$3^3 = 27$$ cara untuk menempatkan tamu-tamu ini.

Jadi, jumlah total cara untuk menyusun tempat duduk tamu adalah hasil kali dari tiga bagian ini. Jadi, jawabannya adalah:

$$C(15, 4) * C(11, 4) * C(7, 4) * (4-1)! * 3^3$$

Mari kita hitung nilai dari masing-masing bagian:

- $$C(15, 4) = \frac{15!}{4!(15-4)!} = 1365$$
- $$C(11, 4) = \frac{11!}{4!(11-4)!} = 330$$
- $$C(7, 4) = \frac{7!}{4!(7-4)!} = 35$$
- $$(4-1)! = 3! = 6$$
- $$3^3 = 27$$

Jadi, jumlah total cara adalah:

$$1365 * 330 * 35 * 6 * 27 = 2541214200$$

Jadi, ada *2,541,214,200 cara* untuk menyusun tempat duduk tamu. Harap dicatat bahwa ini adalah perhitungan teoritis dan mungkin tidak praktis dalam situasi nyata. Misalnya, dalam situasi nyata, kita mungkin perlu mempertimbangkan preferensi tamu, seperti siapa yang ingin duduk di sebelah siapa.
tur tamu di sekitar meja adalah $$(4-1)!$$ untuk setiap meja.

## Problem 2 (Graph 1a)
Suatu graf dikatakan graf bipartite jika kita dapat memisahkan 
himpunan simpul-simpulnya (vertices), $V$ menjadi dua himpunan simpul $V_1$ 
dan $V_2$ yang mana tidak ada busur (edge) sama sekali yang menghubungkan
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

1. Graf tersebut bukan termasuk **Bipartite** karena <i>v</i><sub>3</sub> merupakan titik tengah dari simpul-simpul yang ada dan setiap simpul tidak memiliki sudut penghubung sehingga tidak memenuhi syarat dari **Graf Bipartite**.

2. Graf tersebut bukan termasuk **Bipartite** karena jika kita memisahakan simpulnya. Misalkan <i>V</i><sub>1</sub> = { <i>v</i><sub>1</sub>, <i>v</i><sub>2</sub>, <i>v</i><sub>5</sub> } dan <i>V</i><sub>2</sub> = { <i>v</i><sub>3</sub>, <i>v</i><sub>4</sub>}, maka <i>v</i><sub>1</sub> dan <i>v</i><sub>3</sub> masih terhubung oleh busur dan tidak sesuai dengan definisi **Bipartite**.

3. Termasuk **Graf Bipartite**, karena jika memisahkan simpulnya misal <i>V</i><sub>1</sub> = { <i>v</i><sub>1</sub>, <i>v</i><sub>6</sub>, <i>v</i><sub>5</sub> } dan <i>V</i><sub>2</sub> = { <i>v</i><sub>2</sub>, <i>v</i><sub>3</sub>, <i>v</i><sub>4</sub> }, yang mana dimasing-masing himpunan <i>V</i></sub>1</sub>  dan <i>V</i><sub>2</sub> tidak ada busur penghubung dan pada setiap simpul memiliki setidaknya satu busur penghubung.

## Problem 3 (Graph 1b)
Tentukan dan jelaskan apakah mungkin melalui semua busur hanya sekali
di graf di bawah ini

<img src="../figures/euler-path-Q1.png" width=100>

### Answer

Tidak bisa, karena graf tersebut bukan lintasan euler yang dimana akan ada lintasan yang dilewati dua kali. Bukan lintasan euler dikarenakan terdapat simpul berderajat ganjil yang lebih dari dua

## Problem 4 (Graph coloring)

Lakukan pewarnaan pada setiap simpul graf di bawah ini sedemikian rupa
sehingga tidak ada dua simpul yang terhubung oleh suatu busur memiliki
warna yang sama. Himpunan warna yang dapat dipakai:
(Merah, Jingga, Kuning, Hijau, Biru, Ungu, dst.)

<img src="../figures/graph-coloring-Q1.png" width=300>

Ada berapa jumlah warna paling sedikit yang digunakan untuk mewarnai
graf diatas?

### Answer

| NODE | V2 | V5 | V6 | V1 | V4 | V7 | V3 | V8 | V9 |
| ------- | ------- | ------- | ------- | ------- | ------- | ------- | ------- | ------- | -------- |
| ARC  | 6  | 6  | 5  | 4  | 4  | 4  | 3  | 3  | 3 |
| COLOUR | Green | Orange | Green | Orange | Pink | Pink | Pink | Pink | Orange  |

Dari tabel diatas menunjukkan warna yang paling sedikit sebanyak 3 warna, yaitu hijau, oranye, dan pink

Attachment (image) : https://drive.google.com/drive/folders/1gdtug1C85Kupxrb7mkl1ppmzapU4tZS2?usp=drive_link

## Problem 5 (Tree)

Berikut adalah papan dari ultimate Tic-Tac-Toe berukuran 2x2.

<img src="../figures/ultimate-tix-tac-toe-2x2-Q1.drawio.png" width=300>

Jika pemain pertama memulai dengan simbol X. Tentukan dan gambarkan 
diagram tree untuk 
kemungkinan dua langkah pertama dimulai dari papan kosong.
Petunjuk: Gunakan drawio untuk menggambar langkah papan lebih cepat.

### Answer

Attachment (image) : https://drive.google.com/drive/folders/1Rp2MvmfGiPjoDJhcLiycOxbRjM-jEv-e