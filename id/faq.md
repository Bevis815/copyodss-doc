# FAQ

Jika terjadi masalah, periksa halaman ini terlebih dahulu. Jika masih belum bisa diselesaikan, harap siapkan: email terdaftar Anda, waktu tindakan, tangkapan layar error, serta hash transaksi atau ID riwayat trade.

---

## Akun & masuk

### Apakah pengguna baru perlu mendaftar secara terpisah?

Dalam kebanyakan kasus, memasukkan **email baru** di halaman masuk dan menyelesaikan kode verifikasi akan membuat akun secara otomatis. Jika layar masih meminta nama / persetujuan ketentuan, cukup ikuti petunjuknya.

### Tidak menerima kode verifikasi?

Periksa folder spam dan ejaan email Anda; kirim ulang setelah hitung mundur selesai. Server email perusahaan terkadang memblokirnya — coba email pribadi yang sering Anda gunakan.

### Bagaimana jika Passkey gagal?

Masuklah dengan kode email sebagai gantinya; pastikan browser Anda didukung dan Anda tidak menggunakan WebView tertanam yang tidak kompatibel, lalu tambahkan kembali Passkey di Pengaturan.

---

## Penyiapan akun & otorisasi

### Apakah saya perlu mengajukan akun trading?

**Tidak.** Akun biasanya dibuka secara otomatis setelah masuk, sehingga Anda bisa langsung deposit. Dalam kasus langka yang menampilkan "belum dibuka", ketuk untuk membukanya dan setujui perjanjiannya. Lihat [Akun Trading & Status Halaman Dompet](wallet/trading-account.md).

### Halaman dompet menampilkan "Agent authorization" — apakah saya harus membayar gas?

Tidak. Penandatanganan gratis dan platform menanggung biaya on-chain. Anda hanya memerlukan dompet yang Anda gunakan saat mendaftar, yang dialihkan ke **Polygon (chain ID 137)**.

### Apakah "Polymarket trading authorization incomplete" merupakan masalah?

Cukup ketuk **Re-authorize Polymarket**. Ini adalah masalah pada langkah otorisasi dan **tidak memengaruhi dana yang sudah Anda depositkan**.

### Mengapa ada dua angka, "saldo on-chain" dan "saldo tersedia"?

Saldo on-chain adalah USDC native yang benar-benar sudah masuk; saldo tersedia adalah bagian yang sudah diproses dan siap untuk copy. Keduanya mungkin berbeda selama beberapa menit tepat setelah deposit — itu normal.

---

## Deposit & saldo

### Mengapa saldo saya belum diperbarui setelah deposit?

Periksa bahwa: jaringannya adalah **Polygon atau BSC (sesuai dengan halaman)**, asetnya adalah **USDC/USDT**, alamatnya sama persis dengan halaman ini, dan transaksi sudah dikonfirmasi on-chain. BSC mungkin lebih lambat. Muat ulang saldo Anda setelah konfirmasi; jika masih belum masuk, berikan hash transaksinya.

### Bisakah saya deposit USDT?

Bisa, tetapi harus USDT di jaringan yang dipilih pada halaman, dan hanya dikirim ke alamat di halaman ini. Jangan memaksakan penarikan dari jaringan yang salah.

### Apa yang terjadi jika dompet tujuan tidak memiliki MATIC?

Penarikan akan berhasil, tetapi **Anda tidak akan bisa memindahkan USDC tersebut secara on-chain setelahnya**. Simpan sedikit MATIC (POL) di alamat penerima.

### Penarikan menampilkan "channel busy" — apa yang harus saya lakukan?

Tunggu beberapa menit atau jam sesuai petunjuk lalu coba lagi. **Dana Anda aman**, dan Anda tidak perlu mengajukan ulang.

### Tepat setelah masuk, muncul "automatically converting to tradable balance"?

Itu normal. USDC native yang masuk on-chain perlu diproses menjadi saldo yang dapat ditradingkan secara otomatis — tunggu beberapa menit lalu muat ulang.

### Bisakah saya mengonfirmasi penarikan dengan Passkey atau kode email?

**Tidak.** Saat ini penarikan hanya menerima **kode Authenticator**; Passkey dan kode email hanya untuk masuk dan skenario serupa.

### Apakah menonaktifkan Authenticator memerlukan kode?

Ya. Demi keamanan, menonaktifkannya juga memerlukan kode 6 digit. Jika Anda berganti perangkat, lebih mudah untuk langsung menautkan ulang di perangkat baru.

### Mengapa jumlah yang dapat ditarik lebih kecil dari saldo saya?

Posisi dan order terbuka mengikat dana. Ikuti angka **Max withdrawable**.

### Apakah alamat Polygon dan BSC sama?

**Tidak.** Jangan pernah tertukar. Lihat [Jaringan yang Didukung](wallet/supported-networks.md).

---

## Gas & copy

### Apa perbedaan antara Gas Platform dan MATIC / BNB?

Gas Platform adalah kredit biaya layanan CopyOdds yang dibeli dengan USDC di Gas Store. MATIC / BNB adalah token native on-chain yang digunakan untuk biaya jaringan — **keduanya bukan hal yang sama**.

### Mengapa saya tidak bisa menambahkan atau melanjutkan aturan copy?

Alasan paling umum adalah **Gas = 0**. Beli Gas, lalu aktifkan / lanjutkan.

### Berapa banyak USDC yang saya perlukan untuk mulai meng-copy?

Mengaktifkan aturan biasanya hanya memerlukan Gas > 0. Namun setiap pembelian sebenarnya memerlukan sekitar **$1** atau lebih USDC yang tersedia.

### Saya sudah membeli Gas / mendepositkan dana — mengapa masih belum ada pembelian copy?

Saat dana tidak mencukupi, pembelian dilewati tetapi aturan belum tentu dijeda. Setelah mengisi saldo, buka **My copies** dan ketuk **Resume buys** (lanjutkan pembelian). Periksa juga Trade history untuk kegagalan slippage, ketidaksesuaian arah, atau tercapainya batas tidak-menambah-posisi.

---

## Eksekusi copy

### Mengapa beberapa trade tidak di-copy?

Alasan umum: pengaturan arah, jumlah terlalu kecil, batas tidak-menambah-posisi, slippage, USDC/Gas tidak mencukupi, tidak ada share untuk dijual, likuiditas tidak mencukupi. Buka Trade history untuk melihat status spesifiknya.

### Aktivitas copy menunjukkan trader membeli — mengapa saya tidak?

Aktivitas copy ≠ transaksi Anda. Periksa Trade history.

### Trader menjual — mengapa saya tidak?

Anda harus memegang share di pasar tersebut. Jika Anda tidak pernah membeli atau sudah menjual semuanya, penjualan yang dilewati adalah hal normal.

### Apa perbedaan antara menjeda dan menghapus?

Aturan yang dijeda dapat dilanjutkan; aturan yang dihapus harus dibuat ulang. Keduanya tidak menutup posisi Anda secara otomatis.

---

## Penarikan & keamanan

### Mengapa penarikan memerlukan verifikasi tambahan?

Untuk melindungi dana Anda dan mencegah aset dipindahkan langsung jika sesi dibajak. Saat ini penarikan hanya menerima kode **Authenticator**; jika Anda belum menyiapkannya, aktifkan terlebih dahulu di Pengaturan. Passkey dan kode email tidak dapat digunakan untuk penarikan.

### Bisakah Passkey digunakan untuk penarikan?

Tidak. Passkey adalah jalan pintas untuk **masuk**; penarikan hanya menerima kode Authenticator.

### Tidak bisa menarik dana setelah masuk di ponsel baru?

Masa tunggu perangkat baru mungkin terpicu, atau Authenticator belum disiapkan di lingkungan baru. Coba lagi nanti dan periksa manajemen perangkat serta penautan TOTP Anda; hubungi dukungan jika terus gagal.

### Apakah tim resmi akan pernah meminta seed phrase saya?

**Tidak pernah.** Lihat [Anti-Phishing](security/anti-phishing.md).

---

## Smart money

### Apakah papan peringkat menjamin keuntungan?

**Tidak.** Metrik didasarkan pada data publik dan model serta mencakup asumsi simulasi; kinerja masa lalu ≠ imbal hasil masa depan.

### Bagaimana cara membuka profil trader?

`https://app.copyodds.io/@0xADDRESS` (tambahkan `/zh` untuk UI berbahasa Mandarin).

### Apakah "Copy fit / backtest P&L" adalah imbal hasil nyata saya?

Bukan. Sebagian besar merupakan simulasi dengan asumsi penundaan + slippage; hasil aktual Anda ada di Trade history.

---

## Mode copy

### Mode copy apa saja yang tersedia, dan mana yang sebaiknya saya pilih?

**Ratio** (default), **By balance %**, dan **Fixed amount**. Jika ini pertama kalinya, cukup gunakan **Ratio** default: Anda membeli persentase dari apa pun yang dibeli trader, sehingga paling sulit bagi satu taruhan besar mereka untuk menghancurkan akun Anda. Lihat [Tiga Mode Copy](copy-trading/copy-modes.md).

### Apa arti "Ratio"?

Jika trader membeli $5,000 dalam satu trade dan rasio Anda 10%, Anda membeli $500. Rentang rasio adalah 0.1%–100%.

### Untuk apa "Leader order size range" dalam mode Ratio?

Untuk menyaring order debu yang sangat kecil dan order yang terlalu besar. Order di bawah batas bawah dilewati; order di atas batas atas tetap di-copy, tetapi jumlahnya dihitung sebagai "batas atas × rasio", sehingga satu taruhan besar dari trader tidak diperbesar.

### Bisakah saya langsung menggunakan "Suggested ratio" yang diberikan halaman?

Bisa. Nilai ini dihitung sebagai "saldo tersedia Anda ÷ (batas atas rentang × perkiraan jumlah trade trader per hari)", dirancang agar **Anda menggunakan senilai sekitar jumlah trade tersebut dalam sehari**. Turunkan secara manual jika Anda ingin lebih konservatif.

### Mengapa trade saya dilewati dengan "Outside size band"?

Order trader terlalu kecil (di bawah batas bawah rentang). Ini adalah order debu yang sengaja disaring, bukan bug.

### Apa yang terjadi jika jumlah yang dihitung di bawah $1?

Selama saldo Anda mencukupi, sistem secara otomatis **menggenapkannya menjadi $1** (pembelian minimum di bursa) dan menempatkan order alih-alih melewatinya.

### Apakah slippage default 30% atau 15%?

Default di pengaturan copy adalah **15%**, dapat disesuaikan dari 1% hingga 100%.

### Mengapa parameter sudah terisi saat saya meng-copy dari profil trader?

Sistem menggunakan hasil "simulasi copy" untuk mengisi slippage dan maksimum pembelian copy untuk Anda; halaman akan menampilkan "Pre-filled from copy simulation".

---

## Fitur baru

### Apa perbedaan antara Leaderboard dan Smart money?

Leaderboard menampilkan **peringkat profit harian akun copy pool** (halaman beranda); Smart money menampilkan **skor dan profil alamat trader individu**. Untuk memilih trader, gunakan Leaderboard untuk menemukan arah terlebih dahulu, lalu persempit dengan filter Smart money.

### Apakah "Copy activity" dan "Trade history" sama?

Tidak. Copy activity menunjukkan **apa yang dilakukan trader**; Trade history menunjukkan **hasil upaya copy Anda**. Membandingkan keduanya adalah cara termudah untuk menemukan masalah.

### Apakah simulasi copy trading menggunakan uang sungguhan saya?

**Tidak.** Simulasi copy trading berjalan di akun virtual terpisah dan juga tidak memerlukan Gas.

### Mengapa saya tidak bisa menjual posisi saya?

Mungkin statusnya "menunggu penyelesaian" (pasar sudah berakhir dan menunggu diselesaikan), atau mungkin saat ini tidak ada order beli di pasar tersebut. Jika Anda menang, tombol **Redeem** (tukarkan) akan muncul.

### Apakah "Transaction history" di halaman dompet sama dengan menu riwayat trade?

Tidak. **Executions** di menu adalah **riwayat trade copy** Anda; **Transaction history (`/wallets/ledger`)** di dompet adalah **buku besar pergerakan dana dan pengeluaran Gas** Anda.

### Apakah menghapus perangkat di manajemen perangkat akan memengaruhi copy saya?

Tidak akan menghapus aturan copy Anda, tetapi sesi masuk perangkat lama langsung dibatalkan dan perangkat tersebut perlu masuk kembali.

### Apakah komisi di halaman afiliasi selalu 10%?

Tidak. Tingkat komisi Anda bergantung pada **tingkat (tier)** Anda (dari L1 sebesar 10% hingga tingkat teratas). L1 diaktifkan secara otomatis setelah Anda melakukan pembelian, lalu Anda naik tingkat secara otomatis berdasarkan jumlah referral langsung Anda; tingkat teratas harus dibeli.

### Apakah saya harus mengunduh App di ponsel?

Tidak. Versi web memiliki fitur lengkap; untuk pengalaman yang lebih mirip aplikasi, gunakan "Tambahkan ke Layar Utama" di browser Anda. Lihat [Menggunakan CopyOdds di Ponsel](getting-started/mobile-app.md).

---

## Pemberitahuan risiko

- Harga pasar berfluktuasi dan copy trading dapat merugi
- Copy otomatis dapat menyimpang dari trader karena slippage, penundaan, dan likuiditas
- Rantai yang salah, alamat yang salah, atau token yang salah dapat menyebabkan dana tidak masuk atau tidak dapat dipulihkan
- Gas / USDC yang tidak mencukupi menyebabkan pembelian dilewati
- Hasil papan peringkat dan simulasi hanya untuk referensi dan bukan janji imbal hasil

Pengguna baru sebaiknya menjalankan seluruh alur dengan jumlah kecil terlebih dahulu: Deposit → Beli Gas → Copy → Periksa Trade history → Lalu coba penarikan kecil.
