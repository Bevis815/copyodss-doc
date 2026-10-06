# Tiga Mode Copy (Pemula Mulai di Sini)

Hal pertama yang harus dipilih dalam pengaturan copy adalah **mode copy**. Saat ini ada tiga:

| Mode | Ringkasan satu baris | Paling cocok untuk |
|------|------------------|----------|
| **Ratio** (baru, default) | Anda membeli **persentase tetap** dari apa pun yang dibeli trader | Kebanyakan orang, terutama saat ukuran order trader sangat bervariasi |
| **By balance %** | Setiap trade menggunakan **persentase dari saldo Anda sendiri** | Orang yang ingin ukuran posisi menyesuaikan secara otomatis dengan saldo mereka |
| **Fixed amount** | Setiap trade membeli **jumlah yang sama** | Trader yang ukuran ordernya cukup konsisten |

> **Pengguna baru secara default menggunakan mode Ratio.** Ini adalah mode yang paling direkomendasikan saat ini dan dibahas paling rinci di bawah.

***

## Mengapa mode Ratio ditambahkan?

Fixed amount memiliki masalah umum: trader membeli $30 di satu waktu dan $3,000 di waktu berikutnya, tetapi Anda selalu meng-copy $10 — sehingga Anda sama sekali kehilangan ritme mereka, entah meng-copy terlalu sedikit hingga tidak berarti atau meng-copy terlalu banyak secara membabi buta.

Mode Ratio mengubahnya menjadi: **berapa pun yang mereka tempatkan, Anda menempatkan jumlah yang proporsional**.

| Transaksi trader | Mode Fixed amount Anda | Mode Ratio Anda (10%) |
|---------------|------------------------|-----------------------|
| $50 | Copy $10 | Copy $5 |
| $500 | Copy $10 | Copy $50 |
| $5,000 | Copy $10 | Copy $500 |

Keuntungannya adalah mode ini **secara alami mengikuti ukuran posisi trader**, tanpa satu taruhan besar sesekali dari mereka menghancurkan akun Anda.

***

## Mode Ratio secara rinci

### Tiga hal yang perlu diatur

| Pengaturan | Lokasi | Deskripsi |
|---------|-------|-------------|
| **Copy ratio** | Slider di bawah mode | 0.1%–100%. Transaksi trader × rasio ini = jumlah order Anda |
| **Leader order size range** | Slider kedua di bawah mode | Hanya meng-copy order trader yang "berukuran normal", menyaring order debu dan order yang terlalu besar |
| **Slippage tolerance** | Di bawah mode | 1%–100%, default **15%** |

### 1. Copy ratio

Ini adalah rasio "berapa banyak yang di-copy". Halaman pengaturan menampilkan baris pratinjau:

> Leader 100, Anda mengatur 10%, jadi milik Anda adalah 10.

Halaman biasanya juga menampilkan **Suggested ratio** (rasio yang disarankan) di samping "sekitar N trade/hari". Cara menghitungnya seperti ini:

> **Rasio yang disarankan ≈ saldo tersedia Anda ÷ (batas atas rentang × perkiraan jumlah trade trader per hari)**

Contoh: Anda memiliki $1,000 yang tersedia, trader membeli sekitar 5 kali sehari, dan batas atas rentang adalah $800.
Rasio yang disarankan ≈ 1000 ÷ (800 × 5) = 25%. Dengan kata lain, **Anda akan menggunakan senilai sekitar 5 trade dalam sehari**, dan satu order besar tidak akan menghabiskan saldo Anda sekaligus.

Jika Anda tidak ingin menggunakan nilai yang disarankan, cukup geser slider untuk menentukan sendiri, dari 0.1% hingga 100%.

> Tips: setelah Anda menggeser slider, sistem berhenti menimpa pilihan Anda secara otomatis; saran hanya dihitung ulang saat Anda memuat ulang atau memilih trader lagi.

### 2. Leader order size range

Rentang ini diturunkan dari **transaksi tunggal terbesar trader secara historis**, dan secara default berada di bagian tengah (sekitar 5%–95%). Rentang ini menyaring dua jenis order:

| Situasi | Penanganan | Alasan |
|-----------|----------|-----|
| Trader membeli **terlalu sedikit** (di bawah batas bawah) | **Dilewati**, tidak di-copy | "Order debu" ini tidak layak di-copy dan hanya akan memakan Gas |
| Trader membeli **dalam rentang** | Di-copy secara normal sesuai rasio Anda | Ini adalah aktivitas reguler trader |
| Trader membeli **terlalu banyak** (di atas batas atas) | **Tetap di-copy**, tetapi jumlahnya dihitung sebagai "batas atas × rasio Anda" | Mencegah satu taruhan besar sesekali memasukkan seluruh uang Anda |

Halaman ini memiliki preset siap pakai:

| Preset | Arti | Paling cocok untuk |
|--------|---------|----------|
| **All 0–100%** | Tanpa penyaringan sama sekali | Trader yang ukuran ordernya sangat teratur |
| **Balanced 1–99%** | Meng-copy hampir semuanya, hanya menyaring yang ekstrem | **Default, paling cocok untuk pemula** |
| **Core 20–80%** | Hanya meng-copy bagian tengah utama | Lebih konservatif, hanya meng-copy aktivitas inti |

**Contoh resmi**: rentang $200–$800, rasio 10%, trader membeli $5,000 → Anda hanya meng-copy $80.

> Tips: tepat setelah memilih trader, jika belum ada data transaksi historis untuk mereka, halaman akan menampilkan "No cache yet; copying at the default ratio for now, actual amounts will be capped by your balance" (belum ada cache; untuk sementara meng-copy dengan rasio default, jumlah aktual akan dibatasi oleh saldo Anda) — ini normal.

### 3. Slippage tolerance

- Arti: deviasi harga transaksi maksimum yang diizinkan
- Default **15%**, dapat disesuaikan dari 1% hingga 100%
- **Lebih ketat**: lebih mungkin dilewati atau gagal saat harga bergerak
- **Lebih longgar**: lebih mungkin terisi, tetapi mungkin dengan harga yang lebih buruk

> Saat Anda mulai meng-copy dari profil trader, sistem menggunakan hasil "simulasi copy" untuk mengisi slippage dan maksimum pembelian copy terlebih dahulu; halaman akan menampilkan "Pre-filled from copy simulation".

***

## Bagaimana satu trade copy sebenarnya dihitung

Misalkan Anda mengatur: rasio **10%**, rentang **$200–$800**, saldo $1,000.

| Langkah | Deskripsi |
|------|-------------|
| 1. Lihat transaksi trader | Mereka membeli $5,000 |
| 2. Periksa apakah berada dalam rentang | Di atas batas atas $800, jadi **tidak dilewati**, tetapi dihitung dari batas atas |
| 3. Hitung jumlahnya | Ambil yang **lebih kecil** antara "transaksi trader × 10%" dan "batas atas × 10%" = $80 |
| 4. Periksa saldo Anda | Lanjutkan jika saldo ≥ $1; jika tidak cukup, order dengan jumlah yang benar-benar dimungkinkan oleh saldo Anda |
| 5. Genapkan ke minimum | Jika hasilnya di bawah $1, akan **digenapkan menjadi $1** (pembelian minimum di bursa) selama saldo Anda mencukupi |
| 6. Potong Gas | Setelah terisi, sekitar 0.5% dipotong dalam bentuk Gas Platform |

Sekarang kasus di dalam rentang: trader membeli $500 → 500 × 10% = $50, di-copy secara normal sebesar $50.

***

## Kapan trade dilewati

| Pesan di App | Dengan kata sederhana | Apa yang harus dilakukan |
|--------------------|----------------|------------|
| **Outside size band** | Order trader terlalu kecil — order debu | Tidak ada; ini memang dirancang demikian |
| **Insufficient funds** | Saldo tersedia Anda di bawah $1 | Deposit, atau turunkan rasio |
| **Your size < $1** | Terlalu kecil bahkan setelah digenapkan | Naikkan rasio atau turunkan batas atas rentang |
| **Price ≥ $0.85** | Trader membeli hasil yang harganya sudah "hampir pasti" | Tidak ada |
| **Already open (no add-on)** | Anda sudah meng-copy ke pasar ini | Pertahankan default "tidak menambah" atau ubah pengaturan |
| **Slippage too high** | Harga sudah bergerak menjauh | Pertimbangkan untuk melonggarkan slippage |
| **Low Gas** | Gas Platform Anda habis | Isi ulang di [Gas Store](../wallet/gas.md) |

> Catatan: aturan **"di bawah $1 digenapkan menjadi $1"** berlaku di ketiga mode (Ratio, Fixed amount, By balance %). Jadi order di bawah $1 tidak dilewati — order tersebut digenapkan dan di-copy (selama saldo Anda mencukupi).

***

## Dua mode lainnya

### By balance %

- Setiap trade menggunakan **persentase dari saldo USDC tersedia milik Anda sendiri**; misalnya pada 5% dengan saldo $1,000, setiap trade membeli $50
- Saat saldo Anda bertambah, setiap trade ikut membesar secara otomatis; saat saldo menyusut, trade ikut mengecil
- Hasil di bawah $1 juga digenapkan menjadi $1

**Paling cocok untuk**: orang yang ingin ukuran posisi menyesuaikan dengan saldo tanpa harus terus-menerus menyesuaikan jumlah secara manual.

### Fixed amount

- Setiap trade membeli **jumlah yang sama**, misalnya $25 setiap kali
- Minimum $1
- Aturan khusus untuk order kecil: saat jumlahnya di bawah $1, jika **≥ 5 share** order menggunakan jumlah yang Anda tetapkan; jika **di bawah 5 share**, jumlahnya disesuaikan menjadi $1 secara otomatis

**Paling cocok untuk**: trader yang ukuran ordernya cukup konsisten (misalnya sekitar $200 per trade dalam jangka panjang), saat Anda ingin mengontrol biaya setiap trade dengan tepat.

***

## Mana yang sebaiknya saya pilih?

| Situasi Anda | Rekomendasi |
|----------------|----------------|
| Pertama kali, tidak yakin harus memilih apa | **Ratio** (default) |
| Ukuran order trader sangat bervariasi | **Ratio** |
| Anda ingin mengontrol jumlah setiap trade dengan tepat | **Fixed amount** |
| Anda ingin ukuran posisi menyesuaikan dengan saldo Anda | **By balance %** |

***

## FAQ

**Berapa jumlah maksimum yang dapat dikenakan per trade dalam mode Ratio?**

Tidak ada batas per trade yang terpisah — rasio Anda × transaksi trader adalah jumlahnya, tetapi dibatasi oleh "batas atas rentang" dan "saldo Anda". Agar lebih konservatif, turunkan rasio dan batas atas rentang.

**Saya ragu menggunakan rasio yang disarankan secara langsung.**

Anda dapat menggunakannya secara langsung; sistem sudah memperhitungkan "sekitar berapa trade per hari". Agar lebih aman, mulailah aturan kecil dengan rasio yang lebih rendah, amati selama satu atau dua hari apakah ada banyak yang dilewati, lalu tingkatkan secara bertahap.

**Apakah mode Ratio bertentangan dengan "tidak menambah posisi"?**

Tidak. Default "maksimum 1 pembelian copy" (tidak menambah) berarti **pasar yang sama** hanya dibeli sekali; rasio mengatur **berapa banyak yang dibeli dalam satu trade ini**. Untuk menambah posisi, naikkan "Max open copy buys" di pengaturan lanjutan — **maksimumnya adalah All (tanpa batas)**.

**Apakah slippage default di pengaturan 30% atau 15%?**

Sekarang **15%**, dapat disesuaikan dari 1% hingga 100%.

**Apakah ada "Ratio guide" resmi di App juga?**

Ya. Ketuk **Ratio guide** di kanan atas mode Ratio (atau di halaman pengaturan) untuk membukanya. Itu adalah versi rinci milik platform sendiri; halaman ini adalah penjelasan lengkap untuk pemula.

***

## Halaman terkait

- Ikuti langkah demi langkah: [Cara Meng-copy Trader](how-to-follow.md)
- Arti setiap parameter: [Pengaturan Copy](settings.md)
- Cara mengelola setelah mengaktifkan: [Mengelola Copy](managing.md)
- Coba tanpa mengeluarkan uang terlebih dahulu: [Simulasi Copy Trading](simulation.md)
