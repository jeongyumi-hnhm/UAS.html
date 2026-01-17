# Aplikasi To-Do List Interaktif Sederhana

## Deskripsi Project
Aplikasi ini dibuat untuk membantu mengelola daftar tugas harian dengan fitur dasar seperti menambah, menandai selesai, menghapus tugas, validasi input, dan penghitungan total serta tugas yang selesai. Tampilan dilengkapi latar belakang pemandangan alam untuk memberikan kesan nyaman saat digunakan.


## Alur Logika / Algoritma

### 1. Inisialisasi
- Ambil elemen-elemen penting dari DOM (input, tombol, daftar tugas, counter).
- Buat array kosong untuk menyimpan data tugas.
- Update counter awal (nilai 0 untuk total dan selesai).


### 2. Menambah Tugas
1. Ambil nilai dari input dan bersihkan spasi di awal/akhir.
2. Validasi: jika input kosong, tampilkan pesan peringatan dan hentikan proses.
3. Jika input valid, tambahkan objek tugas baru ke array (dengan properti `name` dan `completed: false`).
4. Kosongkan input dan panggil fungsi untuk merender ulang daftar serta update counter.


### 3. Menampilkan Tugas
1. Kosongkan konten lama pada daftar tugas.
2. Lakukan perulangan pada array tugas:
   - Buat elemen baru untuk setiap tugas.
   - Berikan kelas khusus jika tugas sudah selesai (untuk styling berbeda).
   - Tambahkan event listener pada tombol "selesai" dan "hapus".
   - Sisipkan elemen tugas ke dalam daftar di DOM.


### 4. Menandai Tugas Selesai
- Ketika tombol "selesai" ditekan, ubah nilai properti `completed` pada tugas yang dipilih (dari `false` ke `true` atau sebaliknya).
- Panggil fungsi merender ulang daftar dan update counter.


### 5. Menghapus Tugas
- Ketika tombol "hapus" ditekan, hapus elemen tugas dari array berdasarkan indeksnya.
- Panggil fungsi merender ulang daftar dan update counter.


### 6. Update Counter
- Hitung jumlah total tugas dari panjang array.
- Hitung jumlah tugas selesai dengan menyaring array berdasarkan properti `completed: true`.
- Tampilkan kedua nilai tersebut di elemen counter pada DOM.
