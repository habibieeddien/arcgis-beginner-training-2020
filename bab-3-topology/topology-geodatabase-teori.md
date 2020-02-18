# TOPOLOGY GEODATABASE \(teori\)

**MODUL PELATIHAN**

**TOPOLOGY GEODATABASE**

**Kompetensi :**

1. Peserta pelatihan mampu mengetahui dan memahami pengertian dan konsep dasar dari geodatabase dan topologi

**Ulasan Teori**

1. **Geodatabase dan Topologi**

Geodatabase merupakan database relasional yang mencakup informasi geografis. Geodatabase memuat kelas - kelas/golongan feature dan table. Kelas - kelas feature dapat diorganisasikan ke dalam set data feature.

Topology adalah pendefinisian secara matematis yang menerangkan hubungan relative antara objek yang satu dengan objek yang lain. Dalam GIS topology didefinisikan oleh user sesuai dengan karakteristik data seperti line, polygon maupun point/titik. Setiap karakteristik data tertentu mempunyai rule/aturan tertentu. Rule atau aturan tersebut secara default telah disediakan oleh software GIS.

Kata topologi memiliki beberapa makna ketika dibahas dalam konteks GIS. Itu bisa merujuk ke:

* Teori atau model matematika dari fitur yang terdapat di dalam ruang.
* Mekanisme yang memungkinkan fitur dalam kelas yang sama atau berbeda untuk berbagi geometri,
* Kumpulan dari tools yang digunakan untuk editing,
* Kumpulan aturan validasi untuk fitur geografis,
* Mekanisme untuk melakukan navigasi antar fitur menggunakan hubungan topologis.

1. **Kegunaan Topologi**

Topologi digunakan secara fundamental untuk memastikan kualitas data dan membantu kompilasi data. Contoh dari penggunaan topologi adalah membantu memodelkan dunia nyata secara terpadu meliputi pemodelan bidang tanah, poligon tanah, atau batas wilayah; jaringan transportasi dengan garis tengah jalan dan rute bus.

Topologi di ArcGIS dimulai dengan definisi parameter yang akan dimasukkan. Parameter-parameter ini didefinisikan melalui wizard di ArcCatalog. Topologi memiliki karakteristik sebagai berikut :

* Dikelompokkan dalam set data fitur \(Gambar 1\) karena semua kelas fitur yang berpartisipasi harus memiliki referensi spasial yang sama.
* Mungkin ada beberapa topologi dalam satu dataset
* Fitur class hanya dapat disertakan dalam satu topologi.
* Fitur class tidak dapat disertakan dalam topologi dan jaringan geometrik.
* Topologi dapat berisi beberapa fitur titik, garis, dan kelas poligon.

![](../.gitbook/assets/0%20%283%29.png)

**Gambar 1**

Selain parameter diatas, ada parameter lain yang membantu menentukan topologi. Parameter tambahan ini adalah :

* Toleransi cluster
* Peringkat relatif untuk setiap fitur class
* Rules \(aturan – aturan pada topologi\)

1. **Kesalahan Pada Topologi**

Beberapa tipe kesalahan topology yang akan dikoreksi dalam latihan ini adalah sebagai berikut:

1. Polygon
2. _Must Not Overlap_

_**Subtract**_: Menghapus bagian yang overlap dari masing2 feature dan akan meninggalkan area yang kosong pada daerah error. Perbaikan ini bisa diterapkan ke satu atau lebih kesalahan yang terjadi \(terselesi\) pada aplikasi rule Must Not Overlap errors.

_**Merge**_: Menambah/menggabung feature dari feature overlap yang melangar aturan yg dipakai. Pemilihan feature tergantung justifikasi kita mana yg akan dipilih sebagai feature yang dianggap salah. Koreksi ini bisa diterapkan pada satu kesalahan Must Not Overlap saja.

_**Create Feature**_: Membuat polygon baru diluar kesalahan yang terjadi dan menghapus kesalahan yang ada. Koreksi ini bisa diterapkan ke satu atau lebih kesalahan yang terselect oleh penerapan aturan Must Not Overlap errors.

1. Must Not Have Gap

_**Create Feature**_: Membuat polygon baru dari garis batas yang saling membentuk polygon kosong \(gap\). Koreksi ini bisa diterapkan pada satu atau lebih kesalahan pada penerapan aturan Must Not Have Gaps errors.

_**Substract**_: Menghapus segmen line yang overlapping dari feature2 yang membentuk kesalahan. Anda harus melakukan seleksi lebih dulu sebelum menghapus obyek dimaksud. Koreksi ini dapat diterapkan pada satu kesalahan Must Not Overlap saja.

1. Line
2. Must Not Overlap

_**Substract**_: Menghapus segmen line yang overlapping dari feature feature yang membentuk kesalahan. Anda harus melakukan seleksi lebih dulu sebelum menghapus obyek tersebut. Koreksi ini hanya dapat diterapkan pada satu kesalahan must not overlap saja.

1. Must Not Intersect

_**Subtract**_: Menghapus segmen line yang overlapping dari feature yang membentuk kesalahan. Anda harus melakukan seleksi lebih dulu sebelum menghapus obyek dimaksud. Koreksi ini dapat diterapkan pada satu kesalahan Must Not Intersect saja.

_**Split**_: Memotong feature line yang saling berpotongan menjadi 4 segmen

garis. Koreksi ini bisa diterapkan pada satu atau lebih kesalahan Must Not

Intersect.

1. Must Not Have Dangles

_**Extend**_: Menyambung dangle pada akhir segmen line ke feature di depannya sepanjang toleransi jarak snapping terpenuhi. Jika tidak masuk dalam toleransi jarak snapping, maka dangle akan tetap dipertahankan \(tidak berubah\), hanya obyek yang terselek yg akan di validasi. Koreksi ini dapat diterapkan ke satu atau lebih kesalahan Must Not Have Dangles.

_**Trim**_: Menghapus feature line jika dangle \(point\) pada akhir intersection line masuk dalam toleransi jarak snapping yg diterapkan. Koreksi ini dapat diterapkan ke satu atau lebih kesalahan Must Not Have Dangles.

_**Snap**_: Akan menyatukan dangle line ke line terdekat yang masuk dalam toleransi jarak snapping, target line sendiri posisinya tetap. Akan dicari endpoint terlebih dulu, vertex dan pada akhirnya garis. Koreksi ini dapat diterapkan ke satu atau lebih kesalahan Must Not Have Dangles.

1. Points

Pada jenis kesalahan points hanya ada dua koreksi yang bisa dilakukan yaitu membiarkannya atau menghapus feature yang dianggap salah.

