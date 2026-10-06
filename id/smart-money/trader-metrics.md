# Memahami Metrik Trader

Angka di halaman papan peringkat dan profil tidak selalu dihitung dengan cara yang sama. Berikut adalah kolom-kolom yang paling sering Anda lihat. **Semua metrik hanya untuk referensi dan tidak menjamin kinerja di masa depan.**

***

## Skor keseluruhan dan tier

| Konsep | Deskripsi |
|---------|-------------|
| **Skor keseluruhan / Skor trader** | Hasil dari model multi-faktor; semakin tinggi biasanya berarti kinerja keseluruhan semakin baik |
| **Peringkat papan** | Peringkat keseluruhan default dapat menggabungkan beberapa peringkat dan **tidak** sekadar diurutkan berdasarkan skor keseluruhan |
| **Tier (S–D)** | Label tingkat kualitas untuk alamat (misalnya S = smart money teratas → D = hati-hati / risiko tinggi) |
| **Risiko** | Petunjuk tingkat risiko seperti Rendah / Sedang / Tinggi |

### Faktor skor (umum)

| Faktor | Arti (disederhanakan) |
|--------|----------------------|
| Edge | Keunggulan prediksi / penetapan harga |
| Profitabilitas | Kemampuan menghasilkan uang |
| Copyability | Apakah mereka mudah diikuti dengan asumsi penundaan dan slippage |
| Kesehatan drawdown | Apakah drawdown terkendali |
| Konsistensi | Apakah kinerja berkelanjutan dan stabil |
| Penalti gaya | Sifat seperti konsentrasi taruhan dapat menurunkan skor |

Jendela penilaian sebagian besar merupakan sampel terbaru, bukan seluruh riwayat akun sejak dibuat.

***

## Metrik daftar / kartu yang umum

| Metrik | Cara membacanya |
|--------|----------------|
| **Total L&R** | L&R berdasarkan metodologi yang disebutkan; perhatikan apakah itu jendela waktu terbaru atau layanan PnL resmi |
| **L&R 7 hari** | Kinerja jangka pendek; kurang bermakna saat volatil |
| **Win rate** | Proporsi sampel tertutup yang ditebak dengan benar; win rate tinggi ≠ profit terjamin |
| **Drawdown / DD** | Penurunan dari puncak; semakin rendah biasanya semakin baik |
| **Copy fit** | Copyability simulasi: Tinggi / Sedang / Rendah |
| **Profit factor** | Metrik berjenis rasio antara total profit vs. total kerugian |
| **Stabilitas / Aktivitas** | Terkait dengan volatilitas imbal hasil dan frekuensi trading |
| **Trade 7 hari / Volume** | Apakah mereka masih aktif trading |
| **Rata-rata imbal hasil tertutup** | Metrik berjenis imbal hasil rata-rata di seluruh sampel tertutup |

Kolom yang ditandai sebagai "simulated" (backtest P&L, copy loss, slippage, dll.) adalah simulasi **dengan asumsi transaksi tertunda**, **bukan** hasil copy nyata pengguna platform.

***

## Ringkasan profil (kolom umum)

| Kolom | Deskripsi |
|-------|-------------|
| Dana saat ini | Referensi ukuran modal trader |
| Total L&R / L&R belum terealisasi | L&R terealisasi dan L&R mengambang dari posisi terbuka |
| Total volume | Referensi aktivitas trading |
| Total imbal hasil / Rata-rata margin profit | Rasio berjenis imbal hasil |
| Menang / Kalah | Struktur sampel |
| Profit factor | Kualitas profit |
| Kemenangan terbesar / Kerugian terbesar (drawdown) | Risiko ekor |
| Aktivitas terbaru | Apakah mereka masih trading |

***

## "Kinerja copy nyata" vs. "Simulasi copy"

| Jenis | Arti |
|------|---------|
| **Simulasi copy** | Sistem melakukan backtest "apa yang akan terjadi jika Anda meng-copy" dengan asumsi penundaan + slippage |
| **Kinerja copy nyata** | Sampel dari pengguna yang benar-benar meng-copy alamat ini di platform (ROI, L&R copy, pelanggan, dll.); dapat disembunyikan jika sampel tidak mencukupi |

**Keduanya tidak** menjamin hasil Anda setelah meng-copy.

***

## Tips membaca

1. Lihat skor, drawdown, dan copyability sebelum total L&R
2. Dengan sampel yang terlalu sedikit, win rate dan ROI mudah terdistorsi
3. Untuk alamat market maker / taruhan yang sangat terkonsentrasi, metrik yang tampak bagus tidak berarti mereka cocok untuk di-copy
4. Pada akhirnya, nilailah hasil copy berdasarkan **Trade history** Anda sendiri
