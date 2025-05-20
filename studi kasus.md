# STUDI KASUS 1 
# # Penjelasan Fungsi dan Rekursi pada Faktorial

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
# # Penjelasan penggunaan perulangan dan array (list) 


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

# STUDI KASUS 4
# # Penjelasan Penghitungan Total Harga Barang Menggunakan Python
**1. Mulai (Start)**
**Program dimulai oleh pengguna.**

**2. Input Harga Barang Pertama**
**Program meminta pengguna untuk memasukkan harga barang pertama, lalu menyimpannya dalam variabel harga1.**

**3. Input Harga Barang Kedua**
Program meminta pengguna untuk memasukkan harga barang kedua, lalu menyimpannya dalam variabel harga2.

**4. Input Harga Barang Ketiga**
Program meminta pengguna untuk memasukkan harga barang ketiga, lalu menyimpannya dalam variabel harga3.

**5. Hitung Total Harga**
Program menghitung total dengan menjumlahkan ketiga harga:
total = harga1 + harga2 + harga3

**6. Tampilkan Total Harga**
Program mencetak atau menampilkan hasil total harga kepada pengguna.

**7. Selesai (End)**
Program selesai dijalankan.

# STUDI KASUS 5
# # Penjelasan Program Rata-rata Kelulusan

# Peran Tipe Data dalam Program
**Tipe data menentukan jenis nilai yang dapat disimpan dan dioperasikan dalam program. Dalam konteks program ini:**

**1.Integer (int):**
**Digunakan untuk menyimpan jumlah nilai yang akan dimasukkan oleh pengguna.
Contoh: jumlah_nilai = int(input("Masukkan jumlah nilai: "))**

**2. Float (float):**
Digunakan untuk menyimpan nilai-nilai ujian yang mungkin berupa angka desimal.
Contoh: nilai_input = float(input(f"Masukkan nilai ke-{i+1}: "))

**3. List (list):**
**Digunakan untuk menyimpan kumpulan nilai yang dimasukkan oleh pengguna.
Contoh: nilai = []**

**4. String (str):**
**Digunakan untuk menyimpan dan menampilkan status kelulusan.
Contoh: return "Lulus" if rata_rata >= 75 else "Tidak Lulus"**

**5. Boolean (bool):
Digunakan secara implisit dalam operasi perbandingan untuk menentukan kondisi benar atau salah.
Contoh: rata_rata >= 75 menghasilkan True atau False**

# Peran Operator dalam Program
Operator digunakan untuk melakukan operasi pada variabel dan nilai. Dalam program ini:
MySertifikasi

**1. Operator Aritmatika:**
Penjumlahan (+):
Digunakan untuk menjumlahkan semua nilai dalam list.
Contoh: sum(nilai_list)

Pembagian (/):
Digunakan untuk menghitung rata-rata nilai.
Contoh: sum(nilai_list) / len(nilai_list)

**2. Operator Perbandingan:**

Lebih besar atau sama dengan (>=):
Digunakan untuk menentukan apakah rata-rata memenuhi syarat kelulusan.
Contoh: rata_rata >= 75

**3. Operator Penugasan (=):**
Digunakan untuk memberikan nilai ke variabel.
Contoh: nilai = [], rata_rata = hitung_rata_rata(nilai)

**4. Operator Logika:**
Digunakan secara implisit dalam struktur kontrol seperti if untuk menentukan alur program berdasarkan kondisi.
Contoh:

    if rata_rata >= 75:
    status = "Lulus"
    else:
    status = "Tidak Lulus"

# Kesimpulan

**Dalam program Python untuk menentukan kelulusan siswa berdasarkan rata-rata nilai:**

**-Tipe data memastikan bahwa nilai yang dimasukkan dan diolah sesuai dengan jenisnya, memungkinkan operasi yang tepat dan menghindari kesalahan tipe.**

**-Operator memungkinkan program melakukan perhitungan matematis dan logika untuk menentukan hasil akhir, seperti menghitung rata-rata dan mengevaluasi kondisi kelulusan.**

Pemahaman yang baik tentang tipe data dan operator sangat penting dalam pemrograman, karena mereka adalah dasar dari manipulasi data dan kontrol alur program.**
