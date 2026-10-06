# Jaringan yang Didukung

Deposit dan penarikan mendukung **jaringan yang berbeda**. Selalu pilih persis seperti yang ditampilkan halaman untuk menghindari dana tidak masuk.

***

## Ringkasan

| Tindakan | Jaringan yang didukung | Aset | Jenis alamat |
|--------|--------------------|--------|--------------|
| **Deposit** | **Polygon (PoS)**, **BSC** (jika diaktifkan) | USDC / USDT | Alamat berbeda untuk setiap jaringan |
| **Penarikan** | **Hanya Polygon (PoS)** | **USDC** | Alamat penerima milik Anda sendiri |

Contoh jaringan yang tidak didukung untuk deposit: **Ethereum mainnet, Arbitrum, Optimism**, dll. (kecuali produk secara eksplisit menambahkannya di masa mendatang).

***

## Polygon (PoS)

| Item | Deskripsi |
|------|-------------|
| Deposit | Didukung; alamat yang ditampilkan adalah alamat dompet kustodian Anda (Custodial address) |
| Aset | USDC, USDT |
| Penarikan | **Satu-satunya** jaringan penarikan; tarik USDC ke alamat yang dapat menerima Polygon USDC |

Sebagian besar pengguna lebih memilih Polygon: jalurnya lebih langsung dan sesuai dengan jaringan penarikan.

***

## BSC

| Item | Deskripsi |
|------|-------------|
| Deposit | Didukung (jika bridge / jaringan produk diaktifkan) |
| Aset | USDC, USDT |
| Alamat | **Alamat bridge**, berbeda dari alamat Polygon |
| Penarikan | Penarikan dari CopyOdds ke BSC **tidak didukung** |

Saat menarik dana dari bursa melalui BSC, alihkan halaman deposit ke BSC terlebih dahulu, lalu salin alamatnya. Dana mungkin memerlukan beberapa menit tambahan untuk masuk.

***

## Kesalahan umum

| Kesalahan | Akibat |
|---------|-------------|
| Menarik di BSC tetapi menyalin alamat Polygon | Mungkin tidak dikreditkan / sulit dipulihkan |
| Menarik di Polygon tetapi menyalin alamat BSC | Sama seperti di atas |
| Mengirim USDC Ethereum | Biasanya tidak dikreditkan secara otomatis |
| Memasukkan alamat halaman deposit sebagai alamat penarikan | Dana dapat kembali ke sisi kustodian dan menimbulkan kebingungan; penarikan harus ke alamat eksternal **milik Anda sendiri** |
| Mengharapkan penarikan ke BSC | Saat ini penarikan hanya mendukung Polygon USDC |

***

## Aturan praktis

1. **Pilih jaringan terlebih dahulu, lalu salin alamatnya**
2. **Deposit di Polygon, tarik di Polygon — paling sederhana**
3. **BSC hanya untuk deposit; Anda tidak dapat menarik ke BSC dari App ini**
4. **Hanya gunakan alamat dari halaman resmi + fitur Verify deposit address**
