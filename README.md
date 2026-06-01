# JAGO Telekomunikasi

Platform edukatif berbasis web untuk mempelajari **telekomunikasi**, **fiber optik**, dan **konfigurasi FTTH** (Fiber to the Home). Proyek ini dikembangkan sebagai media pembelajaran interaktif bagi siswa/i jurusan **Teknik Transmisi Telekomunikasi** di **SMK Telkom Makassar**.

---

## Daftar Isi

- [Tentang Proyek](#tentang-proyek)
- [Fitur Utama](#fitur-utama)
- [Halaman Website](#halaman-website)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Struktur Proyek](#struktur-proyek)
- [Prasyarat](#prasyarat)
- [Cara Menjalankan](#cara-menjalankan)
- [Aset yang Diperlukan](#aset-yang-diperlukan)
- [Panduan Navigasi](#panduan-navigasi)
- [Pengaturan & Aksesibilitas](#pengaturan--aksesibilitas)
- [Deployment](#deployment)
- [Kontribusi](#kontribusi)
- [Kredit](#kredit)
- [Lisensi](#lisensi)

---

## Tentang Proyek

**JAGO Telekomunikasi** (Telekomunikasi Elite) menghadirkan pengalaman belajar modern melalui antarmuka responsif dengan animasi, tema gelap/terang, dan konten terstruktur tentang:

- Dasar-dasar telekomunikasi dan perannya di era digital
- Prinsip kerja, jenis, dan komponen **fiber optik**
- Arsitektur dan perangkat **FTTH** (OLT, ODC, ODP, ONT, dan lainnya)

Website ini tidak memerlukan backend atau database; seluruh konten disajikan sebagai halaman HTML statis yang dapat dijalankan di browser modern.

---

## Fitur Utama

| Fitur | Deskripsi |
|--------|-----------|
| **Desain responsif** | Tampilan optimal di desktop, tablet, dan ponsel |
| **Tema gelap & terang** | Toggle mode visual melalui panel pengaturan |
| **Animasi partikel** | Latar belakang interaktif berbasis HTML5 Canvas |
| **Animasi scroll (AOS)** | Efek fade saat konten masuk ke viewport |
| **Hero typing effect** | Teks ketik otomatis di halaman beranda |
| **Navbar adaptif** | Menu desktop + hamburger menu untuk mobile |
| **Kursor kustom** | Efek kursor pada perangkat desktop (≥ 998px) |
| **Preloader** | Indikator pemuatan di halaman beranda |
| **Tombol kembali ke atas** | Muncul setelah scroll ke bawah |
| **Progress bar scroll** | Indikator progres membaca halaman |
| **Modal gambar** | Perbesar diagram/gambar (FTTH & Fiber Optik) |
| **Navigasi keyboard** | `Home`, `End`, dan `Esc` untuk navigasi cepat |

---

## Halaman Website

| File | Judul | Konten |
|------|--------|--------|
| `index.html` | Telekomunikasi Elite | Beranda dengan hero section, sambutan, dan CTA ke materi |
| `telecom.html` | Tentang Telekomunikasi | Jurusan TTT, definisi telekomunikasi, pentingnya telekomunikasi |
| `fiber.html` | Fiber Optik | Definisi, ciri-ciri, konektor, cara kerja, kelebihan/kekurangan, jenis SMF/MMF, bagian-bagian kabel |
| `ftth.html` | Konfigurasi FTTH | Pengenalan FTTH, manfaat, diagram konfigurasi, tabel fungsi perangkat (OLT–ONT) |

---

## Teknologi yang Digunakan

- **HTML5** — struktur halaman
- **CSS3** — variabel tema, animasi, layout responsif
- **JavaScript (Vanilla)** — partikel, navigasi, toggle tema, modal
- **[Bootstrap](https://getbootstrap.com/) 5.3.3** — grid, komponen UI, modal
- **[AOS](https://michalsnik.github.io/aos/) 2.3.1** — animasi on scroll
- **[Google Fonts](https://fonts.google.com/)** — Montserrat, Poppins, Fira Code
- **CDN** — jsDelivr, unpkg

Tidak ada proses build, package manager, atau framework JavaScript tambahan.

---

## Struktur Proyek

```
JAGO-TELEKOMUNIKASI/
├── index.html          # Halaman beranda
├── telecom.html        # Materi telekomunikasi
├── fiber.html          # Materi fiber optik
├── ftth.html           # Materi konfigurasi FTTH
├── README.md           # Dokumentasi proyek
│
├── telkom.svg          # Logo SMK Telkom (aset)
├── jago.id2.svg        # Logo JAGO (aset)
├── satelit.png         # Ilustrasi satelit (beranda)
├── contoh.jpg          # Diagram struktur fiber optik
├── IMG_0648.PNG        # Diagram konfigurasi FTTH
└── images-removebg-preview (1).png   # Logo jurusan (telecom)
```

> **Catatan:** Pastikan semua file aset berada di folder yang sama dengan file HTML agar referensi gambar dan logo berfungsi dengan benar.

---

## Prasyarat

- Browser modern (disarankan: **Chrome**, **Firefox**, **Edge**, atau **Safari** versi terbaru)
- Koneksi internet (untuk memuat library CDN dan Google Fonts)
- Opsional: web server lokal untuk pengujian path relatif yang konsisten

---

## Cara Menjalankan

### Opsi 1: Buka langsung di browser

1. Clone atau unduh repositori ini.
2. Buka file `index.html` dengan double-click atau drag ke jendela browser.

### Opsi 2: Live Server (VS Code / Cursor)

1. Pasang ekstensi **Live Server**.
2. Klik kanan `index.html` → **Open with Live Server**.

### Opsi 3: Python HTTP Server

```bash
cd JAGO-TELEKOMUNIKASI
python -m http.server 8080
```

Buka `http://localhost:8080/index.html` di browser.

### Opsi 4: Node.js (npx)

```bash
npx serve .
```

---

## Aset yang Diperlukan

Website mereferensikan aset berikut. Jika file tidak ada, logo atau gambar tidak akan tampil:

| Aset | Digunakan di |
|------|----------------|
| `telkom.svg` | Navbar semua halaman |
| `jago.id2.svg` | Navbar semua halaman |
| `satelit.png` | `index.html` (hero) |
| `images-removebg-preview (1).png` | `telecom.html` |
| `contoh.jpg` | `fiber.html` |
| `IMG_0648.PNG` | `ftth.html` (diagram, dapat diklik untuk modal) |

---

## Panduan Navigasi

Menu utama (semua halaman):

1. **BERANDA** → `index.html`
2. **TENTANG TELEKOMUNIKASI** → `telecom.html`
3. **FIBER OPTIK** → `fiber.html`
4. **KONFIGURASI FTTH** → `ftth.html`

Di halaman beranda, tombol **Jelajahi Sekarang** mengarah ke materi telekomunikasi.

---

## Pengaturan & Aksesibilitas

Panel pengaturan (ikon gear di pojok kanan atas):

- **Mode terang/gelap** — mengubah skema warna seluruh halaman
- **Toggle suara** — UI tersedia; elemen audio perlu ditambahkan jika fitur suara diaktifkan penuh

**Pintasan keyboard:**

| Tombol | Fungsi |
|--------|--------|
| `Home` | Scroll ke atas halaman |
| `End` | Scroll ke bawah halaman |
| `Esc` | Tutup menu mobile / modal gambar |

---

## Deployment

Proyek ini cocok di-host sebagai **static site** pada layanan seperti:

- GitHub Pages
- Netlify
- Vercel
- Shared hosting (cPanel / public_html)

**Perhatian path:** Beberapa tautan di HTML menggunakan prefix `/web/` (misalnya `/web/index.html`). Sesuaikan path tersebut ke struktur folder deployment Anda, atau gunakan path relatif (`index.html`, `telecom.html`, dll.) agar navigasi berfungsi di semua lingkungan.

Contoh struktur di server:

```
/public_html/web/
├── index.html
├── telecom.html
├── fiber.html
├── ftth.html
└── [aset gambar & svg]
```

---

## Kontribusi

Kontribusi untuk perbaikan konten, perbaikan bug, atau peningkatan aksesibilitas sangat diterima. Langkah umum:

1. Fork repositori
2. Buat branch fitur (`git checkout -b fitur/nama-fitur`)
3. Commit perubahan dengan pesan yang jelas
4. Push ke branch dan buat Pull Request

Pastikan perubahan diuji di desktop dan mobile sebelum merge.

---

## Kredit

| Peran | Detail |
|--------|--------|
| **Institusi** | SMK Telkom Makassar |
| **Program keahlian** | Teknik Transmisi Telekomunikasi |
| **Pengembang** | Vinod Jangid |
| **Branding** | JAGO Telekomunikasi / Telekomunikasi Elite |

---

## Lisensi

© 2025 Telekomunikasi Elite — SMK Telkom Makassar.

Hak cipta konten edukatif dan aset visual mengikuti kebijakan institusi pengembang. Untuk penggunaan ulang di luar konteks pembelajaran internal, hubungi pihak SMK Telkom Makassar terlebih dahulu.

---

<p align="center">
  <strong>🚀 Innovation in Telecommunications</strong><br>
  <em>Platform Edukatif — Jaringan, Fiber Optik, dan Teknologi Komunikasi Masa Kini</em>
</p>
