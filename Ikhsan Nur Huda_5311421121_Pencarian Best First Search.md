Nama		: Ikhsan Nur Huda
NIM		  : 5311421121
Rombel 	: 3

PRAKTIKUM 6 BEST FIRST SEARCH
PERMAINAN TIC TAC TOE


# Tugas
Tuliskan semua Java Code, kemudian pelajari code nya, dan ubahkan beberapa bagian untuk melihat perubahannya

# Penyelesaian
Pada praktikum ke-6 ini, kita akan mempelajari cara membuat sebuah permainan tic tac toe. Saat pemain pertama mengklik salah satu kotak, kotak tersebut akan ditandai dengan tanda silang. Pemain kedua akan mencoba menghalangi pemain pertama agar tidak berhasil membuat tiga tanda silang berturut-turut dalam posisi vertikal, horizontal, atau diagonal. Permainan ini akan mencapai kondisi tujuan (goal state) ketika salah satu pemain telah berhasil menyusun tanda mereka secara berurutan, baik secara vertikal, horizontal, atau diagonal.

# Implementasi Permainan Tic Tac Toe Menggunakan Graphical User Interface (GUI)
Permainan ini dibuat menggunakan Java Swing, yang terdiri dari tiga kelas Java dan tiga pendeklarasian enum. Enam file tersebut ditulis secara terpisah, tetapi semua disimpan dalam folder yang sama, yaitu folder TicTacToe seperti berikut ini.

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-1.png)

1. GameState.Java


![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-2.png)

- GameState adalah sebuah file yang berisi enumerasi GameState. Enum ini digunakan untuk mengidentifikasi berbagai kondisi dalam permainan.
- Terdapat empat nilai dalam enumerasi ini:
   1. PLAYING: Menunjukkan bahwa permainan sedang berlangsung, dan belum ada pemenang atau hasil seri.
   2. DRAW: Menunjukkan bahwa permainan berakhir dalam hasil seri.
   3. CROSS_WON: Menunjukkan bahwa pemain yang menggunakan tanda "CROSS" (X) telah memenangkan permainan.
   4. NOUGHT_WON: Menunjukkan bahwa pemain yang menggunakan tanda "NOUGHT" (O) telah memenangkan permainan.


2. Seed.Java

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-3.png)

- Seed adalah sebuah file yang berisi enumerasi Seed. Enum ini digunakan untuk menggambarkan isi dari sel-sel pada papan permainan Tic Tac Toe.
- Terdapat tiga nilai dalam enumerasi ini:
   1. EMPTY: Mengindikasikan bahwa sel pada papan permainan masih belum terisi.
   2. CROSS: Mengindikasikan bahwa sel diisi dengan simbol "CROSS" (X).
   3. NOUGHT: Mengindikasikan bahwa sel diisi dengan simbol "NOUGHT" (O).


3. State.Java

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-4.png)

- Dalam kode di atas, terdapat enumerasi State yang digunakan untuk mendefinisikan berbagai kondisi permainan dalam Tic Tac Toe:
   1. PLAYING: Mengindikasikan bahwa permainan masih berlangsung, dan belum ada pemenang.
   2. DRAW: Mengindikasikan bahwa permainan berakhir dengan hasil seri karena tidak ada pemenang.
   3. CROSS_WON: Mengindikasikan bahwa pemain yang menggunakan tanda "CROSS" (X) telah berhasil memenangkan permainan.
   4. NOUGHT_WON: Mengindikasikan bahwa pemain yang menggunakan tanda "NOUGHT" (O) telah berhasil memenangkan permainan.

4. Cell.Java

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-5%20cell.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-6%20board.png)

Kelas Cell dalam permainan Tic Tac Toe adalah bagian kunci yang digunakan untuk merepresentasikan setiap sel atau kotak pada papan permainan. Peran utama kelas ini adalah untuk menggambar sel-sel pada papan permainan dan memberikan informasi apakah sel tersebut kosong, berisi "CROSS", atau "NOUGHT". Ini sangat penting dalam memvisualisasikan permainan kepada pemain dan memastikan bahwa permainan berjalan dengan lancar.

- Seed content: Variabel ini digunakan untuk menyimpan isi dari sel tersebut, yang bisa berupa Seed.EMPTY, Seed.CROSS, atau Seed.NOUGHT.
- int row, col: Variabel ini digunakan untuk menyimpan baris dan kolom dari sel tersebut.
- Konstruktor Cell(int row, int col): Konstruktor ini digunakan untuk memulai sel dengan baris dan kolom yang ditentukan dan mengosongkan isinya dengan memanggil metode clear().
- Metode clear(): Metode ini digunakan untuk mengosongkan sel dengan mengatur content ke Seed.EMPTY.
- Metode paint(Graphics g): Metode ini digunakan untuk menggambar sel pada papan permainan.
    - Pertama, jika content adalah Seed.CROSS, kode akan menggambar garis-garis simbol "CROSS" (X) dengan mengatur warna menjadi merah (Color.RED) dan menggunakan Graphics2D untuk menggambar dua garis yang membentuk simbol "X".
    - Kedua, jika content adalah Seed.NOUGHT, kode akan menggambar simbol "NOUGHT" (O) dengan mengatur warna menjadi biru (Color.BLUE) dan menggambar lingkaran (oval) pada sel sesuai dengan ukuran simbol.

5. Board.Java

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-7%20cell.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-8%20board.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-9%20board.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-10%20board.png)

Kelas Board dalam permainan Tic Tac Toe bertugas mewakili papan permainan dan mengelola sel-selnya. Peran utama kelas Board adalah mengurus seluruh aspek papan permainan, termasuk penggambaran sel-sel dengan benar, serta menentukan apakah permainan berakhir dengan hasil seri atau ada pemenang.

- Cell[][] cells: Ini adalah array 2D yang berisi sel-sel pada papan permainan, dan papan permainan keseluruhannya terdiri dari sel-sel ini.
- Konstruktor Board(): Konstruktor ini bertanggung jawab untuk memulai papan permainan. Ia menginisialisasi array 2D untuk sel-sel papan dan menginisialisasi masing-masing sel dengan baris dan kolom yang sesuai menggunakan objek Cell.
- Metode init(): Metode ini digunakan untuk mengosongkan semua sel di papan permainan, memungkinkan inisialisasi ulang untuk memulai permainan baru.
- Metode isDraw(): Metode ini mengembalikan true jika permainan berakhir dengan hasil seri, yaitu saat tidak ada sel kosong (Seed.EMPTY) tersisa di papan permainan. Ini memeriksa semua sel di papan dan memeriksa apakah ada sel kosong yang tersisa.
- Metode hasWon(Seed seed, int seedRow, int seedCol): Metode ini mengembalikan true jika pemain dengan simbol (seed) yang diberikan telah memenangkan permainan setelah menempatkan simbolnya di sel tertentu (seedRow, seedCol). Ini memeriksa apakah pemain telah berhasil menyusun tiga simbol yang sama berurutan dalam baris, kolom, atau diagonal yang melewati sel yang ditentukan.
- Metode paint(Graphics g): Metode ini digunakan untuk menggambar papan permainan beserta sel-selnya.
   - Pertama, kode menggambar garis-garis grid pada papan dengan warna abu-abu (Color.GRAY).
   - Selanjutnya, kode melakukan iterasi melalui semua sel pada papan dan memanggil metode paint() pada masing-masing sel untuk menggambar simbolnya.

6. GameMain.Java

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-11%20main%20Game.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-12.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-13.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-14.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-15.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-16.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-17.png)
   
Kelas GameMain dalam permainan Tic Tac Toe bertugas sebagai antarmuka grafis (GUI) untuk permainan. Kelas GameMain ini adalah elemen integral dalam implementasi permainan Tic Tac Toe, menggabungkan komponen-komponen permainan, mengelola logika permainan, dan menangani tampilan GUI. Ketika pemain mengklik papan permainan, permainan akan merespons dengan memperbarui tampilan layar dan memberikan pesan status.

- Kode ini mendefinisikan berbagai konstanta yang digunakan dalam permainan, seperti jumlah baris dan kolom pada papan permainan, ukuran sel, lebar garis grid, dan sebagainya.
- Konstruktor digunakan untuk menginisialisasi antarmuka pengguna (UI) dan komponen permainan.
- MouseListener didefinisikan untuk menangani klik mouse pada papan permainan.
- StatusBar (JLabel) diinisialisasi untuk menampilkan pesan status permainan.
- Tata letak dan dimensi panel permainan diatur.
- Papan permainan diinisialisasi dengan memanggil initGame().
- Metode initGame(): Ini digunakan untuk mengosongkan konten papan permainan dan mengatur currentState ke PLAYING. Seluruh sel di papan diatur sebagai kosong (EMPTY), dan pemain pertama adalah "CROSS."
- Metode updateGame(Seed theSeed, int row, col): Metode ini bertanggung jawab memperbarui keadaan permainan setelah pemain dengan simbol "theSeed" meletakkan simbolnya di sel (row, col). Ini memeriksa apakah pemain tersebut telah memenangkan permainan atau apakah permainan berakhir dengan seri. Jika ya, currentState diubah sesuai.
- Metode paintComponent(Graphics g): Metode ini menggambar komponen permainan di dalam panel. Ini meminta papan permainan (board) untuk menggambar dirinya sendiri dan menampilkan pesan status di status bar sesuai dengan currentState.
- Metode main(String[] args): Metode main yang berfungsi sebagai titik awal program. Ini menjalankan kode konstruksi GUI dalam thread Event-Dispatching untuk keamanan thread dan membuat serta menampilkan frame permainan.

##### Hasil Program dan Percobaan
Percobaan pemain pertama "CROSS" (X) = MENANG

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-20%20menang%20X.png)

Percobaan pemain kedua "NOUGHT" (O) = MENANG

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-19%20menang%200.png)

Percobaan KALAH untuk Kedua Pemain

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/6-18%20kalah.png)

##### Analisa Hasil Percobaan

Dalam permainan Tic Tac Toe, goal state adalah situasi di mana salah satu pemain berhasil menempatkan tiga simbol (X atau O) secara berturut-turut dalam satu baris, kolom, atau salah satu dari dua diagonal. Dalam kasus ini, pemain yang mencapai goal state ini akan menjadi pemenang. Selain itu, goal state juga tercapai ketika seluruh sel pada papan permainan terisi, dan tidak ada pemain yang memenangkan permainan. Hal ini menunjukkan bahwa permainan berakhir dalam keadaan seri (draw). Dalam kedua situasi ini, GameState akan diatur sesuai, yaitu CROSS_WON atau NOUGHT_WON jika ada pemenang, atau DRAW jika permainan berakhir seri.
Jadi, dalam permainan Tic Tac Toe, ada dua goal state utama: pemain memenangkan permainan atau permainan berakhir dengan seri. Tujuan pemain adalah mencapai goal state pertama, sementara tujuan lainnya adalah menghindari goal state kedua saat bermain agar tidak berakhir seri.

##### Analisa Algoritma Best First Search dalam Permainan Tic Tac Toe 

Tic Tac Toe dan algoritma pencarian Best-First Search (BFS) memiliki keterkaitan yang erat dalam konteks kecerdasan buatan dan permainan. Berikut adalah gambaran hubungannya:

- Pohon pencarian dalam Tic Tac Toe akan tumbuh seiring berjalannya permainan. Pemain akan mencoba berbagai langkah dan menjelajahi cabang-cabang pohon pencarian untuk mencapai goal state yang menguntungkan, yaitu kemenangan atau seri.
- Tic Tac Toe merupakan permainan papan untuk dua pemain yang bersifat deterministik, yang berarti setiap langkah yang diambil oleh pemain dapat memprediksi keadaan permainan selanjutnya. Karena itu, permainan ini dapat diabstraksikan dan dimodelkan sebagai pohon pencarian, di mana setiap simpul dalam pohon mewakili satu keadaan permainan yang mungkin.
- Best-First Search dalam konteks pencarian permainan adalah algoritma yang digunakan untuk menemukan langkah terbaik dalam suatu permainan. Algoritma ini mencoba menjelajahi pohon pencarian dengan memilih simpul yang dianggap paling menjanjikan berdasarkan fungsi evaluasi atau heuristik tertentu. Dalam permainan Tic Tac Toe, fungsi evaluasi tersebut umumnya mempertimbangkan seberapa menguntungkan atau merugikan keadaan permainan saat ini bagi pemain, serta sejauh mana keadaan saat ini mendekati goal state (kemenangan atau seri).
- Heuristik adalah elemen kunci dalam Best-First Search untuk Tic Tac Toe. Ini adalah fungsi evaluasi yang memberikan skor pada setiap keadaan permainan yang dianalisis. Fungsi ini harus dirancang dengan baik sehingga dapat membedakan keadaan yang menguntungkan dan merugikan bagi pemain, sehingga Best-First Search dapat memutuskan langkah yang optimal.
- Implementasi Best-First Search dalam Tic Tac Toe melibatkan pencarian melalui pohon pencarian untuk menentukan langkah terbaik yang harus diambil oleh pemain pada titik tertentu. Ini melibatkan pemilihan simpul dengan nilai evaluasi terbaik, yang akan membawa pemain menuju kemenangan atau menghindari kekalahan.
