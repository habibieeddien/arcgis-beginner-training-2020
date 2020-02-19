# Latihan 3a: Merubah Label Menjadi Anotasi

## 3.1 Fitur Anotasi

Anotasi merupakan cara untuk menyimpan teks\(informasi\) yang berkaitan dengan suatu tempat dalam peta. Dengan fitur anotasi, setiap bagian teks memiliki informasi posisinya, teksnya itu sendiri, serta seperti apa bentuk tampilannya. Sedangkan label, yang mana berasal dari satu atau lebih atribut fitur, adalah cara lain ketika ingin menempatkan teks pada peta. Apabila suatu bagian teks harus tepat menempati posisinya, sebaiknya digunakan fitur anotasi pada geodatabase. Ketika menggunakan anotasi, cukup mudah mengatur tampilan serta penempatan suatu teks, karena dapat ditentukan perbagian teks yang akan di-edit. Selain itu juga bisa dilakukan konversi label menjadi fitur anotasi.

Pada latihan ini, akan dilakukan konversi label menjadi anotasi geodatabase, sehingga kemudian dapat dilakukan perubahan fitur-fitur teks.

## 3.2 Menyiapkan Label untuk Dikonversi

Peta yang akan digunakan pada latihan ini berisi fitur jalan dan air di taman nasional zion. Layer-layer pada peta memiliki label-label yang dinamis, akan tetapi sebagian fitur peta tidak dapat dilabeli karena keterbatasan tempat. Ketika suatu label di-konversi menjadi anotasi, maka dapat dilakukan penempatan secara manual untuk setiap bagian teks tersebut.

1. Klik tombol **Open**![Open](../../.gitbook/assets/0.png) pada toolbar **Standard**.
2. Cari dokumen **Exercise3.mxd** yang terletak di direktori editing. \(C:\ArcGIS\ArcTutor adalah lokasi defaultnya\).
3. Pilih petanya dan klik **Open**.
4. Jika dokumen peta tersebut masih digunakan akan ada peringatan untuk menutupnya.

Masing-masing layer fitur memiliki label dinamis, dan layer Streams memiliki pengelompokan label berdasarkan simbol layer. Pengelompokan label digunakan untuk membuat label yang berbeda untuk tipe fitur berbeda pada layer tertentu. Misalnya, _intermittent streams_ bisa diberikan label yang lebih kecil daripada aliran _perennial streams._

1. Klik **Customize**, cari **Toolbars**, kemudian klik **Labeling**.
2. Untuk melihat label yang kurang pas, periksa label yang belum diposisikan. Dengan cara klik tombol **View Unplaced Labels** ![https://desktop.arcgis.com/en/arcmap/latest/manage-data/editing-fundamentals/GUID-A1087704-B02D-4FC8-92A3-EA8D335833B3-web.png](../../.gitbook/assets/1%20%286%29.png).

Label yang tidak bisa diposisikan ditandai dengan warna merah. Untuk menyesuaikan label dapat dilakukan dengan cara mengatur ukurannya, merubah bobot fitur dan label, atau dengan cara menjadikan petanya lebih besar. Akan tetapi, dalam latihan ini yang dilakukan adalah melakukan konversi dari label menjadi anotasi, selanjutnya menempatkan anotasi tersebut atau menghapus anotasi yang tidak ditempatkan

![https://desktop.arcgis.com/en/arcmap/latest/manage-data/editing-fundamentals/GUID-30D04B57-B628-4208-8F3E-C1556FF0A5DC-web.png](../../.gitbook/assets/2%20%285%29.png)

Label yang tidak diposisikan ditampilkan berwarna merah.

1. Klik tombol **View Unplaced Labels**  ![View Unplaced Labels](../../.gitbook/assets/3%20%285%29.png) sekali lagi untuk menyembunyikan label yang tidak diposisikan.

Fitur anotasi memiliki posisi serta ukuran yang fix, jadi ketika dilakukan pembesaran\(zoom\) pada map fitur anotasi akan ikut terlihat membesar juga. Sedangkan label tampil lebih dinamis, sesuai dengan properti label layer tersebut. Jika petanya tidak memiliki referensi skala, label akan tampil spesifik sesuai dengan ukuran fontnya, tanpa memperdulikan skala peta. Agar label berperilaku seperti anotasi, dapat dilakukan dengan cara mengatur skala referensi petanya. Sehingga label akan tampil relatif terhadap skala referensi. Ketika melakukan konversi label menjadi anotasi, harus dilakukan penentukan skala referensi. Jika tidak, maka skala peta yang sekarang, akan digunakan sebagai skala referensi untuk anotasinya.

1. Ketik-kan **170000** pada kotak **Map Scale** di toolbar **Standard** kemudian tekan ENTER.
2. Pada bagian table of contents, klik tombol **List By Drawing Order**  ![List By Drawing Order](../../.gitbook/assets/4%20%283%29.png), jika belum dalam posisi aktif mengurutkan layer. kemudian, klik kanan **Layers** \(nama dari frame data\), arahkan ke **Reference Scale**, kemudian **Set Reference Scale**.

Maka sekarang, jika ingin zoom in atau out, maka label akan menyesuaikan menjadi lebih besar atau kecil. Sehingga sekarang siap untuk konversi label menjadi anotasi.

## 3.3 Merubah Label Menjadi Anotasi

Anotasi dapat disimpan dalam dokumen peta atau pada kelompok fitur dalam geodatabase. Dalam latihan ini, label yang akan dikonversi menjadi anotasi akan disimpan di geodatabase. Dalam kotak dialog konversi label menjadi anotasi, dapat ditentukan seperti apa anotasi yang mau dibuat, yang mana fitur yang akan dibuat anotasinya, serta dimana anotasi nantinya akan disimpan.

1. Pada table of contents, klik kanan **Layers** kemudian **Convert Labels to Annotation**.

Menggunakan ArcGIS Desktop Basic dapat melihat anotasi yang terkait dengan fitur, akan tetapi tidak dapat membuat atau mengedit dataset yang yang berisikan anotasi tersebut. Dalam ArcGIS Desktop Basic license, fitur “Linked column” tidak dapat digunakan. Pada latihan ini, akan dibuat fitur anotasi standar. Dimana, ArcGIS Desktop Basic tidak dapat digunakan.

1. Hilangkan centang pada kolom Feature Linked.

![](../../.gitbook/assets/5%20%289%29.png)

Ikon folder kecil adalah tombol browse, yang terletak di samping kelas fitur anotasi yang telah dihilangkan centangnya. Anotasi “Feature-linked” harus disimpan beserta kelas fitur terkait di dalam geodatabase. Kelas fitur anotasi standar dapat disimpan di dalam geodatabase yang lain; setelah menghilangkan centang, ada pilihan menentukan lokasi anotasi baru. Kelas fitur anotasi defaultnya disimpan dalam dataset yang sama dengan kelas fitur asalnya. Jika layer fitur dalam peta berasal dari shapefile atau kelas fitur yang tercakup, tombol browse akan tidak berfungsi, sehingga tidak bisa membuka geodatabase untuk menyimpan kelas fitur anotasi yang baru.

1. Pastikan **Convert unplaced labels to unplaced annotation** telah tercentang. Sehingga memungkinkan untuk meletakkan secara manual anotasi untuk fitur yang belum terlabel.
2. Klik **Convert**.

Sekarang, label telah terkonversi menjadi anotasi. Proses ini harusnya memakan waktu kuran dari semenit tergantung kecepatan komputer. Saat kelas fitur anotasi telah terbentuk, maka otomatis ditambahkan dalam ArcMap

Setiap kelas label pada layer menyimpan kelas anotasi terpisah ke dalam sebuah kelas fitur anotasi, Intermittent dan Perennial, di dalam kelas fitur anotasi. Kelas fitur anotasi ini dapat di aktifkan\(on\) dan dinon-aktifkan\(off\) secara independen, dan dapat memiliki jarak skala visible sendiri.

Label telah terkonversi menjadi anotasi, selanjutnya akan diletakkan pada peta dan merubah posisinya.

