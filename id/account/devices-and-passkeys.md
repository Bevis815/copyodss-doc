# Perangkat & Passkey

Halaman ini membahas dua topik keamanan: **perangkat mana saja yang telah masuk ke akun Anda**, dan **cara masuk dengan cepat menggunakan Face ID / sidik jari**.

Titik masuk: Settings → Security → **Devices** → `/settings/devices`; Passkey dikelola di Settings → `/settings/passkeys`

***

## 1. Perangkat

### Yang akan Anda lihat

| Kolom | Arti |
|-------|---------|
| Nama perangkat | misalnya model ponsel atau nama OS Anda; menampilkan "Unknown device" jika tidak dapat diidentifikasi |
| **Current device** | Perangkat yang sedang Anda gunakan saat ini |
| **Last active** | Kapan terakhir kali digunakan |
| Sesi aktif | Berapa banyak sesi masuk di perangkat ini |
| Penarikan tersedia pada | Perangkat baru biasanya harus menunggu beberapa saat sebelum dapat melakukan penarikan |

### Menghapus perangkat

1. Temukan perangkat yang tidak Anda kenali → ketuk **Remove** (hapus)
2. Setelah Anda mengonfirmasi, perangkat dihapus dan **sesi masuknya langsung dibatalkan**

### Kapan harus menghapus perangkat

- Anda berganti ponsel / komputer dan perangkat lama masih tercantum
- Ada perangkat dalam riwayat masuk Anda yang tidak Anda kenali
- Anda mencurigai orang lain menggunakan akun Anda

> Setelah dihapus, perangkat tersebut harus masuk kembali (kode email / Telegram / Passkey).

***

## 2. Passkey

Passkey memungkinkan Anda masuk dengan **Face ID, sidik jari, atau kunci layar** ponsel Anda alih-alih memasukkan kode.

### Menambahkan Passkey

1. Settings → Passkeys → **Add passkey** (tambahkan passkey)
2. Selesaikan verifikasi Face ID / sidik jari sesuai petunjuk
3. Setelah selesai, Passkey muncul di daftar beserta waktu pembuatan, waktu terakhir digunakan, dan apakah sudah disinkronkan

### Menggunakannya untuk masuk

Pilih **Passkey** di halaman masuk — tidak perlu email.

### Menghapus Passkey

Pilih → **Delete** (hapus) → konfirmasi. Setelah dihapus, perangkat tersebut tidak dapat lagi masuk dengan Passkey.

### Pemecahan masalah

| Gejala | Apa yang harus dilakukan |
|---------|------------|
| Face ID tidak muncul saat menambahkan | Batalkan dan **ketuk "Add Passkey" lagi**, selesaikan verifikasi segera setelah petunjuk muncul; tutup banner notifikasi terlebih dahulu |
| Menyatakan perangkat ini tidak didukung | Gunakan browser bawaan sistem (Safari di iOS, Chrome di Android), atau cukup gunakan kode email |
| Menyatakan Passkey dengan nama yang sama sudah ada | Hapus entri "Android device" yang lama terlebih dahulu; jika Anda menggunakan proxy / VPN, matikan lalu coba lagi |
| Gagal masuk | Masuk dengan kode email sebagai gantinya; kegagalan Passkey tidak memengaruhi keamanan akun Anda |

> Passkey hanya dapat digunakan untuk masuk dan **tidak dapat digunakan untuk verifikasi penarikan**.
