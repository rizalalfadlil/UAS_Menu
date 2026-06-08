# Dokumentasi Aplikasi Menu Manajemen

## 📋 Daftar Isi
1. [Pendahuluan](#pendahuluan)
2. [Cara Menggunakan](#cara-menggunakan)
3. [Struktur Program](#struktur-program)
4. [Perintah-Perintah](#perintah-perintah)
5. [Contoh Penggunaan](#contoh-penggunaan)

---

## 🎯 Pendahuluan

Aplikasi ini dibuat sebagai projek Ujian Akhir Semester mata kuliah Struktur Data

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

**Selamat menggunakan Aplikasi Menu Manajemen! 🎉**
