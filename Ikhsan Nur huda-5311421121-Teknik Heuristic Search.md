Ikhsan Nur Huda

5311421121

TEKNIK ELEKTRO 


MODUL 5 TEKNIK HEURISTIC SEARCH

1.Pelajari class EightPuzzleSearch, EightPuzzleSpace, dan Node. 

Parafraza dari teks yang diberikan:

A.Kelas EightPuzzleSearch:

1.Kelas EightPuzzleSearch bertanggung jawab untuk menemukan solusi dalam permasalahan 8-puzzle.

2.Kelas ini menggunakan vektor 'open' untuk menyimpan simpul-simpul yang perlu dijelajahi dan vektor 'closed' untuk menyimpan simpul-simpul yang sudah dijelajahi.

3.Kelas ini memiliki dua fungsi heuristik, yaitu 'h1Cost()' dan 'h2Cost()', untuk menghitung biaya simpul berdasarkan dua heuristik yang berbeda.

-Metode 'hCost(Node node)' digunakan untuk memilih heuristik yang akan digunakan (h1 atau h2).

Metode:

1.Metode 'getBestNode(Vector nodes)' mengembalikan simpul dengan biaya terendah dari vektor simpul yang diberikan.

2.Metode 'getPreviousCost(Node node)' mengembalikan biaya simpul jika simpul tersebut ada dalam daftar 'open' atau 'closed'.
 
3.Metode 'printPath(Vector path)' mencetak jalur dari akar ke tujuan.
 
4.Metode 'run()' adalah metode utama yang menjalankan algoritma pencarian.

B.Kelas EightPuzzleSpace:

1.Kelas ini mendefinisikan keadaan awal dan tujuan dalam permasalahan 8-puzzle serta menghasilkan simpul-simpul penerus.

2Metode 'getRoot()' mengembalikan keadaan awal sebagai simpul.

3.Metode 'getGoal()' mengembalikan keadaan tujuan sebagai simpul.

4.Metode 'getSuccessors(Node parent)' menghasilkan simpul-simpul penerus berdasarkan perpindahan ubin kosong.

5.Metode 'transformState()' digunakan untuk membuat simpul baru dengan menukar dua ubin dalam keadaan.

C.Kelas Node:

1.Kelas Node mewakili sebuah simpul atau keadaan dalam ruang pencarian, khususnya dalam konteks penyelesaian permasalahan 8-puzzle.

2.Bidang 'state' adalah array yang berisi 9 bilangan bulat yang mewakili keadaan atau posisi ubin dalam papan permainan.
 
3.Bidang 'cost' adalah biaya yang terkait dengan mencapai simpul ini.

4.Bidang 'parent' adalah referensi ke simpul induk dalam pohon pencarian.

5.Bidang 'successors' adalah vektor yang berisi simpul-simpul anak.

Metode:

1.Konstruktor 'Node(int s[], Node parent)' menginisialisasi sebuah simpul dengan keadaan tertentu dan simpul induk.

2.Metode 'toString()' mengembalikan representasi string dari keadaan simpul.

3.Metode 'equals(Object node)' membandingkan dua simpul untuk memeriksa apakah mereka memiliki keadaan yang sama.

4.Metode 'getPath(Vector<Node> v)' mengembalikan jalur dari akar ke simpul saat ini dalam bentuk vektor.

5.Metode 'getPath()' mengembalikan jalur dalam vektor baru.

Dalam kelas tersebut, kode mengimplementasikan algoritma pencarian berdasarkan heuristik untuk menemukan solusi dalam permasalahan 8-puzzle dengan cara menjelajahi berbagai kemungkinan keadaan, menilai biaya dengan menggunakan heuristik, dan memilih simpul-simpul yang paling menjanjikan untuk dianalisis lebih lanjut. Proses pencarian akan berlanjut hingga solusi ditemukan atau semua kemungkinan sudah dieksplorasi.

Hasil Pogram 

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/5.1.png)

Keadaan Awal: Papan puzzle terdiri dari sembilan ubin yang tersusun dalam matriks 3x3. Ubin dengan angka 0 mewakili ubin kosong yang dapat digerakkan ke atas, bawah, kiri, atau kanan untuk mencapai tujuan.

tahap 1: Pada tahap pertama, ubin kosong dipindahkan dari posisi (3,3) ke posisi (2,3).

tahap 2: Selanjutnya, ubin kosong dipindahkan dari posisi (2,3) ke posisi (2,2).

tahap 3: Ubin kosong dipindahkan dari posisi (2,2) ke posisi (1,2).

tahap 4 (Tujuan Tercapai): Pada langkah terakhir, ubin kosong dipindahkan dari posisi (1,2) ke posisi (1,1).

Dengan demikian, masalah 8-puzzle berhasil dipecahkan dari keadaan awal ke keadaan tujuan dalam lima langkah. Setiap pergerakan ubin kosong dalam setiap langkah mendekatkan keadaan menuju tujuan, dan akhirnya mencapai keadaan tujuan yang benar.

2.Ubahlah initial dan goal state dari program di atas sehingga bentuk initial dan goal statenya Gambar 8. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1. 

Hasil Pogram 

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/5.2.png)


Tahap 1: Memindahkan ubin kosong dari (3,3) ke (3,2)

Tahap 2: Memindahkan ubin kosong dari (3,2) ke (3,1)

Tahap 3: Memindahkan ubin kosong dari (3,1) ke (2,1)

Tahap 4: Memindahkan ubin kosong dari (2,1) ke (2,2)

Tahap 5: Memindahkan ubin kosong dari (2,2) ke (1,2)

Tahap 6: Memindahkan ubin kosong dari (1,2) ke (1,3)

Tahap 7: Memindahkan ubin kosong dari (1,3) ke (2,3)

Tahap 8: Memindahkan ubin kosong dari (2,3) ke (2,2)

Tahap 9: Memindahkan ubin kosong dari (2,2) ke (2,1)

Tahap 10: Memindahkan ubin kosong dari (2,1) ke (1,1)

Tahap 11: Memindahkan ubin kosong dari (1,1) ke (1,2)

Tahap 12: Memindahkan ubin kosong dari (1,2) ke (1,3)

Tahap 13: Memindahkan ubin kosong dari (1,3) ke (2,3)

Tahap 14: Memindahkan ubin kosong dari (2,3) ke (2,2)

Tahap 15: Memindahkan ubin kosong dari (2,2) ke (2,1)

Tahap 16: Memindahkan ubin kosong dari (2,1) ke (1,1)

Tahap 17: Memindahkan ubin kosong dari (1,1) ke (1,2)

Tahap 18: Memindahkan ubin kosong dari (1,2) ke (1,3), sehingga sesuai dengan tujuan yang diinginkan.

Analisis perbandingan dengan solusi poin 1 sebagai berikut:

A.Jumlah Langkah:

1.Dalam solusi pertama, hanya diperlukan 5 langkah untuk mencapai keadaan tujuan.
2.Sebaliknya, dalam solusi poin 2, dibutuhkan 18 langkah untuk mencapai keadaan tujuan.

B.Kompleksitas:

1.Solusi pertama adalah solusi yang lebih sederhana dan efisien karena memerlukan lebih sedikit langkah.

2.Di sisi lain, solusi poin 2 lebih kompleks dan memerlukan lebih banyak langkah untuk mencapai tujuan. Ini dikarenakan keadaan awal yang berbeda, sehingga perlu menjalani jalur pencarian yang lebih panjang.

Dengan demikian, kedua solusi berhasil mencapai tujuan mereka, tetapi terdapat perbedaan dalam kompleksitas dan jumlah langkah yang dibutuhkan. Solusi pertama adalah solusi yang lebih sederhana dan efisien, sementara solusi poin 2 memerlukan lebih banyak langkah karena perbedaan keadaan awal. Hal ini menunjukkan bagaimana perbedaan dalam keadaan awal dapat memengaruhi jalur pencarian dalam konteks masalah 8-puzzle.

3.Ubahlah initial dan goal state dari program di atas sehingga bentuk initial dan goal statenya Gambar 5.9. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1 dan 2.

Hasil Pogram 

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/5.3.png)


Kondisi awal yaitu pada 

153 

468

270 

Penggeseran pada setiap tahap dalam solusi ini adalah sebagai berikut:

Tahap 1: Awalnya, ubin kosong (0) berada di posisi (3, 1), dan langkah pertama adalah menggesernya ke kanan, sehingga ubin 0 berada di posisi (3, 2).

Tahap 2: Selanjutnya, ubin 0 digeser ke kanan lagi ke posisi (3, 3).

Tahap 3: Langkah ketiga menggeser ubin 0 ke atas ke posisi (2, 3).

Tahap 4: Langkah berikutnya menggeser ubin 0 ke kiri ke posisi (2, 2).

Tahap 5: Ubin 0 digeser ke atas lagi ke posisi (1, 2).

Tahap 6: Langkah selanjutnya menggeser ubin 0 ke kiri ke posisi (1, 1).

Tahap 7: Ubin 0 digeser ke atas lagi ke posisi (2, 1).

Tahap 8: Langkah berikutnya menggeser ubin 0 ke kanan ke posisi (2, 2).

Tahap 9: Ubin 0 digeser ke bawah ke posisi (2, 3).

Tahap 10: Langkah selanjutnya menggeser ubin 0 ke kanan ke posisi (2, 2).

Tahap 11: Ubin 0 digeser ke atas ke posisi (1, 2).

Tahap 12: Langkah berikutnya menggeser ubin 0 ke kiri ke posisi (1, 1).

Tahap 13: Ubin 0 digeser ke atas lagi ke posisi (2, 1).

Tahap 14: Langkah selanjutnya menggeser ubin 0 ke kanan ke posisi (2, 2).

Tahap 15: Ubin 0 digeser ke atas ke posisi (1, 2).

Tahap 16: Langkah berikutnya menggeser ubin 0 ke kiri ke posisi (1, 1).

Tahap 17: Ubin 0 digeser ke atas lagi ke posisi (1, 2).

Tahap 18: Terakhir, ubin 0 digeser ke kanan ke posisi (1, 3), sehingga mencapai tujuan akhir.

Analisis Perbandingan dengan Solusi 1,2 DAN 3

Solusi 1:

1.Solusi pertama adalah yang paling sederhana dengan hanya memerlukan 18 langkah untuk mencapai tujuan.

2.Proses penyelesaian berlangsung sangat cepat, dengan total waktu eksekusi sekitar 1 detik.

Solusi 2:

1.Solusi kedua juga memerlukan 18 langkah untuk mencapai tujuan dan memiliki prinsip urutan langkah yang sama dengan solusi pertama.

2.Waktu eksekusi yang singkat, dengan total waktu sekitar 1 detik.

Solusi 3:

1.Sebaliknya, solusi ketiga adalah yang paling kompleks dengan memerlukan 38 langkah untuk mencapai tujuan.

2.Waktu eksekusi yang jauh lebih lama dibandingkan dengan solusi sebelumnya, dengan total waktu sekitar 52 menit.

Kesimpulan Analisis Perbandingan dengan Cara Pengerjaan Nomor 1,2 dan 3

Kedua solusi pertama dan kedua adalah solusi yang sangat sederhana karena proses penyelesaiannya berjalan sangat cepat, dengan total waktu eksekusi sekitar 1 detik.
Sementara itu, ketika menggunakan cara pengerjaan nomor 3, dibutuhkan total waktu 52 menit yang jauh lebih lama.

4.Ubahlah initial dan goal state dari program di atas sehingga bentuk initial dan goal statenya Gambar 5.10. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1, 2, dan 3. 

Hasil Pogram 

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/5.4.png)



Penggeseran setiap tahap dalam solusi ini adalah sebagai berikut:

Tahap pertama, ubin kosong (0) berada di posisi (3, 3), yang terletak di sudut kanan bawah papan permainan.

Tahap kedua, menggeser ubin 0 ke kiri, sehingga berada di posisi (3, 2).

Tahap ketiga, ubin 0 digeser ke kiri lagi ke posisi (3, 1).

Tahap keempat, menggeser ubin 0 ke atas, sehingga berada di posisi (2, 1).

Tahap kelima, ubin 0 digeser ke kanan ke posisi (2, 2).

Tahap berikutnya, menggeser ubin 0 ke atas lagi, sehingga berada di posisi (1, 2).

Tahap berikutnya, ubin 0 digeser ke kiri ke posisi (1, 1).

Tahap ke-8, menggeser ubin 0 ke atas lagi ke posisi (2, 1).

Tahap berikutnya, ubin 0 digeser ke kanan ke posisi (2, 2).

Tahap selanjutnya, menggeser ubin 0 ke atas lagi, sehingga berada di posisi (1, 2).

Tahap berikutnya, ubin 0 digeser ke kiri ke posisi (1, 1).

Tahap ke-12, menggeser ubin 0 ke atas lagi ke posisi (2, 1).

Tahap berikutnya, ubin 0 digeser ke kanan ke posisi (2, 2).

Tahap berikutnya, menggeser ubin 0 ke atas lagi ke posisi (1, 2).

Tahap berikutnya, ubin 0 digeser ke kanan ke posisi (1, 3).

Terakhir, ubin 0 digeser ke kanan lagi ke posisi (2, 3) sehingga mencapai tujuan akhir yang merupakan urutan yang sesuai.

Analisis Perbandingan:

Solusi 1 dan 4 berhasil mencapai tujuan dengan jumlah langkah yang lebih sedikit dan dalam waktu yang sangat cepat (kurang dari 1 detik).

Solusi 2 dan 3 memerlukan lebih banyak langkah dan waktu yang signifikan untuk mencapai tujuan.

Solusi 2 adalah yang terpanjang dalam hal jumlah langkah.

Solusi 3 memerlukan waktu yang sangat lama (52 menit) untuk menyelesaikan masalah, bahkan jika jumlah langkahnya mirip dengan Solusi 2.

Dari analisis ini, dapat disimpulkan bahwa Solusi 1 dan Solusi 4 adalah yang paling efisien, sementara Solusi 3 adalah yang paling lambat dan memerlukan waktu yang sangat lama. Solusi 2 berada di tengah-tengah dalam hal jumlah langkah, tetapi masih memerlukan waktu yang signifikan dibandingkan dengan Solusi 1 dan Solusi 4.

5.Ubahlah initial dan goal state dari program dan class-class di atas sehingga bentuk initial dan goal statenya Gambar 5.11. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state.

Kondisi Awal 

int ex[] = {D, B, E, A, F, G, H, C, 0}; // initial state 

Kondisi Akhir/Tujuan 

int state[] = {A, H, G, B, 0, F, C, D, E}; // goal state


Penggeseran setiap tahap dalam solusi ini adalah sebagai berikut:

Tahap 1: Geser ubin C ke atas, sehingga keadaannya menjadi "DBEAF0HCCG".

Tahap 2: Geser ubin G ke kiri, sehingga keadaannya menjadi "DBEAFGH0CC".

Tahap 3: Geser ubin H ke kiri, sehingga keadaannya menjadi "DBEAFH0GCC".

Tahap 4: Geser ubin C ke atas, sehingga keadaannya menjadi "DBEAF0HCFC".

Tahap 5: Geser ubin F ke kanan, sehingga keadaannya menjadi "DBEAFHF0CC".

Tahap 6: Geser ubin E ke kanan, sehingga keadaannya menjadi "DBEAF0EFCH".

Tahap 7: Geser ubin C ke atas, sehingga keadaannya menjadi "DBEAFCE0FH".

Tahap 8: Geser ubin D ke kiri, sehingga keadaannya menjadi "DBEAF0CDEF".

Tahap 9: Geser ubin E ke atas, sehingga keadaannya menjadi "DBE0FCEAHF".

Tahap 10: Geser ubin F ke kanan, sehingga keadaannya menjadi "DBEFCE0AHF".

Tahap 11: Geser ubin A ke kanan, sehingga keadaannya menjadi "DBEF0CEAHF".

Tahap 12: Geser ubin H ke kanan, sehingga keadaannya menjadi "DBEFCEAH0F".

Tahap 13: Geser ubin H ke kanan, sehingga keadaannya menjadi "DBEFCEA0HF".

Tahap 14: Geser ubin F ke kanan, sehingga keadaannya menjadi "DBEFCE0AHF".

Tahap 15: Geser ubin C ke atas, sehingga keadaannya menjadi "DBE0CEFAHF".

Tahap 16: Geser ubin E ke atas, sehingga keadaannya menjadi "DBECE0FAHF".

Tahap 17: Geser ubin F ke kanan, sehingga keadaannya menjadi "DBECEF0AHF".

Tahap 18: Geser ubin A ke kanan, sehingga mencapai keadaan tujuan "AHGB0FCDE".

Dengan melakukan 18 tahap tersebut, Anda dapat mencapai keadaan tujuan "AHGB0FCDE" dari keadaan awal "DBEAFGHC0" dalam permainan 8-puzzle.

