# Anggota Kelompok 
### Takbir Ahmad Fauzan  
### Mohamad Irfan
### Ikhsan Nur Huda

# Aplikasi penghitung kendaraan yang menggunakan metode YOLO (You Only Look Once) Object Detection

### PENDAHULUAN 
Berbagai macam dampak yang dihasilkan oleh kemacetan dan bersifat negatif, setelah dilihat dari berbagai aspek. Kemacetan menimbulkan banyak kerugian dari berbagai segi materi, waktu, dan tenaga. Seperti dari aspek ekonomi kemacetan menghambat proses produksi dan distribusi sehingga menghambat laju perekonomian yang harusnya berjalan Dari aspek Kesehatan kemacetan menyebabkan dampak negatif yaitu mempengaruhi kondisi fisik dan psikis para pengguna jalan raya Sudah banyak upaya yang dilakukan untuk megurangi kepadatan kendaraan di jalan raya Dengan cara membuat sebuah sistem penghitung jumlah kendaraan dengan menggunakan CCTV yang ada pada salah satu lampu lalu lintas di Surabaya dilakukan secara otomatis dan diproses pada pengolahan citra digital menggunakan metode YOLO object detection. Hasil pengujian yang didapatkan aplikasi YOLO object detection yang sudah bisa mendeteksi dan membedakan kendaraan dengan unsur lain. Dengan pendeteksian kali ini akan lebih mudah untuk dapat menghitung kendaraan yang lewat pada jalan raya di video

### Tujuan 
Sistem pemantauan kendaraan yang lalu Lalang di jalan raya atau area tertentu dengan mengumpulkan informasi banyaknya Kendaraan yang melalui satu ruas jalan sehingga  kepadatan lalu lintas dapat di pantau dan tujuannya yaitu untuk manajemen lalu lintas, dan perencanaan infrastruktur transportasi.

### Followchart

### Cara Kerja Aplikasi 
1.	Input Rekaman Video ialah ketika memasukan rekaman video yang dibutukan program untuk mendeteksi kendaraan yang lewat.

2.	Pre Processing ialah proses mengklasifikasi objek gambar secara manual menggunakan software User dapat mengklasifikasi semua objek dan menyimpan hasil gambar beserta rr ke folder data sebelun masuk ke program
  
3.	YOLO Object Detection ialah ketika program sudah memulai bekerja mendeteksi kendaraan dan membuat garis untuk menghitung kendaraan yang melewatinya
   
4.	Kotak mendeteksi kendaraan ialah ketika program sudah berhasil mendeteksi kendaraan yang akan melintas.
   
5.	Menghitung jumlah kendaraan ialah ketika kendaraan yang sudah terdeteksi melewati garis dan counter otomatis akan bertambah.
   
6.	Menunggu kendaraan melewati garis ialah ketika garis masih menunggu kendaraan yang akan melewatinya

### Knowladge Base
Sumber utama dataset dalam sistem ini berasal dari gambar kamera lalu lintas atau CCTV yang ada di jalan. Dataset tersebut terdiri dari gambar-gambar yang diambil pada suatu ruas jalan dalam jangka waktu tertentu. Basis pengetahuan dalam aplikasi ini dapat mencakup model neural network yang telah dilatih dengan data citra kendaraan untuk mengenali dan menghitung kendaraan di jalan raya. Knowledge base berisi informasi tentang fitur-fitur untuk mengenali kendaraan. Semua gambar tersebut menjadi bagian dari sampel pelatihan dan pengujian, digunakan untuk melatih dan memvalidasi model pembelajaran mendalam. Model tersebut ditargetkan untuk menjalankan tugas penghitungan jumlah kendaraan.

### Interface Engine 
Sistem pemantauan lalu lintas yang diusulkan, ditingkatkan oleh kecerdasan buatan (AI), memanfaatkan algoritma canggih dalam deep learning  untuk secara real-time memonitor kondisi lalu lintas. Proses ini melibatkan pembuatan dan pelatihan model jaringan saraf konvolusional mendalam menggunakan gambar lalu lintas yang telah dianotasi secara manual sebagai sumber data utama dengan memanfaatkan data yang ada pada kamera jalan atau CCTV yang terpasang pada sepanjang ruas jalan. Model-model ini kemudian digunakan untuk penghitungan jumlah kendaraan dalam jangkauan waktu 

Sistem ini memanfaatkan berbagai algoritma pembelajaran mendalam seperti  YOLO, deep learning dan dengan bantuan Computer vision. Deep learning disini adalah paradigma pembelajaran mesin yang menggunakan jaringan saraf tiruan dengan banyak lapisan untuk memodelkan data kompleks. Sedangkan YOLO merupakan suatu implementasi konkret dari deep learning yang dikhususkan untuk deteksi objek real-time. Computer vision adalah domain yang mencakup pengembangan algoritma dan teknologi untuk memberikan kemampuan penglihatan komputer atau perangkat untuk memahami dan berinteraksi dengan dunia visual.

Sistem ini mampu mengidentifikasi banyaknya kendaraan yang melintas di ruas jalan, bergerak secara real time. Kinerja algoritma sistem dievaluasi, dengan menggunakan YOLO mencapai tingkat akurasi 90% dalam memprediksi objek.

### User Interface 
Front-end antarmuka pengguna grafis (GUI), Melalui GUI ini, operator lalu lintas dapat memonitor alur lalu lintas, Banyaknya kendaran yang dilalui ruas jalan dan pemantauan CCTV di jalan raya. Selain itu, GUI ini memberikan keahlian kepada operator untuk mengidentifikasi lokasi kamera yang mengelola lalu lintas. User Interface (UI) akan menampilkan hasil penghitungan kendaraan dengan cara yang mudah dimengerti. Ini mungkin mencakup angka jumlah kendaraan yang telah dihitung, visualisasi deteksi objek seperti bounding boxes atau garis lintasan kendaraan, serta metrik kinerja seperti tingkat akurasi atau kecepatan penghitungan

### Kesimpulan 
Aplikasi penghitung kendaraan menggunakan metode YOLO Object Detection dirancang untuk memonitor lalu lintas secara efektif. Dengan menggabungkan deep learning, YOLO, dan computer vision, sistem ini mampu mendeteksi dan menghitung kendaraan dengan tingkat akurasi yang tinggi. Pengguna dapat memanfaatkan antarmuka pengguna grafis (GUI) untuk memantau alur lalu lintas, tingkat kemacetan, dan kondisi lingkungan melalui pemantauan CCTV. Dengan basis pengetahuan yang berfokus pada pelatihan model menggunakan gambar kamera lalu lintas, serta implementasi algoritma pembelajaran mendalam, sistem ini diharapkan dapat memberikan kontribusi dalam manajemen lalu lintas dan perencanaan infrastruktur transportasi.



