# Istilah Penting di ArcMap

### Dokumen Peta \(.mxd\)

Sebuah peta yang digunakan dalam ArcMap itu disimpan ke dalam sebuah file dengan ekstensi .mxd. Setiap dokumen peta berisi spesifikasi berupa lapisan peta, page layout, dan semua properti lain yang ada pada peta. Adanya dokumen peta mempermudah dalam pekerjaan seperti menyimpan, menggunakannya kembali, dan berbagi dengan rekan kerja Anda di ArcMap. Double-click pada dokumen peta ini dapat membuka sesi baru di ArcMap.

### Shapefile \(.shp\)

Untuk menyimpan data spasial nontopologis berbasis vektor. Shapefile digunakan untuk menyimpan data peta digital pada sistem informasi geografis. Format data ini dikembangkan oleh ESRI.

Format data ini mampu menyimpan data spasial seperti bidang \(untuk menyimpan data pulau, wilayah provinsi\), garis \(untuk menyimpan data jalan, sungai\), titik \(untuk menyimpan lokasi kota, bangunan, bangunan\) dan informasi mengenai ketiga data spasial tersebut \(untuk menyimpan nama suatu kota, jenis suatu jalan, dll\).

Format data ini berbasis vektor. Jadi, data spasial seperti titik, garis dan bidang disimpan dalam bentuk kumpulan titik. Untuk data garis, disimpan titik-titik sudutnya. Sedangkan untuk bidang, juga disimpan titik-titik sudutnya.

Format data ini menyimpan data spasial yang sifatnya nontopologis. Setiap data spasial hanya disimpan sebagai individu. Hubungan antar data spasial tidak disimpan. \([Wikipedia](https://id.wikipedia.org/wiki/Shapefile)\)

### Layer

Sebuah lapisan peta mendefinisikan dataset GIS yang disimbolkan dan dilabeli di dalam tampilan peta Anda. Setiap lapisan merepresentasikan data geografis di ArcMap seperti tema tertentu pada masing-masing data. Contohnya lapisan peta dapat berisi sungai, danau, perbukitan, jalan, batas administratif, bidang, bangunan, garis, dan citra ortofoto.

### Table of contents

Istilah ini untuk menjelaskan daftar isi dari semua lapisan yang ada pada peta dan menunjukkan fitur-fitur yang ada pada setiap lapisan. Check box menunjukkan lapisan itu aktif ditampilkan pada peta. Urutan lapisan menunjukkan urutan menggambar di data frame atau peta yang berurutan dari bawah ke atas.

### Data frame

Ini merupakan tampilan utama pada ArcMap untuk menampilkan peta, lapisan, dan semua yang berkaitan dengan proyek dokumen kerja Anda.

### Page layouts

Layout atau tata letak yang digunakan untuk menampilkan peta Anda dalam versi cetak \(print out\) sesuai dengan ukuran kertas yang Anda tentukan. Biasanya ada elemen-elemen peta seperti panah utara, judul peta, deskripsi peta, legenda, dan sebagainya.

### The Catalog Window

ArcMap, ArcGlobe, dan ArcScene termasuk ke dalam Catalog yang digunakan untuk memanajemen berbagai jenis informasi geografis seperti data, peta, hasil project GIS Anda ketika bekerja dengan ArcGIS.

### Labels

Teks yang tampil pada peta. Seperti nama sungai, kota, bangunan, dan sebagainya.

### Annotation

Anotasi digunakan untuk mewakili label fitur yang disimpan sebagai lokasi fitur grafik di geodatabase. Lokasi teks disimpan bersama dengan properti teks lainnya untuk setiap keterangan fitur. Anotasi berbeda dari label karena setiap lokasi dan penggambaran anotasi hanya dihitung sekali dan disimpan. Ini digunakan kembali setiap kali Anda menggambar ulang peta Anda. Karena posisi anotasi sudah disetel, tidak ada perhitungan label yang perlu dilakukan setiap kali peta digambar ulang.

### Symbols

Simbol adalah elemen grafis yang digunakan dalam tampilan peta. Ada beberapa jenis simbol, seperti: 

* Marker yang terutama digunakan untuk menampilkan lokasi titik;
* Simbol garis digunakan untuk menampilkan fitur dan batas linear;
* Isi simbol yang digunakan untuk mengisi poligon;
* Simbol teks yang digunakan untuk mengatur font, ukuran, warna, dan properti teks lainnya.

### Styles

Gaya adalah kumpulan simbol, warna, dan elemen peta yang cocok dengan tema atau domain aplikasi — misalnya, gaya yang ditetapkan untuk peta transportasi atau peta geologi.

### Basemap layers

Basemap digunakan untuk referensi lokasi dan menyediakan kerangka kerja di mana pengguna melapisi atau menyatukan lapisan operasional mereka, melakukan tugas, dan memvisualisasikan informasi geografis. Di ArcMap, lapisan basemap dapat digunakan untuk menahan lapisan peta yang lebih statis dan dengan demikian dapat digunakan untuk mendukung tampilan peta dinamis yang berkinerja tinggi.

### Coordinate System \(Spatial Reference\)

Untuk menampilkan data Anda dengan benar, setiap frame data menggunakan sistem koordinat. Ini menentukan proyeksi peta untuk tampilan peta dalam bingkai data. Sistem koordinat frame data tidak harus sama dengan data yang Anda gunakan, meskipun jika ArcMap harus memproyeksikan data Anda dengan cepat, mungkin butuh waktu lebih lama untuk menggambar.

Ketika ArcMap dimulai dengan peta baru yang kosong, sistem koordinat untuk bingkai data default tidak ditentukan. Lapisan pertama ditambahkan ke bingkai data kosong menetapkan sistem koordinat untuk bingkai data, tetapi Anda dapat mengubahnya jika perlu. Saat Anda menambahkan lapisan berikutnya, mereka ditampilkan secara otomatis menggunakan sistem koordinat bingkai data selama sistem koordinat sumber data ditentukan.

