# Mengelola Copy

Kelola semua aturan copy Anda di **My copies** → `/copy-rules`.

![Copy saya](../.gitbook/assets/my_copies_doc.png)

***

## Ringkasan di bagian atas halaman (umum)

| Kolom | Arti |
|-------|---------|
| Realized | L&R yang terealisasi dari posisi yang sudah ditutup |
| Position | Ringkasan nilai pasar posisi saat ini |
| Unrealized | L&R mengambang |
| Win Rate | Statistik menang / kalah |

Jika Anda belum membuat aturan apa pun, halaman mungkin menampilkan panduan pengenalan: Masuk → Deposit → Beli Gas → Mulai meng-copy.

***

## Status aturan

| Status | Arti | Apa yang harus dilakukan |
|--------|---------|------------|
| **Following** | Meng-copy secara normal | Cukup pantau Trade history |
| **Manually paused** | Anda menjedanya sendiri | Lanjutkan saat diperlukan |
| **Funding alert** | Pembelian terpengaruh oleh masalah dana / Gas | Deposit atau beli Gas, lalu ketuk **Resume buys** (lanjutkan pembelian) |

> Saat dana menipis, aturan **sering tetap aktif** dan hanya pembelian yang dilewati — ini memang dirancang demikian, agar setelah mengisi saldo Anda dapat terus meng-copy penjualan pada posisi yang sudah ada.

***

## Tindakan pada satu aturan

| Tindakan | Deskripsi |
|--------|-------------|
| Pause / Resume | Menjeda atau melanjutkan seluruh aturan |
| Resume buys | Menghapus peringatan dana dan melanjutkan meng-copy pembelian |
| Edit | Mengubah jumlah, persentase, slippage, dll. |
| Delete | Menghapus aturan (riwayat biasanya tetap disimpan) |
| Positions / Activity / Detail | Lompat ke posisi, aktivitas, atau profil |

Jeda / lanjutkan / hapus secara massal juga didukung (lihat UI).

***

## Jeda vs. Hapus

| | Jeda | Hapus |
|--|-------|--------|
| Dapatkah dipulihkan dengan cepat nanti? | Ya, Resume | Harus membuat ulang aturan |
| Riwayat trade | Disimpan | Biasanya disimpan |
| Posisi yang ada | **Tidak** dijual otomatis | **Tidak** dijual otomatis |

Tutup posisi sendiri di **Positions**, atau tunggu penyelesaian lalu tukarkan.

***

## Halaman terkait

| Halaman | Jalur | Tujuan |
|------|------|---------|
| Aktivitas copy | `/feed` | Melihat transaksi publik leader dan tag status copy |
| Riwayat trade | `/executions/records` | Hasil transaksi Anda |
| Posisi | `/executions/positions` | Posisi dan penutupan |
| L&R harian | `/executions/daily-pnl` | L&R terealisasi harian |

![Aktivitas copy](../.gitbook/assets/feed_doc.png)

Tag status di Copy activity membantu Anda memahami "apakah transaksi publik ini dicoba untuk di-copy"; **Trade history adalah acuan akhir**.

***

## Pelajari lebih lanjut

- Mengapa setiap trade di-copy atau tidak: [Aktivitas Copy](copy-activity.md)
- Posisi dan penyelesaian: [Posisi Saya & Riwayat Trade](positions-and-records.md)
- Coba tanpa mengeluarkan uang sungguhan: [Simulasi Copy Trading](simulation.md)
