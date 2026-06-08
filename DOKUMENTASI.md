# Dokumentasi Aplikasi Menu Manajemen

## 📋 Daftar Isi
1. [Pendahuluan](#pendahuluan)
2. [Instalasi dan Setup](#instalasi-dan-setup)
3. [Cara Menggunakan](#cara-menggunakan)
4. [Fitur Aplikasi](#fitur-aplikasi)
5. [Struktur Program](#struktur-program)
6. [Perintah-Perintah](#perintah-perintah)
7. [Contoh Penggunaan](#contoh-penggunaan)
8. [Troubleshooting](#troubleshooting)

---

## 🎯 Pendahuluan

**Aplikasi Menu Manajemen** adalah aplikasi berbasis Java yang dirancang untuk mengelola struktur menu hierarchi. Aplikasi ini memungkinkan pengguna untuk:
- Melihat seluruh struktur menu dan submenu
- Menambah menu dan submenu baru
- Mencari menu tertentu
- Mengurutkan menu secara alfabetis

Aplikasi ini cocok digunakan sebagai sistem manajemen menu untuk sistem akademik, perpustakaan, atau aplikasi manajemen lainnya.

---

## 💻 Instalasi dan Setup

### Prasyarat
- **Java Development Kit (JDK)** versi 8 atau lebih baru
- **Visual Studio Code** (opsional) dengan ekstensi Java
- Command Line/Terminal

### Langkah-Langkah Instalasi

1. **Clone atau Download Repository**
   ```bash
   git clone https://github.com/rizalalfadlil/UAS_Menu.git
   cd UAS_Menu
   ```

2. **Compile Program**
   ```bash
   # Jika menggunakan command line
   javac -d bin src/*.java
   ```

3. **Jalankan Aplikasi**
   ```bash
   java -cp bin App
   ```

---

## 🚀 Cara Menggunakan

### Antarmuka Utama

Ketika aplikasi dijalankan, Anda akan melihat tampilan seperti ini:

```
=== Aplikasi Menu ===
Ketik /h untuk bantuan

=== Struktur Menu ===
1. Mahasiswa
  1A. KRS
  1B. Jadwal
  1C. Nilai
2. Dosen
  2A. Input Nilai
  2B. Presensi
3. Keuangan
  3A. Pembayaran
  3B. Tagihan

Masukkan Perintah: 
```

### Struktur Menu Default

Aplikasi dilengkapi dengan struktur menu awal yang mencakup:

**1. Menu Mahasiswa**
   - KRS (Kartu Rencana Studi)
   - Jadwal (Jadwal Kuliah)
   - Nilai (Nilai Akademik)

**2. Menu Dosen**
   - Input Nilai
   - Presensi (Kehadiran)

**3. Menu Keuangan**
   - Pembayaran
   - Tagihan

---

## 🎨 Fitur Aplikasi

### 1. **Tampilkan Bantuan** (`/h`)
Menampilkan daftar semua perintah yang tersedia dan informasi singkat tentang penggunaan.

### 2. **Keluar dari Program** (`/q`)
Mengakhiri aplikasi dengan aman.

### 3. **Cari Menu** (`/f`)
Mencari menu atau submenu tertentu berdasarkan nama yang diinput. Hasil pencarian akan menunjukkan:
- Apakah menu ditemukan sebagai menu utama atau submenu
- Lokasi menu dalam struktur hierarchi (nomor dan kode)
- Pesan jika menu tidak ditemukan

### 4. **Tambah Menu/Submenu** (`/a`)
Menambahkan menu baru atau submenu ke dalam struktur menu yang ada. Anda dapat:
- Menambah submenu ke menu yang sudah ada
- Membuat menu utama baru

### 5. **Urutkan Menu** (`/s`)
Mengurutkan semua menu utama dan submenu secara alfabetis (A-Z).

---

## 🏗️ Struktur Program

### File Utama

#### **App.java**
File utama yang mengatur alur aplikasi:
- `InitialData()`: Menginisialisasi struktur menu awal
- `home()`: Menampilkan halaman utama aplikasi
- `run(String input)`: Memproses perintah yang diinput pengguna
- `help()`: Menampilkan bantuan
- `main()`: Entry point aplikasi

#### **Functions.java**
File yang berisi fungsi-fungsi utama dan struktur data:

**Kelas MenuNode:**
- Merepresentasikan setiap menu atau submenu
- Menyimpan nama dan daftar children (submenu)

**Kelas Functions:**
Berisi method-method untuk mengelola menu:
- `allMenu(boolean showSubmenu)`: Menampilkan semua menu
- `addMenu()`: Fungsi untuk menambah menu/submenu
- `searchMenu()`: Fungsi untuk mencari menu
- `sortMenu()`: Fungsi untuk mengurutkan menu

---

## 📝 Perintah-Perintah

| Perintah | Deskripsi |
|----------|-----------|
| `/h` | Tampilkan bantuan dan daftar perintah |
| `/q` | Keluar dari program |
| `/f` | Cari menu atau submenu |
| `/a` | Tambah menu atau submenu baru |
| `/s` | Urutkan menu secara alfabetis |

---

## 📖 Contoh Penggunaan

### Contoh 1: Mencari Menu

```
=== Aplikasi Menu ===
Ketik /h untuk bantuan

=== Struktur Menu ===
1. Dosen
  1A. Input Nilai
  1B. Presensi
2. Keuangan
  2A. Pembayaran
  2B. Tagihan
3. Mahasiswa
  3A. Jadwal
  3B. KRS
  3C. Nilai

Masukkan Perintah: /f

Masukkan nama menu yang ingin dicari: Nilai

--- Hasil Pencarian ---
Ditemukan: "Nilai" merupakan Submenu dari "Mahasiswa" (3C)
Ditemukan: "Nilai" merupakan Submenu dari "Dosen" (1A)
```

### Contoh 2: Menambah Submenu Baru

```
Masukkan Perintah: /a

Pilih Menu yang akan ditambahkan submenu:

=== Struktur Menu ===
1. Mahasiswa
2. Dosen
3. Keuangan
0. Tambahkan menu baru

Masukkan Pilihan: 1

Masukkan nama submenu: Beasiswa

=== Aplikasi Menu ===
Ketik /h untuk bantuan

=== Struktur Menu ===
1. Mahasiswa
  1A. KRS
  1B. Jadwal
  1C. Nilai
  1D. Beasiswa
2. Dosen
  2A. Input Nilai
  2B. Presensi
3. Keuangan
  3A. Pembayaran
  3B. Tagihan

Masukkan Perintah:
```

### Contoh 3: Menambah Menu Utama Baru

```
Masukkan Perintah: /a

Pilih Menu yang akan ditambahkan submenu:

=== Struktur Menu ===
1. Mahasiswa
2. Dosen
3. Keuangan
0. Tambahkan menu baru

Masukkan Pilihan: 0

Masukkan nama menu: Perpustakaan

=== Aplikasi Menu ===
Ketik /h untuk bantuan

=== Struktur Menu ===
1. Mahasiswa
  1A. KRS
  1B. Jadwal
  1C. Nilai
2. Dosen
  2A. Input Nilai
  2B. Presensi
3. Keuangan
  3A. Pembayaran
  3B. Tagihan
4. Perpustakaan

Masukkan Perintah:
```

### Contoh 4: Menampilkan Bantuan

```
Masukkan Perintah: /h

=== Bantuan ===
/h - Tampilkan bantuan ini
/q - Keluar dari program
/f - Cari menu/submenu
/a - Tambah menu/submenu
/s - Urutkan menu dan submenu

Tekan Enter untuk kembali...
```

---

## ⚠️ Troubleshooting

### Masalah: "command not found: java"
**Solusi:** 
- Pastikan JDK sudah terinstall di sistem
- Tambahkan path Java ke environment variable
- Periksa di Control Panel > System > Environment Variables

### Masalah: "Perintah tidak valid"
**Solusi:** 
- Ketik `/h` untuk melihat daftar perintah yang valid
- Pastikan Anda memasukkan perintah yang benar (mulai dengan `/`)
- Perintah hanya terdiri dari `/h`, `/q`, `/f`, `/a`, `/s`

### Masalah: Input tidak tersimpan setelah menambah menu
**Solusi:** 
- Data menu hanya tersimpan dalam memori program
- Jika program ditutup, semua perubahan akan hilang
- Untuk menyimpan data permanen, program perlu dimodifikasi untuk menggunakan file atau database

### Masalah: Program terasa lambat
**Solusi:** 
- Jika menu sudah sangat banyak, program mungkin perlu optimisasi
- Pertimbangkan untuk menggunakan struktur data yang lebih efisien

---

## 🔄 Mengembangkan Aplikasi Lebih Lanjut

Beberapa ide pengembangan:

1. **Simpan ke File** - Tambahkan fitur untuk menyimpan dan membaca struktur menu dari file
2. **Database** - Integrasikan dengan database untuk penyimpanan data permanen
3. **GUI** - Buat antarmuka graphical menggunakan Swing atau JavaFX
4. **Validasi Input** - Tambahkan validasi input yang lebih ketat
5. **Undo/Redo** - Tambahkan fitur untuk membatalkan dan mengulangi operasi
6. **Edit Menu** - Tambahkan fitur untuk mengubah nama menu yang sudah ada
7. **Hapus Menu** - Tambahkan fitur untuk menghapus menu atau submenu

---

## 📞 Kontak dan Support

Untuk pertanyaan atau laporan bug, silakan buat issue di repository GitHub:
https://github.com/rizalalfadlil/UAS_Menu/issues

---

**Selamat menggunakan Aplikasi Menu Manajemen! 🎉**
