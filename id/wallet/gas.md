# Gas Platform

**Gas Platform** adalah **kredit biaya layanan** di dalam akun CopyOdds Anda, digunakan untuk membayar biaya pada transaksi copy otomatis.

> **Gas Platform ≠ gas on-chain.** Ini bukan MATIC, POL, atau BNB, dan bukan gas yang Anda gunakan di dompet untuk membayar biaya jaringan.

Titik masuk: **Gas Store** → `/store`.

![Gas Store](../.gitbook/assets/store_doc.png)

***

## Mengapa Anda memerlukan Gas?

Setiap transaksi copy (beli atau jual) memotong kredit biaya layanan berdasarkan nilai nominal transaksi. Tanpa Gas:

- **Anda tidak dapat membuat atau melanjutkan aturan copy**
- Pada aturan yang ada, **pembelian biasanya dilewati**
- Jika Anda masih memegang posisi, **penjualan mungkin masih di-copy** (aturan sering tetap berjalan)

***

## Biaya (ketentuan produk saat ini)

| Item | Deskripsi |
|------|-------------|
| Biaya | **Pembelian dan penjualan** masing-masing dikenakan sekitar **0.5%** dari jumlah transaksi aktual, dipotong dalam bentuk Gas |
| Konversi | Sekitar **1 USDC = 100 Gas** |
| Contoh | Transaksi senilai $100 memakai sekitar **50 Gas** (pembelian dan penjualan masing-masing dikenakan biaya sekali) |
| Sumber pembayaran | Paket dibayar dari **saldo USDC tersedia** kustodian Anda |
| Dapat ditarik? | **Tidak** — tidak dapat ditarik atau ditransfer |

Lihat halaman toko untuk paket saat ini dan bonus apa pun (seperti peningkatan dari tingkat referral).

> Jika Anda memiliki order yang belum selesai, posisi terbuka, atau penarikan yang tertunda, toko untuk sementara mungkin **tidak mengizinkan pembelian Gas dengan saldo Anda** dan akan meminta Anda menyelesaikannya di halaman Dompet; setelah selesai, Anda dapat membeli seperti biasa.

***

## Cara membeli

1. Buka Gas Store dan pastikan Anda memiliki cukup USDC
2. Baca deskripsi biaya
3. Pilih paket → konfirmasi pembayaran
4. Gas langsung dikreditkan
5. Jika sebelumnya pembelian dilewati karena Gas tidak mencukupi: buka **My copies** dan ketuk **Resume buys** (lanjutkan pembelian)

***

## Gas vs. USDC

| | USDC | Gas Platform |
|--|------|--------------|
| Tujuan | Modal copy | Biaya layanan copy |
| Cara mendapatkannya | Deposit on-chain | Beli dengan USDC di toko |
| Dapat ditarik on-chain? | Ya (lihat Penarikan) | Tidak |

***

## FAQ

**Apakah saya perlu melakukan sesuatu setelah membeli Gas?**  
Kami menyarankan untuk membuka **My copies** dan mengetuk **Resume buys** untuk menghapus peringatan dana apa pun.

**Apakah aturan saya akan berhenti saat Gas habis?**  
Biasanya seluruh aturan tidak dijeda — pembelian dilewati, dan penjualan mungkin masih di-copy jika Anda memegang posisi.
