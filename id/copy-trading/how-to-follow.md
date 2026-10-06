# Cara Meng-copy Trader

Tambahkan alamat smart money ke copy otomatis dan simpan aturannya.

![Wizard copy](../.gitbook/assets/follow_doc.png)

***

## Daftar periksa sebelum memulai

| Syarat | Catatan |
|-----------|-------|
| Sudah masuk dengan akun trading yang aktif | Biasanya dibuka secara otomatis setelah masuk |
| Gas Platform > 0 | **Wajib**; jika tidak, Anda tidak dapat mengaktifkan / melanjutkan |
| Saldo USDC tersedia | Disarankan sekitar $1 atau lebih; jika tidak, pembelian kemungkinan besar dilewati |

***

## Titik masuk

Salah satu dari berikut ini:

1. Ketuk **Follow** (ikuti) di daftar **Smart money** atau halaman profil
2. **Quick copy / New copy** di **My copies**
3. Buka `/copier` (Quick copy) secara langsung dan tempelkan alamat
4. Buka tautan profil `https://app.copyodds.io/@0x...` dan ketuk Follow

***

## Langkah-langkah

1. Konfirmasi **Leader address** (alamat leader, 0x…); membawanya langsung dari papan peringkat menghindari salah ketik
2. Opsional: beri nama aturan (Name this copy trade)
3. Pilih **Copy mode** — pilih salah satu dari tiga:
   - **Ratio** — **Mode default**; meng-copy persentase tetap dari setiap transaksi leader (leader membeli $500 dengan rasio 10% → Anda membeli $50)
   - **By balance %** — Persentase dari **USDC tersedia Anda** (1%–100%)
   - **Fixed amount** — Membeli jumlah yang sama setiap kali (minimum $1)
4. Atur **Slippage tolerance** — default **15%**, dapat disesuaikan dari 1% hingga 100%

   > Untuk perbedaan ketiga mode, cara rasio dihitung, dan asal nilai yang disarankan, lihat [Tiga Mode Copy](copy-modes.md)
5. Secara opsional buka **Advanced settings** (pengaturan lanjutan):
   - **Direction** (arah): Both / Buy only / Sell only
   - **Max open copy buys**: default **1** (tidak menambah posisi); maksimumnya adalah **All (tanpa batas)**
6. Simpan (**Copy trade / Save**)
7. Buka **My copies** dan pastikan statusnya **Following**

***

## Jumlah tetap vs. % dari saldo

| Mode | Perilaku | Paling cocok untuk |
|------|----------|----------|
| Jumlah tetap | Baik trader membeli $50 atau $500, Anda meng-copy dengan jumlah yang Anda tetapkan | Mengontrol risiko per trade |
| % dari saldo | Meng-copy pembelian dengan % dari saldo tersedia Anda pada saat itu | Menyesuaikan secara otomatis dengan modal Anda |

Jika jumlah yang dihitung dari persentase berada di bawah ukuran order minimum, sistem dapat menaikkannya ke minimum sebelum mencoba.

***

## Catatan

- Setiap alamat leader biasanya hanya memiliki satu set pengaturan aktif; menyimpan lagi akan menimpanya
- Mengubah aturan hanya memengaruhi copy di masa mendatang dan tidak mengubah transaksi sebelumnya
- Menghentikan / menghapus aturan **tidak** secara otomatis menjual posisi Anda
- Uji dengan jumlah kecil terlebih dahulu, dan hanya tingkatkan setelah Trade history terlihat normal

***

## Tempat melihat setelah meng-copy

| Yang ingin Anda lihat | Tempat yang dituju |
|----------------------|-------------|
| Apa yang baru saja dilakukan trader, dan apakah saya meng-copy-nya | [Aktivitas Copy](copy-activity.md) |
| Apa yang sedang saya pegang | [Posisi Saya & Riwayat Trade](positions-and-records.md) |
| Status aturan, jeda / lanjutkan | [Mengelola Copy](managing.md) |
