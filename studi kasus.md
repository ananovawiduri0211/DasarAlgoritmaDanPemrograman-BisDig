# STUDI KASUS 1 
 # Penjelasan Fungsi dan Rekursi pada Faktorial

## Manfaat Penggunaan Fungsi

- **Modularitas**  
  Fungsinya adalah memisahkan logika penghitungan dari bagian input/output, sehingga kode lebih mudah dibaca dan diperbaiki.
- **Penggunaan Ulang Kode**  
  Kode dapat dipanggil berkali-kali dengan input yang berbeda tanpa harus menulis ulang logika perhitungan.
- **Memudahkan Debugging dan Pemeliharaan**  
  Fokus memperbaiki fungsi tanpa harus meninjau seluruh program.
- **Meningkatkan Readabilitas**  
  Nama fungsi menjelaskan tujuan kode sehingga mudah dimengerti.


## Cara Kerja Rekursi dalam Menghitung Faktorial
**Rekursi adalah teknik pemanggilan fungsi dari dalam fungsi itu sendiri. Pada kode faktorial(n), fungsi akan terus memanggil dirinya sendiri dengan nilai n - 1, sampai mencapai basis kasus yaitu n == 0 atau n == 1. Saat itulah pemanggilan berhenti dan hasilnya dihitung mundur.**
1. **Basis Kasus**  
   Jika `n` adalah 0 atau 1, fungsi mengembalikan 1 sebagai nilai faktorial.
2. **Langkah Rekursif**  
   Jika `n > 1`, fungsi memanggil dirinya sendiri dengan `n - 1` dan mengalikan hasilnya dengan `n`.  


**Contoh:
Jika n = 4, maka prosesnya seperti ini:**

    faktorial(4)
    =4 * faktorial(3)
    = 4 * 3 * faktorial(2)
    = 4 * 3 * 2 * faktorial(1)
    = 4 * 3 * 2 * 1
    = 24



# STUDI KASUS 2 
# Penjelasan penggunaan perulangan dan array (list) 


#  1. Perulangan

    for i in range(jumlah_siswa):
    nilai_siswa = float(input(f"Masukkan nilai siswa ke-{i + 1}: "))
    nilai.append(nilai_siswa)

**Perulangan ini berfungsi untuk mengulangi proses input sebanyak jumlah siswa yang dimasukkan sebelumnya.
Setiap iterasi akan meminta pengguna untuk memasukkan satu nilai, dan menyimpannya ke dalam list.
Dengan perulangan, program menjadi lebih efisien dan tidak perlu menulis kode input secara manual lima kali.**

# 2. Array (List)
**Di bagian ini, list nilai [] digunakan untuk menyimpan seluruh nilai siswa.
List memungkinkan kita menyimpan banyak data dalam satu variabel, dan memprosesnya dengan mudah — seperti mencari nilai tertinggi, rata-rata, dsb.
Saat setiap siswa menginput nilai, nilainya akan ditambahkan ke list nilai menggunakan:**

    nilai.append(nilai_siswa)

# 3. Mencari Nilai Tertinggi
    tertinggi = max(nilai)
    indeks = nilai.index(tertinggi) + 1

**Fungsi max(nilai) mencari nilai tertinggi dalam list.
nilai.index(tertinggi) mengembalikan posisi (indeks) nilai tersebut dalam list (dimulai dari 0).
Dan setelahnya tambahkan +1 agar siswa ditampilkan sebagai urutan ke-1, ke-2, dst., bukan indeks 0.**

# 4. Output Program
    Masukkan jumlah siswa: 5
    Masukkan nilai siswa ke-1: 99
    Masukkan nilai siswa ke-2: 98
    Masukkan nilai siswa ke-3: 97
    Masukkan nilai siswa ke-4: 96
    Masukkan nilai siswa ke-5: 95

  **Maka Hasil yang diperoleh sebagi berikut:**
  
    Nilai tertinggi adalah 99.0 dan siswa ke-1 mendapatkannya.
# 5. Kesimpulan 

**Konsep	Fungsi di Program**

**/Perulangan guna	Mengotomatisasi input nilai 5 siswa tanpa menulis berulang.
Array/List berguna untuk	Menyimpan semua nilai siswa dalam satu tempat.
Dan Max()	Mengambil nilai tertinggi dari semua nilai yang dikumpulkan.**



#  STUDI KASUS 3 
# # Penjelasan Struktur Kontrol Percabangan pada Logika Pemberian Diskon

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
# Contoh Output Program 
**Input:**

    Masukkan total belanja: 700000

Logika:

    Total belanja: Rp700.000
    Batas diskon: Rp500.000
    Karena 700000 > 500000, maka pelanggan berhak mendapatkan diskon
    Diskon = 10% dari 700000 = 70000
    Total bayar setelah diskon = 700000 - 70000 = 630000
**Output:**

    Anda mendapatkan diskon sebesar 70000.00.
    Total bayar setelah diskon adalah: 630000.00



