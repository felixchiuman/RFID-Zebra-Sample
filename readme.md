# Aplikasi Pemindai RFID

Aplikasi Android ini menggunakan Zebra RFID SDK untuk terhubung ke pembaca RFID Zebra dan membaca tag RFID. Aplikasi ini menampilkan komponen-komponen kunci dan fungsionalitas utama untuk operasi RFID.

## Komponen Kunci

### 1. MainActivity
- Aktivitas utama yang menangani elemen antarmuka pengguna.
- Terhubung dan memutuskan koneksi dari pembaca RFID.
- Mengelola operasi inventaris.

### 2. RFIDHandler
- Mengelola koneksi ke pembaca RFID.
- Menangani peristiwa seperti pembacaan tag dan pembaruan status.

### 3. EventHandler
- Mengimplementasikan antarmuka `RfidEventsListener`.
- Menerima pemberitahuan peristiwa dari pembaca RFID.

## Fungsionalitas Utama

### 1. Terhubung ke Pembaca RFID
- Menginisialisasi Zebra RFID SDK dan mencari pembaca RFID yang tersedia.
- Terhubung ke pembaca dan mengonfigurasikannya untuk operasi inventaris.
- Menampilkan status koneksi saat ini di antarmuka pengguna.

### 2. Melakukan Inventaris
- Memulai dan menghentikan operasi inventaris melalui tombol.
- Mengirim perintah ke pembaca untuk mulai membaca tag.
- Memproses peristiwa data tag ketika pembaca menemukan tag.

### 3. Menangani Data Tag
- Memproses peristiwa data tag dan menampilkan ID tag di antarmuka pengguna.

### 4. Menangani Pencetan Pemicu
- Menerima pemberitahuan saat tombol pemicu di pembaca ditekan atau dilepaskan.
- Memulai atau menghentikan inventaris berdasarkan peristiwa pencetan pemicu.

## Fitur Tambahan

- Memungkinkan pengguna untuk mengubah konfigurasi pembaca (misalnya, tingkat daya, sesi).
- Menyediakan opsi untuk menghapus data tag yang ditampilkan di antarmuka pengguna.

## Detail Kode

- Variabel `readers`: Mengakses instansi pembaca RFID.
- Variabel `reader`: Mengakses pembaca RFID yang terhubung.
- Variabel `eventHandler`: Menangani peristiwa dari pembaca RFID.
- Metode `handleTagData`: Dipanggil saat menerima peristiwa data tag.
- Metode `handleTriggerPress`: Dipanggil saat menerima peristiwa pencetan pemicu.
- Variabel `MAX_POWER`: Menyimpan tingkat daya maksimum yang didukung oleh pembaca.
- Variabel `readerName`: Menyimpan nama pembaca yang akan dihubungkan.

## Catatan

Kode ini hanya sebagai contoh dasar dan mungkin perlu dimodifikasi berdasarkan persyaratan aplikasi spesifik Anda. Pastikan untuk menyesuaikannya sesuai kebutuhan proyek Anda.

Silakan jelajahi dan perluas kode ini untuk meningkatkan fungsionalitas aplikasi pembaca RFID Anda.
