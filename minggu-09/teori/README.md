# Minggu-09

## Virtual Environments and Packages

### Introduction
   Aplikasi Python akan sering menggunakan paket dan modul yang tidak datang sebagai bagian dari pustaka standar. Aplikasi kadang-kadang membutuhkan versi pustaka tertentu, karena aplikasi mungkin mensyaratkan bug tertentu telah diperbaiki atau aplikasi dapat ditulis menggunakan versi usang dari antarmuka pustaka.

   Ini berarti tidak mungkin bagi satu instalasi Python untuk memenuhi persyaratan setiap aplikasi. Jika aplikasi A membutuhkan versi 1.0 dari modul tertentu tetapi aplikasi B membutuhkan versi 2.0, maka persyaratannya bertentangan dan menginstal versi 1.0 atau 2.0 akan membuat satu aplikasi tidak dapat berjalan.

   Solusi untuk masalah ini adalah membuat virtual environment, sebuah struktur direktori mandiri yang berisi instalasi Python untuk versi tertentu dari Python, serta sejumlah paket tambahan.

   Aplikasi yang berbeda kemudian dapat menggunakan lingkungan virtual yang berbeda. Untuk menyelesaikan contoh sebelumnya dari persyaratan yang saling bertentangan, aplikasi A dapat memiliki lingkungan virtual sendiri dengan versi 1.0 yang diinstal sementara aplikasi B memiliki lingkungan virtual lain dengan versi 2.0. Jika aplikasi B membutuhkan pustaka ditingkatkan ke versi 3.0, ini tidak akan mempengaruhi lingkungan aplikasi A.

### Creating Virtual Environments
   Modul yang digunakan untuk membuat dan mengelola lingkungan virtual disebut venv. venv biasanya akan menginstal versi Python terbaru yang Anda miliki. Jika Anda memiliki beberapa versi Python di sistem Anda, Anda dapat memilih versi Python tertentu dengan menjalankan python3 atau versi mana pun yang Anda inginkan.

   Untuk membuat lingkungan virtual, tentukan direktori tempat Anda ingin meletakkannya, dan jalankan modul venv sebagai skrip dengan jalur direktori :
   
   `!python3 -m venv tutorial-env`
   
   Ini akan membuat direktori tutorial-env jika tidak ada, dan juga membuat direktori di dalamnya yang berisi salinan interpreter Python, pustaka standar, dan berbagai berkas pendukung.

   Lokasi direktori yang umum dipakai untuk lingkungan virtual adalah .venv. Nama ini membuat direktori biasanya tersembunyi di shell Anda dan dengan demikian terpencil sambil memberikan nama yang menjelaskan mengapa direktori itu ada. Ini juga mencegah bentrok dengan berkas definisi variabel lingkungan .env yang didukung beberapa peralatan.
   
   Setelah membuat lingkungan virtual, Kita dapat mengaktifkannya.

   Pada Windows, operasikan :
   
   `!tutorial-env\Scripts\activate.bat`
   
   Pada Unix atau MacOS, operasikan :
   
   `!source tutorial-env/bin/activate`

### Managing Packages with pip
   pip memiliki sejumlah sub-perintah: "search", "install", "uninstall", "freeze", dll. Kita dapat menginstal versi terbaru dari suatu paket dengan menyebutkan nama suatu paket dengan menggunakan perintah :
   
   `!pip install novas`
   
   Kita juga dapat menginstal versi spesifik suatu paket dengan memberikan nama paket diikuti dengan == dan nomor versi dengan menggunakan perintah :
   
   `!pip install requests==2.6.0`

Jika Kita menjalankan kembali perintah ini, pip akan melihat bahwa versi yang diminta sudah diinstal dan tidak melakukan apa-apa.

pip show akan menampilkan informasi tentang paket tertentu dengan menggunakan perintah :
    
    `!pip show requests`

pip list akan menampilkan semua paket yang diinstal di lingkungan virtual dengan menggunakan perintah :

    `!pip list`
    
pip freeze akan menghasilkan daftar yang sama dari paket yang diinstal, tetapi keluarannya menggunakan format yang diharapkan oleh pip install. Sebuah konvensi yang umum digunakan adalah meletakkan daftar ini dalam file requirements.txt.

    `!pip freeze > requirements.txt`

requirements.txt kemudian dapat dikirimkan atau commit ke sistem kontrol versi dan dikirim sebagai bagian dari aplikasi. Pengguna kemudian dapat menginstal semua paket yang diperlukan dengan install -r.