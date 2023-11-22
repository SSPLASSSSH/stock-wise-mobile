# stock_wise

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.


Tugas 7

1. Perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter adalah
cara mengelola dan merender data yang berubah
pada statelesswidget tidak memliki keadaan ketika data berubah,yang berarti widget tidak akan berubah dan cocok digunakan untuk tampilan statis dan karena hal ini statelesswidget menjadi lebih efisien dalam segi performa sedangkan pada statefulwidget memiliki keadaan ketika data berubah dan digunakan untuk tampilan data yang berubah dan memiliki lebihbanyak kode untuk setiap implementasinya

2.  seluruh widget yang saya gunakan untuk menyelesaikan tugas ini dan fungsinya masing-masing.
    - MyApp
        - root widget aplikasi
    
    - MaterialApp
        - widget yang digunakan untuk mengkonfigurasi aplikasi dengan properti seperti judul, tema, dan halaman beranda
    
    - MyHomeApp
        - digunakan untuk mengatur tampilan dan perilaku halaman beranda.
    
    - title
        - menentukan judul app
    
    - Theme
        - menentukan tema app seperti themeData, colorScheme
    - home
        - menunjuk ke homepage() yg merupkan halaman utama

    - Scaffold
         - Digunakan untuk membuat kerangka dasar aplikasi dengan AppBar, tubuh, dan lainnya.

    - Appbar 
        - Digunakan untuk membuat bilah atas dengan judul "Stock Wise"

    - SingleChildScrollView
        -  memungkinkan kontennya dapat di-scroll.
    
    - Padding
        - Digunakan untuk memberi padding ke kontennya.

    - Text
        - Digunakan untuk menampilkan teks "Your Stock Wise Inventory" dengan properti tertentu seperti fontsize dan fontWeight.

    - GridView.count
        - widget yang membuat grid layout dengan daftar item.

    - shopcard (statelesswidget)
        -  widget yang digunakan untuk membuat setiap card dengan ikon dan teks.
    
    - Material
        -  digunakan untuk memberikan latar belakang berwarna kuning untuk setiap card.

    - InkWell
        - Digunakan untuk membuat area responsif terhadap sentuhan
    
    - Container
        - Digunakan untuk mengatur konten dalam setiap card

    - Icon
        - Menampilkan ikon yang sesuai dengan setiap item dalam card.

    - SnackBar
        - Digunakan untuk menampilkan pesan yang muncul saat card diklik.

3. Langkah-langkah 

    - Jalankan "flutter create stock_wise"

    - Jalankan "flutter config --enable-web"

    - lalu untukmerapikan proyek buat file dart baru dan import "import 'package:flutter/material.dart';"

    - Kemudian pindahkan claass myhomepage dan myhomepagestate dari main.dart ke menu.dart dan import "import 'package:shopping_list/menu.dart';"

    - ubah sifat widget halaman menjadi stateless dengan mengubah di main dart myHomePage pada bagian MyHomePage(title: 'Flutter Demo Home Page') menajdi MyHomePage()

    - extends StatelessWidget di menu.dart dan ubah key menjadi "MyHomePage({Key? key}) : super(key: key);" dan hapus fungsi state dibawahnya

    - define barangdan icon yang ditambahkan dengan membuat class baru

    - dan buat kode di myHomePage untuk menampilkan logo dan tulisan apa saja

    - lalu saya menambahkan bagian widget build dan membuat class ShopCard untuk menampilkan sesuatu ketika dipencet




Tugas 8

1. `Navigator.push()` berfungsi untuk menambahkan rute tambahan ke tumpukan layar saat ini, menampilkan halaman baru di atas halaman sebelumnya. Di sisi lain, `Navigator.pushReplacement()` juga berfungsi untuk pergantian halaman, namun yang membedakannya adalah navigasi ini tidak menyimpan histori, sehingga halaman baru langsung menggantikan yang sebelumnya tanpa menyimpan jejak histori. penggunaan `Navigator.push()` adalah seperti memindahkan rute dari halaman utama ke suatu halaman lain, sedangkan `Navigator.pushReplacement()` untuk pergantian halaman dari suatu halaman yang retriksi seperti halaman konfirmasi pembayaran.

2.  masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing
    - Container:
        - Menyediakan wadah untuk menempatkan widget lain dan memungkinkan pengaturan seperti padding, margin, dan dekorasi.

    - Row:
        - Menyusun widget secara horizontal dalam satu baris, sering digunakan untuk menyusun elemen-elemen sejajar.

    - Column:
        - Menyusun widget secara vertikal dalam satu kolom, ideal untuk menyusun elemen-elemen berurutan dari atas ke bawah.

    - ListView:
        - Menyusun widget dalam daftar gulir, berguna untuk menampilkan daftar item yang dapat di-scroll.

    - Stack:
        - Menyusun widget secara tumpukan (z-index), memungkinkan penumpukan elemen satu di atas yang lain.

    - Expanded:
        - Mengisi sebanyak mungkin ruang yang tersedia dalam parent widget, umumnya digunakan dalam Row atau Column.

    - Flexible:
        - Memberikan bobot fleksibel untuk anak-anaknya dalam Row atau Column, memungkinkan pengaturan proporsi.

    - GridView:
        - Menyusun widget dalam bentuk grid atau matriks, cocok untuk menampilkan elemen-elemen dalam pola teratur.

    - SizedBox:
        - Memberikan dimensi tetap atau kosong pada widget, membantu mengontrol ukuran atau jarak antara elemen.


3.  Elemen input pada form yang saya pakai pada tugas kali ini dan mengapa saya menggunakan elemen input tersebut

    - Textfield
        - untuk menerima input  berupa teks dari nama buku, deskripsi,amount,harga dan kategori

    - Elevated Button
        -  Untuk menghighlight tombol menyimpan

    - Text Button
        - untuk tombol lainnya dengan tetap menampilkan text

4. Clean Architecture dalam Flutter melibatkan pembagian proyek ke dalam tiga lapisan utama: Domain, Data, dan Presentation. Lapisan Domain berisi aturan bisnis dan logika aplikasi, independen dari platform. Lapisan Data menangani akses ke sumber data, seperti database atau API, sementara lapisan Presentation menangani UI. Penggunaan Use Cases dalam lapisan Domain membantu mengisolasi logika aplikasi, sedangkan Repository memisahkan logika akses data dari implementasinya. Dengan pendekatan ini, aplikasi menjadi lebih mudah diuji, dipelihara, dan memungkinkan perubahan platform tanpa memengaruhi inti aplikasi.

5. Step by Step 
    - membuat drawer dengan membuat file dart baru di direktori baru di lib bernama widgets
    - tambahkan drawer di menu utama dengan diimport dan menambahkan drawer: const LeftDrawer()
    - buat form untuk memasukkan buku di file dart baru
    - pada file dart yang sama munculkan data
    - buat tombol agar bisa dinavigasi menggunakan `Navigator.push()` atau `Navigator.pushReplacement()`
    - melakukan refactoring file dengan membuat terlebih dahulu folder screen di lib, lalu pindahkan sesuai dengan fungsinya.



Tugas 9

1. Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?
    - Kita bisa mengambil data JSON secara langsung ke dalam bentuk `Map<String, dynamic>` tanpa perlu membuat model terlebih dahulu. Meskipun demikian, pendekatan ini tidak dianggap sebagai praktik terbaik karena dapat membuat kode menjadi sulit dibaca dan dipahami, terutama karena sifat dinamis dari nilai-nilainya.

2. Fungsi dari CookieRequest dan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
    - CookieRequest merupakan suatu kelas atau objek yang umumnya digunakan dalam konteks pengembangan aplikasi Flutter untuk menangani permintaan HTTP yang melibatkan pengelolaan cookie. CookieRequest biasanya digunakan untuk menyimpan dan mengelola informasi cookie yang berkaitan dengan permintaan HTTP, seperti menambah atau menghapus cookie.  dan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen dalam aplikasi Flutter agar informasi cookie dapat diakses dan dikelola secara konsisten. Dengan berbagi instance ini, ketika suatu komponen melakukan permintaan HTTP dan mengubah cookie, perubahan tersebut dapat terlihat oleh komponen lainnya. Ini memastikan bahwa seluruh aplikasi dapat berinteraksi dengan server sambil mempertahankan dan memanfaatkan informasi sesi atau keadaan lain yang disimpan dalam cookie, meningkatkan koordinasi dan konsistensi.

3. Mekanisme pengambilan data dari JSON hingga dapat ditampilkan pada Flutter
    - Mendapatkan Data dari API atau Sumber JSON
    - Menerjemahkan Data JSON ke Dart Objects
    - Membuat model Dart yang sesuai dengan struktur data JSON
    - Menerjemahkan data JSON ke dalam objek Dart menggunakan model yang telah dibuat
    - Menampilkan Data di Flutter

4. Mekanisme autentikasi dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter
    - Input Data Akun pada Flutter
        - Pengguna memasukkan informasi akun seperti nama pengguna dan kata sandi melalui antarmuka pengguna Flutter. Data ini kemudian dikirim ke backend Django.

    - Permintaan ke API Django
        - Aplikasi Flutter menggunakan paket-paket seperti `http` untuk mengirim permintaan HTTP ke API Django. Permintaan ini membawa informasi akun yang dimasukkan oleh pengguna.

    - Proses Autentikasi Django
        - Di backend Django, terdapat sistem autentikasi yang memproses permintaan dari Flutter. Django akan memverifikasi kecocokan informasi akun yang diterima dengan data yang ada di database.

    - Token JWT (JSON Web Token)
        - Jika informasi akun valid, backend Django dapat menghasilkan token JWT. Token ini merupakan tanda bahwa pengguna telah berhasil diautentikasi dan akan digunakan untuk otorisasi di permintaan-permintaan selanjutnya.

    - Pengiriman Token ke Flutter
        - Token JWT kemudian dikirim kembali ke aplikasi Flutter sebagai respons dari permintaan autentikasi. Aplikasi Flutter menyimpan token ini secara lokal.

    - Otorisasi Permintaan Berikutnya
        - Pada setiap permintaan selanjutnya ke API Django, aplikasi Flutter menyertakan token JWT di header permintaan. Django akan memvalidasi token ini untuk memastikan bahwa pengguna memiliki akses yang diperlukan.

    - Tampilan Menu pada Flutter
        - Jika token valid dan pengguna berhasil diautentikasi, aplikasi Flutter dapat menampilkan menu atau halaman tertentu yang hanya dapat diakses oleh pengguna yang telah login.

5. seluruh widget yang saya pakai pada tugas ini dan jelaskan fungsinya masing-masing

     - MyApp
        - root widget aplikasi
    
    - MaterialApp
        - widget yang digunakan untuk mengkonfigurasi aplikasi dengan properti seperti judul, tema, dan halaman beranda
    
    - MyHomeApp
        - digunakan untuk mengatur tampilan dan perilaku halaman beranda.
    
    - title
        - menentukan judul app
    
    - Theme
        - menentukan tema app seperti themeData, colorScheme
    - home
        - menunjuk ke homepage() yg merupkan halaman utama

    - Scaffold
         - Digunakan untuk membuat kerangka dasar aplikasi dengan AppBar, tubuh, dan lainnya.

    - Appbar 
        - Digunakan untuk membuat bilah atas dengan judul "Stock Wise"

    - SingleChildScrollView
        -  memungkinkan kontennya dapat di-scroll.
    
    - Padding
        - Digunakan untuk memberi padding ke kontennya.

    - Text
        - Digunakan untuk menampilkan teks "Your Stock Wise Inventory" dengan properti tertentu seperti fontsize dan fontWeight.

    - GridView.count
        - widget yang membuat grid layout dengan daftar item.

    - shopcard (statelesswidget)
        -  widget yang digunakan untuk membuat setiap card dengan ikon dan teks.
    
    - Material
        -  digunakan untuk memberikan latar belakang berwarna kuning untuk setiap card.

    - InkWell
        - Digunakan untuk membuat area responsif terhadap sentuhan
    
    - Container
        - Digunakan untuk mengatur konten dalam setiap card

    - Icon
        - Menampilkan ikon yang sesuai dengan setiap item dalam card.

    - SnackBar
        - Digunakan untuk menampilkan pesan yang muncul saat card diklik.

    - Listtile
        - untuk menampilkan judul menu pada left drawer
    
    - Listview
        - sebagai wadah untuk menampung widget dan dapat dibuat banyak secara otomatis dengan bantuan builder







