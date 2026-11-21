# 👑 Website Pribadi: Pink Princess

Website portofolio pribadi satu halaman dengan tema **pink princess**. Dibuat hanya dengan **HTML, CSS, dan JavaScript Vanilla**, tanpa framework dan tanpa proses build.

## Isi Folder

```
pink-princess-website/
├── index.html    → struktur dan isi halaman
├── style.css     → tampilan, warna, dan tata letak
├── script.js     → interaksi (menu, mode malam, kilau, formulir)
├── README.md     → panduan ini
└── assets/       → (buat sendiri) taruh foto profilmu di sini
```

## Cara Membuka

1. Unduh dan ekstrak semua file ke satu folder.
2. Klik dua kali `index.html`. Website langsung terbuka di browser.

> Font (Cormorant Garamond dan Quicksand) dimuat dari Google Fonts, jadi butuh koneksi internet. Tanpa internet, website tetap tampil dengan font cadangan.

## Fitur

- Hero dengan **mahkota interaktif**: ketuk mahkota untuk menebar kilau dan memunculkan pesan kecil
- Jejak kilau mengikuti kursor (hanya di perangkat dengan mouse)
- **Mode malam** ("midnight princess") yang tersimpan di browser
- Bar keahlian yang terisi saat di-scroll
- Linimasa perjalanan hidup
- Formulir kontak yang membuka aplikasi email
- Responsif untuk HP, tablet, dan desktop
- Mendukung navigasi keyboard dan menghormati pengaturan "kurangi gerakan" di perangkat

## Cara Mengganti Isi dengan Datamu

Semua teks contoh ada di `index.html`. Cari dan ganti bagian berikut:

| Yang diganti | Cari di `index.html` |
| --- | --- |
| Nama | `Nama Kamu` (muncul di judul tab, logo, hero, footer) |
| Profesi / status | `[profesi atau status kamu]` |
| Kalimat pembuka | paragraf `class="lead"` |
| Cerita tentang diri | bagian `id="tentang"` |
| Asal, kesibukan, suka, impian | daftar `class="facts"` |
| Keahlian dan persentasenya | daftar `class="meters"`. Ubah teks, angka `%`, dan nilai `--level` |
| Hobi | daftar `class="chips"` |
| Perjalanan | daftar `class="timeline"` |
| Link sosial media | daftar `class="links"`. Ganti `usernamekamu` |

Di `script.js`, ubah bagian `CONFIG` paling atas:

```js
const CONFIG = {
  email: "emailkamu@example.com", // email tujuan formulir kontak
  namaKamu: "Nama Kamu",
};
```

## Cara Menambahkan Foto

1. Buat folder bernama `assets` di samping `index.html`.
2. Simpan fotomu sebagai `foto.jpg` di dalamnya (lebih bagus jika berbentuk persegi).
3. Muat ulang halaman. Selama foto belum ada, yang tampil adalah siluet bawaan.

## Cara Mengganti Warna

Buka `style.css` dan ubah variabel di bagian `:root`:

```css
:root {
  --blush: #fff1f6;     /* latar halaman */
  --petal: #ffd6e6;     /* pink lembut untuk hover */
  --rose: #e85d9f;      /* pink utama */
  --raspberry: #b82a73; /* pink tua untuk tombol dan aksen */
  --gold: #c98f3c;      /* emas untuk mahkota dan garis */
  --lilac: #eeddf8;     /* ungu muda untuk bar dan chip */
}
```

Warna mode malam ada di blok `[data-theme="dark"]` tepat di bawahnya.

## Cara Mengunggah ke Internet (Gratis)

- **GitHub Pages**: unggah folder ke repository, lalu aktifkan *Settings → Pages*.
- **Netlify**: buka [app.netlify.com/drop](https://app.netlify.com/drop), lalu seret folder website ke halaman tersebut.
- **Vercel / Cloudflare Pages**: hubungkan repository, tanpa pengaturan build.

## Catatan

- Formulir kontak memakai `mailto:`, jadi pesan dikirim lewat aplikasi email pengunjung dan tidak lewat server. Jika ingin pesan masuk langsung tanpa membuka aplikasi email, kamu bisa memakai layanan formulir seperti Formspree.
- Semua kode diberi komentar agar mudah dipelajari dan diubah.

Selamat berkreasi! 💖
