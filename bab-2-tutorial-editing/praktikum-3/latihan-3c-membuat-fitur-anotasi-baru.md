# Latihan 3c: Membuat Fitur Anotasi Baru

## 3.7 Membuat Anotasi Lurus

Pastikan **Exercise3.mxd** terbuka dan Anda dalam sesi edit.

Akan digunakan tool untuk membuat anotasi Lurus, dimana digunakan untuk menempatkan anotasi yang memiliki garis dasar lurus tetapi dapat diputar secara miring. Akan ditambahkan beberapa teks ke peta Anda untuk mengidentifikasi ngarai di taman.

1. Buka jendela **Create Features** dengan cara klik **Create Features** ![Create Features](../../.gitbook/assets/0%20%286%29.png)pada toolbar **Editor**.
2. Pada jendela **Create Features,** klik template fitur anotasi **Canyons** pada layer **CanyonsAnno**.

Saat Anda mengaktifkan templat anotasi, jendela Konstruksi Anotasi muncul sehingga Anda dapat memasukkan teks dan mengubah pemformatan fitur yang akan Anda buat.

1. Klik **Straight** construction tool ![Straight](../../.gitbook/assets/1%20%287%29.png) pada jendela **Create Features**.
2. Ketikkan **Zion Canyon** pada jendela **Annotation Construction**. Maka text pada pointer akan berubah.

![Annotation Construction window](../../.gitbook/assets/2%20%283%29.png)

1. Klik peta di sebelah kiri jalan dekat **Grotto Springs**. Lokasi yang Anda klik adalah titik tengah dari fitur baru.

![Creating straight annotation](../../.gitbook/assets/3%20%283%29.png)

1. Putar sketsa anotasi berlawanan arah jarum jam untuk membuat anotasi yang selaras dengan jalan, aliran, dan ngarai.
2. Klik untuk menempatkan anotasi.
3. Tekan tombol E, sehingga mengaktifkan alat Edit Annotation. Tombol E beralih di antara alat konstruksi, alat Edit, dan alat Edit Anotasi.
4. Tempatkan pointer di atas segitiga merah di tepi fitur anotasi Zion Canyon. Pointer berubah menjadi dua-titik pointer Annotation, memungkinkan Anda untuk mengubah ukuran secara interaktif sehingga fitur lebih sesuai.
5. Seret ke bagian tengah fitur anotasi. Fitur akan mengecil saat Anda menyeretnya.

![Resizing the annotation](../../.gitbook/assets/4%20%288%29.png)

1. Seret fitur anotasi jika Anda perlu memposisikannya kembali.

![Resized annotation feature](../../.gitbook/assets/5%20%283%29.png)

## 3.8 Membuat Anotasi Yang Mengikuti Tepi Garis

Model anotasi berikutnya yang akan dibuat adalah model anotasi yang mengikuti anotasi fitur, yang dirancang untuk mengikuti atau menyesuaikan bentuk garis atau tepi poligon. Akan digunakan construction tool **Follow Feature** untuk membuat anotasi yang mengikuti bentuk jalan dan menggunakan atribut jalan sebagai teks untuk anotasi.

1. Dalam jendela **Create Features**, klik template fitur anotasi **Default** dalam layer **RoadsAnno**.
2. Klik construction tool   **Follow Feature** ![Follow Feature](../../.gitbook/assets/6%20%281%29.png) pada jendela **Create Features**.
3. Dalam jendela **Annotation Construction**, klik **Follow Feature Options** ![Follow Feature Options](../../.gitbook/assets/7%20%284%29.png) untuk mengatur opsi seperti apa anotasi akan ditempatkan saat diseret di sepanjang aliran. Opsiharus diset saat membuat anotasi follow feature. Jika tidak, maka dibuat anotasi melengkung dan yang ditempatkan di sisi kursor aktif pada posisi 100 meter. Klik  **OK** jika telah selesai.

![Follow Feature Options dialog box](../../.gitbook/assets/8%20%285%29.png)

1. Klik **Find Text** ![Find Text](../../.gitbook/assets/9%20%283%29.png) dalam jendela **Annotation Construction**. **Find Text** memungkinkan Anda mengklik fitur dan mengisi string anotasi dengan atribut dari fitur lain.
2. Gerakkan pointer ke fitur jalan yang bercabang ke timur dari persimpangan **Zion Canyon Scenic Drive** kemudian snap dan klik jalan. **Highway 9** harusnya muncul pada **Text** box dalam jendela **Annotation Construction** and pada pointer tool. Jika Taman Nasional Zion atau Clear Creek muncul, tekan tombol N untuk menelusuri string teks yang mungkin atau klik **Find Text**, gerakkan pointer di atas fitur jalan, lalu coba lagi.
3. Klik fitur jalan, yang telah tersorot, dan drag fitur anotasi Highway 9 di sepanjang garis. Tekan tombol L jika Anda perlu membalik arah baca.![Making the Highway 9 feature follow the road](../../.gitbook/assets/10%20%282%29.png)
4. Klik untuk menempatkan anotasi.

Anda dapat terus menempatkan anotasi yang belum ditempatkan, mengedit anotasi, membuat fitur anotasi baru, dan menghapus anotasi yang tidak diinginkan hingga peta sesuai dengan kebutuhan Anda. Anotasi ini disimpan dalam kelas fitur anotasi geodatabase, yang masing-masing dapat digunakan kembali pada peta lain. Setelah selesai mengedit, jangan lupa menyimpannya.

1. Klik menu **Editor** pada toolbar **Editor** kemudian klik **Stop Editing**.
2. Klik **Yes** untuk menyimpan editan.
3. Tutup ArcMap jika sudah selesai mengejakan tutorial ini. Tidak perlu menyimpan kembali dokumen peta.

Dalam latihan ini, Anda membuat fitur anotasi baru, mengedit ukuran dan posisinya, mengatur string teks untuk fitur anotasi baru menggunakan atribut dari fitur lain, dan menempatkan fitur anotasi sepanjang garis.

