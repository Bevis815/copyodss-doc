# Aktivitas Copy

**Copy activity** memberi tahu Anda dua hal: **apa yang baru saja dilakukan trader**, dan **apakah Anda meng-copy-nya**.

Titik masuk: **Copy activity** → `/feed` (biasanya dibuka dari **My copies** atau menu)

***

## Isi halaman

1. **Atas: dompet yang saya copy** — Menampilkan alamat yang telah Anda aktifkan copy-nya; ketuk salah satu untuk melihat hanya alamat tersebut
2. **Tiga tab**

| Tab | Isi |
|-----|---------|
| **Activity** | Pembelian / penjualan publik trader |
| **My orders** | Hasil setiap order yang ditempatkan sistem untuk Anda |
| **My positions** | Posisi dan L&R Anda saat ini |

3. **Filter**: All / Successful / Buys / Sells / Copying
4. Setiap entri menampilkan waktu (**just now**, **a few minutes ago**); tarik ke bawah di ponsel untuk memuat ulang

***

## Membaca status copy

| Status | Arti | Apa yang harus dilakukan |
|--------|---------|------------|
| **Copying** | Sedang mencoba menempatkan order | Tunggu sebentar |
| **Copied** | Berhasil di-copy | Tidak ada |
| **Skipped** | Tidak di-copy kali ini | Periksa alasan kegagalannya |
| **Failed** | Order ditolak atau mengalami error | Periksa alasannya — mungkin saldo / slippage / Gas |
| **Not copied** | Entri ini tidak berada dalam cakupan copy Anda | Tidak ada |

Ketuk entri mana pun untuk melihat **detail trade**: pasar, arah, alamat, volume, aturan copy, dompet copy, status, waktu, dan hash transaksi on-chain.

***

## Alasan umum dilewati

- Ketidaksesuaian arah (Anda mengatur Buy only / Sell only)
- Jumlah terlalu kecil (di bawah pembelian minimum bursa sekitar $1)
- Mencapai "Max open copy buys" (default 1, yaitu tidak menambah posisi)
- Slippage terlalu besar
- **Gas tidak mencukupi** atau **USDC tidak mencukupi**
- Trader menjual tetapi Anda tidak memegang posisi yang sesuai
- Tidak ada yang menerima order di pasar tersebut pada saat itu

***

## Tips

- Gunakan **Activity** untuk memantau orang lain dan **Trade history** untuk memeriksa diri sendiri — membandingkan keduanya adalah cara termudah untuk menemukan masalah
- Jika ada banyak yang dilewati, periksa Gas dan saldo terlebih dahulu, lalu pertimbangkan untuk menyesuaikan slippage atau menurunkan jumlah
- Saat membagikan entri kepada dukungan, sertakan **ID catatan** atau **hash transaksi**
