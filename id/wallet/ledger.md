# Riwayat Transaksi

**Transaction history** mencatat setiap pergerakan dana masuk dan keluar dari akun Anda, ditambah pengeluaran Gas — anggap saja seperti rekening koran bank.

Titik masuk: **Transaction history** → `/wallets/ledger` (biasanya dapat dibuka dari halaman deposit / penarikan)

***

## Kolom tabel

| Kolom | Arti |
|-------|---------|
| **Network / Asset** | misalnya Polygon (PoS) + USDC, BSC + USDT, Platform + Gas |
| **Type (In / Out)** | Masuk atau keluar |
| **Status** | Received, Completed, Posted |
| **Balance after** | Berapa yang tersisa di akun setelah entri ini |
| **View on-chain** | Membuka transaksi ini di block explorer |

Tiga jenis catatan:

| Jenis | Deskripsi |
|------|-------------|
| **Deposit** | USDC / USDT yang ditransfer masuk dari dompet eksternal |
| **Penarikan** | Dikirim ke alamat milik Anda sendiri |
| **Pengeluaran Gas** | Kredit biaya layanan yang dipotong untuk setiap transaksi copy |

***

## Saat angkanya tidak sesuai

| Gejala | Yang perlu diperiksa |
|---------|---------------|
| Deposit tidak muncul | Apakah jaringannya benar, apakah asetnya USDC/USDT, apakah alamatnya sama persis dengan halaman untuk jaringan tersebut, apakah sudah dikonfirmasi on-chain (BSC lebih lambat)? |
| Penarikan tertahan di "Processing" | Anda perlu menyelesaikan verifikasi tambahan penarikan terlebih dahulu; mungkin ada masa tunggu setelah perangkat baru atau perubahan terkait risiko |
| Gas yang dipotong lebih banyak dari perkiraan | Setiap pembelian dan penjualan dikenakan sekitar 0.5% dari jumlah transaksi; bandingkan dengan contoh di [Gas Platform](gas.md) |
| Saldo tidak sesuai dengan posisi | Posisi dan order terbuka mengikat dana; ikuti angka **Max withdrawable** |

Jika Anda tidak dapat menemukannya, kirimkan kepada dukungan **waktu, jumlah, dan status** dari buku besar beserta hash on-chain-nya.
