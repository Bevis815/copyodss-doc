# Pengaturan Copy

Arti setiap parameter di wizard copy. Untuk kolom yang tidak ditampilkan di wizard (seperti beberapa batas harian atau penundaan), ikuti antarmuka App saat ini; batasan lanjutan dari dokumentasi lama mungkin sudah digabungkan.

***

## Pengaturan dasar

| Pengaturan | Deskripsi |
|---------|-------------|
| **Leader address** | Alamat dompet yang akan di-copy; harus benar |
| **Name** | Nama tampilan untuk aturan, opsional |
| **Copy mode** | Pilih satu: **Ratio** (default) / **By balance %** / **Fixed amount** |
| **Copy ratio** | Hanya mode Ratio: transaksi leader × rasio = jumlah order Anda |
| **Slippage tolerance** | Deviasi yang dapat diterima dari harga transaksi trader; default **15%**, dapat disesuaikan dari 1% hingga 100% |

### Cara memahami slippage

Slippage diatur **terlalu ketat**: lebih mungkin dilewati atau gagal saat harga bergerak.  
Slippage diatur **terlalu longgar**: lebih mungkin terisi, tetapi mungkin dengan harga yang lebih buruk.  
Default 15% dimaksudkan untuk meningkatkan tingkat keterisian; sesuaikan dengan selera risiko Anda sendiri. Mode Ratio juga memiliki dua parameter tambahan, "Leader order size range" dan "Copy ratio" — lihat [Tiga Mode Copy](copy-modes.md).

***

## Parameter mode Ratio

| Pengaturan | Deskripsi |
|---------|-------------|
| **Copy ratio** | 0.1%–100%; halaman menampilkan nilai yang disarankan dengan "sekitar N trade/hari" |
| **Leader order size range** | Diturunkan dari transaksi historis terbesar leader; di bawah batas bawah dilewati, di atas batas atas dihitung sebagai "batas atas × rasio" |

Untuk penjelasan lengkap dan contoh, lihat [Tiga Mode Copy](copy-modes.md).

***

## Pengaturan lanjutan

| Pengaturan | Deskripsi |
|---------|-------------|
| **Direction · Both sides** | Meng-copy pembelian dan penjualan |
| **Direction · Buy only** | Hanya meng-copy pembelian |
| **Direction · Sell only** | Hanya meng-copy penjualan |
| **Max open copy buys** | Jumlah maksimum pembelian copy bersamaan dalam aturan yang sama; **default 1 = tidak menambah posisi**; nilai maksimum ditampilkan sebagai **All = tanpa batas** |

### Mengapa defaultnya tidak menambah posisi?

Posisi di satu pasar prediksi dapat menumpuk dengan cepat. Default 1 membantu membatasi risiko satu pasar; naikkan setelah Anda memastikan strateginya cocok untuk Anda.

***

## Perilaku default platform (perlu diketahui)

- **Penundaan copy**: saat ini produk biasanya langsung mencoba (tanpa penundaan buatan tambahan)
- **Jeda setelah kegagalan berturut-turut**: platform dapat menjeda pembelian sebentar setelah kegagalan berulang (ambang batas pastinya dapat bervariasi); setelah memperbaiki masalah, Anda dapat melanjutkan di **My copies**

***

## "Batasan lunak" terkait dana

Ini belum tentu merupakan pengaturan, tetapi berfungsi seperti batasan:

| Situasi | Dampak |
|-----------|--------|
| Gas = 0 | Pembelian dilewati; beli Gas dan ketuk **Resume buys** (lanjutkan pembelian) |
| USDC tidak mencukupi | Pembelian dilewati; deposit lebih banyak atau turunkan jumlah / persentase |
| Di bawah sekitar $1 | Pembelian mungkin tidak memenuhi nilai nominal minimum bursa |

***

## Mengubah pengaturan

1. Buka **My copies**
2. Temukan aturannya → **Edit**
3. Setelah disimpan, hanya transaksi di masa mendatang yang terpengaruh

Jika Simulasi diaktifkan di lingkungan Anda, mungkin akan menampilkan lebih banyak parameter jenis batasan; untuk copy sungguhan, kolom-kolom di wizard-lah yang berlaku.

***

## Kolom di halaman Quick copy

Selain memulai copy dari profil trader, Anda juga dapat menempelkan alamat secara langsung di halaman **Quick copy** (`/copier`):

| Kolom | Deskripsi |
|-------|-------------|
| **Copy ratio** | Mengikuti sebagai persentase dari saldo tersedia Anda; 100% menggunakan seluruh saldo, 5% adalah posisi ringan |
| **Per-trade cap (USDC)** | Jumlah maksimum yang akan Anda masukkan ke satu trade |
| **Total cap (USDC)** | Jumlah maksimum yang akan Anda masukkan ke semua copy secara keseluruhan |
| **Auto-copy toggle** | Saat aktif, sistem menggunakan dompet kustodian Anda untuk meng-copy order pengguna ini secara otomatis |

Mengatur alamat yang sama lagi akan **menimpa** aturan sebelumnya; setelah melakukan perubahan, periksa sekali di **My copies**.
