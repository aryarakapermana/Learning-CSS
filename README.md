# Prompt untuk Antigravity — Praktik Web Design Pertemuan 7

## Peran
Bertindak sebagai web developer dan asisten coding. Baca instruksi ini sampai selesai, lalu periksa file proyek yang sedang terbuka sebelum mengubah apa pun.

## Konteks tugas
Tugas mata kuliah **Web Design — Pertemuan 7: Praktik Styled Web Page**. Buat website **Campus Life**, yaitu portal informasi kegiatan mahasiswa. Fokus tugas adalah menerapkan CSS pada website HTML yang sudah dibuat pada pertemuan sebelumnya.

## Tujuan
- Menghubungkan satu file external CSS bernama `style.css` ke setiap halaman HTML.
- Menggunakan element selector, class, dan ID secara tepat.
- Menerapkan warna, background, typography, border, `border-radius`, margin, dan padding.
- Mengelola cascade, specificity, dan inheritance dengan benar.
- Membangun visual hierarchy, readability, whitespace, dan komponen yang konsisten.
- Memastikan navigasi dan form tetap dapat digunakan setelah styling.

## Instruksi penting
1. **Periksa struktur dan file proyek yang sudah ada terlebih dahulu.** Jika sudah ada website dari pertemuan sebelumnya, lanjutkan dan perbaiki proyek tersebut. Jangan menimpa atau menghapus pekerjaan yang sudah ada tanpa alasan.
2. Pertahankan struktur semantic HTML dan tujuan informasi yang sudah ada. Jangan mengubah tujuan atau isi penting halaman hanya demi desain.
3. Gunakan HTML, CSS, dan JavaScript biasa jika memang diperlukan. Jangan menambahkan framework atau dependency baru kecuali proyek yang ada sudah menggunakannya atau benar-benar diperlukan.
4. Gunakan satu file CSS bersama: `style.css`.
5. Pastikan semua link navigasi mengarah ke nama file yang benar-benar tersedia. Dokumen tugas mencantumkan `index.html`, `registration.html`, `contact.html`, dan `detail.html`, sedangkan contoh navigasi juga menyebut `content.html`. Periksa file yang ada dan konsistenkan tautan dengan halaman yang benar-benar dibuat; jangan biarkan link rusak.
6. Jika tidak ada proyek awal, buat struktur dasar berikut:

```text
web-project/
├── index.html
├── registration.html
├── contact.html
├── detail.html
├── style.css
└── images/
```

Folder `images/` hanya perlu diisi jika gambar digunakan.

## Arahan desain
Buat desain yang modern, rapi, mudah dibaca, ramah mahasiswa, dan responsif untuk desktop maupun ponsel. Gunakan palet warna yang konsisten. Contoh warna awal yang disarankan dari materi:
- Navy: `#1d3557`
- Biru utama: `#2563eb`
- Latar halaman: `#f5f7fa`
- Latar hero: `#eaf2ff`
- Teks utama: `#333333`
- Border netral: `#dddddd`

Warna boleh disesuaikan selama konsisten dan kontras teks tetap baik. Terapkan:
- Header dengan judul **Campus Life** dan tagline **Portal informasi kegiatan mahasiswa**.
- Navigasi yang jelas dengan status hover dan fokus keyboard.
- Area hero berisi judul **Temukan Aktivitas Kampusmu**, deskripsi singkat, dan CTA **Lihat Kegiatan**.
- Bagian **Kegiatan Terbaru**, dengan contoh kartu **Workshop Web Design** dan deskripsi **Pelajari HTML dan CSS untuk membangun website.**
- Card/section yang dapat digunakan ulang.
- Footer dengan teks hak cipta `© 2026 Campus Life`.
- Form registrasi dan/atau kontak yang rapi, memiliki label yang jelas, serta input yang mudah digunakan.
- Tampilan responsif tanpa horizontal overflow pada layar kecil.
- State `hover` dan `focus-visible` yang terlihat untuk link, tombol, dan elemen interaktif.

Jangan menggunakan efek berlebihan yang mengurangi keterbacaan. Jika proyek awal memiliki wireframe atau desain terdahulu, utamakan kesesuaian dengannya.

## Persyaratan teknis CSS
- Gunakan reset/base style secukupnya, `box-sizing: border-box`, font yang mudah dibaca, warna teks, warna latar, dan `line-height`.
- Atur lebar konten utama dengan `max-width` dan margin yang sesuai.
- Gunakan class reusable minimal dua jenis, misalnya `.card` dan `.button`.
- Gunakan ID hanya ketika memang dibutuhkan, bukan untuk setiap elemen.
- Bedakan penggunaan `margin` (jarak di luar elemen) dan `padding` (ruang di dalam elemen).
- Gunakan border dan `border-radius` secara proporsional.
- Pastikan selector sederhana, mudah dipelihara, dan tidak bergantung pada `!important` tanpa alasan kuat.
- Gunakan media query jika diperlukan untuk layout mobile.
- Jangan menghilangkan outline fokus keyboard tanpa menyediakan pengganti yang jelas.
- Hubungkan CSS di dalam `<head>` pada semua halaman, contohnya:

```html
<link rel="stylesheet" href="style.css">
```

## Halaman dan fungsi
### `index.html`
- Halaman utama Campus Life.
- Memuat header, navigasi, hero, kegiatan terbaru, dan footer.
- CTA menuju halaman kegiatan/detail yang benar-benar ada.

### `registration.html`
- Halaman pendaftaran kegiatan mahasiswa.
- Pertahankan atau buat form sederhana yang relevan, dengan label dan input yang sesuai.
- Pastikan tombol submit terlihat dan form bisa diisi. Jangan mengklaim data tersimpan di server jika backend tidak tersedia.

### `contact.html`
- Halaman kontak dengan informasi kontak yang sesuai konteks dan form pesan jika diperlukan.
- Gunakan label input dan tipe input yang tepat.

### `detail.html`
- Halaman detail kegiatan, jika sesuai dengan struktur proyek.
- Tampilkan judul, deskripsi, informasi kegiatan, dan tautan kembali atau daftar kegiatan.
- Jika proyek memakai `content.html` sebagai daftar kegiatan, pertahankan file itu dan tautkan dengan benar; jangan membuat tautan ke halaman yang tidak tersedia.

Jika tugas hanya membutuhkan halaman utama dan minimal satu halaman tambahan, tetap usahakan konsistensi seluruh halaman yang sudah tersedia dalam proyek.

## Starter content referensi
Gunakan konten berikut jika belum tersedia konten yang lebih sesuai di proyek:

```html
<header>
  <h1>Campus Life</h1>
  <p>Portal informasi kegiatan mahasiswa</p>
</header>

<nav aria-label="Navigasi utama">
  <a href="index.html">Home</a>
  <a href="detail.html">Kegiatan</a>
  <a href="contact.html">Kontak</a>
</nav>

<main>
  <section class="hero">
    <h2>Temukan Aktivitas Kampusmu</h2>
    <p>Informasi kegiatan terbaru untuk mahasiswa.</p>
    <a class="button" href="detail.html">Lihat Kegiatan</a>
  </section>

  <section class="content">
    <h2>Kegiatan Terbaru</h2>
    <article class="card">
      <h3>Workshop Web Design</h3>
      <p>Pelajari HTML dan CSS untuk membangun website.</p>
    </article>
  </section>
</main>

<footer>
  <p>&copy; 2026 Campus Life</p>
</footer>
```

Tambahkan metadata responsif pada halaman HTML:

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

## Pemeriksaan cascade dan specificity
Periksa apakah ada aturan CSS yang saling bertentangan. Pastikan hasil akhirnya dapat dijelaskan melalui cascade, specificity, dan inheritance. Rapikan selector agar mudah dipahami; jangan meninggalkan konflik buatan yang merusak desain.

## Checklist sebelum selesai
- [ ] `style.css` terhubung ke semua halaman HTML yang relevan.
- [ ] Element selector, class, dan ID digunakan dengan tepat.
- [ ] Ada minimal dua class reusable untuk komponen berbeda.
- [ ] Warna, background, dan typography konsisten.
- [ ] Border, `border-radius`, margin, dan padding diterapkan secara proporsional.
- [ ] Navigasi memiliki hierarchy yang jelas dan semua tautan berfungsi.
- [ ] Tombol/CTA mudah dikenali dan berfungsi sebagai tautan atau tombol sesuai tujuannya.
- [ ] Form tetap bisa digunakan setelah styling dan memiliki label yang jelas.
- [ ] Hover dan keyboard focus tersedia untuk elemen interaktif.
- [ ] Layout responsif pada desktop dan ponsel.
- [ ] Tidak ada error path file atau tautan ke halaman yang tidak tersedia.
- [ ] Desain tetap sesuai dengan struktur dan wireframe yang tersedia.

## Output yang diminta
Kerjakan langsung di workspace proyek dan hasilkan:
1. File HTML yang diperlukan.
2. File `style.css` bersama.
3. Folder `images/` jika gambar digunakan.
4. Screenshot hasil akhir jika lingkungan kerja memungkinkan.

Setelah selesai, berikan ringkasan:
- File yang dibuat atau diubah.
- Fitur dan styling yang diterapkan.
- Cara menjalankan atau melihat website.
- Hasil checklist dan hal yang belum dapat diverifikasi.

Jangan hanya memberikan contoh atau menjelaskan langkah-langkah. Terapkan perubahan pada file proyek yang ada, lalu periksa kembali tautan, struktur HTML, dan CSS sebelum menyatakan pekerjaan selesai.
