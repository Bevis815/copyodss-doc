# Penarikan

Tarik **USDC** yang tersedia bebas dari akun trading Anda ke dompet eksternal. Titik masuk: **Wallets → Withdraw** → `/wallets/withdraw`.

![Halaman penarikan](../.gitbook/assets/usdc2_doc.png)

![Verifikasi tambahan penarikan](../.gitbook/assets/withdraw_stepup_doc.png)

***

## Aturan penarikan

| Item | Deskripsi |
|------|-------------|
| Jaringan | **Hanya Polygon (PoS)** |
| Aset | **USDC** |
| Alamat penerima | Harus dapat menerima Polygon USDC; **jangan** memasukkan alamat kustodian dari halaman deposit, dan tidak boleh **alamat deposit Anda saat ini itu sendiri** |
| Dompet tujuan | Sebaiknya memiliki sedikit **MATIC (POL)**; Anda akan memerlukannya untuk membayar gas saat memindahkan USDC ini secara on-chain nanti |
| Verifikasi tambahan | Diperlukan untuk setiap penarikan (lihat di bawah) |

***

## Langkah-langkah

1. Buka halaman penarikan dan periksa **Max withdrawable** (jumlah maksimum yang dapat ditarik; mungkin lebih kecil dari total saldo Anda)
2. Masukkan alamat penerima Polygon dan jumlahnya
3. Periksa ulang jaringan, alamat, dan jumlahnya
4. Ketuk lanjutkan dan selesaikan **verifikasi tambahan penarikan**
5. Setelah mengirim, lacak statusnya di laporan / catatan Anda

***

## Mengapa "Max withdrawable" lebih kecil dari saldo saya?

Dana berikut biasanya tidak dapat langsung ditarik:

- Dana yang terikat dalam posisi terbuka
- Dana yang dibekukan dalam order yang belum terisi
- Margin / dana lain yang dikunci oleh sistem

Ikuti angka **Max withdrawable** di halaman, bukan total saldo Anda.

***

## Verifikasi tambahan penarikan

Setiap penarikan harus dikonfirmasi dengan kode **Authenticator (TOTP)** 6 digit — **saat ini ini adalah satu-satunya metode yang didukung**.

Jika Anda belum menyiapkannya, sistem akan memandu Anda untuk mengaktifkannya di Pengaturan; **Anda tidak dapat melakukan penarikan tanpanya**.

**Passkey dan kode email tidak dapat digunakan untuk mengonfirmasi penarikan** (keduanya hanya untuk masuk dan skenario serupa).

Lihat [Keamanan Penarikan](../security/withdrawal-security.md) dan [Autentikasi Dua Faktor (2FA)](../security/2fa.md).

***

## Untuk sementara tidak dapat melakukan penarikan?

| Pesan | Arti | Apa yang harus dilakukan |
|---------|---------|------------|
| **Withdrawal channel busy** | Banyak permintaan penarikan hari ini | Tunggu beberapa menit atau jam sesuai petunjuk; **dana Anda aman dan Anda tidak perlu mengajukan ulang** |
| **New device / new network cooldown** | Anda baru saja berganti perangkat atau IP Anda berubah | Coba lagi setelah masa tunggu berakhir |
| **Unfilled orders exist** | Anda masih memiliki order terbuka | Batalkan atau tunggu hingga terisi |
| **Positions still open** | Alamat kustodian Anda masih memegang posisi pasar | Tutup atau tunggu penyelesaian |
| **Previous withdrawal in progress** | Masih dikonfirmasi on-chain | Tunggu hingga selesai sebelum mengirim yang berikutnya |
| **Address is your deposit address** | Anda tidak dapat menarik kembali ke alamat deposit Anda | Gunakan alamat penerima milik Anda sendiri sebagai gantinya |

Periksa sesi dan pengaturan keamanan di **Settings → Devices / Security**. Jika masih gagal, hubungi dukungan dan sebutkan apakah Anda baru saja berganti perangkat.

***

## Tips keamanan

- Sebelum penarikan besar pertama Anda: uji dengan jumlah kecil terlebih dahulu
- Penarikan biasanya tidak dapat dibatalkan setelah dikirim — periksa alamat karakter demi karakter
- CopyOdds tidak akan pernah mengirimi Anda pesan langsung untuk "membantu penarikan" atau meminta kode verifikasi Anda

***

## Tempat melihat catatan penarikan

**Transaction history** → `/wallets/ledger` menampilkan status setiap penarikan dan "saldo setelahnya", dengan tautan ke block explorer. Lihat [Riwayat Transaksi](ledger.md).
