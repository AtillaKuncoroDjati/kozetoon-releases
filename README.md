# KOZETOON — Unduhan Android

Rilis stabil, 11 Oktober 2026. Android 7.0+ ARM64; x86_64 untuk emulator.
Kode sumber tetap private. APK dan panduan tersedia melalui kanal distribusi
publik terpisah.

**[Unduh APK 1.1.0](https://github.com/AtillaKuncoroDjati/kozetoon-releases/releases/download/v1.1.0/KOZETOON-1.1.0-local.apk)**

## Perubahan versi ini

**Tampilan pembuka baru — versi tetap 1.1.0, build 19:**

- **Pembuka edisi 1.1:** tumpukan poster Manga, Manhwa dan Manhua, monogram K
  besar, aksen ungu, garis panel komik dan
  tulisan “Cerita baru. Dunia baru.”. Logo masuk dengan gerakan halus, disertai
  detail sayap K dan garis loading yang bergerak selama aplikasi menyiapkan data.
- Tampilan muncul sejak awal APK menyiapkan katalog, kemudian memudar ke Home
  ketika halaman siap. Tidak ada persentase palsu atau durasi tunggu minimum
  untuk memperpanjang loading. Sembilan thumbnail lokal berjumlah **410.250 byte
  (sekitar 400 KB)**; background tidak mengunduh poster atau membaca seluruh
  katalog saat aplikasi dibuka. Bagian tengah digelapkan agar logo tetap jelas.
- Background Android disiapkan di latar belakang dengan gambar yang diperkecil,
  lalu digabung menjadi satu bitmap sekitar 680 KB. WebView tidak memuat salinan
  poster kedua. Background dilepas setelah transisi selesai.
- Layar pembuka bawaan Android 12 ke atas juga memakai background gelap dan logo KOZETOON
  yang serasi dengan tampilan aplikasi.
- Tata letak menyesuaikan layar kecil dan landscape. Animasi dijeda saat aplikasi
  tidak terlihat, dihentikan setelah pembuka selesai, dan menghormati pengaturan
  perangkat untuk mengurangi/menonaktifkan animasi.

**Perbaikan sebelumnya pada 11 Oktober 2026 — build 18:**

- **Progres akhir chapter diperbaiki:** membaca sampai gambar terakhir kini
  tercatat penuh, misalnya **26 dari 26** atau **17 dari 17**. Sebelumnya, gambar
  terakhir yang pendek sudah terlihat seluruhnya, tetapi penghitung masih
  mengikuti halaman sebelumnya di bagian atas layar.
- Status selesai hanya dicatat setelah gambar terakhir berhasil dimuat dan
  bagian bawahnya terlihat. Gambar yang masih memuat/gagal dan gambar panjang
  yang belum mencapai akhir tidak ditandai selesai. Menggulir melewati gambar
  ke tombol chapter berikutnya tetap mempertahankan progres penuh.
- Halaman terakhir dan penanda selesai disimpan untuk Home, Library, daftar
  chapter, pembukaan ulang aplikasi serta backup memori lokal.

Untuk riwayat lama yang masih **25/26** atau **16/17**, buka kembali chapter
tersebut setelah memasang APK terbaru dan gulir sampai gambar terakhir selesai
dimuat. Progres diperbarui otomatis; tidak perlu menghapus riwayat atau backup.
Posisi yang belum benar-benar selesai tetap dipertahankan.

**Penyempurnaan sebelumnya pada 11 Oktober 2026 — build 17:**

- **Banner Cerita pilihan benar-benar bergeser** mengikuti swipe kiri/kanan,
  dengan transisi 420 ms dan pergantian otomatis setiap 5 detik. Tombol panah
  serta tombol titik untuk berpindah banner dihapus; indikator posisi tetap ada.
  Pergantian dijeda ketika banner di luar layar, aplikasi di latar belakang atau
  dialog terbuka. Gerakan vertikal tetap menggulir halaman.
- **Penanda bacaan pada daftar chapter:** hijau dengan tanda centang untuk
  chapter selesai dibaca, ungu dengan tulisan **Terakhir dibaca** untuk posisi
  terakhir. Reader menampilkan **Sedang dibaca** pada chapter yang sedang dibuka.
  Penanda memakai riwayat tersimpan sehingga tetap ada setelah aplikasi dibuka lagi.
- **Pemeriksaan katalog lebih ringan:** indeks terbaru dibandingkan dengan ID
  chapter yang sudah tersimpan. Cerita yang chapter terbarunya sudah ada tidak
  diambil ulang hanya karena ada perbedaan metadata sampul/sinopsis. Manifest
  gambar yang sudah siap dipertahankan; hanya chapter yang belum siap diambil.
- Pemeriksaan mengikuti daftar yang diurutkan dari update terbaru, berhenti pada
  halaman yang seluruh chapter terbarunya sudah dikenal. Antrean perubahan yang
  belum selesai disimpan sebelum pengambilan detail dan dilanjutkan dari antrean
  tersebut pada batch berikutnya. Pemeriksaan ringan tidak menampilkan spinner
  pengambilan chapter, dan membuka ulang aplikasi tidak melewati jeda pemeriksaan.

Fitur 1.1.0 berikut tetap tersedia:

- **Memori lokal otomatis** di Documents/KOZETOON, tanpa akun Google: bookmark,
  riwayat, posisi di dalam gambar, chapter selesai dibaca, profil dan pengaturan.
- **Salinan katalog terakhir** ikut disimpan: judul, metadata, daftar chapter,
  tanggal rilis dan alamat gambar yang sudah dikumpulkan. Setelah reinstall,
  hasil pengumpulan yang ada di backup dapat dipulihkan bersama simpanan pribadi.
- **Tanggal pada daftar chapter**, termasuk pemilih chapter di reader: baru saja,
  menit/jam/hari lalu untuk tujuh hari terakhir, kemudian tanggal. Jika sumber
  tidak memberikan tanggal, aplikasi menjelaskannya; waktu tidak dikarang.
- **Cek chapter otomatis** ketika aplikasi dibuka/kembali aktif. Bookmark dan
  riwayat diprioritaskan; hasil batch sebelumnya tetap disimpan.
- **Posisi baca lebih tepat**, sampai proporsi di dalam gambar panjang. Pemulihan
  menunggu gambar siap; gerakan pembaca menghentikan penyesuaian otomatis.
- **Keterangan proses lebih mudah dipahami**, seperti “Menyiapkan chapter baru
  agar siap dibaca”, tanpa alamat URL atau nama sumber dalam status update.
- **Updater APK aktif kembali** memakai kanal publik khusus unduhan. Keterangan
  perubahan tampil langsung di aplikasi; unduhan diperiksa sebelum pemasangan.

Home, rekomendasi geser, pilihan grid/daftar, pencarian langsung, filter beberapa
genre, fullscreen, auto-scroll, Library, download offline, crop profil, Clear cache,
safe area Android dan tarik untuk refresh tetap tersedia. Tombol Edit cerita
tidak ditampilkan pada detail bacaan. Tidak ada login atau backup Google Drive.

## Memasang pembaruan

Unduh APK dan pilih **Update**, menimpa aplikasi lama. Package `id.kozetoon.local`
dan sertifikat tetap sama; versionCode 19. Seed awal tidak menimpa database lama.
**Jangan uninstall dahulu** agar katalog terbaru, Library dan offline tetap ada.
Sediakan sedikitnya 1 GB ruang kosong untuk operasi katalog dan backup.

APK 1.0.7 lama masih memakai alamat repository sebelumnya yang kini private.
Pengguna versi tersebut perlu memasang 1.1.0 dari tautan di atas sekali. Setelah
memakai versi ini, update berikutnya bisa diperiksa melalui **Kelola → Versi aplikasi**.
Versi beta sebelumnya juga dapat ditimpa APK stabil ini tanpa menghapus aplikasi.

Jika **1.1.0 build 16, 17 atau 18** sudah terpasang, unduh APK dari tautan di atas lalu pilih
**Update** sekali lagi. Nama versi tetap sama, sehingga updater build lama tidak
menawarkan perbaikan ini hanya berdasarkan nama versi. APK terbaru memakai build
19 agar Android mengenalinya sebagai pembaruan. Build sebelumnya diarsipkan dengan
nama file yang menyebut nomor build; pilih file utama `KOZETOON-1.1.0-local.apk`.

## Mengaktifkan dan memastikan backup

1. Buka **Kelola → Memori KOZETOON → Pilih folder memori**.
2. Pilih **Documents / Dokumen** dan berikan akses. Aplikasi membuat subfolder
   KOZETOON; memilih folder KOZETOON yang sudah ada juga diperbolehkan.
3. Tunggu sampai proses selesai. Pastikan **Terakhir disimpan** dan
   **Katalog dicadangkan** menampilkan tanggal berhasil.
4. Jika folder sudah terhubung dari beta, pasang 1.1.0 menimpa versi tersebut,
   lalu tekan **Cadangkan sekarang** dan tunggu kedua tanggal diperbarui.

Folder tersebut menyimpan:

| File | Isi |
| --- | --- |
| `kozetoon-memory.json` | Simpanan pribadi terbaru, maksimal 8 MiB. |
| `kozetoon-memory.previous.json` | Simpanan pribadi valid sebelumnya. |
| `kozetoon-catalog.jsonl.gz` | Katalog terakhir, daftar chapter dan alamat gambar. |
| `kozetoon-catalog.previous.jsonl.gz` | Salinan katalog valid sebelumnya. |

Setelah folder terhubung, perubahan pribadi dicadangkan otomatis setelah jeda
singkat. Katalog dicadangkan ketika berubah dan pemeriksaan chapter sudah tidak
berjalan. Tombol **Cadangkan sekarang** meminta keduanya. Penulisan katalog besar
berjalan di latar belakang, sehingga halaman aplikasi tetap dapat digunakan.
Proses dapat memakan waktu; tunggu status selesai sebelum menutup paksa aplikasi.
Storage penuh, izin dicabut atau force stop dapat menggagalkan backup.

Backup lama yang hanya memiliki file JSON belum menyimpan seluruh katalog.
File katalog baru harus dibuat dari aplikasi yang masih memiliki hasil update
sebelum uninstall. Menginstal 1.1.0 setelah data lama hilang tidak dapat mengambil
kembali hasil yang belum pernah dicadangkan.

Katalog contoh 1.572 judul / 149.626 chapter menghasilkan arsip sekitar **97 MiB**.
Salinan sebelumnya membutuhkan ruang tambahan yang sebanding. Ukuran berbeda
tergantung isi katalog; arsip dibatasi 512 MiB. Pemulihan membutuhkan sedikitnya
512 MiB ruang sementara di penyimpanan aplikasi.

File lokal tidak dienkripsi. Orang yang memperoleh file memori dapat membaca
profil dan riwayatnya. Jangan membagikan folder backup pribadi. Tidak ada unggahan
cloud; pengguna memilih sendiri lokasi folder melalui pemilih Android.

## Setelah uninstall atau Hapus data

File di Documents berada di luar data aplikasi. Uninstall/Hapus data Android
tidak dimaksudkan menghapus file tersebut, tetapi akses folder aplikasi hilang.
**Pilih lagi folder yang sama satu kali** setelah install ulang. Pemulihan tidak
bisa berjalan tanpa pemberian akses ini.

- Jika data pribadi aplikasi masih kosong, backup valid dipulihkan otomatis.
- Jika sudah ada simpanan pribadi, pilih **Pulihkan dan gabungkan**. Bookmark dan
  catatan selesai baca digabung; riwayat yang lebih baru di HP dipertahankan.
- **Gunakan simpanan HP** mengganti backup utama dengan data HP setelah pilihan
  dikonfirmasi. Salinan valid sebelumnya dipertahankan jika tersedia.

Format, ukuran, checksum, identitas chapter, relasi dan alamat gambar diperiksa
sebelum katalog digabungkan. File rusak ditolak; salinan valid sebelumnya dicoba.
Katalog HP yang lebih baru dan alamat gambar yang masih siap tetap dipertahankan.
Kegagalan salinan katalog dilaporkan terpisah agar simpanan pribadi valid masih
dapat dipulihkan. Selalu periksa status kedua jenis backup.

**Pemulihan mengembalikan kondisi saat backup terakhir.** Jika baru memasang lagi
setahun kemudian, chapter yang telah tersimpan tidak perlu dikumpulkan ulang.
Chapter yang terbit sesudah backup tetap perlu diperiksa lewat internet, secara
bertahap dari data terbaru. Proses bukan pengulangan scraping untuk setiap hari.
Ketersediaan gambar tetap bergantung pada alamat yang masih berlaku di sumber.

Gambar chapter offline, APK, cache dan data proses updater tidak masuk backup.
Gambar offline perlu diunduh ulang setelah uninstall/Hapus data. Menghapus folder
Documents/KOZETOON atau reset perangkat dapat menghapus backup itu sendiri.

## Chapter terbaru dan cara membaca

Home menampilkan Update terbaru dengan filter jenis yang tetap berada di Home,
pilihan dua kolom/daftar dan tiga chapter terakhir. Rekomendasi bisa digeser.
Jelajahi menyediakan pencarian langsung, jenis cerita dan beberapa genre.
Library memuat bookmark, riwayat dan progres; tab Offline mengelompokkan download
per cerita dengan ringkasan ruang penyimpanan. Batas gambar offline adalah 1 GB.

Ketuk gambar saat membaca untuk menyembunyikan/menampilkan kontrol. Gunakan daftar
chapter untuk berpindah, tombol putar untuk auto-scroll, dan pengaturan untuk
mengubah kecepatan. Posisi baca disimpan saat membaca; **Lanjut baca** membuka
kembali posisi tersimpan. Clear cache di Kelola hanya membersihkan cache sementara,
tanpa sengaja menghapus Library, katalog, profil atau file offline.

**Cek chapter otomatis** aktif secara default, dengan jeda normal enam jam.
Tarik layar dari posisi paling atas lalu lepaskan, atau tekan **Cek chapter baru**
di Home / **Update katalog** di Kelola untuk cek manual. Jeda manual 60 detik;
hasil parsial atau proses yang terjeda karena aplikasi masuk latar belakang bisa
dilanjutkan setelah 30 menit, kegagalan setelah 15 menit. Membuka aplikasi kembali
tidak memulai ulang pengambilan data ketika jeda tersebut belum terpenuhi.

Satu sesi dibatasi tiga batch, masing-masing hingga 20 metadata judul, 100
manifest chapter dan 180 detik. Pembacaan tersimpan diprioritaskan. Backlog besar
bisa memerlukan lebih dari satu sesi; status menjelaskan pekerjaan tersisa.
Masuk latar belakang menjeda pemeriksaan; jeda manual tidak dilanjutkan otomatis.
Pemeriksaan tidak mengunduh semua gambar offline secara otomatis.

## Update APK berikutnya

**Kelola → Versi aplikasi → Cek update → Unduh update → Pasang update**.
Catatan perubahan tersedia di aplikasi. APK diperiksa ukuran, SHA-256, package,
versionCode dan sertifikat sebelum Android meminta konfirmasi pemasangan.
Pembaca tidak perlu menavigasi repository kode di GitHub. Update versi aplikasi
dan pemeriksaan chapter terbaru merupakan dua proses yang terpisah.

## Validasi rilis

Build 19: **90 tes lulus**, yaitu 64 JavaScript dan 26 Java. Lint Android selesai
tanpa error. Tes pembuka memeriksa transisi, timer cadangan, pengurangan animasi,
pelepasan guliran halaman dan pencegahan pembuka berjalan ulang pada navigasi.
Preview pembuka diperiksa pada 320 × 568, 393 × 851 dan landscape 851 × 393 px;
Home, guliran dan pencarian dapat dipakai setelah pembuka selesai. Kode backend
pribadi/katalog tidak berubah pada build ini.

Build 18: **121 tes lulus**, yaitu 65 Python Android dan 56 JavaScript. Regresi
mencakup gambar terakhir pendek/panjang, akhir canvas/footer, gambar belum siap,
pembukaan ulang posisi selesai, Home/Library dan round-trip backup penanda selesai.
Pada build 17 sebelumnya, 110 tes sumber/CLI (termasuk 25 tes pembaruan katalog)
dan 26 tes Java juga lulus; kode sumber/Java tersebut tidak berubah pada build 18.
Lint Android build 17: 0 error / 7 warning. APK, modul backup, seed, aset UI, versi dan
sertifikat diperiksa. Seed tidak berisi bookmark/akun pribadi website.

Backup katalog asli 1.572 judul / 149.626 chapter diverifikasi dan dipulihkan,
termasuk alamat gambar bertanda tangan dan integritas relasi database. Tes
mencakup file rusak, batas ukuran, relasi yang salah, pemulihan data yang belum
ada pada seed serta pelestarian riwayat/katalog HP yang lebih baru.

Preview daftar chapter dan memori diperiksa pada lebar 320 dan 393 px. Banner
diuji dengan gerakan geser nyata di browser; seluruh slide tetap berada dalam
satu layout, dan perpindahan memakai transform, bukan pergantian display. Tes
timer, wrap, jeda, resize dan pembatalan gesture lulus. Tes katalog memastikan
chapter yang sudah ada tidak diminta ulang, antrean bertahan setelah reopen,
dan pembukaan ulang aplikasi menghormati jeda. Backup
pribadi beta sebelumnya telah dilaporkan berhasil oleh pengguna di HP. **Bagian
backup katalog baru diuji di PC; pemulihan melalui pemilih folder Android pada
perangkat fisik belum diverifikasi untuk rilis ini.** Perbaikan progres build 18
diverifikasi pada reader asli Chapter 98 melalui preview mobile 393 px: gambar
terakhir pendek tercatat 26/26 di Home. Uji ini dilakukan di PC; pengujian fisik
pada HP pengguna masih diperlukan. Tampilan native pembuka build 19 dikompilasi
dan diperiksa lint; penilaian animasinya di perangkat fisik masih perlu dilakukan.

Ukuran APK: **136.565.004 byte**.

SHA-256:
`1e79b286d703c87a91d59f8bd533109dc4de23ab86020abf3b5190095eb85df9`

![Preview daftar chapter dengan tanggal](https://github.com/AtillaKuncoroDjati/kozetoon-releases/releases/download/v1.1.0/apk-chapter-dates-110.jpg)

![Banner swipe tanpa tombol pindah](https://github.com/AtillaKuncoroDjati/kozetoon-releases/releases/download/v1.1.0/apk-hero-swipe-110.jpg)

![Penanda selesai dan terakhir dibaca](https://github.com/AtillaKuncoroDjati/kozetoon-releases/releases/download/v1.1.0/apk-read-markers-110.jpg)

![Progres halaman terakhir tersimpan penuh](https://github.com/AtillaKuncoroDjati/kozetoon-releases/releases/download/v1.1.0/apk-reader-complete-110.png)

![Pembuka KOZETOON edisi 1.1](https://github.com/AtillaKuncoroDjati/kozetoon-releases/releases/download/v1.1.0/apk-launch-110.png)
