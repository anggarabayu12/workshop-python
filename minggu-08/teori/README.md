# Minggu-08

## Brief Tour of the Standard Library

### Operating System Interface
   Modul os menyediakan puluhan fungsi untuk berinteraksi dengan sistem operasi. Fungsi bawaan dir() dan help() berguna sebagai alat bantu interaktif untuk bekerja dengan modul besar seperti os.

### File Wildcards
   Modul glob menyediakan fungsi untuk membuat daftar berkas dari pencarian wildcard di direktori.

### Command Line Arguments
   RSkrip utilitas umum seringkali perlu memproses argumen baris perintah. Argumen-argumen ini disimpan dalam atribut argv dari modul sys sebagai daftar. Modul argparse menyediakan mekanisme yang lebih canggih untuk memproses argumen baris perintah. Script berikut mengekstrak satu atau lebih nama file dan sejumlah baris opsional untuk ditampilkan.

### Error Output Redirection and Program Termination
   Modul sys juga memiliki atribut untuk stdin, stdout, dan stderr. Yang terakhir berguna untuk mengirimkan peringatan dan pesan kesalahan untuk membuatnya terlihat bahkan ketika stdout telah dialihkan.

### String Pattern Matching
   Modul re menyediakan alat ekspresi reguler untuk pemrosesan string lanjutan. Untuk pencocokan dan manipulasi yang kompleks, ekspresi reguler menawarkan solusi yang ringkas dan dioptimalkan.

### Mathematics
   Modul math memberikan akses ke fungsi-fungsi pustaka C yang mendasari untuk matematika angka pecahan floating point. Modul random menyediakan alat untuk membuat pilihan acak. Dan Modul statistics menghitung sifat statistik dasar (rata-rata, median, varian, dll.) dari data numerik.

### Internet Access
   Ada sejumlah modul untuk mengakses internet dan memproses protokol internet. Dua yang paling sederhana adalah urllib.request untuk mengambil data dari URL dan smtplib untuk mengirim email.
   
### Dates and Times
   Modul datetime menyediakan kelas untuk memanipulasi tanggal dan waktu dengan cara yang sederhana dan kompleks. Sementara aritmatika tanggal dan waktu didukung, fokus implementasi adalah pada ekstraksi anggota yang efisien untuk pemformatan dan manipulasi keluaran. Modul ini juga mendukung objek yang sadar zona waktu.
   
### Data Compression
   Format pengarsipan dan kompresi data umum didukung langsung oleh modul-modul yang ada antara lain: :mod: zlib, gzip, bz2, lzma, zipfile dan tarfile.
   
### Performance Measurement
   Beberapa pengguna Python mengembangkan minat yang mendalam untuk mengetahui kinerja relatif dari berbagai pendekatan untuk masalah yang sama. Python menyediakan alat pengukuran yang segera menjawab pertanyaan-pertanyaan itu.

   Misalnya, mungkin tergoda untuk menggunakan fitur tuple packing dan unpacking daripada pendekatan tradisional untuk bertukar argumen. Modul :mod: timeit dengan cepat menunjukkan keunggulan kinerja secara sederhana. Berbeda dengan granularity tingkat halus timeit, modul profile dan pstats menyediakan alat untuk mengidentifikasi bagian kritis waktu dalam blok kode yang lebih besar.
   
### Quality Control
   Salah satu pendekatan untuk mengembangkan perangkat lunak berkualitas tinggi adalah dengan menulis tes untuk setiap fungsi yang dikembangkan dan untuk sering menjalankan tes tersebut selama proses pengembangan.
   
   Modul doctest menyediakan alat untuk memindai modul dan memvalidasi tes yang tertanam dalam dokumen program. Konstruksi pengujian sesederhana memotong dan menempel panggilan khas beserta hasilnya ke dalam docstring. Ini meningkatkan dokumentasi dengan memberikan contoh kepada pengguna dan memungkinkan modul doctest untuk memastikan kode tetap benar untuk dokumentasi:
   
### Output Formatting
   Modul reprlib menyediakan versi repr() yang disesuaikan untuk tampilan yang disingkat dari wadah containers yang besar. Modul pprint menawarkan kontrol yang lebih canggih atas pencetakan objek bawaan dan yang ditentukan pengguna dengan cara yang dapat dibaca oleh interpreter. Modul textwrap memformat paragraf teks agar sesuai dengan lebar layar yang diberikan. Modul locale mengakses basis data format data kultur khusus. Atribut pengelompokan fungsi format lokal locale menyediakan cara langsung memformat angka dengan pemisah grup.
   
### Templating
   Modul string menyertakan kelas serbaguna Template dengan sintaks yang disederhanakan yang cocok untuk diedit oleh pengguna. Ini memungkinkan pengguna untuk menyesuaikan aplikasi mereka tanpa harus mengubah aplikasi.

   Format ini menggunakan nama penampung yang dibentuk oleh $ dengan pengidentifikasi Python yang valid (karakter alfanumerik dan garis bawah). Mengitari placeholder dengan kurung kurawal memungkinkannya diikuti oleh lebih banyak huruf alfanumerik tanpa spasi. Menulis $$ menciptakan satu yang terpisah $.
   
   Metode substitute() memunculkan KeyError saat placeholder tidak disertakan dalam dictionary atau argumen kata kunci keyword argument. Untuk aplikasi gaya gabungan-surat mail-merge, data yang diberikan pengguna mungkin tidak lengkap dan metode safe_substitute() mungkin lebih tepat --- itu akan membuat placeholder tidak berubah jika data hilang.
   
   Subkelas templat dapat menentukan pembatas khusus. Misalnya, utilitas penggantian nama setumpuk batch untuk browser foto dapat memilih untuk menggunakan tanda persen untuk penampung seperti tanggal saat ini, nomor urut gambar, atau format berkas. Aplikasi lain untuk templating adalah memisahkan logika program dari detail berbagai format output. Ini memungkinkan untuk mengganti templat khusus untuk file XML, laporan teks biasa, dan laporan web HTML.
   
### Working with Binary Data Record Layouts
   Modul struct menyediakan pack() dan unpack() berfungsi untuk bekerja dengan format rekaman biner yang memiliki panjang variabel. Contoh berikut menunjukkan bagaimana cara loop tajuk header informasi dalam berkas ZIP tanpa menggunakan modul zipfile. Kode paket "H" dan "I" masing-masing mewakili dua dan empat byte angka yang tidak bertanda unsigned. "<" Menunjukkan bahwa mereka adalah ukuran standar dan dalam urutan byte little-endian.

### Multi-threading
   Threading adalah teknik untuk memisahkan tugas yang tidak tergantung secara berurutan. Utas threads dapat digunakan untuk meningkatkan responsif aplikasi yang menerima masukan pengguna saat tugas lain beroperasi di latar belakang. Kasus penggunaan terkait menjalankan I/O secara paralel dengan perhitungan di utas thread lainnya.

### Logging
   Modul logging menawarkan sistem pencatatan logging yang lengkap dan fleksibel. Paling sederhana, catatan log pesan dikirim ke berkas atau ke sys.stderr.

### Weak References
   Python melakukan manajemen memori otomatis (penghitungan referensi untuk sebagian besar objek dan garbage collection untuk menghilangkan siklus). Memori dibebaskan tidak lama setelah referensi terakhir untuk itu telah dihilangkan.

   Pendekatan ini berfungsi dengan baik untuk sebagian besar aplikasi tetapi kadang-kadang ada kebutuhan untuk melacak objek hanya selama mereka digunakan oleh sesuatu yang lain. Sayangnya, hanya melacak mereka membuat referensi yang membuatnya permanen. Modul weakref menyediakan alat untuk melacak objek tanpa membuat referensi. Ketika objek tidak lagi diperlukan, itu secara otomatis dihapus dari tabel weakref dan panggilan balik callback dipicu untuk weakref. Aplikasi yang umum termasuk caching objek yang mahal untuk dibuat.

### Tools for Working with Lists
   Banyak kebutuhan struktur data dapat dipenuhi dengan tipe daftar list bawaan. Namun, kadang-kadang ada kebutuhan untuk implementasi alternatif dengan mengorbankan kinerja yang menurun.

   Modul array menyediakan objek array() yang seperti daftar list dimana hanya menyimpan data homogen dan menyimpannya dengan lebih kompak. Contoh berikut menunjukkan array angka yang disimpan sebagai dua byte angka biner yang tidak ditandai (kode tipe "H") daripada 16 byte per entri biasa untuk daftar list reguler objek int Python.
   
   Modul collections menyediakan objek deque() yang seperti daftar list dengan tambahan yang lebih cepat dan muncul dari sisi kiri tetapi pencarian yang lebih lambat di tengah. Objek-objek ini sangat cocok untuk mengimplementasikan antrian dan pencarian pohon pertama yang luas breadth first tree searches.
   
   Selain implementasi daftar list alternatif, di pustaka juga menawarkan alat-alat lain seperti modul bisect dengan fungsi untuk memanipulasi daftar list yang diurutkan.
   
   Modul heapq menyediakan fungsi untuk mengimplementasikan heaps berdasarkan daftar list reguler. Entri dengan nilai terendah selalu disimpan di posisi nol. Ini berguna untuk aplikasi yang berulang kali mengakses elemen terkecil tetapi tidak ingin mengoperasikan daftar pengurutan list secara penuh.

### Decimal Floating Point Arithmetic
   Modul decimal menawarkan Decimal tipe data untuk aritmatika pecahan desimal. Dibandingkan dengan implementasi bawaan float dari pecahan floating point biner, kelas ini sangat membantu

- aplikasi keuangan dan penggunaan lainnya yang membutuhkan representasi desimal yang tepat,

- kontrol atas presisi,

- kontrol atas pembulatan untuk memenuhi persyaratan sah legal atau peraturan,

- pelacakan tempat desimal yang signifikan, atau

- aplikasi tempat pengguna mengharapkan hasil agar sesuai dengan perhitungan yang dilakukan dengan tangan.

   Hasil Decimal menjaga akhiran trailing nol, secara otomatis menyimpulkan empat tempat signifikansi dari multiplicands dengan dua tempat signifikansi. Desimal mereproduksi matematika seperti yang dilakukan dengan tangan dan menghindari masalah yang dapat muncul ketika pecahan floating point biner tidak dapat secara tepat mewakili jumlah desimal.

   Representasi yang tepat memungkinkan kelas Decimal untuk melakukan perhitungan modulo dan tes persamaan yang tidak cocok untuk angka pecahan floating point biner.
   
   Modul decimal menyediakan aritmatika dengan ketelitian sebanyak yang dibutuhkan.
