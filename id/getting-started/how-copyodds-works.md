# Cara Kerja CopyOdds

Dari "trader mendapatkan transaksi" hingga "akun Anda mencoba meng-copy-nya", seluruh alurnya terlihat seperti ini:

```text
Trader smart money mendapatkan transaksi di Polymarket
        ↓
CopyOdds mendeteksi transaksi publik tersebut
        ↓
Mencocokkan dengan aturan copy Anda untuk alamat tersebut
        ↓
Menghitung ukuran order sesuai aturan (jumlah tetap atau % dari saldo Anda)
        ↓
Mencoba menempatkan order dalam batas slippage (memakai Gas Platform)
        ↓
Hasil dicatat di Trade history; kepemilikan muncul di Positions
```

## 1. Menemukan trader

- Sistem terus-menerus menilai dan menyaring dompet Polymarket publik
- **Papan peringkat yang ditampilkan** biasanya mengharuskan skor keseluruhan memenuhi ambang batas (misalnya ≥ 40); alamat dengan skor rendah dapat tersingkir
- Di **Smart money** Anda dapat menelusuri, mencari, atau menganalisis alamat yang tidak terdaftar (jika fitur tersedia, batas harian mungkin berlaku)

## 2. Dana dan biaya terpisah

| Sumber daya dalam akun | Tujuan |
|---------------------|---------|
| **USDC (dll.)** | Modal copy: digunakan saat membeli, dikembalikan saat menjual |
| **Gas Platform** | Kredit biaya layanan: sekitar 0.5% dari nilai nominal dipotong per transaksi copy |

Saat Gas bernilai 0: Anda **tidak dapat membuat / melanjutkan aturan copy**. Aturan yang ada biasanya tetap berjalan, tetapi **pembelian dilewati**; penjualan mungkin masih di-copy jika Anda memegang posisi.

## 3. Bagaimana aturan copy berlaku

Anda menyimpan satu aturan per alamat leader (menyimpan lagi untuk alamat yang sama akan menimpanya):

- **Mode copy** (pilih satu; default **Ratio**):
  - **Ratio**: setiap transaksi leader × rasio Anda = jumlah order Anda
  - **By balance %**: setiap trade menggunakan persentase dari USDC tersedia milik Anda sendiri
  - **Fixed amount**: setiap trade membeli jumlah yang sama
  - Lihat [Tiga Mode Copy](../copy-trading/copy-modes.md)
- **Arah**: Keduanya / Hanya beli / Hanya jual
- **Slippage**: tidak terisi jika harga bergerak terlalu jauh (default 15%)
- **Rasio copy / Rentang ukuran** (hanya mode Ratio): mengatur "berapa banyak yang di-copy" dan "ukuran order mana yang di-copy"
- **Max open copy buys**: default 1 (tidak menambah posisi); dapat dinaikkan, dan maksimumnya adalah **All (tanpa batas)**

Setelah mendeteksi transaksi leader, sistem mencoba menempatkan order menggunakan aturan-aturan ini. Sistem **tidak menjamin** setiap trade akan di-copy.

## 4. Cara mengetahui apakah sebuah trade sudah di-copy

| Tempat melihat | Apa yang ditunjukkan |
|---------------|-------------------|
| Copy activity | Apa yang dilakukan trader |
| Trade history | Hasil upaya copy Anda (terisi / dilewati / gagal) |
| Positions | Apa yang sedang Anda pegang |
| My copies | Status aturan: Following / Manually paused / Funding alert |

## 5. Jaringan deposit dan penarikan berbeda (penting)

- **Deposit**: Polygon (PoS) dan BSC (jika diaktifkan), aset USDC / USDT
- **Penarikan**: hanya **Polygon (PoS) USDC**
- Kedua jaringan deposit menggunakan **alamat yang berbeda** — jangan pernah tertukar

Lihat [Jaringan yang Didukung](../wallet/supported-networks.md).

## 6. Ringkasan model keamanan

CopyOdds menggunakan **akun trading kustodian**: satu dompet per pengguna, dengan private key yang terisolasi. Penarikan memerlukan verifikasi tambahan **Authenticator (TOTP)**. Lihat [Keamanan](../security/wallet-security.md).
