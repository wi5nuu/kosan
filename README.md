# Al'ashar Kos – Website Kosan Modern

Website resmi Al'ashar Kos yang dibangun dengan **Astro** untuk performa super cepat, desain modern, dan fitur booking langsung ke WhatsApp.

---

## 📋 Syarat Sebelum Mulai

Pastikan Anda sudah menginstal hal berikut di komputer Anda:

| Kebutuhan | Versi | Cara Cek |
|---|---|---|
| **Node.js** | 18 atau lebih tinggi | Buka terminal → ketik `node --version` |
| **npm** | Sudah termasuk dengan Node.js | Buka terminal → ketik `npm --version` |

### Cara Instal Node.js (jika belum ada)

1. Buka browser Anda dan pergi ke **https://nodejs.org**
2. Klik tombol **"Download"** yang berwarna hijau (versi LTS / Long Term Support)
3. Jalankan installer yang terunduh dan ikuti langkah-langkahnya sampai selesai
4. Buka terminal baru dan verifikasi dengan mengetik:
   ```
   node --version
   ```
   Hasilnya akan seperti: `v20.x.x` (angka bisa berbeda)

---

## 🚀 Cara Mulai (Dari Nol – Copy Paste Saja)

### Langkah 1 – Unduh / Clone Proyek

Salin folder proyek `alashar-kos` ke komputer Anda, lalu buka **terminal** (Windows: PowerShell / Command Prompt, Mac/Linux: Terminal) dan navigasi ke folder proyek:

```bash
cd alashar-kos
```

> **Tips:** Di Windows bisa ketik `cd ` lalu drag & drop folder ke terminal dan Enter.

---

### Langkah 2 – Instal Dependencies (Paket npm)

Jalankan perintah ini untuk mengunduh semua paket yang dibutuhkan:

```bash
npm install
```

Tunggu sampai selesai. Anda akan melihat folder `node_modules` dan file `package-lock.json` baru muncul. **Jangan hapus kedua hal tersebut.**

---

### Langkah 3 – Jalankan Server Development (Local)

```bash
npm run dev
```

Setelah beberapa detik, Anda akan melihat pesan seperti:

```
   astro  v5.x.x started in XXXms

  ┌─────────────────────────────────┐
  │  localhost:4321  → Buka di browser  │
  └─────────────────────────────────┘
```

Buka browser Anda dan pergi ke **http://localhost:4321**

🎉 **Website sudah berjalan!**

---

### Langkah 4 – Build untuk Production (Deploy)

Ketika Anda sudah siap untuk deploy ke server / hosting:

```bash
npm run build
```

Ini akan membuat folder **`dist/`** yang berisi semua file statis yang siap di-upload ke hosting manapun (Vercel, Netlify, Shared Hosting, dll).

---

### Langkah 5 – Preview Build (Opsional)

Untuk melihat hasil build secara lokal sebelum deploy:

```bash
npm run preview
```

---

## 📁 Struktur Folder Proyek

```
alashar-kos/
├── src/
│   ├── components/          # Komponen-komponen website
│   │   ├── Navbar.astro     # Navigation bar (fixed, blur on scroll)
│   │   ├── Hero.astro       # Seksi hero / banner utama
│   │   ├── About.astro      # Seksi tentang kosan
│   │   ├── Facilities.astro # Seksi fasilitas (9 kartu)
│   │   ├── Gallery.astro    # Galeri foto (grid masonry)
│   │   ├── Pricing.astro    # Paket harga (3 tier)
│   │   ├── Location.astro   # Seksi lokasi + peta ilustrasi
│   │   ├── CTA.astro        # Banner CTA (Call to Action)
│   │   └── Footer.astro     # Footer dengan info kontak
│   ├── layouts/
│   │   └── Layout.astro     # Layout utama (global styles, scroll animation, WhatsApp float)
│   └── pages/
│       └── index.astro      # Halaman utama (assembles semua komponen)
├── astro.config.mjs         # Konfigurasi Astro
├── package.json             # Deskripsi proyek & scripts
├── tsconfig.json            # Konfigurasi TypeScript
└── README.md                # File ini
```

---

## ✏️ Cara Mengedit Konten

Semua konten ada di folder **`src/components/`**. Buka file `.astro` yang sesuai:

| Ingin Edit Apa | Buka File |
|---|---|
| Nama kosan / tagline utama | `Hero.astro` |
| Deskripsi & info tentang | `About.astro` |
| Fasilitas & deskripsinya | `Facilities.astro` |
| Foto galeri / label | `Gallery.astro` |
| Harga & paket | `Pricing.astro` |
| Alamat & lokasi | `Location.astro` |
| Nomor WhatsApp | Cari `08139488240` di file manapun |

---

## 📸 Mengganti Foto

Saat ini foto menggunakan **ilustrasi SVG placeholder**. Untuk mengganti dengan foto nyata:

1. Simpan foto Anda di folder `src/` (misal: `src/images/foto-eksterior.jpg`)
2. Di komponen yang ingin diubah, ganti tag `<svg>` dengan tag `<img>`:
   ```html
   <img src="../images/foto-eksterior.jpg" alt="Eksterior Al'ashar Kos" class="img-placeholder" />
   ```
3. Pastikan foto Anda rasio ukurannya sesuai agar terlihat bagus (landscape untuk hero, portrait untuk galeri kecil).

---

## 🌐 Deploy ke Internet

### Vercel (Rekomendasi – Gratis)
1. Buka **https://vercel.com** dan buat akun
2. Klik **"New Project"** → Upload folder proyek atau connect dari GitHub
3. Pilih framework: **Astro**
4. Klik **Deploy** → Website Anda langsung online!

### Netlify (Alternatif – Gratis)
1. Buka **https://netlify.com** dan buat akun
2. Klik **"New Site"** → Drag & drop folder `dist/` atau connect dari GitHub
3. Selesai!

---

## 📱 Fitur Website

- ✅ **Super cepat** – Astro menghasilkan HTML statis (zero JS di browser)
- ✅ **Animasi scroll** – Reveal animation saat scroll menggunakan Intersection Observer
- ✅ **Booking WhatsApp** – Semua tombol booking langsung ke nomor WhatsApp Anda
- ✅ **Responsive** – Tampilan sempurna di HP, tablet, dan desktop
- ✅ **Navbar blur** – Navbar menjadi frosted glass saat di-scroll
- ✅ **WhatsApp float button** – Tombol WhatsApp mengambang di sudut kanan bawah
- ✅ **Galeri foto** – Grid masonry dengan hover overlay
- ✅ **Peta lokasi** – Ilustrasi peta interaktif dengan pin lokasi
- ✅ **3 paket harga** – Basic, Premium, Elite dengan highlight "Paling Populer"

---

## 📞 Kontak Pemilik

- **WhatsApp:** +62 813-9488-240
- **Nama Kosan:** Al'ashar Kos
