# Keamanan Penarikan

Penarikan memindahkan dana ke alamat eksternal, sehingga setiap penarikan memerlukan **verifikasi tambahan**. Saat ini hanya **Authenticator (TOTP)** yang didukung.

![Verifikasi tambahan penarikan](../.gitbook/assets/withdraw_stepup_doc.png)

***

## Metode verifikasi

- **Satu-satunya metode: kode Authenticator** (Google / Microsoft Authenticator, 1Password, dll.)
- Jika belum ada Authenticator yang ditautkan, alur penarikan akan meminta Anda untuk mengaktifkannya di Pengaturan terlebih dahulu
- **Passkey dan kode email tidak dapat digunakan untuk penarikan** (keduanya tetap berfungsi untuk masuk, dll.)

Anda dapat menemukan deskripsi "Withdrawal step-up verification" di Pengaturan.

***

## Yang harus dilakukan saat melakukan penarikan

1. Pastikan Authenticator sudah ditautkan
2. Isi alamat Polygon dan jumlah di halaman penarikan lalu periksa ulang
3. Di dialog verifikasi tambahan, masukkan kode 6 digit
4. Kirim penarikan setelah verifikasi berhasil

Jika kode salah atau kedaluwarsa, cukup masukkan kode yang berlaku saat ini lagi.

***

## Perlindungan tambahan

| Mekanisme | Deskripsi |
|-----------|-------------|
| Max withdrawable | Dana yang terikat dalam posisi dan order tidak dapat ditarik |
| Masa tunggu perangkat baru / jaringan baru | Penarikan mungkin untuk sementara tidak tersedia setelah berganti perangkat atau perubahan IP |
| Saluran penarikan sibuk | Pada jam sibuk Anda mungkin perlu menunggu beberapa menit hingga jam; dana Anda aman |
| Dompet tujuan memerlukan MATIC | Simpan sedikit MATIC (POL) di alamat baru, atau Anda tidak akan dapat memindahkan USDC ini secara on-chain setelahnya |
| Pembatasan trading | Jika trading akun dibatasi, penarikan juga dapat terpengaruh |
| Pemeriksaan alamat | Dana yang dikirim ke alamat eksternal yang salah biasanya tidak dapat dipulihkan |

***

## Tips keamanan

- Jangan pernah memberikan kode Authenticator Anda kepada siapa pun yang mengaku sebagai dukungan
- Jangan pernah mengubah alamat penarikan ke "alamat perantara" yang diberikan seseorang
- Untuk panduan domain email resmi, lihat [Anti-Phishing](anti-phishing.md)
- Sebelum penarikan besar: uji dengan jumlah kecil → pastikan sudah masuk → lalu tarik lebih banyak
