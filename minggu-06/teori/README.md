# Minggu-06


### Syntax Errors
   Syntax Errors adalah suatu keadaan saat kode python mengalami kesalahan penulisan. Python interpreter dapat mendeteksi kesalahan ini saat kode dieksekusi.

### Exceptions
   Exceptions adalah suatu keadaan saat penulisan syntax sudah benar, namun kesalahan terjadi karena syntax tidak bisa dieksekusi. Banyak hal yang menyebabkan terjadinya Exceptions, mulai dari kesalahan matematika, kesalahan nama function, kesalahan library, dan lain-lain.

### Handling Exceptions
   Exception handling adalah suatu mekanisme penanganan flow normal program karena terjadi exception dengan melanjutkan flow ke code block lainnya.

### Raising Exceptions
   Pernyataan raise memungkinkan programmer untuk memaksa pengecualian tertentu terjadi. Argumen satu-satunya untuk raise menunjukkan pengecualian yang dimunculkan. Ini harus berupa instance pengecualian atau kelas pengecualian (kelas yang berasal dari Exception).

### User-defined Exceptions
   Program dapat memberi nama pengecualian mereka sendiri dengan membuat kelas pengecualian baru. Pengecualian biasanya berasal dari kelas Exception, baik secara langsung maupun tidak langsung. Kelas pengecualian dapat didefinisikan yang melakukan apa saja yang dapat dilakukan oleh kelas lain, tetapi biasanya dibuat sederhana, seringkali hanya menawarkan sejumlah atribut yang memungkinkan informasi tentang kesalahan tersebut diekstraksi oleh penangan sebagai pengecualian.

### Defining Clean-up Actions
   Pernyataan try memiliki klausul opsional lain yang dimaksudkan untuk menentukan tindakan bersih-bersih yang harus dijalankan dalam semua keadaan.
   
   Jika ada klausa finally, klausa finally akan dieksekusi sebagai tugas terakhir sebelum pernyataan try selesai. Klausa finally berjalan atau tidaknya pernyataan try menghasilkan pengecualian. Poin-poin berikut membahas kasus yang lebih kompleks ketika pengecualian terjadi :

- Jika pengecualian terjadi selama eksekusi klausa try, pengecualian dapat ditangani oleh klausa except. Jika pengecualian tidak ditangani oleh klausa except, pengecualian akan muncul kembali setelah klausa finally dieksekusi.

- Pengecualian dapat terjadi selama eksekusi klausa except atau else. Sekali lagi, pengecualian akan dinaikkan kembali setelah klausa finally telah dieksekusi.

- Jika pernyataan try mencapai break, pernyataan continue atau return, klausa finally akan mengeksekusi sesaat sebelum break, eksekusi pernyataan continue atau return.

### Predefined Clean-up Actions
   Beberapa objek mendefinisikan tindakan pembersihan standar yang harus dilakukan ketika objek tidak lagi diperlukan, terlepas dari apakah operasi menggunakan objek berhasil atau gagal.