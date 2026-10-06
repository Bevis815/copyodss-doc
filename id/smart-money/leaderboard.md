# Papan Peringkat Smart Money (Filter berdasarkan Profil Trader)

Papan peringkat Smart Money membantu Anda menemukan trader Polymarket yang layak di-copy. Titik masuk: **Smart money** → `/smart-money` (halaman beranda App sekarang adalah [Papan Profit Harian Copy Pool](copy-pool-board.md); buka Smart money dari menu).

![Papan peringkat Smart Money](../.gitbook/assets/smarket_doc.png)

***

## Apa yang dapat Anda lakukan di sini

1. **Menelusuri papan peringkat** — Melihat L&R, skor, win rate, 7 hari terakhir, dan lainnya dalam bentuk kartu atau tabel
2. **Mencari alamat** — Mencari trader berdasarkan alamat dompet
3. **Menyaring** — Kategori, preset cepat, dan filter lanjutan (tier, gaya, rentang metrik, copyability, dll.)
4. **Periode peringkat** — Keseluruhan / Mingguan / Bulanan (defaultnya biasanya peringkat keseluruhan, yang tidak sekadar diurutkan berdasarkan skor keseluruhan)
5. **Copy** — Ketuk **Follow** (ikuti) untuk membuka pengaturan copy, atau buka profil terlebih dahulu dan putuskan di sana

***

## Cara data papan peringkat dihitung (wajib dibaca)

- Kurva L&R, profit 7 hari terakhir / total, dll. biasanya berasal dari data PnL resmi Polymarket
- Win rate, profit factor, dll. sebagian besar didasarkan pada **pasar yang sudah ditutup**
- Skor dan metrik backtest didasarkan pada **transaksi dalam jendela waktu terbaru** (sekitar 30 hari / hingga sekitar 4,000 trade), **bukan seluruh riwayat sepanjang masa**
- **Papan peringkat yang ditampilkan** biasanya hanya mencakup alamat yang skor keseluruhannya memenuhi ambang batas (misalnya ≥ 40); alamat yang berulang kali mendapat skor rendah dapat tersingkir
- "Copy fit / backtest P&L / slippage" dan sejenisnya sebagian besar adalah **simulasi dengan asumsi penundaan + slippage**, bukan L&R nyata pengguna yang meng-copy di platform

> Papan peringkat **bukan saran investasi**. Kinerja masa lalu tidak menjamin imbal hasil di masa depan.

***

## Filter umum

### Contoh kategori

All, Politics, Sports, Esports, Crypto, Culture, Weather, Economy, Tech, Finance, Mentions, dan lainnya.

### Contoh filter cepat

| Preset | Tujuan kasar |
|--------|---------------|
| Featured | Trader unggulan platform, cenderung dapat di-copy |
| Steady | Gaya yang relatif konservatif |
| High copyability | Lebih mudah diikuti dalam simulasi |
| Recently active | Trading lebih sering dalam jendela waktu terbaru |
| All copyable | Alamat yang tersedia untuk di-copy |
| High win rate / High return / Low drawdown | Mempersempit berdasarkan metrik terkait |
| Long-term stable | Kandidat dengan konsistensi yang lebih baik |

### Filter lanjutan (opsi umum)

- Hanya alamat yang dapat di-copy / Hanya unggulan (tidak termasuk market maker)
- Tier (S–D), gaya trading
- Rentang metrik (misalnya jumlah trade dalam 7 hari terakhir, win rate)
- Mengecualikan tag risiko tertentu
- Copyability: Tinggi / Sedang / Rendah

***

## Tag gaya trading (sebagai referensi)

| Tag | Arti (disederhanakan) |
|-----|----------------------|
| Information edge | Cenderung mengambil posisi lebih awal / didorong oleh informasi |
| Arbitrage | Pola spread / arbitrase |
| Gambler | Pola taruhan dengan volatilitas tinggi; copy dengan sangat hati-hati |
| Market maker | Market making berfrekuensi tinggi; biasanya tidak cocok untuk copy biasa |
| Mixed | Gaya campuran umum |

***

## Saran

1. Mulailah dengan preset seperti Featured / High copyability / Steady untuk mempersempit pilihan
2. Buka profil untuk meninjau faktor skor, drawdown, dan catatan risiko
3. Ikuti dengan jumlah kecil untuk menguji, lalu sesuaikan secara bertahap
4. Saat membagikan trader, gunakan format tautan profil: `https://app.copyodds.io/@0xADDRESS` (tambahkan `/zh` untuk UI berbahasa Mandarin)

***

## Halaman terkait

- Halaman beranda **Leaderboard** (profit harian copy pool): [Papan Profit Harian Copy Pool](copy-pool-board.md)
- Cara berpikir dalam memilih trader: [Cara Memilih Trader](how-to-choose.md)
