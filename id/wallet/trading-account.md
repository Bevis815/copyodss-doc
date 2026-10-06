# Akun Trading & Status Halaman Dompet

**Akun trading** CopyOdds Anda **biasanya dibuka secara otomatis setelah masuk** — tidak perlu pengajuan terpisah. Ini adalah **dompet trading kustodian** Anda: USDC / USDT yang Anda depositkan disimpan di sini dan digunakan untuk copy trading.

Titik masuk: **Wallets** → `/wallets` (item menu **Deposit** membuka halaman ini)

***

## Yang biasanya akan Anda lihat

| Bagian | Isi |
|---------|---------|
| Alamat deposit on-chain | Alamat deposit Anda (**berbeda untuk setiap jaringan**); salin atau simpan kode QR-nya |
| Saldo tersedia | Bagian yang dapat langsung Anda gunakan untuk copy |
| Saldo on-chain | USDC native yang benar-benar sudah masuk di blockchain |
| Gas Platform | Digunakan untuk membayar biaya layanan copy trading |
| Penarikan | Masukkan alamat penerima Polygon dan jumlah |
| Riwayat transaksi | Deposit, penarikan, dan pengeluaran Gas |

Jika Anda melihat semua ini, semuanya berfungsi dan Anda dapat langsung melakukan deposit.

***

## Mengapa kedua saldo berbeda

| Istilah | Arti |
|------|---------|
| **Saldo on-chain** | USDC native yang benar-benar sudah masuk di blockchain |
| **Saldo yang dapat ditradingkan** | Bagian yang telah diproses platform dan dapat digunakan untuk copy |

Jika, tepat setelah deposit, Anda melihat "xx native USDC on-chain, automatically converting to tradable balance" (xx USDC native on-chain, sedang dikonversi otomatis menjadi saldo yang dapat ditradingkan), itu adalah **alur normal** — tunggu beberapa menit lalu muat ulang.

***

## Status yang mungkin sesekali Anda lihat

Tidak semua orang akan melihat ini; jika Anda melihatnya, tangani seperti yang dijelaskan di bawah ini.

### "CopyOdds trading account not yet opened"

Dalam kasus langka, akun tidak dibuka secara otomatis (misalnya terjadi kesalahan saat penyiapan). Ketuk **Open trading account** (buka akun trading), baca dan centang perjanjiannya, lalu konfirmasi.

Ringkasan perjanjian:

| Klausul | Isi |
|--------|---------|
| Layanan | Platform membuatkan dompet trading kustodian untuk Anda, digunakan untuk deposit, copy, order, dan penarikan |
| Kustodian & otorisasi | Aset dipegang oleh platform dan Anda tidak memegang private key secara langsung; Anda mengizinkan platform untuk melakukan penandatanganan dan eksekusi trade yang diperlukan |
| Perlindungan penarikan | Anda mungkin diwajibkan mengaktifkan verifikasi tambahan **Authenticator (TOTP)** sebelum melakukan penarikan |
| Dana & jaringan | Hanya kirim aset yang didukung ke alamat dan jaringan yang ditampilkan di halaman; **memilih jaringan atau aset yang salah dapat membuat dana tidak dapat dipulihkan** |
| Pemberitahuan risiko | Copy trading **berisiko tinggi dan Anda dapat kehilangan seluruh investasi Anda**; slippage, likuiditas, dan penundaan semuanya memengaruhi hasil |
| Kelayakan & kepatuhan | Anda harus berusia minimal 18 tahun; tidak boleh digunakan untuk pencucian uang, penipuan, atau tujuan ilegal lainnya |

> Perjanjian dapat diperbarui; ketentuan lengkap ada di dialog dalam aplikasi dan Ketentuan Layanan Pengguna.

### Muncul bagian "Agent authorization"

Beberapa akun melihat bagian tambahan **Agent authorization** (otorisasi agen) di halaman dompet. Bagian ini memungkinkan Anda **memberikan otorisasi dengan satu tanda tangan**, setelah itu platform menempatkan order untuk Anda dan **menanggung gas on-chain** (Anda tidak memerlukan MATIC sendiri).

Jika Anda melihat bagian ini, cukup ikuti petunjuknya:

| Persyaratan | Deskripsi |
|-------------|-------------|
| Tanda tangani dengan **dompet yang Anda gunakan saat mendaftar** | Memilih akun yang salah di dompet Anda akan menampilkan "Current wallet is not the registered wallet" |
| Alihkan dompet Anda ke **Polygon (chain ID 137)** | Jika tidak, Anda akan melihat "Please switch your wallet to Polygon and try again" |
| Selesaikan tanda tangan dalam satu kali proses | Menutup ekstensi atau mengubah isi di tengah jalan menyebabkan kegagalan; muat ulang dan mulai lagi |
| Perhatikan masa berlakunya | Setelah kedaluwarsa, copy dijeda — ketuk **Renew** (perpanjang); Anda juga dapat **Revoke** (cabut) (Anda perlu memberikan otorisasi ulang setelah mencabut) |

Error umum: dompet salah / rantai salah / permintaan otorisasi kedaluwarsa / isi yang ditandatangani tidak sesuai dengan verifikasi (biasanya karena gangguan ekstensi — muat ulang dan coba lagi).

### "Polymarket trading authorization incomplete"

Ketuk **Re-authorize Polymarket**. Pesan ini menunjukkan adanya masalah pada langkah otorisasi dan **tidak memengaruhi dana yang sudah Anda depositkan**.

> Dalam kasus langka di mana otorisasi otomatis gagal, halaman menyediakan opsi "Manually paste Polymarket API credentials (advanced)" untuk pemecahan masalah. Pengguna biasa tidak perlu menyentuhnya.

***

## FAQ

**Apakah ada biaya untuk akun trading?**  
Pembukaannya gratis. Gas Platform sekitar 0.5% hanya dipotong saat trade copy terisi.

**Di mana private key saya?**  
Tidak ada pada Anda. CopyOdds menggunakan dompet kustodian dengan private key yang disimpan secara terisolasi oleh platform; Anda mengendalikan dana Anda melalui login + verifikasi tambahan untuk penarikan.

**Mengapa saya dapat melihat alamat on-chain tetapi tidak dapat memindahkan dana keluar sendiri?**  
Itulah desain kustodian: alamat tersebut milik platform dan digunakan untuk menerima deposit Anda. Untuk memindahkan dana keluar, Anda harus melalui alur **penarikan** dan menyelesaikan verifikasi tambahan.

**Kapan kedua saldo berbeda?**  
Biasanya hanya selama beberapa menit **tepat setelah deposit saat sedang dikonversi secara otomatis**. Jika tetap berbeda dalam waktu lama, muat ulang; jika masih belum sesuai, hubungi dukungan dengan menyertakan hash transaksi.
