# Deposit

Depositkan USDC / USDT ke **akun trading** CopyOdds Anda untuk digunakan sebagai modal copy. Titik masuk: **Wallets → Deposit** → `/wallets/deposit`.

![Halaman deposit](../.gitbook/assets/usdc1_doc.png)

***

## Deposit dalam empat langkah

1. **Pilih jaringan** — Polygon (PoS) atau BSC, sesuai dengan jaringan yang Anda gunakan untuk menarik dana dari bursa Anda  
2. **Pilih aset** — hanya **USDC** atau **USDT**  
3. **Kirim** — Salin atau pindai **alamat yang ditampilkan di halaman ini**  
4. **Tunggu** — Saldo Anda diperbarui setelah konfirmasi on-chain; BSC mungkin memerlukan beberapa menit tambahan

Halaman ini juga memiliki bagian **Deposit steps** dengan empat langkah yang sama, ditambah tautan video **Watch tutorial** (`/guide-video`). Kami menyarankan untuk menontonnya sebelum deposit pertama Anda.

### Tiga tips praktis

| Tindakan | Deskripsi |
|--------|-------------|
| **Simpan kode QR** | Ketuk **Save image** (simpan gambar) untuk menyimpan kode QR alamat di ponsel Anda; memindai lebih kecil kemungkinan salahnya dibanding mengetik |
| **Salin setelah memilih jaringan** | Setelah beralih ke BSC Anda **harus menyalin alamat lagi** — kedua rantai menggunakan alamat yang berbeda |
| **Hanya gunakan alamat yang saat ini ditampilkan di halaman ini** | Jangan gunakan alamat lama dari riwayat obrolan atau yang dikirim oleh orang lain |

***

## Aturan penting

| Aturan | Deskripsi |
|------|-------------|
| Jaringan yang didukung | **Polygon (PoS)** (disarankan) dan **BSC**; halaman menampilkan tag seperti "Recommended / Fast / Low fees" |
| Alamat bergantung pada jaringan | Alamat kustodian Polygon dan alamat bridge BSC **berbeda** — jangan pernah tertukar |
| Hanya USDC / USDT | Token lain biasanya tidak dapat dikreditkan |
| Jangan gunakan rantai yang salah | Jangan gunakan jaringan yang tidak didukung seperti Ethereum / Arbitrum |
| Verifikasi alamat | Ketuk **Verify deposit address**, dan sistem akan mengirimkan alamat kepada Anda melalui **bot Telegram resmi** atau **email yang tertaut** untuk diperiksa |
| Utamakan USDC | USDT di Polygon sering ditampilkan sebagai "USDT (PoS)"; jangan depositkan BNB atau token lainnya |

### Cara menggunakan Verify deposit address

1. Ketuk **Verify deposit address** (verifikasi alamat deposit)
2. Halaman akan meminta Anda untuk memulai bot Telegram resmi (`@botname`) atau memeriksa email yang tertaut
3. Saat Anda menerima alamatnya, **periksa karakter demi karakter** dengan yang ada di halaman
4. Hanya lanjutkan jika sama persis

### Saldo Anda memiliki dua angka

| Istilah | Arti |
|------|---------|
| **Saldo on-chain** | USDC native yang benar-benar sudah masuk di blockchain |
| **Saldo yang dapat ditradingkan** | Bagian yang telah diproses platform dan dapat digunakan untuk copy |

Jika, tepat setelah deposit, Anda melihat "xx native USDC on-chain, automatically converting to tradable balance" (xx USDC native on-chain, sedang dikonversi otomatis menjadi saldo yang dapat ditradingkan), itu adalah alur normal — tunggu beberapa menit lalu muat ulang.

***

## Detail

1. Masuk dan pastikan akun trading Anda aktif
2. Di halaman deposit, pilih jaringan terlebih dahulu, lalu salin alamatnya
3. Saat menarik dana dari bursa atau dompet Anda: periksa dengan cermat jaringan, token, dan jumlahnya
4. Kembali ke CopyOdds dan tarik untuk memuat ulang saldo Anda jika perlu
5. Sebelum deposit besar pertama Anda: depositkan jumlah kecil → pastikan sudah masuk → lalu depositkan lebih banyak

***

## Deposit lambat atau tidak masuk?

Periksa dengan urutan berikut:

1. Apakah jaringan penarikan sesuai dengan yang dipilih di halaman ini (Polygon vs. BSC)?
2. Apakah tokennya USDC / USDT?
3. Apakah alamat penerima **sama persis** dengan yang ada di halaman ini?
4. Apakah transaksi on-chain sudah dikonfirmasi? (Cari hash-nya di block explorer yang sesuai)
5. Apakah Anda secara tidak sengaja mengirimkannya ke tujuan penarikan atau alamat platform lain?

Masih tidak masuk: hubungi dukungan dengan menyertakan **hash transaksi, jaringan, jumlah, waktu, dan email terdaftar**.

***

## Apa selanjutnya setelah deposit?

- Untuk mulai meng-copy: pertama pastikan **Polymarket sudah siap**, lalu **beli Gas Platform** (lihat [Gas Platform](gas.md))
- Pembelian copy memerlukan USDC yang tersedia (disarankan minimal sekitar $1)

***

## Tempat memeriksa setelah dana masuk

Buka **Transaction history** → `/wallets/ledger` untuk melihat jaringan, aset, status, dan saldo setelah transaksi deposit. Lihat [Riwayat Transaksi](ledger.md).
