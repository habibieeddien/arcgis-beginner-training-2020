# Latihan 4a: Mengedit Fitur Share Dengan Topologi Peta

## 4.1 Topologi Peta

Banyak dataset vektor berisi fitur yang men-share geometri. Misalnya, fitur poligon sering membentuk fabric dan kadang-kadang bertemu dengan garis. Daerah aliran sungai dan daerah hidrologi memiliki tepi yang sama, dan poligon danau mungkin berbatasan dengan poligon tutupan lahan dan garis pantai. Toolbar topologi berisi tool untuk menangani fitur terkait topologi.

Topologi peta membentuk hubungan topologi antara bagian-bagian fitur yang kebetulan bertemu. Anda dapat secara simultan mengedit fitur shared dengan tool-tool topologi saat Anda membuat topologi peta.

ArcGIS Desktop Basic dapat digunakan membuat dan mengedit topologi peta. sedangkan ArcGIS Desktop Standard dan ArcGIS Desktop Advanced juga dapat mengedit topologi geodatabase, yang mendefinisikan seperangkat aturan tentang hubungan antara kelas fitur dalam dataset fitur.

## 4.2 Membuat Topologi Peta

Prasyarat:

Buka aplikasi ArcMap dan tampilkan toolbar **Editor, Gertakan**, dan **Topologi**.

Dalam latihan ini, akan melakukan perbaruan beberapa fitur daerah aliran sungai dalam dua layer dengan membuat topologi peta.

1. Klik tombol **Open**  ![Open](../../.gitbook/assets/0%20%2810%29.png) pada toolbar **Standard**.
2. Cari dokumen peta **MapTopology.mxd** yang terletak di directory \Editing\Topology dimana ArcGis diinstal. \(C:\ArcGIS\ArcTutor is the default location.\)
3. Buka peta tersebut dengan klik **Open**.
4. Jika peta tersebut sudah terbuka, akan ada peringatan untuk menutupnya. Anda dapat menutupnya tanpa menyimpan perubahan.

Tampilan peta:

![Map topology study area](../../.gitbook/assets/1%20%284%29.png)

Peta tersebut memiliki dua layer fitur. Bagian hydrologis berisi fitur poligon merepresentasikan tiga wilayah hidrologis besar di AS bagian baratdaya. Perhatikan bahwa sebagian DAS daerah Great Basin telah dihilangkan dari dataset tutorial. Unit hidrologi mengandung fitur poligon yang mewakili daerah aliran sungai yang lebih kecil di wilayah ini. Fitur-fitur di lapisan unit Hydrologic dapat terlihat karena fitur wilayah Hydrologic sebagian transparan.

Data regional diperoleh dengan meleburkan unit-unit hidrologi yang lebih kecil, sehingga batas-batas fitur di wilayah Hidrologi sudah bertepatan dengan batas-batas daerah aliran sungai yang lebih kecil. Dalam latihan ini, Anda akan membuat topologi peta untuk memungkinkan Anda mengedit simpul yang membentuk garis tepi bersama di persimpangan beberapa fitur.

1. Klik menu **Editor** pada toolbar **Editor** dan klik **Start Editing**.

Sebelum Anda membuat topologi peta, perbesar area yang ingin Anda edit. Memperbesar suatu area akan mengurangi jumlah fitur yang dapat dianalisa saat membangun cache topologi.

1. Klik **Bookmarks** kemudian klik **3 Region Divide**.

Peta akan membesar pada area ter-bookmark. Sehingga terlihat labels untuk aliran sungai yang lebih kecil

1. Klik **Select Topology** ![Select Topology](../../.gitbook/assets/2%20%286%29.png) pada toolbar **Topology**. Kotak dialog **Select Topology** akan muncul.

Pada kotak dialog **Select Topology**, dapat dipilih layer yang akan digunakan dalam topologi dan mengatur toleransi cluser. Toleransi kluster menentukan seberapa dekat bagian-bagian fitur sebelum bagian fitur tersebut dianggap kebetulan. Jika peta Anda memiliki topologi geodatabase di dalamnya \(membutuhkan lisensi ArcGIS Desktop Standard atau ArcGIS Desktop Advanced\), Anda juga dapat memilih untuk mengedit topologi geodatabase.

you can choose the layers that will participate in the topology and set a cluster tolerance. The cluster tolerance defines how close together parts of features must be before they are considered coincident. If your map has a geodatabase topology in it \(and you have an ArcGIS Desktop Standard or ArcGIS Desktop Advanced license\), you could also choose to edit the geodatabase topology instead of the map topology.

1. Klik tombol **Select All**. Dipilih semua fitur yang ada pada peta dari kedua layer untuk diikutkan dalam topologi peta.

![Choosing the layers to participate in the map topology](../../.gitbook/assets/3%20%286%29.png)

Pada bagian Opsi, terdapat toleransi cluster. Dimana, dataset berada dalam sistem koordinat Mercator transversal universal, dan unit toleransi kluster adalah meter. Terima toleransi klaster default, dimana merupakan nilai minimum yang mungkin.

1. Klik **OK**

## 4.3 Menemukan Fitur Shared

Sekarang akan mengedit topologi peta menggunakan tool Edit Topologi untuk memilih garis tepi dan menentukan fitur mana yang men-share-nya. Anda dapat menggunakan Shared Features window untuk menyelidiki fitur mana yang berbagi garis tepi topologi tertentu dan mengontrol apakah pengeditan yang Anda buat untuk elemen topologi tertentu akan dibagikan oleh fitur-fitur tertentu.

1. Klik tool **Topology Edit**  ![Topology Edit Tool](../../.gitbook/assets/4%20%289%29.png) pada toolbar **Topology**.
2. Klik garis tepi yang di-share oleh **East Fork Sevier. Utah. polygon \(\#16030002\)** dan **Kanab. Arizona, Utah. polygon \(\#15010003\)**.

Garis Tepi terpilih akan berubah warna. Garis tepi ini juga di-share oleh poligon regional yang lebih besar. Untuk memeriksanya, dapat digunakan Shared Features window.

1. Klik  **Shared Features** ![Shared Features](../../.gitbook/assets/5%20%288%29.png) pada toolbar **Topology**.

Nama-nama kedua lapisan dalam topologi peta, wilayah Hidrologi dan unit Hidrologi, muncul dengan tanda centang pada jendela ini. Pengecekan ini berarti bahwa elemen topologi yang dipilih dibagikan oleh fitur di lapisan ini dan dipengaruhi oleh pengeditan yang Anda lakukan pada garis tepi yang dibagikan. Selanjutnya, Anda akan melihat fitur mana yang berbagi garis tepi ini.

![The features that share the selected edge](../../.gitbook/assets/6%20%288%29.png)

1. Klik **Great Basin Region** dalam **Hydrologic region**.

bagian Great Basin akan berkedip.

1. Klik **East Fork Sevier. Utah.** dalam  **Hydrologic unit**.

unit Fork Sevier akan berkedip.

1. Tutup jendela **Shared Features**.

4.4 Mengedit Garis Tepi Bersama\(Shared Edge\) Dalam Topologi Peta

Sekarang setelah Anda melihat bahwa fitur yang Anda perlu perbarui berbagi garis tepi ini, Anda akan memperbarui batas daerah aliran sungai agar lebih sesuai dengan medan.

1. Aktifkan layer **Hillshaded terrain** dari table of contents.

![Study area with the hillshade layer displaying](../../.gitbook/assets/7%20%286%29.png)

Ini adalah area kecil berbukit yang diekstraksi dari National Elevation Dataset Shaded Relief Image Service, yang diterbitkan oleh United States Geological Survey. Anda akan menggunakan gambar ini, serta terdapat pedoman yang telah ditambahkan, untuk memperbarui data daerah aliran sungai.

1. Tekan dan tahan tombol Z dan seret kotak di sekitar garis tepi yang dipilih. Pointer menjadi alat Zoom In.

Data DAS yang Anda miliki berasal dari Dataset Hidrografi Nasional resolusi-menengah, yang diterbitkan oleh Survei Geologi AS dan Badan Perlindungan Lingkungan Amerika Serikat. Data ini dikompilasi pada skala 1: 100.000. Hillshade Ketinggian Elevasi Nasional diturunkan dari data model elevasi digital skala 1: 24.000. Anda akan menggunakan data hillshade beresolusi lebih tinggi untuk meningkatkan batas daerah aliran sungai.

1. Klik dua kali pada garis tepi. Dapat melihat simpul \(berwarna hijau\) yang menentukan bentuk garis tepi ini.

![Viewing the vertices that make up the edge](../../.gitbook/assets/8%20%284%29.png)

1. Pindahkan pointer ke atas simpul kedua dari ujung timur garis tepi. Ketika pointer berubah menjadi sebuah kotak dengan empat panah, klik titik tersebut, seret ke arah barat laut, lalu letakkan di guideline biru.

![Dragging the vertex to the guideline](../../.gitbook/assets/9%20%284%29.png)

Anda bisa terus membentuk kembali ujung garis tepi ini, tetapi ada cara yang lebih cepat untuk memperbaruinya.

1. Klik sekali pada peta, dari garis tepi, untuk membatalkan pilihan. Kemudian klik lagi garis tepi untuk memilihnya kembali.

## 4.4 Membentuk Kembali Shared-Edge Dalam Topologi Peta

Sekarang Anda akan menggunakan edit sketch untuk membentuk kembali garis tepi bersama\(shared edge\). Anda harus menggunakan alat Reshape Edge dan snap ke garis tepi batas air.

1. Pastikan edge snapping sudah enabled. Jika belum, klik  **Edge Snapping** ![Edge Snapping](../../.gitbook/assets/10%20%281%29.png) pada toolbar **Snapping**.
2. Klik tool **Reshape Edge**  ![Reshape Edge Tool](../../.gitbook/assets/11%20%281%29.png) pada toolbar **Topology** .
3. Gerakkan pointer ke garis tepi topologi yang dipilih dan guideline biru mulai menyimpang.

![Reshaping the topology edge](../../.gitbook/assets/12.png)

1. Klik garis tepi\(edge\) untuk mulai mengedit sketch.
2. Terus menambahkan simpul di sepanjang guideline. Anda dapat menahan tombol SPACEBAR untuk mematikan snapping sementara jika Anda mengalami kesulitan menempatkan garis reshape di mana Anda ingin berada sepanjang garis biru.
3. Pastikan bahwa simpul terakhir yang Anda tambahkan ke sketch terkunci ke garis tepi dekat simpul yang Anda pindahkan
4. Klik kanan dimana saja pada peta kemudian klik **Finish Sketch**.

Garis tepi terlihat seperti ini setelah Anda menyelesaikan sketsa:

![Edge after being reshaped](../../.gitbook/assets/13%20%281%29.png)

Ada lokasi lain di dataset di mana Anda dapat membentuk kembali dan memodifikasi garis tepi untuk memperbarui fitur agar sesuai dengan pedoman di medan berbukit. Anda dapat melanjutkan mengedit topologi atau menghentikan pengeditan jika Anda selesai.

1. Klik menu **Editor** pada toolbar **Editor** kemudian klik **Stop Editing**.
2. klik **Yes** untuk menyimpan.
3. Tutup ArcMap jika Anda selesai mengerjakan tutorial. Anda tidak perlu menyimpan dokumen peta.

