#  Pengujian dan Evaluasi Performa
**Aplikasi Pemesanan Kopi & Bakery (Dijalankan di Google Colab)**

---

##  Tujuan Pengujian
Pengujian dilakukan untuk memastikan bahwa aplikasi dapat:
- Menampilkan menu dengan benar
- Menerima input berulang dari user (multi-order)
- Menangani kesalahan input
- Memberikan hasil ringkasan dan total yang sesuai

---

##  Metode Pengujian
- Aplikasi dijalankan pada Google Colab melalui link resmi.
- User menginput langsung dari kolom input (di dalam cell).
- Interaksi dilakukan step-by-step sesuai urutan eksekusi kode.

---

##  Tabel Skenario Pengujian

| No | Skenario                        | Input                            | Output yang Diharapkan                       | Status |
|----|----------------------------------|----------------------------------|----------------------------------------------|--------|
| 1  | Pemesanan 2 menu valid          | 2, jumlah: 2; 5, jumlah: 1       | Ringkasan + total Rp60.000                   | ✅     |
| 2  | Kode menu salah                 | 8                                | Pesan error: `Kode menu tidak valid`         | ✅     |
| 3  | Jumlah bukan angka              | Masukkan "dua"                   | Pesan error: `Jumlah harus berupa angka`     | ✅     |
| 4  | Ketik `selesai` langsung        | selesai                          | Ringkasan kosong dan total Rp0               | ✅     |
| 5  | Pesan 3 menu                    | 1,2; 3,1; 6,2                    | Ringkasan & total sesuai jumlah & harga      | ✅     |

---

##  Contoh Output di Google Colab (Asli)

Masukkan nomor menu: 2
Masukkan jumlah Cappuccino: 2

Masukkan nomor menu: 5
Masukkan jumlah Cinnamon Roll: 1

Masukkan nomor menu: selesai

=== Ringkasan Pesanan Anda ===
2x Cappuccino = Rp40000
1x Cinnamon Roll = Rp20000

Total yang harus dibayar: Rp60000

---

##  Evaluasi Performa

| Aspek              | Hasil                                                                 |
|--------------------|-----------------------------------------------------------------------|
| **Akurasi Proses** | Program menghitung total dengan benar dan menampilkan detail jelas   |
| **Error Handling** | Error seperti kode salah & input bukan angka sudah ditangani         |
| **Responsif**      | Respons cepat di Colab, tanpa lag                                     |
| **Kesesuaian UI**  | Sudah cukup friendly meski berbasis teks                             |
| **Kekurangan**     | Tidak menyimpan struk transaksi / riwayat pesanan                    |
| **Rekomendasi**    | Tambah fitur simpan ke file `.txt` atau `.csv` untuk laporan kasir   |

---

##  Kesimpulan

Aplikasi berhasil diuji melalui Google Colab tanpa kendala teknis. Semua fitur utama berjalan dengan baik dan sesuai kebutuhan tugas. Cocok digunakan untuk simulasi kasir kecil berbasis Python.
