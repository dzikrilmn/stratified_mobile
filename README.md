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

