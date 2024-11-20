# Tugas 7

### 1. Stateless Widget dan Stateful Widget
**Stateless Widget** adalah widget yang tidak memiliki status yang dapat berubah. Artinya, ketika widget ini dibangun, ia tidak akan berubah seiring waktu. Contoh penggunaan stateless widget adalah tombol yang tidak memiliki interaksi atau tampilan yang tetap.

**Stateful Widget**, di sisi lain, adalah widget yang memiliki status yang dapat berubah. Widget ini dapat memperbarui tampilan berdasarkan perubahan status. Contoh penggunaan stateful widget adalah form input yang dapat diubah oleh pengguna.

**Perbedaan**:
- Stateless Widget: Tidak memiliki status yang dapat berubah, lebih efisien dalam hal performa.
- Stateful Widget: Memiliki status yang dapat berubah, memungkinkan interaksi dan pembaruan tampilan.

### 2. Widget yang Digunakan dalam Proyek Ini
Dalam proyek ini, beberapa widget yang digunakan antara lain:
- `MaterialApp`: Widget utama yang menyediakan struktur aplikasi.
- `Scaffold`: Menyediakan struktur dasar untuk tampilan aplikasi, termasuk AppBar dan body.
- `GridView`: Menampilkan item dalam bentuk grid.
- `Card`: Menyediakan tampilan yang menarik untuk setiap item.
- `Text`: Menampilkan teks di layar.
- `Icon`: Menampilkan ikon.

### 3. Fungsi dari setState()
Fungsi `setState()` digunakan untuk memberi tahu Flutter bahwa ada perubahan pada status widget, sehingga widget tersebut perlu dibangun ulang. Variabel yang terdampak oleh fungsi ini adalah variabel yang dideklarasikan dalam kelas stateful widget dan digunakan dalam metode build. Ketika `setState()` dipanggil, Flutter akan memanggil kembali metode build untuk memperbarui tampilan.

### 4. Perbedaan antara const dan final
- **const**: Digunakan untuk mendeklarasikan variabel yang nilainya tetap dan tidak dapat diubah. Nilai const harus diketahui pada waktu kompilasi.
- **final**: Digunakan untuk mendeklarasikan variabel yang hanya dapat diatur sekali, tetapi nilainya dapat ditentukan pada waktu runtime.

### 5. Implementasi Checklist
Checklist di atas diimplementasikan dengan cara sebagai berikut:

1. **Membuat Program Flutter Baru dengan Tema E-Commerce**:
   - Proyek ini dibuat dengan tema E-Commerce, di mana pengguna dapat melihat daftar produk, menambah produk, dan melakukan logout.

2. **Membuat Tiga Tombol Sederhana**:
   - Tiga tombol dibuat menggunakan widget `ItemCard`, yang masing-masing mewakili fungsi:
     - **Lihat Daftar Produk**: Tombol ini memungkinkan pengguna untuk melihat daftar produk.
     - **Tambah Produk**: Tombol ini memungkinkan pengguna untuk menambah produk baru.
     - **Logout**: Tombol ini memungkinkan pengguna untuk keluar dari aplikasi.

3. **Mengimplementasikan Warna-Warna yang Berbeda untuk Setiap Tombol**:
   - Setiap tombol diberikan warna yang berbeda:
     - **Lihat Daftar Produk**: Warna biru.
     - **Tambah Produk**: Warna hijau.
     - **Logout**: Warna merah.
   - Warna ini diatur dalam kelas `ItemHomepage` yang digunakan untuk mendefinisikan setiap tombol.

4. **Memunculkan Snackbar dengan Pesan Terkait**:
   - Setiap tombol dilengkapi dengan fungsi `onTap` yang memunculkan `SnackBar` dengan pesan yang sesuai ketika tombol ditekan:
     - "Kamu telah menekan tombol Lihat Daftar Produk" untuk tombol Lihat Daftar Produk.
     - "Kamu telah menekan tombol Tambah Produk" untuk tombol Tambah Produk.
     - "Kamu telah menekan tombol Logout" untuk tombol Logout.
   - Pesan ini ditampilkan menggunakan `ScaffoldMessenger` untuk memberikan umpan balik kepada pengguna.

Implementasi ini memastikan bahwa aplikasi tidak hanya berfungsi dengan baik tetapi juga memberikan pengalaman pengguna yang interaktif dan responsif.

# Tugas 8

### 1. Kegunaan const di Flutter
**Kegunaan const**: `const` digunakan untuk mendeklarasikan variabel yang nilainya tetap dan tidak dapat diubah. Keuntungan menggunakan `const` adalah:
- **Performa**: Mengurangi penggunaan memori karena objek yang dideklarasikan dengan `const` hanya dibuat sekali dan dapat digunakan kembali.
- **Konsistensi**: Memastikan bahwa nilai tidak berubah selama siklus hidup aplikasi.

**Kapan menggunakan const**: Gunakan `const` ketika Anda tahu bahwa nilai tidak akan berubah dan dapat ditentukan pada waktu kompilasi.

**Kapan tidak menggunakan const**: Hindari `const` jika nilai variabel perlu diubah selama runtime.

### 2. Perbandingan Column dan Row
**Column** dan **Row** adalah widget layout yang digunakan untuk mengatur elemen dalam arah vertikal dan horizontal.

- **Column**: Mengatur widget secara vertikal.
  ```dart
  Column(
    children: <Widget>[
      Text('Item 1'),
      Text('Item 2'),
      Text('Item 3'),
    ],
  )
  ```

- **Row**: Mengatur widget secara horizontal.
  ```dart
  Row(
    children: <Widget>[
      Text('Item A'),
      Text('Item B'),
      Text('Item C'),
    ],
  )
  ```

### 3. Elemen Input pada Halaman Form
Pada halaman form yang dibuat, elemen input yang digunakan antara lain:
- `TextField`: Untuk input teks.
- `Checkbox`: Untuk pilihan ya/tidak.
- `DropdownButton`: Untuk pilihan dari daftar.

**Elemen input lain yang tidak digunakan**: 
- `Radio`: Untuk pilihan tunggal dari beberapa opsi.
- `Slider`: Untuk input nilai numerik dalam rentang tertentu.

### 4. Mengatur Tema dalam Aplikasi Flutter
Untuk mengatur tema dalam aplikasi Flutter, Anda dapat menggunakan `ThemeData` dalam widget `MaterialApp`. Ini memastikan konsistensi dalam warna, font, dan gaya di seluruh aplikasi.

**Implementasi tema**: Ya, tema telah diimplementasikan dalam aplikasi dengan mendefinisikan warna dan gaya di `MaterialApp`.

### 5. Menangani Navigasi dalam Aplikasi
Navigasi dalam aplikasi dengan banyak halaman dapat ditangani menggunakan `Navigator` dan `Routes`. Anda dapat mendefinisikan rute dalam `MaterialApp` dan menggunakan `Navigator.push` untuk berpindah antar halaman.

# Tugas 9

## 1. Mengapa Kita Perlu Membuat Model untuk Melakukan Pengambilan atau Pengiriman Data JSON?
Membuat model untuk pengambilan atau pengiriman data JSON sangat penting karena model memberikan struktur yang jelas untuk data yang kita gunakan dalam aplikasi. Dengan model, kita dapat memastikan bahwa data yang diterima atau dikirim sesuai dengan format yang diharapkan. Jika kita tidak membuat model terlebih dahulu, kemungkinan besar akan terjadi error, seperti kesalahan dalam penamaan atribut atau tipe data yang tidak sesuai. Hal ini dapat menyebabkan aplikasi tidak dapat memproses data dengan benar, yang pada akhirnya dapat mengakibatkan crash atau perilaku yang tidak diinginkan.

## 2. Fungsi dari Library HTTP
Library `http` digunakan untuk melakukan permintaan HTTP ke server. Dalam tugas ini, library ini memungkinkan aplikasi untuk berkomunikasi dengan backend Django, baik untuk mengambil data (GET) maupun mengirim data (POST). Dengan menggunakan library ini, kita dapat dengan mudah mengelola permintaan dan respons, serta menangani berbagai jenis data, termasuk JSON.

## 3. Fungsi dari CookieRequest
`CookieRequest` adalah kelas yang digunakan untuk mengelola permintaan HTTP dengan dukungan untuk cookie. Ini penting dalam konteks autentikasi, di mana cookie digunakan untuk menyimpan informasi sesi pengguna. Instance `CookieRequest` perlu dibagikan ke semua komponen di aplikasi Flutter agar setiap permintaan yang dilakukan dapat membawa informasi sesi yang sama, sehingga pengguna tetap terautentikasi saat berpindah antar halaman.

## 4. Mekanisme Pengiriman Data
Mekanisme pengiriman data dimulai dari input pengguna melalui elemen form di Flutter, seperti `TextField` untuk nama produk, harga, deskripsi, dan URL gambar. Setelah pengguna mengisi form dan menekan tombol "Save", data tersebut akan dikumpulkan dan dikirim ke server menggunakan `http` atau `CookieRequest`. Server kemudian memproses data tersebut, menyimpannya dalam database, dan mengirimkan respons kembali ke aplikasi. Aplikasi kemudian dapat menampilkan data yang diperoleh dari server, misalnya, dengan memperbarui tampilan menggunakan `setState()`.

## 5. Mekanisme Autentikasi
Mekanisme autentikasi dimulai dengan pengguna memasukkan data akun (username dan password) pada halaman login di Flutter. Data ini kemudian dikirim ke server Django menggunakan permintaan POST. Django memverifikasi kredensial dan mengembalikan respons yang menunjukkan apakah autentikasi berhasil atau tidak. Jika berhasil, Django mengatur cookie sesi yang menyimpan informasi autentikasi. Setelah itu, pengguna diarahkan ke halaman menu utama di Flutter, di mana mereka dapat melihat opsi yang tersedia. Proses logout dilakukan dengan menghapus cookie sesi, yang mengakhiri sesi pengguna.

## 6. Implementasi Checklist Secara Step-by-Step
1. **Membuat Proyek Flutter**: Saya memulai dengan membuat proyek Flutter baru dengan tema E-Commerce.
2. **Membuat Model**: Saya membuat model untuk produk yang akan digunakan untuk pengambilan dan pengiriman data JSON.
3. **Mengimplementasikan Library HTTP**: Saya menambahkan library `http` untuk melakukan permintaan ke server.
4. **Membuat Halaman Login dan Register**: Saya membuat halaman untuk login dan register, termasuk form input untuk username dan password.
5. **Membuat Halaman Menu**: Saya membuat halaman menu yang menampilkan tombol untuk melihat daftar produk, menambah produk, dan logout.
6. **Mengimplementasikan Navigasi**: Saya menggunakan `Navigator` untuk berpindah antar halaman.
7. **Mengelola Status**: Saya menggunakan `setState()` untuk memperbarui tampilan berdasarkan interaksi pengguna.
8. **Mengimplementasikan Autentikasi**: Saya menghubungkan halaman login dan register dengan backend Django untuk autentikasi pengguna.
9. **Menangani Respons**: Saya menangani respons dari server untuk memberikan umpan balik kepada pengguna, seperti berhasil atau gagal dalam proses login dan register.
10. **Pengujian**: Saya melakukan pengujian untuk memastikan semua fitur berfungsi dengan baik dan tidak ada error.

Implementasi ini memastikan bahwa aplikasi tidak hanya berfungsi dengan baik tetapi juga memberikan pengalaman pengguna yang interaktif dan responsif.

