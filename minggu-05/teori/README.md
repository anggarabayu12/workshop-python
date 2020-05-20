# Minggu-05


### Fancier Output Formatting

- Untuk menggunakan string yang diformat , mulailah string dengan f atau F sebelum tanda kutip pembuka atau triple quotation mark. Di dalam string ini, Anda bisa menulis ekspresi Python antara { dan } karakter yang bisa merujuk ke variabel atau nilai literal.

- Metode string str.format() membutuhkan usaha lebih manual. Anda masih akan menggunakan { dan }untuk menandai di mana suatu variabel akan diganti dan dapat memberikan arahan pemformatan terperinci, tetapi Anda juga harus memberikan informasi yang akan diformat.

   Fungsi str() dimaksudkan untuk mengembalikan representasi dari nilai-nilai yang cukup terbaca-manusia, sementara repr() dimaksudkan untuk menghasilkan representasi yang dapat dibaca oleh interpreter (atau akan memaksa SyntaxError jika tidak ada setara sintaks). Untuk objek yang tidak memiliki representasi khusus untuk konsumsi manusia, str() akan mengembalikan nilai yang sama dengan repr(). Banyak nilai, seperti angka atau struktur seperti daftar dan kamus, memiliki representasi yang sama menggunakan kedua fungsi tersebut.

### Formatted String Literals

   Formatted String Literals (f-strings) memungkinkan untuk memasukkan nilai ekspresi Python di dalam string dengan mengawali string dengan f atau F dan menulis ekspresi sebagai {eksprsi}.

### The String format() method

   Tanda kurung dan karakter di dalamnya (disebut bidang format) diganti dengan objek yang diteruskan ke metode str.format(). Angka dalam tanda kurung dapat digunakan untuk merujuk ke posisi objek yang dilewatkan ke dalam metode str.format().

### Manual String Formatting

   Metode string str.rjust() membenarkan string dalam bidang lebar yang diberikan oleh padding dengan spasi di sebelah kiri. Ada metode serupa str.ljust() dan str.center(). Metode ini tidak menulis apa pun, mereka hanya mengembalikan string baru. Jika string input terlalu panjang, mereka tidak memotongnya, tetapi mengembalikannya tidak berubah. Ada metode lain str.zfill(), yang melapisi string angka di sebelah kiri dengan nol.

### Old string formatting

   Operator % dapat digunakan untuk string format. Ini menafsirkan argumen kiri seperti string sprintf() untuk diterapkan ke argumen yang benar dan mengembalikan string yang dihasilkan dari operasi pemformatan ini.

### Reading and Writing Files

   open()mengembalikan file objek , dan ini paling sering digunakan dengan dua argumen: .open(filename, mode).
`f = open('workfile', 'w')`

   Argumen pertama adalah string yang berisi nama file. Argumen kedua adalah string lain yang berisi beberapa karakter yang menggambarkan cara file akan digunakan. mode bisa 'r' ketika file hanya akan dibaca, 'w' hanya untuk menulis (file yang ada dengan nama yang sama akan dihapus), dan 'a'membuka file untuk ditambahkan; setiap data yang ditulis ke file secara otomatis ditambahkan ke bagian akhir. 'r+' membuka file untuk membaca dan menulis. The Modus argumen adalah opsional; 'r' akan diasumsikan jika dihilangkan.

### Methods of File Objects

   Untuk membaca konten file, panggil menggunakan f.read(size), yang membaca sejumlah data dan mengembalikannya sebagai string (dalam mode teks) atau objek byte (dalam mode biner). Size adalah argumen numerik opsional. Ketika size dihilangkan atau negatif, seluruh isi file akan dibaca dan dikembalikan. Jika akhir file telah tercapai, f.read()akan mengembalikan string kosong ('').
   
   f.readline() membaca satu baris dari file; karakter baris baru (\n) dibiarkan di akhir string, dan hanya dihilangkan pada baris terakhir file jika file tidak berakhir pada baris baru. Ini membuat nilai pengembalian tidak ambigu; jika f.readline()mengembalikan string kosong, akhir file telah tercapai, sementara baris kosong diwakili oleh '\n', string yang hanya berisi satu baris baru.
   
   f.write(string)menulis isi string ke file, mengembalikan jumlah karakter yang ditulis.
   
   f.tell() mengembalikan integer yang memberikan posisi objek file saat ini dalam file yang direpresentasikan sebagai jumlah byte dari awal file ketika dalam mode biner dan angka buram ketika dalam mode teks.
   
### Saving structured data with json

   String dapat dengan mudah ditulis dan dibaca dari file. Angka membutuhkan sedikit usaha, karena read()metode ini hanya mengembalikan string, yang harus diteruskan ke fungsi seperti int(), yang mengambil string seperti '123' dan mengembalikan nilai numerik 123. Ketika Anda ingin menyimpan tipe data yang lebih kompleks seperti daftar bersarang dan kamus, penguraian dan serialisasi dengan tangan menjadi rumit.