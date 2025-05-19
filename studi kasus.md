# STUDI KASUS 1 
# Penjelasan Fungsi dan Rekursi pada Faktorial

## Manfaat Penggunaan Fungsi

- **Modularitas**  
  Memecah program menjadi bagian kecil yang mudah dikelola dan dipahami.
- **Penggunaan Ulang Kode**  
  Fungsi dapat dipanggil berkali-kali tanpa menulis ulang kode.
- **Memudahkan Debugging dan Pemeliharaan**  
  Fokus memperbaiki fungsi tanpa harus meninjau seluruh program.
- **Meningkatkan Readabilitas**  
  Nama fungsi menjelaskan tujuan kode sehingga mudah dimengerti.

## Cara Kerja Rekursi dalam Menghitung Faktorial

1. **Basis Kasus**  
   Jika `n` adalah 0 atau 1, fungsi mengembalikan 1 sebagai nilai faktorial.
2. **Langkah Rekursif**  
   Jika `n > 1`, fungsi memanggil dirinya sendiri dengan `n - 1` dan mengalikan hasilnya dengan `n`.  

# STUDI KASUS 2 
# Penjelasan Struktur Kontrol Percabangan untuk Logika Pemberian Diskon

## Apa itu Struktur Kontrol Percabangan?

Struktur kontrol percabangan adalah mekanisme dalam pemrograman yang memungkinkan program mengambil keputusan berdasarkan kondisi tertentu. Dengan percabangan, program dapat menjalankan perintah berbeda sesuai dengan nilai kondisi yang diperiksa.


## Contoh Penggunaan Percabangan dalam Logika Pemberian Diskon

Misalnya, kita ingin memberikan diskon kepada pelanggan yang melakukan pembelian di atas jumlah tertentu. Logika sederhananya adalah:

- Jika total belanja lebih dari 100.000, maka pelanggan mendapatkan diskon 5% dan voucher.
- Jika tidak, maka tidak ada diskon atau voucher diberikan.

Struktur percabangan `if` dan `else` sangat cocok untuk kasus ini.

---

## Penjelasan Struktur Percabangan pada Contoh Kode Faktorial dan Nilai Tertinggi

Meskipun kode berikut tidak langsung memberikan diskon, prinsip percabangan dapat diterapkan untuk logika pemberian diskon. Berikut penjelasan singkat kode contoh:


---

## Cara Kerja Struktur Percabangan dalam Logika Diskon

- **If**: Mengecek apakah kondisi tertentu terpenuhi (misal, nilai tertinggi >= 90). Jika benar, jalankan blok kode diskon 10%.
- **Elif**: Jika kondisi pertama salah, cek kondisi berikutnya (nilai >= 75). Jika benar, jalankan diskon 5%.
- **Else**: Jika semua kondisi sebelumnya salah, jalankan blok kode alternatif (tidak ada diskon).

---

## Kesimpulan

Struktur kontrol percabangan memungkinkan program untuk membuat keputusan berdasarkan kondisi tertentu, seperti memberikan diskon jika syarat terpenuhi. Dengan menggunakan `if`, `elif`, dan `else`, kita dapat mengatur berbagai skenario pemberian diskon sesuai kebutuhan logika bisnis.



#  STUDI KASUS 3 
# # Penjelasan Struktur Kontrol Percabangan pada Logika Pemberian Diskon

## Deskripsi Singkat

Kode berikut menunjukkan bagaimana **struktur kontrol percabangan** (`if` dan `else`) digunakan untuk menentukan apakah pelanggan berhak mendapatkan diskon berdasarkan total belanja mereka.

---

## Kode Program

---

## Penjelasan Struktur Kontrol Percabangan

### 1. Fungsi `total_bayar`

- **Percabangan `if`**  
  Mengecek apakah `total_belanja` lebih besar dari `batas_diskon`.  
  - Jika **benar** (`total_belanja > batas_diskon`), maka program:  
    - Menghitung diskon dengan memanggil fungsi `hitung_diskon`.  
    - Mengurangi `total_belanja` dengan nilai diskon.  
    - Mengembalikan nilai total yang sudah dikurangi diskon dan nilai diskon itu sendiri.  
  - Jika **salah**, program mengembalikan nilai `total_belanja` tanpa perubahan dan diskon 0.

### 2. Percabangan di Main Program

- Setelah mendapatkan nilai `diskon` dan `total` dari fungsi `total_bayar`, program menggunakan percabangan:  
  - Jika `diskon > 0`, artinya pelanggan mendapatkan diskon, maka program menampilkan pesan pemberitahuan besaran diskon.  
  - Jika tidak, program menampilkan pesan bahwa pelanggan tidak mendapatkan diskon.

### 3. Penanganan Error

- Blok `try-except` digunakan untuk menangani kesalahan input, misalnya jika pengguna memasukkan nilai yang bukan angka, maka program akan menampilkan pesan error yang sesuai.

---

## Kesimpulan

Struktur kontrol percabangan `if-else` sangat penting dalam logika pemberian diskon karena:

- Memungkinkan program **memutuskan** apakah pelanggan berhak mendapatkan diskon berdasarkan kondisi tertentu (total belanja melebihi batas).
- Mengatur alur program agar memberikan respons yang sesuai (menampilkan besaran diskon atau tidak).
- Membuat program lebih dinamis dan interaktif sesuai dengan input pengguna.

---

## Contoh Output

