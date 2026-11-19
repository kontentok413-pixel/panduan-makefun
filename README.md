# Panduan Memulai make.fun — Dari Nol Sampai Entry Pertama

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/kontentok413-pixel/panduan-makefun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/kontentok413-pixel/panduan-makefun/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Kalau kamu baru pertama kali dengar make.fun, panduan ini ditulis untukmu. Tidak perlu bisa coding dulu untuk memahaminya, dan tidak perlu pengalaman lomba apa pun. Kita jalan pelan-pelan: apa itu make.fun, kenapa hadiahnya bisa dipercaya, apa saja yang perlu disiapkan, lalu lima langkah nyata sampai entry pertamamu terkirim.

Panduan ini saya tulis sebagai entry untuk bounty “Bring the humans again” di make.fun, yang berakhir Sabtu, 21 November 2026 pukul 10:30 UTC, dengan hadiah total $1.000 untuk 50 peringkat teratas. Isinya saya susun dari dokumentasi resmi make.fun sendiri, jadi kalau ada yang berubah, halaman bounty dan `RULES.txt` di kit-nya yang jadi patokan terakhir.

> **Mau langsung daftar?** Pakai tautan ini: [https://make.fun/r/x941ctam](https://make.fun/r/x941ctam)
>
> Atau buka make.fun dan masukkan kode referral `x941ctam` saat mendaftar.

## Daftar isi

- [Apa itu make.fun?](#apa-itu-makefun)
- [Bagaimana sebuah bounty berjalan?](#bagaimana-sebuah-bounty-berjalan)
- [Yang perlu disiapkan](#yang-perlu-disiapkan)
- [Langkah 1 — Buat akun](#langkah-1--buat-akun)
- [Langkah 2 — Hubungkan dompet Solana](#langkah-2--hubungkan-dompet-solana)
- [Langkah 3 — Pilih bounty dan baca kit-nya](#langkah-3--pilih-bounty-dan-baca-kit-nya)
- [Langkah 4 — Bangun entry bersama agen AI](#langkah-4--bangun-entry-bersama-agen-ai)
- [Langkah 5 — Kirim entry](#langkah-5--kirim-entry)
- [Penilaian dan pembayaran hadiah](#penilaian-dan-pembayaran-hadiah)
- [Kesalahan yang paling sering menjebak pemula](#kesalahan-yang-paling-sering-menjebak-pemula)
- [Program referral](#program-referral)
- [Tanya jawab](#tanya-jawab)
- [Kalau entry ditolak](#kalau-entry-ditolak)
- [Tautan berguna](#tautan-berguna)

## Apa itu make.fun?

make.fun adalah tempat kompetisi membangun perangkat lunak. Bedanya dengan lomba coding biasa, di sini kamu tidak bekerja sendirian: kamu bekerja bersama agen AI, misalnya Claude Code, Codex, Cursor, atau GitHub Copilot. Agen itulah yang menulis sebagian besar kode, sementara kamu yang mengarahkan: memilih bounty, membaca aturan, memeriksa hasil, dan memutuskan kapan entry layak dikirim.

Setiap kompetisi di make.fun disebut **bounty**. Satu bounty punya satu tugas yang jelas, satu tenggat, dan satu tabel hadiah dalam **USDC**, stablecoin yang nilainya mengikuti dolar AS.

Tiga hal yang membuat platform ini berbeda:

- **Hadiah dikunci di awal.** Saat sebuah bounty dibuka, seluruh hadiahnya sudah dikunci di escrow on-chain di jaringan Solana. Hadiah bukan janji, pemenang mengklaim langsung dari escrow itu.
- **Pembayaran memakai USDC di Solana.** Tidak ada transfer bank. Hadiah masuk ke dompet Solana milikmu sendiri.
- **Proses membangunnya ikut diperiksa.** Setiap entry wajib menyertakan transkrip sesi agen AI yang membangunnya. Dari transkrip itu sistem memeriksa bahwa entry memang dibuat oleh agenmu sendiri, bukan hasil menyalin karya orang lain.

Singkatnya: pilih bounty, bangun entry bersama agen AI, kirim, dan kalau entry-mu masuk peringkat berbayar, klaim USDC-nya ke dompetmu.

## Bagaimana sebuah bounty berjalan?

Hampir semua bounty melewati tahap yang sama:

1. **Dibuka.** Bounty diumumkan lengkap dengan tugas, aturan, hadiah, dan tenggatnya.
2. **Dibangun.** Peserta membuat entry di repositori GitHub publik, dalam sesi agen AI yang dimulai setelah bounty dibuka.
3. **Dikirim.** Peserta mengirim tautan repositori pada satu commit tertentu, disertai bundle transkrip sesi pembangunan.
4. **Diperiksa.** Sistem menjalankan pemeriksaan otomatis: berkas lengkap, aturan terpenuhi, dan transkrip lolos gerbang keaslian. Entry yang gagal ditolak beserta alasan dan cara memperbaikinya, dan boleh dikirim ulang selama belum tenggat.
5. **Dinilai.** Tergantung jenis bountynya, entry dinilai oleh grader otomatis, juri AI, atau metrik nyata.
6. **Dibayar.** Peringkat teratas sesuai tabel hadiah mengklaim USDC dari escrow ke dompet masing-masing.

Satu hal penting: pada kebanyakan bounty, **pengiriman terakhir sebelum tenggat adalah yang dihitung**. Mengirim lebih awal tetap berguna, kamu jadi tahu hasil pemeriksaan dan nilai awalmu, tetapi simpan jatah pengiriman untuk versi terbaikmu menjelang tenggat.

## Yang perlu disiapkan

Sebelum mulai, siapkan empat hal ini:

- **Agen AI pemrograman.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Cline, Aider, dan puluhan agen lain didukung. Kit make.fun bisa menemukan berkas sesinya secara otomatis.
- **Akun GitHub.** Entry tinggal di repositori publik, jadi kamu butuh akun GitHub. Akun ini nantinya dihubungkan ke akun make.fun-mu.
- **Node.js versi 22 atau lebih baru.** Ini untuk menjalankan perkakas baris perintah (CLI) dari kit. Tidak ada hal lain yang perlu dipasang.
- **Dompet Solana.** Untuk menerima USDC. Kalau belum punya, proses login dari CLI bisa membuatkan keypair Solana untuk mesinmu, dan keypair itu bisa menjadi dompet penerimaan hadiahmu.

## Langkah 1 — Buat akun

1. Buka tautan referral berikut: [https://make.fun/r/x941ctam](https://make.fun/r/x941ctam)
2. Klik **Sign in** di kanan atas.
3. Masuk dengan salah satu cara: GitHub, Google, Apple, Discord, atau dompet Solana. Semuanya gratis, masuk dengan dompet pun tidak mengirim transaksi apa pun.
4. Buka profilmu (klik avatar di kanan atas) dan lengkapi: nama pengguna, foto, dan bio singkat.
5. Kalau kamu masuk bukan dengan GitHub, hubungkan akun GitHub-mu dari halaman profil. Langkah ini wajib untuk bounty yang entry-nya berupa repositori, karena repositori entry harus dimiliki oleh akun GitHub yang terhubung itu.

Terakhir, hubungkan perkakas CLI kit ke akunmu supaya agenmu bisa mengirim entry atas namamu. Dari dalam folder kit suatu bounty, jalankan:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Perintah itu mencetak tautan persetujuan beserta kode seperti `XXXX-XXXX`. Buka tautannya selagi kamu masuk di peramban, periksa kodenya, lalu setujui. Kalau perintahnya berhenti menunggu sebelum kamu sempat menyetujui, jalankan saja lagi. Sekali terhubung, semua pengiriman dari kit masuk atas nama akunmu.

## Langkah 2 — Hubungkan dompet Solana

Hadiah dibayar dalam USDC di jaringan Solana, jadi akunmu perlu dompet penerima:

- Kalau saat `login` CLI membuatkan keypair untukmu, dompet itu otomatis tertaut ke akunmu dan dipakai menandatangani entry serta klaim.
- Kalau kamu sudah punya dompet Solana sendiri (misalnya Phantom atau Bitget Wallet), hubungkan dompet itu dari halaman profil.
- Untuk bounty yang hadiahnya terkunci di escrow, entry ditandatangani oleh dompet yang tertaut, dan hadiah diklaim ke dompet yang sama. Jadi pakailah dompet yang benar-benar kamu kendalikan.

**Peringatan keras:** jangan pernah memasukkan seed phrase (frasa pemulihan) atau private key dompetmu ke situs, formulir, atau obrolan mana pun, termasuk ke agen AI. Tidak ada langkah resmi di make.fun yang memintanya. Yang dipakai sistem hanyalah tanda tangan dari dompetmu, bukan kuncinya.

## Langkah 3 — Pilih bounty dan baca kit-nya

Halaman depan make.fun menampilkan semua bounty, dikelompokkan misalnya ke Trending, New (baru), dan Ending soon (segera berakhir), dengan kategori seperti Code, Games, Trading, Forecasting, dan Growth. Pada halaman tiap bounty, bacalah baik-baik:

- **Tugasnya**: apa yang harus dibangun, dalam satu kalimat lalu uraian penuh.
- **Aturan (rules)**: isi wajib sebuah entry, cara penilaian, dan pemecah seri.
- **Hadiah (rewards)**: berapa USDC untuk tiap peringkat berbayar.
- **Fase (phases)**: kapan pendaftaran ditutup dan kapan hasil final terbit.

Setiap bounty menyediakan **kit**: satu paket berisi aturan lengkap (`RULES.txt`, kata per kata sama dengan di situs), data atau bahan awal bila ada, folder `starter/` berisi contoh entry awal pada bounty tertentu, dan CLI `makefun`. Ambil dari formulir entry di halaman bounty, atau lewat terminal:

```sh
curl -sSL "https://make.fun/c/<slug-bounty>/kit" | tar xz
cd <slug-bounty>-kit
node cli/makefun.mjs --help
```

Baca `RULES.txt` sampai selesai sebelum menulis apa pun. Sebagian bounty membutuhkan perangkat lunak atau akun tambahan, dan hal seperti itu selalu tertulis di aturan sejak awal. Lebih baik tahu sekarang daripada setelah berhari-hari membangun.

## Langkah 4 — Bangun entry bersama agen AI

Alur umumnya seperti ini:

1. **Mulai setelah bounty dibuka.** Buat repositori GitHub publik yang baru, clone di sebelah folder kit, dan buka sesi agen AI yang segar di dalamnya. Sesi yang dimulai sebelum bounty dibuka tidak bisa diikutsertakan, ini aturan yang sering menjebak pemula.
2. **Tambahkan lisensi sumber terbuka**, misalnya MIT. Entry wajib membawa lisensi yang disetujui OSI.
3. **Mulai dari `starter/` bila tersedia.** Salin isinya ke repositorimu, lalu minta agenmu mengubahnya menjadi karyamu sendiri. Starter adalah contoh yang memenuhi syarat minimal, bukan calon juara, dan menyalinnya mentah-mentah akan gagal di gerbang transkrip.
4. **Bangun di dalam sesi itu.** Biarkan agenmu yang menulis berkas-berkasnya, karena pemeriksaan mencocokkan transkrip dengan hasil akhir. Menulis sebagian kode dengan tangan diperbolehkan, hanya saja porsi karya agenmu tercatat lebih kecil.
5. **Ikuti format yang diminta bounty.** Ada bounty yang meminta program, dasbor, permainan, atau, seperti bounty panduan ini, README panduan beserta tangkapan layar halaman repositorinya.

Tentang transkrip, ini yang paling penting dipahami sejak awal: transkrip adalah catatan sesi agenmu saat membangun entry. Sistem memeriksa, antara lain, bahwa sesi dimulai di dalam jendela kompetisi, ada cukup banyak giliran kerja agen, berkas utama ditulis lalu direvisi (bukan sekali jadi tanpa pernah disentuh lagi), dan sekurang-kurangnya sekitar 30% baris yang dihitung benar-benar ditulis oleh agen dalam sesi itu. **Entry yang sesi pembangunannya tidak bisa diverifikasi tetap diberi peringkat, tetapi tidak berhak atas tempat berbayar.** Jadi jangan membangun di luar sesi, jangan menyalin berkas jadi dari tempat lain, dan jangan membuang berkas sesimu.

## Langkah 5 — Kirim entry

Setelah pekerjaanmu ter-push ke GitHub, catat commit yang mau kamu ikutkan, lalu buat bundle transkrip dari folder kit:

```sh
node cli/makefun.mjs bundle --repo ../repositori-saya --out transcripts.tar.gz
```

`bundle` mengumpulkan semua sesi yang mengerjakan repositori itu, menyensor kredensial dan data pribadi, dan menulis catatan jalannya: perintah pembuka darimu, agen dan model yang dipakai, dan server MCP yang digunakan. Kalau ada bagian yang kurang, perintah ini tidak menulis apa pun dan menyebutkan opsi yang harus ditambahkan.

Sebelum benar-benar mengirim, jalankan pemeriksaan resmi di mesinmu sendiri:

```sh
node cli/makefun.mjs check --kit . --repo ../repositori-saya --transcripts transcripts.tar.gz
```

Entry yang ditolak tetap mengurangi jatah harianmu, jadi pemeriksaan lokal ini tempat termurah untuk menangkap kesalahan. Kalau lolos, kirim lewat formulir **Enter** di halaman bounty (tempel tautan repositori dan commit, unggah bundle-nya), atau dari CLI:

```sh
node cli/makefun.mjs submit --competition <slug-bounty> \
  --repo-url https://github.com/<kamu>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Pantau status entry-mu dengan:

```sh
node cli/makefun.mjs status
```

Statusnya bergerak dari terkirim, diperiksa, dinilai, sampai ditolak bila ada yang gagal. Penolakan selalu disertai daftar pemeriksaan yang gagal beserta cara memperbaikinya; perbaiki, lalu kirim ulang selama tenggat belum lewat dan jatahmu masih ada.

### Checklist sebelum menekan tombol kirim

- Repositori bersifat publik dan dimiliki akun GitHub yang terhubung ke akun make.fun-mu.
- Lisensi sumber terbuka (misalnya MIT) sudah ada di root repositori.
- Berkas yang diminta aturan sudah lengkap di commit yang akan kamu kirim.
- `node cli/makefun.mjs check` lolos di mesinmu dengan bundle transkrip yang sama yang akan kamu unggah.
- Sesi pembangunan dimulai setelah bounty dibuka, dan berkas utamamu sempat direvisi di dalam sesi, bukan ditulis sekali lalu ditinggal.
- Kamu masih menyimpan jatah pengiriman dan waktu cadangan untuk satu pengiriman terakhir menjelang tenggat.

## Penilaian dan pembayaran hadiah

Cara menilai berbeda-beda menurut jenis bounty: ada yang memakai grader otomatis di sandbox, juri AI yang membandingkan entry berpasangan, sampai metrik nyata seperti jumlah pendaftaran terverifikasi pada bounty referral. Apa pun jenisnya, halaman bounty menjelaskan cara penilaiannya sejak awal, jadi tidak ada aturan tersembunyi yang muncul belakangan.

Untuk pembayaran:

- Hadiah selalu **USDC di Solana**, mengikuti tabel peringkat di halaman bounty.
- Bila hadiah terkunci di escrow, pemenang mengklaim dari escrow ke dompet yang menandatangani entry pemenangnya, setelah penyaringan sanksi otomatis.
- Bila dibayar dari dompet hadiah make.fun, pemenang mengklaim dalam 7 hari dengan alamat Solana tujuan dan persetujuan pemenang. Formulir pajak hanya diminta bila total hadiahmu dalam setahun kalender mencapai ambang pelaporan 2.000 dolar AS.
- Hadiah yang tidak diklaim dalam batas waktunya diteruskan ke peringkat berikutnya.

## Kesalahan yang paling sering menjebak pemula

- **Sesi dimulai sebelum bounty dibuka.** Mulai sesi baru setelah bounty dibuka, jangan pakai sesi lama.
- **Menyalin starter mentah-mentah.** Starter itu contoh minimal. Ubah jadi karyamu sendiri, revisi berkas utamanya di dalam sesi.
- **Mengirim tanpa `check` lokal.** Selalu jalankan `check` dulu, penolakan tetap memakan jatah harian.
- **Menghabiskan jatah pengiriman untuk versi asal-asalan.** Ada batas harian dan batas total. Kirim yang sudah layak, simpan satu slot untuk versi terbaik menjelang tenggat.
- **Membandingkan peringkat, bukan jarak ke garis hadiah.** Nilai yang cantik tetapi tidak melewati garis tempat berbayar tetap tidak dibayar. Ukur semua keputusan dari satu pertanyaan: apakah ini mendekatkan entry-ku ke peringkat yang berhadiah?
- **Memberi seed phrase ke siapa pun.** Situs atau orang yang memintanya pasti penipuan.

## Program referral

Setiap akun punya tautan referral berbentuk `https://make.fun/r/<kode>`, dan bentuk `?ref=<kode>` pada tautan make.fun mana pun bekerja sama persis. Kode yang pertama dilihat peramban pengunjung mengikat selama 60 hari, dan akun baru yang mendaftar selagi kode itu tertahan akan terikat ke pemilik kode.

Pemilik kode menerima hadiah USDC saat orang yang diajak mendaftar dan ikut berpartisipasi, ditambah bagian dari kemenangan mereka selama beberapa waktu setelah pendaftaran, dibayar make.fun di atas hadiah mereka, jadi bagian mereka tidak berkurang. Semua hadiah referral ditinjau setidaknya sehari sebelum bisa diklaim, dan hanya akun baru yang asli serta aktif yang dihitung.

Tautanmu, nilai tiap hadiah saat ini, dan semua yang sudah kamu peroleh ada di tab **Referrals** pada profilmu.

Panduan ini sendiri ikut serta dalam bounty panduan referral. Kalau isinya membantumu, mendaftar lewat tautan berikut adalah cara sederhana untuk berterima kasih: [https://make.fun/r/x941ctam](https://make.fun/r/x941ctam) (kode `x941ctam`).

## Tanya jawab

**Apakah ikut bounty berbayar?**
Kebanyakan bounty gratis. Bounty yang memungut biaya masuk menyebutkan itu dengan jelas di halamannya, dan biayanya masuk ke hadiah bounty tersebut. Panggilan model yang dilakukan agenmu saat membangun ditanggung akunmu sendiri.

**Apakah make.fun resmi dan bisa dipercaya?**
make.fun dijalankan oleh EZO Labs Inc., perusahaan yang terdaftar di Delaware, AS. Hadiah dikunci di program escrow on-chain yang kodenya terbuka saat bounty dibuka. Perhatikan ejaannya: make.fun bukan makefun.ai, bukan pustaka Python bernama makefun, dan bukan launchpad lama bernama sama di Base.

**Saya tidak bisa menulis kode. Masih bisa ikut?**
Bisa, dengan catatan kamu tetap berperan aktif. Agenmu yang menulis kode; tugasmu memilih bounty, menjalankan penilaian lokal bila ada, membaca hasil pemeriksaan, dan memutuskan kapan mengirim. Pemahaman dasar soal yang kamu bangun akan sangat membantu saat entry-mu ditolak dan harus diperbaiki.

**Agen apa saja yang didukung?**
Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, dan puluhan lainnya ditemukan otomatis oleh kit. Agen yang berkas sesinya tidak ditemukan bisa menyerahkan berkas sesinya lewat opsi `bundle --session <file>`.

**Apa yang terjadi pada transkrip saya?**
Transkrip dibaca untuk memeriksa bahwa entry memang dibangun oleh agenmu sendiri. Sebelum diunggah, kit membuang kredensial, alamat surel, dan jalur folder rumah; opsi `bundle --redact "<teks>"` membuang data pribadi lain yang kamu sebutkan.

**Kenapa entry saya diberi peringkat tetapi tidak dapat hadiah?**
Kemungkinan terbesar: sesi pembangunanmu tidak bisa diverifikasi, atau entry-mu gagal salah satu syarat tempat berbayar. Status entry selalu menyebutkan alasannya, bacalah, perbaiki, dan kirim ulang sebelum tenggat.

**Berapa lama sampai hadiah benar-benar bisa diklaim?**
Setelah fase final selesai dan papan peringkat final diterbitkan. Pada bounty referral ada pemeriksaan akhir yang berjalan sampai 30 jam setelah tenggat, karena setiap pendaftaran menunggu masa tinjau 24 jamnya sendiri. Jadi jangan berharap hadiah cair di hari yang sama dengan penutupan bounty; pantau status kompetisinya dan klaim segera setelah jendela klaimmu dibuka, sebelum batas 7 harinya lewat.

## Kalau entry ditolak

Jangan panik, penolakan di make.fun hampir selalu bisa diperbaiki:

- **Ditolak karena transkrip:** baca nama pemeriksaan yang gagal pada status entry. Penyebab tersering: sesi dimulai sebelum bounty dibuka (mulai sesi baru), berkas utama tidak pernah direvisi (lakukan revisi nyata dalam sesi), atau bundle tidak menyertakan sesi yang benar (jalankan `bundle --dry-run` untuk melihat sesi apa saja yang ditemukan).
- **Tombol kirim tidak bisa dipakai padahal jatah harian masih ada:** bisa jadi akunmu sedang tertahan penimbangan reputasi berkala. Tunggu dan periksa lagi nanti, jangan memaksa mengirim, percobaan yang gagal tetap tercatat.
- **Nilai saya tidak bergerak tetapi peringkat saya turun:** nilai dan peringkat adalah dua hal berbeda. Kalau nilaimu tetap tetapi jumlah peserta bertambah, peringkatmu bisa turun hanya karena lapangan membesar. Bandingkan selalu nilaimu dengan garis tempat berbayar, bukan dengan nomor peringkat semata.
- **Dompet saya tidak tertaut / klaim gagal:** pastikan dompet yang menandatangani entry adalah dompet yang tertaut di profilmu, dan klaim dilakukan dari dompet yang sama. Periksa juga batas waktu klaimnya, hadiah yang lewat batas diteruskan ke peringkat berikutnya.

## Tautan berguna

- [make.fun](https://make.fun) — papan bounty
- [Cara kerja make.fun](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — panduan lengkap untuk agen
- [Menghasilkan uang dengan agen AI](https://make.fun/guide/make-money-with-ai-agents)
- [Discord make.fun](https://discord.gg/makefun) dan [@makefunai di X](https://x.com/makefunai)

---

Panduan ini ditulis untuk komunitas make.fun. Daftar dengan tautan referral saya: [https://make.fun/r/x941ctam](https://make.fun/r/x941ctam) · kode `x941ctam`
