# Posisi Saya & Riwayat Trade

Setelah Anda mulai meng-copy, semua posisi Anda dan hasil setiap order ada di kedua halaman ini. **Sebagai pemula, kedua halaman inilah yang perlu Anda ketahui.**

| Halaman | Titik masuk | Pertanyaan yang dijawab |
|------|-------|-----------------|
| **My positions** | My positions → `/executions/positions` | Apa yang saya pegang sekarang, dan apakah saya untung atau rugi? |
| **Trade history** | Executions → `/executions/records` | Hasil setiap upaya copy |
| **Profit/Loss** | Executions → Profit/Loss → `/executions/daily-pnl` | Berapa banyak yang telah saya hasilkan selama periode ini? |

***

## Posisi saya

### Yang akan Anda lihat

| Kolom | Arti |
|-------|---------|
| **Market / Outcome** | Peristiwa dan hasil mana (Yes / No) yang Anda beli |
| **Avg. price / Current price** | Biaya masuk Anda dan harga pasar saat ini |
| **Cost / Value / P&L** | Berapa yang Anda keluarkan, berapa nilainya sekarang, dan apakah Anda untung |
| **Copy sources** | Aturan copy mana yang membentuk posisi ini |
| **Status** | Open / Pending settlement / Settled / Archived |

### Yang dapat Anda lakukan

| Tindakan | Deskripsi |
|--------|-------------|
| **Buy more** | Membeli sedikit lagi sendiri dengan memasukkan jumlah dalam USD |
| **Close** | Menjual dengan harga pasar untuk mengunci L&R; harga bergerak mengikuti pasar |
| **Bulk close** | Menutup hingga sejumlah posisi tertentu sekaligus |
| **Redeem** | Pasar telah berakhir dan Anda menang — konversikan posisi menjadi USDC |
| **View details** | Melihat waktu pembelian, metode penyelesaian, dan linimasa lengkap |

### Arti status

| Status | Deskripsi |
|--------|-------------|
| **Open** | Pasar belum berakhir; Anda dapat menjual |
| **Pending settlement** | Tidak dapat dijual untuk sementara; jika Anda menang, Redeem akan muncul; jika Anda kalah, posisi ditutup secara otomatis |
| **Settled** | Telah dikonversi menjadi USDC dan dikembalikan ke saldo Anda |
| **Archived** | Posisi sangat kecil atau tidak likuid yang untuk sementara tidak dapat dijual; tidak memengaruhi hal lain |

***

## Riwayat trade (riwayat copy)

Setiap baris adalah satu upaya yang dilakukan sistem atas nama Anda:

| Status | Arti |
|--------|---------|
| **Filled** | Berhasil di-copy |
| **In progress** | Masih diproses |
| **Skipped** | Tidak ada order yang ditempatkan (lihat alasan kegagalannya) |
| **Failed** | Order ditolak atau mengalami error |

Anda dapat menyaring berdasarkan **Filled / Settled / Unsuccessful**. Ketuk baris mana pun untuk melihat: aturan copy, ID order, harga beli dan jumlah share, cara penutupannya (dijual / ditukarkan / kedaluwarsa), biaya, hasil, L&R, linimasa lengkap, dan hash on-chain.

***

## Halaman Profit/Loss

- Bagian atas menampilkan **kurva L&R kumulatif**, dapat dialihkan antara 1 hari / 1 minggu / 1 bulan, dll.
- Bagian bawah menampilkan **rincian periode**, termasuk hari ini, kemarin, dan perubahan L&R akun setiap hari
- Kurva ini sesuai dengan metodologi L&R akun Polymarket; jika data resmi untuk sementara tidak tersedia, halaman akan mencatat bahwa halaman menggunakan data buku besar platform sebagai gantinya

> Waktu mulai hari kerja sesuai dengan yang ditampilkan di halaman (misalnya dimulai pukul 08:00), jadi perhatikan hal ini saat melihat data lintas hari.

***

## Pertanyaan umum pemula

**Mengapa L&R posisi saya tidak sesuai dengan saldo saya?**  
L&R posisi adalah "perkiraan berdasarkan harga pasar saat ini", dan bagian yang belum terealisasi berubah mengikuti harga; saldo Anda baru mencerminkannya setelah Anda menjual atau menukarkan.

**Mengapa penjualan saya gagal?**  
Alasan umum: tidak ada order beli di pasar pada saat itu, share terikat dalam order terbuka, atau sisa posisi berada di bawah ukuran jual minimum. Coba lagi nanti.

**Saya menang — mengapa saya tidak melihat uangnya?**  
Diperlukan sedikit waktu untuk dikreditkan setelah pasar diselesaikan; Anda dapat mengetuk **Redeem** (tukarkan) untuk menukarkan secara manual. Selama statusnya "Pending settlement", Anda belum dapat melakukan tindakan apa pun.
