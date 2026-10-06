# Autentikasi Dua Faktor (2FA)

Secara default CopyOdds memasukkan Anda dengan **kode verifikasi email** (tanpa kata sandi tradisional). Kami menyarankan untuk mengaktifkan Authenticator dan Passkey sekaligus untuk masing-masing memperkuat keamanan penarikan dan masuk.

![Pengaturan keamanan](../.gitbook/assets/settings_security_doc.png)

***

## Metode yang tersedia

| Metode | Tujuan |
|--------|---------|
| **Email OTP** | Masuk, verifikasi penautan |
| **Authenticator (TOTP)** | **Verifikasi tambahan penarikan (satu-satunya metode)**; juga memperkuat keamanan akun |
| **Passkey** | Wajah / sidik jari / kunci layar untuk verifikasi **masuk** dengan cepat |
| **Telegram** | Metode masuk / penautan opsional (lihat Pengaturan) |
| **Manajemen perangkat** | Melihat dan menghapus perangkat; perangkat baru dapat memengaruhi penarikan |

***

## Urutan penyiapan yang disarankan

1. Tautkan dan verifikasi email Anda
2. **Aktifkan Authenticator (wajib sebelum melakukan penarikan)**
3. Tambahkan **Passkey** di perangkat yang sering Anda gunakan (untuk mempermudah masuk)
4. Kenali daftar **Devices** dan hapus perangkat apa pun yang tidak Anda kenali

***

## Authenticator (TOTP)

1. Buka **Settings → Security**
2. Ikuti panduan untuk memindai kode QR dengan aplikasi Authenticator Anda, atau masukkan kuncinya secara manual
3. Masukkan kode 6 digit untuk menyelesaikan pengaktifan

Jika Anda datang ke sini dari alur penarikan, Anda akan **dibawa kembali ke halaman dompet secara otomatis untuk melanjutkan penarikan** setelah selesai.

### Menonaktifkan Authenticator

Demi keamanan, **menonaktifkannya juga memerlukan kode 6 digit**. Jika Anda hanya ingin berganti perangkat, lebih mudah untuk menautkan ulang di perangkat baru.

### Pesan umum

| Pesan | Penyebab | Apa yang harus dilakukan |
|---------|-------|------------|
| Kode salah atau kedaluwarsa | Salah ketik, atau sudah lewat lebih dari 30 detik | Tunggu kode baru lalu masukkan |
| Kode sudah digunakan | Kode yang sama dikirim dua kali | Tunggu kode baru berikutnya |
| Penautan kedaluwarsa | Terlalu lama antara memindai dan mengonfirmasi | Mulai penautan lagi |
| Terlalu banyak percobaan | Terlalu banyak salah memasukkan dalam waktu singkat | Tunggu sebentar lalu coba lagi |
| Authenticator sudah diaktifkan | Menautkan untuk kedua kalinya | Tidak perlu melakukannya lagi |

***

## Passkey

1. Buka Pengaturan di browser / OS yang didukung
2. Tambahkan Passkey dan selesaikan verifikasi biometrik atau kunci layar sesuai petunjuk
3. Di halaman masuk Anda dapat memilih Passkey untuk masuk dengan cepat

Catatan: Passkey **tidak dapat** digunakan untuk mengonfirmasi penarikan. Dukungan bervariasi antar browser, WebView, dan versi OS; jika gagal masuk, gunakan kode email sebagai alternatif.

***

## Perangkat dan sesi

- Lihat perangkat yang telah masuk di `/settings/devices`
- Setelah masuk di perangkat atau lingkungan baru, **penarikan mungkin dikunci sementara** untuk beberapa waktu (masa tunggu keamanan)
- Di komputer umum, jangan memercayai ekstensi yang tidak dikenal dalam jangka panjang atau menyimpan kode di tempat yang tidak aman

***

## Kehilangan authenticator Anda?

Jika Anda masih dapat mengakses email Anda:

1. Masuk dengan kode email
2. Tautkan ulang Authenticator (dan Passkey apa pun yang Anda perlukan) di Pengaturan
3. Periksa daftar perangkat dan hapus perangkat yang hilang

Jika Anda juga tidak dapat mengakses email Anda: hubungi dukungan dan siapkan materi verifikasi identitas (sesuai proses dukungan).
