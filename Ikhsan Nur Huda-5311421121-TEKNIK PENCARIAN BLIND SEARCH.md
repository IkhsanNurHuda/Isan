IKHSAN NUR HUDA
/5311421121
/TEKNIK ELEKTRO 

MODUL 4 TEKNIK PENCARIAN BLIND SEARCH


                                              
1.Tentukan bagaimana algoritma BFS di atas dapat menentukan node ke 8, 6, dan 7. 2. 

Jawab:
    Algoritma Breadth-First Search (BFS) adalah sebuah algoritma pencarian yang digunakan dalam ilmu komputer untuk mengeksplorasi atau mencari informasi di dalam struktur data atau graf berdasarkan tingkat jarak atau kedalaman dari simpul awal. BFS digunakan untuk menemukan jalur terpendek dari satu simpul ke simpul lain dalam graf. Algoritma ini mengikuti proses berikut:
a. Pertama, simpul awal, yang dalam contoh ini adalah simpul 3, diinisialisasi dan dimasukkan ke dalam antrian.
b. Kemudian, simpul 3 akan mengeksplorasi simpul-simpul yang langsung terhubung dengannya, yaitu simpul 2 dan simpul 4, karena keduanya memiliki jarak 1 dari simpul 3. Selanjutnya, simpul 4 akan melanjutkan dengan mengeksplorasi simpul 1, 6, dan 5 yang terhubung dengan simpul 4.
c. Selanjutnya, simpul 5 akan mengeksplorasi simpul 8 dan 7.
d. Proses ini akan terus berlanjut hingga semua simpul yang terhubung dengan simpul awal telah diperiksa. Oleh karena itu, simpul-simpul 8, 6, dan 7 akan ditemukan dan diproses sesuai dengan aturan BFS.


![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/4.1.png)


Berdasarkan hasil di atas, BFS dimulai dari simpul (node) ke-3 (n3). Mari kita lihat langkah-langkahnya untuk mencapai node ke-8, 6, dan 7:
•	Node 3 (d=0): BFS dimulai dari simpul n3 dengan jarak 0.

•	Node 4 (d=1): n3 memiliki tetangga n4, sehingga BFS melanjutkan ke n4 dengan jarak 1.

•	Node 2 (d=1): n4 memiliki tetangga n2, tetapi n2 sudah diwarnai GRAY (dalam proses BFS), jadi BFS tidak melanjutkan ke n2.

•	Node 5 (d=2): n4 juga memiliki tetangga n5, yang belum diwarnai, jadi BFS melanjutkan ke n5 dengan jarak 2.

•	Node 6 (d=2):n5 memiliki tetangga n6, yang belum diwarnai, jadi BFS melanjutkan ke n6 dengan jarak 2.

•	Node 1 (d=2): n5 juga memiliki tetangga n1, yang belum diwarnai, jadi BFS melanjutkan ke n1 dengan jarak 2.

•	Node 7 (d=3): n6 memiliki tetangga n7, yang belum diwarnai, jadi BFS melanjutkan ke n7 dengan jarak 3.

•	Node 8 (d=3): n6 juga memiliki tetangga n8, yang belum diwarnai, jadi BFS melanjutkan ke n8 dengan jarak 3.



2.Ubahlah method static void main sehingga bentuk tree seperti Gambar 4.5 dapat dibentuk. Kemudian tentukan bagaimana algoritma BFS dapat menemukan node 5. 




![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/4.2%20(1).png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/4.2%20(2).png)

Hasil Program 

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/hasil%204.2.png)

Hasil tersebut memvalidasi kesesuaian antara hasil pohon yang dihasilkan oleh program dengan gambar 4.5.

a. Ketika mencari node 5, algoritma BFS pertama-tama dimulai dengan langkah memasukkan node 1 ke dalam antrian.

b. Kemudian, node 1 akan mengeksplorasi node 2 dan node 3, yang langsung terhubung ke node 1 atau berada pada kedalaman tingkat 1.

c. Selanjutnya, node 3 akan melanjutkan dengan mengeksplorasi node yang memiliki jarak atau kedalaman 2, dimulai dengan memeriksa node 4, node 5, node 6, dan node 7.

d. Setelah menemukan node 5, proses akan terus berlanjut sampai semua node yang terhubung dengan node awal telah diperiksa. Oleh karena itu, node 5 akan ditemukan dan diproses sesuai dengan aturan algoritma BFS.

3.Ubahlah method static void main sehingga bentuk tree seperti Gambar 4.6 dapat dibentuk. Kemudian tentukan bagaimana algoritma BFS dapat menemukan node 9. 


![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/4.3%20(1).png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/4.3%20(2).png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/4.3%20(3).png)

Hasil Program 

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Hasil%204.3.png)

Hasil tersebut mengonfirmasi kesesuaian antara pohon hasil yang diperoleh dari program dengan gambar 4.6.
a. Dalam mencari node 9, algoritma BFS memulai dengan langkah memasukkan node 1 ke dalam antrian.

b. Selanjutnya, node 1 akan mengeksplorasi node 2, node 3, dan node 4 yang langsung terhubung dengan node 1 atau memiliki kedalaman tingkat 1.

c. Kemudian, node 4 akan mengeksplorasi node yang memiliki kedalaman 2, dimulai dari pemeriksaan node 5, node 6, node 7, dan node 8.

d. Proses dilanjutkan oleh node 8, yang akan mengeksplorasi node 9. Setelah menemukan node 9, proses akan terus berlanjut untuk memeriksa node 10, node 11, dan node 12 hingga semua node yang terhubung dengan node awal telah diperiksa. Dengan demikian, pada akhir proses BFS, node 9 akan ditemukan dan diproses sesuai dengan aturan algoritma BFS.

4.Ubahlah kode program di atas sehingga bentuk tree seperti Gambar 4.7 dapat dibentuk. Kemudian tentukan bagaimana algoritma BFS dapat menemukan node C.

a. Di dalam kelas Node, untuk memungkinkan penerimaan huruf, perlu mengubah tipe data variabel 'data' dari semula 'int' menjadi 'String'.

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/4.4%20(1).png)

b.Kemudian pada Metode main, memasukkan nilai node dengan tipe data string sebagai berikut.
![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/4.4%20(2).png)

c.Selanjutnya pada Metode addEdge dan bfs, memasukkan logika pemrosesan data untuk tipe data String sebagai berikut.
![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/4.4%20(3).png)

d.Kemudian di-Run dan mendapatkan Hasil Program
![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Hasil%204.4.png)

Hasil tersebut mengonfirmasi bahwa pohon hasil yang diperoleh dari program sesuai dengan gambar 4.7.

• Dalam pencarian node 3 (C), algoritma BFS dimulai dengan memasukkan node 6 (F) ke dalam antrian.

• Kemudian, node 6 akan memeriksa node 2 (B) dan node 7 (G), yang terhubung langsung dengan node 6 atau memiliki kedalaman tingkat 1.

• Selanjutnya, node 7 akan memeriksa node yang memiliki kedalaman 2, dimulai dari pemeriksaan node 1 (A), node 4 (D), dan node 9 (I).

• Kemudian, node 9 akan memeriksa node 3 (C). Setelah menemukan node 3 (C), proses akan terus berlanjut untuk memeriksa node 5 (E) dan node 8 (H) hingga semua node yang terhubung dengan node awal telah diperiksa.

Dengan demikian, pada akhir proses BFS, node 3 (C) akan ditemukan dan diproses sesuai dengan aturan algoritma BFS.
