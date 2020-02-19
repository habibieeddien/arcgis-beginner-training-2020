# Pengenalan Geodatabase

## Basis Data \(Database\)

Basis data \(database\) adalah sekumpulan logis dari informasi yang saling terkait yang dikelola dan disimpan sebagai satu kesatuan. Basis data GIS \(Geodatabase\) umumnya mencangkup lokasi spatial dan bentuk dari feature yang disimpan dalam bentuk titik, garis, polygon, pixel/grid/cell atau TIN \(Triangulated Irregular Network\) lengkap dengan data atributnya.

Dalam pengertian lain, database juga merupakan himpunan atau kumpulan data atau file yang saling berhubungan yang disimpan dalam satu media \(elektronik\) secara terorganisir, sehingga dapat diakses dengan mudah dan cepat. Jadi geodatabase merupakan database tentang data geografis. Agar database dapat diakses dengan mudah dan cepat, maka database yang dibuat harus mempunyai struktur basis data yang kompak, struktur table efisien dan sistematis, space \(memori\) penyimpanan yang kompak, ukuran table efisien untuk mempercepat proses pengolahan, sedikit/tidak ada pengulangan, dan tidak ada ambiguitas data dari semua table yang ada. Atau secara umum dapat disebut geodatabase \(database berbasis GIS\).

## Geodatabase

Geodatabase adalah suatu tempat yang digunakan untuk menyimpan data feature, dataset, raster dataset, topologi, network dataset, terrain dataset dan lain sebagainya. Ada tiga jenis geodatabase dalam ArcGIS seperti yang ditunjukkan pada Gambar 1. 1. Personal Geodatabase, semua dataset disimpan dalam format \*.mdb microsoft database dengan limit size sampai 2 Giga byet, hanya berjalan pada windows operating system. Dapat dipakai oleh single user dan kelompok kecil. Sering digunakan untuk manajemen data atribut melalui microsfot access untuk jenis atribut string \(teks\) 2. File Geodatabase, disimpan dalam bentuk sistem file, setiap dataset dapat disimpan sampai 1 Terra byet tetapi dapat dibesarkan mencapai 256 Terra byet untuk menyimpan data citra satelit yang besar dan banyak. 3. ArcSDE Geodatabase, dapat juga disebut dengan multiuser geodatabase, disimpan dalam bentuk relasional database menggunakan Microsoft SQL Server, IBM DB2, Oracle, PostgreSQL, IBM Informix. Syarat penggunaan jenis ini memerlukan ArcSDE sebagai penghubung dan tidak terbatas dalam penyimpanan serta penggunanya. Dapat digunakan pada platform windows, UNIX, Linux, dan koneksi langsung ke DBMS

Gambar 1 Jenis Geodatabase dalam ArcGIS

File Geodatabase dan Personal Geodatabase tersedia untuk semua pengguna ArcGIS Dekstop \(Basc, Standard, Advanced\) dirancang untuk mendukung model informasi pada geodatabase seperti topologi, raster katalog, network dataset, terrain dataset, address locator, dan lain-lain. Personal geodatabase didesain hanya dapat diedit oleh satu user saja, untuk file geodatabase dimungkinkan dapat diedit lebih dari satu editor pada waktu yang sama untuk feature yang berbeda. Perbedaan lainnya dapat dilihat pada gambar 2.

Gambar 2 Perbedaan feature Database

Ada beberapa hal yang perlu di perhatikan dalam membuat geodatabase: Inventarisasi peta atau data spasial apa saja yang dibuat dan data atau feature class apa saja yang dibutuhkan, nantinya sangat berhubungan erat dengan populasi data dan juga analisa terhadap data yang akan digunakan.

