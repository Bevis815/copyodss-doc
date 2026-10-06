# Simulasi Copy Trading

**Simulasi copy trading** menjalankan strategi copy Anda dengan "dompet virtual" — **tanpa melibatkan uang sungguhan**, murni untuk menguji parameter dan melihat hasilnya. Ini ideal untuk pemula yang belum siap menggunakan uang sungguhan.

Titik masuk: **Simulation copy trading** → `/copy-trading/simulation`

> Simulasi copy trading sedang diluncurkan secara bertahap. Jika Anda tidak melihat menu ini, berarti fitur ini belum diaktifkan untuk Anda.

***

## Perbedaannya dengan copy sungguhan

| | Simulasi | Copy sungguhan |
|--|------------|--------------|
| Uang | Saldo virtual | USDC kustodian Anda |
| Gas | Tidak diperlukan | Diperlukan (biaya layanan sekitar 0.5% per trade) |
| Bisakah Anda kehilangan uang? | Tidak secara nyata | Ya |
| Tujuan | Menguji parameter, melihat kinerja jangka panjang | Imbal hasil nyata |

***

## Mulai dalam tiga langkah

### 1. Buat akun virtual

Ketuk **Create virtual account** (buat akun virtual) dan isi:

| Kolom | Deskripsi |
|-------|-------------|
| Nama akun | Sesuatu untuk membedakannya, misalnya "Test-A" |
| Saldo awal | Modal simulasi |
| Durasi (hari) | Setelah kedaluwarsa, tidak ada posisi baru yang dibuka; posisi yang ada masih dapat ditutup atau diselesaikan |

### 2. Tambahkan alamat untuk di-copy

Tambahkan alamat trader di bawah **Copy addresses**; Anda dapat memberi nama strategi dan menambahkan catatan.

### 3. Konfigurasikan strategi

| Pengaturan | Deskripsi |
|---------|-------------|
| Metode copy | Ratio / Fixed amount |
| Arah | Beli dan jual / Hanya beli / Hanya jual |
| Min / Maks per trade | Rentang jumlah untuk setiap trade |
| Batas per pasar | Jumlah maksimum yang dimasukkan ke satu pasar |
| Batas harian | Jumlah maksimum yang dimasukkan per hari |
| Slippage maksimum | Tidak terisi jika terlampaui |
| Penundaan eksekusi | Menyimulasikan "bereaksi sedikit lebih lambat" |
| Cooldown pasar | Interval minimum antara dua copy di pasar yang sama |
| Jeda setelah kegagalan berturut-turut | Menjeda setelah sejumlah kegagalan berturut-turut ini (default 10) |

Ketuk **Start simulation copy** (mulai simulasi copy) untuk menjalankannya.

***

## Melihat hasil: lima tab

| Tab | Isi |
|-----|---------|
| **Copy addresses** | Alamat yang Anda tambahkan, pengaturan strategi, dan status |
| **Positions** | Posisi simulasi; Anda dapat menyimulasikan penutupannya secara manual |
| **Executions** | Jumlah share, biaya, dan status untuk setiap transaksi simulasi |
| **Performance** | Kurva ekuitas, total L&R, win rate, drawdown maksimum, biaya slippage, biaya fee, dll. |
| **Ledger** | Detail setiap pergerakan dana |

### Status

| Status akun | Arti |
|----------------|---------|
| Active | Berjalan normal |
| Paused | Anda menjedanya; dapat dilanjutkan |
| Expired | Tidak ada posisi baru; ekuitas yang ada masih dapat dikelola |
| Archived | Disimpan; tidak dapat diarsipkan selama masih memegang posisi |

### Catatan tentang menutup posisi

Menutup secara manual memerlukan **harga pasar dari 15 menit terakhir** untuk mendapatkan kuotasi; jika harga sudah usang atau tidak ada, Anda akan diminta untuk memperbarui kuotasi. Sebelum mengonfirmasi, Anda akan melihat perkiraan harga transaksi, slippage, biaya, perkiraan hasil, dan perkiraan L&R.

***

## Dalam satu kalimat

Nilai sebenarnya dari simulasi copy trading adalah: **sebelum mengeluarkan uang sungguhan, Anda dapat melihat ke mana sebenarnya "copy yang sering + slippage tinggi + modal kecil" akan membawa Anda.**
