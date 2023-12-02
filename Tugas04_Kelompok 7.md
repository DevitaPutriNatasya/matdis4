# Assignment 04

**Group members**
- Andini Permata Dewanti (10231014) (Problem #1)
- Djaky Abbyyu Fauzan Timumum (10231032) (Problem #2)
- Krishandy Dhanysa Pratama (10231050) (Problem #5)
- Nazwa Amelia Zahra (10231068) (Problem #4)
- Salsabila Putri Zahrani (10231086) (problem #3)


## Problem 1 (Combinatorial)
Dalam suatu acara makan bersama, terdapat 3 meja bundar yang dapat diisi oleh 4 orang. Total tamu yang didata sebanyak 15 orang. Ada berapa banyak cara menyusun lokasi tempat duduk tamu-tamu tersebut? 

### Answer
Jumlah cara yang dapat digunakan untuk mengatur tempat duduk 15 orang tamu pada 3 meja bundar yang masing-masing dapat diisi dengan 4 orang yaitu, dengan menggunakan rumus Kombinasi 

C (n,r) = n! </sup>/<sub>r!(n-r)!</sub>

n = Jumlah tamu yang didata

r = Kapasitas tamu pada satu meja

 1. Mengatur meja pertama :

 C (15,4) = 15! </sup>/<sub>4! (15-4)!</sub> = =15! </sup>/<sub>4!&times;11! </sub>= 1365

 Jadi, pada meja pertama terdapat 1365 cara untuk mengatur tempat duduk 15 orang tamu.

 2. Mengatur meja kedua :

 karena pada meja pertama sudah diisi dengan 4 orang, maka pada meja kedua  ini tersisa 11 orang yang akan diatur tempat duduknya.

 C (11,4) = 11! </sup>/<sub>4! (11-4)!</sub> = =11! </sup>/<sub>4!&times;7! </sub>= 330

 Jadi, pada meja kedua terdapat 330 cara untuk mengatur duduk 11 orang tamu.

 3. Mengatur meja ketiga :

 Pada meja ketiga tersisa 7 orang yang akan diatur tempat duduknya.

 C (7,4) = 7! </sup>/<sub>4! (7-4)!</sub> = =7! </sup>/<sub>4!&times;3! </sub>= 35

 Jadi, pada meja ketiga terdapat 35 cara untuk mengatur duduk 7 orang tamu.

 Tersisa 3 orang tamu yang belum mendapatkan tempat duduk, 3 orang tersebut bisa memilih tempat duduk diantara 3 meja yang disediakan. 

Total cara menyusun tempat duduk 15 orang tamu pada 3 meja bundar yang dapat diisi dengan 4 orang yaitu 1365&times;330&times;35 = 15.765.750 cara

## Problem 2 (Graph 1a)
Suatu graf dikatakan graf _bipartite_ jika kita dapat memisahkan 
himpunan simpul-simpulnya (_vertices_), $V$ menjadi dua himpunan simpul $V_1$ 
dan $V_2$ yang mana tidak ada busur (_edge_) sama sekali yang menghubungkan
dua simpul di dalam satu himpunan yang sama.

## Answer
1.<b>Bukan Bipartite</b>,Karena <i>v</i><sub>3</sub> merupakan titik tengah dari semua simpul dan setiap simpul tidak memiliki sudut penghubung sehingga tidak memenuhi syarat graf <b>Bipartite</b>.

2.<b>Bukan Bipartite</b>,Karena jika kita memisahakan simpulnya.Misal <i>V</i><sub>1</sub> = { <i>v</i><sub>1</sub>,<i>v</i><sub>2</sub>,<i>v</i><sub>5</sub> } dan <i>V</i><sub>2</sub> = { <i>v</i><sub>3</sub>,<i>v</i><sub>4</sub>,}.Maka <i>v</i><sub>1</sub> dan <i>v</i><sub>3</sub> masih terhubung dengan busur

3.<b>Bipartite</b>,Jika memisahkan simpulnya <i>V</i><sub>1</sub> = { <i>v</i><sub>1</sub>,<i>v</i><sub>6</sub>,<i>v</i><sub>5</sub> },dan <i>V</i><sub>2</sub> = { <i>v</i><sub>2</sub>,<i>v</i><sub>3</sub>,<i>v</i><sub>4</sub> } tiap himpunan tidak memiliki busur penghubung dan tiap simpul memiliki satu busur penghubung

## Problem 3 (Graph 1b)
Tentukan dan jelaskan apakah mungkin melalui semua busur hanya sekali
di graf di bawah ini

<img src="../figures/euler-path-Q1.png" width=100>

### Answer
Tidak bisa, karena lintasan tersebut menggunakan lintasan euler yang mana pasti akan ada satu busur yang dilewati sebanyak lebih dari satu kali. 

## Problem 4 (Graph coloring)

Lakukan pewarnaan pada setiap simpul graf di bawah ini sedemikian rupa
sehingga tidak ada dua simpul yang terhubung oleh suatu busur memiliki
warna yang sama. Himpunan warna yang dapat dipakai:
(Merah, Jingga, Kuning, Hijau, Biru, Ungu, dst.)

<img src="../figures/graph-coloring-Q1.png" width=300>

Ada berapa jumlah warna paling sedikit yang digunakan untuk mewarnai
graf diatas?

### Answer

<img src="graph-hasil-coloring.png" width=300>

|simpul | v1 | v4  |  v2  |  v8  | v3  |   v5   |   v6  |   v7  |   v9  |
|-------|----|-----|------|------|-----|--------|-------|-------|-------|
|derajat| 6  |  5  |  4   |   4  |  3  |   3    |   3   |   3   |   3   |
|warna  | merah  | jingga   |  jingga    |  merah    |  kuning   |   kuning  |   jingga    |  kuning     |  kuning     |

x(G)= 3 

## Problem 5 (Tree)

Berikut adalah papan dari _ultimate Tic-Tac-Toe_ berukuran 2x2.

<img src="../figures/ultimate-tix-tac-toe-2x2-Q1.drawio.png" width=300>

Jika pemain pertama memulai dengan simbol X. Tentukan dan gambarkan 
diagram tree untuk 
kemungkinan dua langkah pertama dimulai dari papan kosong.
_Petunjuk_: Gunakan drawio untuk menggambar langkah papan lebih cepat.

### Answer

link :
 https://drive.google.com/file/d/11oOvjUUktEcUOiWTn8HVnxbUsCTaHGaq/view?usp=drivesdk