# Tugas-oak-4



# 1.Jelaskan Struktur Antar Hubungan dan Beri Contohnya? 
Struktur antar hubungan merujuk pada pola atau mekanisme interaksi antara elemen-elemen dalam suatu sistem atau kelompok. Struktur ini dapat dijumpai dalam berbagai bidang, seperti masyarakat, ekonomi, politik, organisasi, maupun teknologi.Adapun contoh Struktur antar hubungan sebagai berikut.
1. Struktur hierarki
   Struktur hirerarki adalah hubungan yang tersusun secara bertingkat atau berjenjang, dengan tingkatan yang lebih tinggi memiliki otoritas lebih besar dibandingkan yang lebih rendah.
Contoh: Dalam sebuah perusahaan, CEO berada di posisi teratas, diikuti oleh manajer, supervisor, dan karyawan di tingkat bawah.

![image](https://github.com/user-attachments/assets/0a987f0e-592f-4947-bc4c-663c3f23e360)

2. Struktur Jaringan (Network)

Struktur ini bersifat non-hierarki, di mana setiap elemen atau individu dapat terhubung satu sama lain, baik secara langsung maupun tidak langsung, tanpa adanya tingkatan tertentu.
Contoh: Jaringan pertemanan di media sosial, di mana semua pengguna bebas berinteraksi tanpa batasan hierarki.

![image](https://github.com/user-attachments/assets/02324026-97d9-4673-bb5e-44adea322441)

3.Struktur Matriks

Struktur ini menghubungkan elemen berdasarkan lebih dari satu dimensi atau kategori, memungkinkan interaksi lintas bidang.
Contoh: Dalam sebuah perusahaan proyek, seorang karyawan dapat bekerja di bawah dua manajer berbeda, misalnya dari departemen teknis dan pemasaran.

![image](https://github.com/user-attachments/assets/857f2aa0-84d1-4bd0-8479-59d72a048aba)


4.Struktur Sirkular

  Struktur ini berbentuk lingkaran atau siklus, di mana setiap elemen saling bergantung dan memiliki hubungan timbal balik.
Contoh: Dalam rantai pasokan (supply chain), produsen, distributor, dan pengecer saling terhubung dalam proses produksi dan distribusi barang.

![image](https://github.com/user-attachments/assets/8277fbbd-e809-4bd8-92d8-9586dd3d41fd)


5.Struktur Hub-and-Spoke
  Struktur ini memiliki satu titik utama sebagai pusat penghubung bagi elemen-elemen lainnya.
Contoh: Bandara utama (hub) seperti Bandara Soekarno-Hatta yang menjadi pusat konektivitas untuk berbagai rute penerbangan di Indonesia.

![image](https://github.com/user-attachments/assets/e93d660e-8a43-43d6-8111-ec10d80521c7)



# 2. Bila terlalu banyak modul atau perangkat dihubungkan pada bus maka akan terjadi penurunan kinerja, sebutkan penyebabnya?
Jika terlalu banyak modul atau perangkat yang dihubungkan ke bus, kinerjanya akan menurun akibat beberapa faktor berikut:  

- **Kemacetan Lalu Lintas Data (Bus Contention)**  
  Semakin banyak perangkat yang terhubung, semakin besar kemungkinan terjadinya persaingan dalam mengakses bus, sehingga dapat menyebabkan keterlambatan dalam pengiriman data.  

- **Kapasitas Bandwidth Terbatas**  
  Bus memiliki kapasitas transfer data yang terbatas. Jika terlalu banyak perangkat menggunakan jalur komunikasi yang sama, maka kecepatan transfer data akan menurun.  

- **Peningkatan Waktu Tunggu**  
  Karena bus digunakan secara bergiliran, semakin banyak perangkat yang terhubung, semakin lama waktu yang dibutuhkan sebelum suatu perangkat dapat mengirim atau menerima data.  

- **Kenaikan Latensi**  
  Banyaknya antrian permintaan akses ke bus menyebabkan peningkatan waktu tunda (latensi) sebelum data dapat dikirim.  

- **Beban Sinyal dan Konsumsi Daya**  
  Bertambahnya jumlah perangkat yang terhubung meningkatkan beban sinyal pada bus, yang dapat menyebabkan penurunan kualitas transmisi serta meningkatkan risiko kesalahan dalam pengiriman data.  

- **Gangguan Sinyal dan Interferensi (Noise)**  
  Banyaknya perangkat yang terkoneksi dapat meningkatkan gangguan elektromagnetik (EMI), yang berpotensi mengurangi efisiensi komunikasi antar perangkat.


Solusi untuk Mencegah Penurunan Kinerja pada Bus
Salah satu cara untuk meningkatkan kinerja bus adalah dengan menggunakan bus yang memiliki bandwidth lebih besar, seperti beralih dari PCI ke PCIe. Selain itu, penerapan teknologi buffering atau caching dapat membantu mengurangi beban langsung pada bus.
Alternatif lain adalah dengan memanfaatkan topologi jaringan yang berbeda, seperti star atau ring, jika memungkinkan. Penggunaan teknik multiplexing juga dapat meningkatkan efisiensi dengan memungkinkan beberapa perangkat mengakses bus secara bersamaan.
Dengan mengelola jumlah perangkat yang terhubung dan menerapkan strategi yang tepat, sistem dapat tetap bekerja secara optimal meskipun jumlah perangkat terus bertambah.


# 3. Umumnya perangkat berprioritas paling rendah memiliki waktu tunggu rata-rata yang paling singkat. Dengan dasar ini biasanya CPU diberi perioritas tertinggi pada SBI. Sebutkan alasan perangkat berprioritas 16 memiliki waktu tunggu rata-rata paling rendah? Dibawah kondisi seperti apa keadaan diatas tidak berlaku?:

### **Mengapa Perangkat dengan Prioritas 16 Memiliki Waktu Tunggu Rata-rata Lebih Singkat?**  
Dalam sistem bus yang menerapkan **penjadwalan berbasis prioritas**, perangkat dengan **prioritas lebih tinggi** biasanya mendapatkan akses terlebih dahulu dibandingkan perangkat berprioritas lebih rendah. Namun, dalam beberapa metode **pengelolaan waktu tunggu**, perangkat dengan prioritas paling rendah justru bisa memiliki **waktu tunggu rata-rata lebih pendek** karena beberapa alasan berikut:  

1. **Jarang Mengalami Penundaan**  
   - Perangkat berprioritas rendah tidak sering bersaing dengan perangkat prioritas tinggi, karena mereka hanya mengakses bus saat perangkat prioritas tinggi sedang tidak menggunakannya.  

2. **Frekuensi Permintaan Lebih Rendah**  
   - Perangkat dengan prioritas tinggi lebih sering mengajukan permintaan akses, sehingga antrean mereka bisa lebih panjang dibandingkan perangkat prioritas rendah yang lebih jarang menggunakan bus, tetapi mengalami latensi lebih kecil.  

3. **Metode Penjadwalan yang Digunakan**  
   - Jika sistem menggunakan metode **round-robin atau fair queuing**, perangkat prioritas rendah tetap mendapatkan akses dalam waktu yang ditentukan, sehingga waktu tunggunya tetap rendah meskipun memiliki prioritas lebih kecil.  

---

### **Kondisi di Mana Keadaan Ini Tidak Berlaku**  
Ada beberapa situasi di mana perangkat dengan prioritas rendah justru memiliki waktu tunggu yang lebih lama:  

1. **Sistem dengan Penjadwalan Prioritas Ketat**  
   - Jika sistem menerapkan **strict priority scheduling**, perangkat berprioritas tinggi selalu mendapat akses terlebih dahulu, yang dapat menyebabkan perangkat berprioritas rendah mengalami **kelaparan (starvation)** sehingga waktu tunggunya semakin panjang.  

2. **Beban Tinggi pada Perangkat Prioritas Tinggi**  
   - Jika perangkat dengan prioritas tinggi terus-menerus mengakses bus (seperti CPU atau penyimpanan berkecepatan tinggi), perangkat dengan prioritas rendah akan lebih sering tertunda dan harus menunggu lebih lama.  

3. **Tingkat Persaingan yang Tinggi**  
   - Jika banyak perangkat mengajukan permintaan akses secara bersamaan, perangkat dengan prioritas lebih rendah dapat terus tertunda, terutama jika tidak ada mekanisme penjadwalan yang adil.  

4. **Sistem dengan Penanganan Interupsi Berbasis Prioritas**  
   - Jika sistem menggunakan **interrupt-driven I/O**, perangkat berprioritas tinggi dapat terus menghasilkan interupsi, menyebabkan perangkat prioritas rendah semakin jarang mendapatkan kesempatan mengakses bus.  

---

### **Kesimpulan**  
Perangkat dengan prioritas paling rendah bisa memiliki waktu tunggu rata-rata lebih pendek jika sistem menerapkan penjadwalan yang adil atau jika perangkat prioritas tinggi tidak sering menggunakan bus. Namun, dalam sistem yang menggunakan **penjadwalan prioritas ketat** atau dalam kondisi **beban tinggi**, perangkat dengan prioritas rendah dapat mengalami waktu tunggu yang lebih lama akibat terbatasnya akses ke bus.





