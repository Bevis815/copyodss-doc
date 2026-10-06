# Cara Kerja Copy Trading

Setelah copy diaktifkan, CopyOdds **mencoba** menempatkan order di akun trading Anda sesuai aturan Anda setiap kali trader yang Anda ikuti mendapatkan transaksi.

**Apakah copy berhasil ditentukan oleh Trade history**; Copy activity hanya menampilkan tindakan publik trader.

![Riwayat trade](../.gitbook/assets/change_doc.png)

***

## Alur eksekusi

1. Mendeteksi transaksi publik leader (beli / jual) di Polymarket
2. Mencari aturan copy Anda untuk alamat tersebut dan memeriksa apakah arahnya cocok
3. Menghitung target nilai nominal dari **jumlah tetap** atau **persentase USDC tersedia Anda**
4. Mencoba menempatkan order dalam batas toleransi slippage Anda
5. Saat terisi, memotong **Gas Platform** yang sesuai (sekitar 0.5% dari nilai nominal) dan memperbarui posisi / catatan

***

## Terisi vs. Dilewati vs. Gagal

| Hasil | Arti |
|--------|---------|
| **Filled** | Order copy terisi |
| **Skipped** | Tidak ada order yang ditempatkan karena pengaturan, dana, dll. (umum) |
| **Failed** | Order ditolak atau mengalami error |
| **Settled, dll.** | Status penyelesaian / selesai sebagaimana ditampilkan oleh filter UI |

### Alasan umum dilewati

- Ketidaksesuaian arah (Hanya beli / Hanya jual)
- Jumlah di bawah pembelian minimum sekitar **$1**
- Mencapai **Max open copy buys** (default 1 = tidak menambah posisi)
- Slippage terlalu besar
- **Gas tidak mencukupi** atau **USDC tidak mencukupi**
- Trader menjual tetapi Anda tidak memegang posisi yang sesuai
- Tidak ada pihak lawan di pasar pada saat itu

***

## Apa yang terjadi pada aturan saat dana menipis?

| Situasi | Status aturan | Pembelian | Penjualan (saat Anda memegang posisi) |
|-----------|-------------|------|---------------------------------|
| Gas = 0 | Biasanya masih "berjalan"; peringatan dana mungkin muncul | Dilewati | Mungkin masih di-copy |
| USDC tidak cukup untuk membeli | Sama seperti di atas | Dilewati | Mungkin masih di-copy |
| Dijeda secara manual | Manually paused | Tidak di-copy | Tidak di-copy |

Setelah mengisi Gas / USDC, buka **My copies** dan ketuk **Resume buys** (lanjutkan pembelian) (jika seluruh aturan dijeda secara manual, ketuk Resume sebagai gantinya).

***

## Copy activity vs. Trade history vs. Positions

| Halaman | Isi |
|------|---------|
| Copy activity | Pembelian dan penjualan publik trader |
| Trade history | Upaya copy Anda dan hasilnya |
| Positions | Posisi Anda saat ini; Tutup / tukarkan share yang sudah diselesaikan |
| Daily P&L | Kurva L&R terealisasi per hari trading |

L&R terealisasi hari ini biasanya direset setiap hari pada waktu tertentu di zona waktu akun Anda (misalnya 8:00 AM); lihat deskripsi di dalam aplikasi untuk detailnya.
