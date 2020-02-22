# Bab 2 Tutorial Editing

## Membuat Dokumen Peta Baru

Ada dua kondisi untuk membuat dokumen peta baru pada ArcMap, yaitu:

### Kondisi 1: Saat aplikasi ArcMap pertama kali dibuka

1. Tampilan saat ArcMap baru pertama kali dibuka seperti pada gambar berikut. 
2. Pilih **ISO \(A\) Page Sizes** kemudian klik **ISO A3 Landscape**.
3. Klik **OK** untuk membuat dokumen peta baru.

![Tampilan saat ArcMap baru pertama kali dibuka](../.gitbook/assets/onstartup.jpg)

![Tampilan saat memilih ukuran kertas untuk dokumen baru](../.gitbook/assets/iso-a3.jpg)

### Kondisi 2: Saat sedang bekerja menggunakan ArcMap

Pada kondisi ini, ada tiga cara untuk membuat dokumen peta baru, yaitu:

{% tabs %}
{% tab title="Cara 1: Menu" %}
**Cara 1**: klik **File** &gt; **New**

![Cara 1: File kemudian New...](../.gitbook/assets/file-new.jpg)
{% endtab %}

{% tab title="Cara 2: Icon" %}
Cara 2: klik pada icon **New**  

![icon New: membuat dokumen peta baru](../.gitbook/assets/icon-new.jpg)
{% endtab %}

{% tab title="Cara 3: Shortcut" %}
Cara 3: menekan tombol **Ctrl + N** pada keyboard
{% endtab %}
{% endtabs %}

Dari ketiga cara tersebut, kemudian akan tampil kotak dialog untuk membuat dokumen peta baru seperti pada gambar berikut ini.

![Tampilan untuk membuat dokumen peta baru](../.gitbook/assets/new-dok.jpg)

## Menambah Peta Dasar Secara Online

### Langkah 1

{% hint style="warning" %}
Pastikan koneksi internet stabil dan lancar saat ingin menambahkan peta dasar secara online
{% endhint %}

Pilih menu icon seperti pada gambar berikut ini. Lalu pilih **Add Basemap...**.

![Menu icon untuk menambah peta dasar](../.gitbook/assets/add-basemap.jpg)

### Langkah 2

Maka akan tampil kotak dialog seperti pada gambar berikut ini. Misalnya di sini memilih **Imagery with Labels**. Kemudian klik tombol **Add** di pojok kanan bawah.

![Tampilan kotak dialog saat memilih peta dasar](../.gitbook/assets/basemap.jpg)

Tunggu proses memuat peta sampai selesai, maka akan muncul layer baru di bagian **Table of Contents**.

## Menambah Peta Dasar Secara Offline

Anda perlu memahami bahwa peta dasar merupakan jenis data raster hasil dari citra satelit. Foto raster memiliki kualitas berbeda berdasarkan tingkat _zoom_. Terkadang Anda membutuhkannya di ArcMap ketika koneksi internet tidak mendukung. Berikut langkah-langkah untuk mengunduh citra satelit secara gratis yang dapat disesuaikan dengan kebutuhan Anda.

### Langkah 1

Silakan unduh terlebih dahulu aplikasi SAS Planet dari [tautan ini](https://bitbucket.org/sas_team/sas.planet.bin/downloads).

![](../.gitbook/assets/unduh-sas-planet.jpg)

{% hint style="info" %}
**SAS Planet** adalah program untuk menampilkan dan sekaligus bisa dimanfaatkan untuk melakukan download image resolusi tinggi dari Google Map, Bing, Nokia, Yahoo, dan sebagainya.
{% endhint %}

### Langkah 2

Setelah proses unduhan selesai, Anda dapat mengekstraknya dengan aplikasi 7zip, WinZip, atau aplikasi bawaan sistem dengan mengklik kanan pada file hasil unduhan.

![](../.gitbook/assets/ekstrak.jpg)

Lalu klik file ![](../.gitbook/assets/sas-planetexe.jpg) untuk menggunakan aplikasi tersebut.

### Langkah 3

Peringatan! Pastikan Anda memiliki koneksi internet yang cukup agar proses unduh peta dapat berjalan dengan lancar.

Pilih penyedia citra satelit, misalnya di sini menggunakan Google Maps Satellite.

![](../.gitbook/assets/google-maps.jpg)

Kemudian zoom in ke area kampus Polinema.

![](../.gitbook/assets/zoom-in-polinema-sas-planet.jpg)

### Langkah 4

Pilih shift tool lalu buat area pemotongan foto satelit sesuai kebutuhan seperti pada gambar berikut.

![](../.gitbook/assets/shift-tool.jpg)

Cara memotong citra satelit adalah klik kiri sekali, lalu geser mouse  sesuai besar area yang ingin dipotong, dan klik kiri sekali.

![](../.gitbook/assets/crop-area.jpg)

### Langkah 5

Kotak dialog **Selection Manager** akan muncul. Pilih tab **Stitch** &gt; pilih **Zoom** **21**.

**Output format:** Pilih **GeoTIFF \(Tagged Image File Format\)**

**Zoom:** 21

**Projection:** Geographic \(Latitude/Longitude\) / WGS84 / EPSG: 4326

![](../.gitbook/assets/selection-manager.jpg)

Buat folder dan tentukan nama file citra, misalnya **polinema\_basemap\_raster.tiff**

Klik **Start** untuk memulai unduhan. Tunggu hingga proses unduhan selesai.

### Langkah 6

Ada dua cara untuk menambah peta dasar secara offline di ArcMap.

{% tabs %}
{% tab title="Cara 1" %}
Cara 1 - Pilih icon ![](../.gitbook/assets/add-icon.jpg) **Add Data** &gt; Pilih file **polinema\_basemap\_raster.tiff**
{% endtab %}

{% tab title="Cara 2" %}
Cara 2 - Pilih dari jendela Catalog, lalu drag dan drop file **polinema\_basemap\_raster.tiff** ke Layers \(Table of Contents\).
{% endtab %}
{% endtabs %}

Dari kedua cara tersebut, kemudian akan muncul kotak dialog untuk menentukan Sistem Koordinat. Misalnya pada pelatihan ini, kita akan menggunakan WGS UTM 49S. Alasannya, karena posisi Malang berada di 49S berdasarkan zona UTM Indonesia \(Anda dapat mencarinya di internet\). Alasan lain, nanti kita akan menggunakan satuan meter untuk proses digitasi.

{% hint style="success" %}
Anda telah praktik membuat dokumen peta baru, menambah peta dasar secara online maupun offline di ArcMap.
{% endhint %}

