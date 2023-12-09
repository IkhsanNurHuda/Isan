### Kelomopok Mushroom ###
Anggota Kelompok : 
1. Paulus Rionaldo
2. Takbir Ahmad Fauzan
3. Mohamad Irfan
4. Ikhsan Nur Huda

Pada kesempatan ini kelompok kami akan membahas dataset mengenai mushoom, dibawah ini adalah gambar source codenya 

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%201.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%202.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%203.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%204.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%205.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%206.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%207.png)

1. Dalam konteks ini, terdapat 8 model neural network dalam satu populasi. (solusi dalam satu populasi model neural network)
   
2. Dalam konteks ini, 4 individu dengan fitness tertinggi akan dipilih sebagai orangtua. (banyak orangtua yang akan dipilih dari populasi pada setiap generasi untuk membentuk mating pool.)
   
3. Dalam konteks ini, algoritma akan dijalankan sebanyak 100 generasi untuk memperbaharui populasi model neural network. (banyak generasi atau iterasi yang akan dilakukan dalam algoritma genetika.)
   
4. Dalam konteks ini, sebanyak 20% dari bobot pada setiap keturunan akan mengalami perubahan nilai akibat mutasi. (persentase bobot pada setiap keturunan yang akan mengalami mutasi.)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%208.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%209.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%2010.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%2011.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%2012.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%2013.png)

![alt text](https://github.com/IkhsanNurHuda/Isan/blob/main/Mushroom%2014.png)



Dari code yang diberikan, implementasi algoritma genetika mencakup beberapa metode utama, yaitu metode seleksi (selection), metode crossover, metode mutasi, dan metode evaluasi fitness. Berikut adalah penjelasan masing-masing metode:
    
1. Metode Seleksi (Selection):
Metode seleksi digunakan untuk memilih individu-individu yang akan menjadi orangtua untuk generasi berikutnya. Pada code tersebut, metode seleksi yang digunakan disebut "mating pool selection".
Setiap individu memiliki peluang dipilih sebagai orangtua proporsional terhadap nilai fitnessnya. Semakin tinggi nilai fitness, semakin besar peluangnya untuk dipilih.

2. Metode Crossover:
Metode crossover digunakan untuk menggabungkan informasi genetik dari dua orangtua untuk menghasilkan keturunan baru. Pada code tersebut, metode crossover yang digunakan disebut "single-point crossover" atau "one-point crossover".

3. Metode Mutasi:
Metode mutasi digunakan untuk memperkenalkan variasi genetik ke dalam populasi dengan mengubah beberapa nilai gen secara acak. Pada code tersebut, metode mutasi yang digunakan disebut "random uniform mutation".

4. Hasil tingkat akurasi:
Pada percobaan pertama mengevaluasi sejauh mana evolusi telah meningkatkan performa model neural network pada data latih, dan mendapatkan hasil yaitu 0.849454801266268, tetapi setelah melakukan percobaan kedua dengan melakukan evaluasi pada data uji (x_test dan y_test) maka didapatkan hasil yaitu  0.844954881050041.
Hasilnya lebih akurat pada percobaan pertama yang telah dilakukan dengan menggunkan data sempel yang ada dibandingkan dengan pada percobaan yang kedua. 




