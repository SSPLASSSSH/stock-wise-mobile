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



    

    
