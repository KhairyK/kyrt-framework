# Dokumentasi CSS Framework Kyrt

## 1. Pengantar
Kode CSS ini adalah sebuah framework styling yang dirancang untuk mempermudah pengembangan interface web. Framework ini mendefinisikan:
- **Variabel CSS (Custom Properties)**: Untuk mengelola warna, ukuran, dan efek yang dapat digunakan secara dinamis.
- **Kelas Utility**: Kelas-kelas sederhana untuk styling elemen seperti tombol, teks, layout, animasi, dan komponen UI (seperti navbar, form, modal).
- **Animasi**: Berbagai efek animasi yang dapat diterapkan pada elemen.
- **Responsif Design**: Menggunakan media queries untuk menyesuaikan layout pada berbagai ukuran layar.

Framework ini mirip dengan Tailwind CSS atau Bootstrap, tetapi lebih ringkas dan disesuaikan. Untuk menggunakan kode ini:
- **Instalasi**: Salin kode CSS ke file `.css` (misalnya, `style.css`), lalu link-kan ke file HTML Anda:  
  `<link rel="stylesheet" href="style.css">`.
- **Cara Kerja**: Kelas-kelas diterapkan langsung pada elemen HTML, seperti `<div class="btn-default">Tombol</div>`.

## 2. Struktur Kode
Kode dibagi menjadi beberapa bagian utama:
- **Root dan Variabel CSS**: Mendefinisikan variabel global di `:root`.
- **Kelas Dasar**: Untuk elemen umum seperti tombol, cursor, positioning, display, grid, teks, box, padding, margin, dan animasi.
- **Komponen UI**: Kelas untuk komponen seperti navbar, form (fieldline, searchframe), modal, alert, tooltip, dan tombol khusus.
- **Animasi**: Keyframes dan kelas untuk efek animasi.
- **Responsif**: Media queries untuk ukuran layar (misalnya, mobile dan tablet).
- **Ekstra**: Kelas untuk warna khusus, border, dan font.

## 3. Referensi Lengkap
Berikut adalah daftar rinci dari elemen-elemen dalam kode. Saya mengelompokkannya berdasarkan kategori untuk kemudahan.

### 3.1 Variabel CSS
Variabel ini didefinisikan di `:root` dan dapat digunakan di seluruh stylesheet dengan `var(--nama-variabel)`. Ini membantu dalam menjaga konsistensi dan memudahkan perubahan global.

| Nama Variabel          | Deskripsi                  | Nilai Contoh              |
|------------------------|----------------------------|---------------------------|
| `--kyrt-primary`       | Warna utama (biru)        | `#007bff`                |
| `--kyrt-danger`        | Warna bahaya (merah)      | `#e63946`                |
| `--kyrt-text-white`    | Warna teks putih          | `#fff`                   |
| `--kyrt-radius`        | Radius border default     | `6px`                    |
| `--kyrt-transition`    | Transisi default          | `3s ease`                |
| `--primary`            | Warna primer (biru)       | `#007bff`                |
| `--secondary`          | Warna sekunder (abu)      | `#6c757d`                |
| `--success`            | Warna sukses (hijau)      | `#28a745`                |
| `--danger`             | Warna bahaya (merah)      | `#dc3545`                |
| `--warning`            | Warna peringatan (kuning) | `#ffc107`                |
| `--info`               | Warna info (biru muda)    | `#17a2b8`                |
| `--light`              | Warna latar terang        | `#f8f9fa`                |
| `--dark`               | Warna latar gelap         | `#212529`                |
| `--text-white`         | Warna teks putih          | `#fff`                   |
| `--text-dark`          | Warna teks gelap          | `#111`                   |
| `--radius`             | Radius border alternatif  | `8px`                    |
| `--transition`         | Transisi cepat            | `.3s ease`               |
| `--shadow`             | Bayangan default          | `0 4px 20px #00000026`   |
| `--font-main`          | Font utama                | `Poppins, Roboto, sans-serif` |
| `--bg-body`            | Latar belakang body       | `#fff`                   |
| `--bg-alt`             | Latar belakang alternatif | `#f5f6f8`                |
| `--border`             | Warna border default      | `#0000001a`              |
| `--dark-blue`          | Warna biru gelap          | `#0a0f2c`                |
| `--dark-blue-light`    | Biru gelap terang         | `#162152`                |
| `--dark-blue-accent`   | Biru gelap aksen          | `#1d3eff`                |
| `--neon-purple`        | Ungu neon                 | `#a21cff`                |
| `--neon-purple-light`  | Ungu neon terang          | `#c084fc`                |
| `--neon-purple-accent` | Ungu neon aksen           | `#e879f9`                |
| `--solar-yellow`       | Kuning cerah              | `#ffdb0f`                |
| `--solar-yellow-light` | Kuning cerah terang       | `#ffee6f`                |
| `--solar-yellow-accent`| Kuning cerah aksen        | `#facc15`                |
| `--glow-blue`          | Efek cahaya biru          | `0 0 15px #1d3eff99`     |
| `--glow-purple`        | Efek cahaya ungu          | `0 0 15px #e279f999`     |
| `--glow-yellow`        | Efek cahaya kuning        | `0 0 15px #ffdb0f99`     |

**Contoh Penggunaan:**  
`background-color: var(--kyrt-primary);` untuk mengatur warna latar biru.

### 3.2 Kelas Utility
Kelas-kelas ini untuk styling umum dan dapat dikombinasikan.

- **Tombol (Button):**
  - `.button`: Dasar untuk tombol (padding, border-radius, dll.).
  - `.btn-default`: Tombol biru default.
  - `.btn-red-danger`: Tombol merah untuk bahaya.
  - `.btn-green-success`: Tombol hijau untuk sukses.
  - `.btn-yellow-warning`: Tombol kuning untuk peringatan.
  - `.btn-dark-blue`, `.btn-neon-purple`, `.btn-solar-yellow`: Tombol dengan warna khusus.
  - **Contoh:** `<button class="btn-default">Klik Saya</button>`.

- **Cursor:**
  - `.cursor-pointer`, `.cursor-not-allowed`, dll.: Mengatur cursor mouse.
  - **Contoh:** `<div class="cursor-pointer">Arahkan Kursor</div>`.

- **Positioning:**
  - `.pos-relative`, `.pos-absolute`, `.pos-fixed`, dll.
  - `.top-0`, `.bottom-0`, `.left-0`, `.right-0`, `.pos-center`.
  - **Contoh:** `<div class="pos-absolute top-0 left-0">Posisi Atas Kiri</div>`.

- **Display dan Flexbox:**
  - `.dis-block`, `.dis-flex`, `.dis-none`.
  - `.flex-row`, `.flex-col`, `.justify-center`, `.items-center`.
  - **Contoh:** `<div class="dis-flex justify-center">Elemen Tengah</div>`.

- **Grid:**
  - `.grid`: Membuat grid dasar.
  - `.grid-auto`: Grid responsif.
  - `.col-2`, `.col-3`, dll.: Menentukan span kolom.
  - Responsif: `.col-lg-2` untuk layar besar, `.col-md-2` untuk medium, `.col-sm-2` untuk kecil.
  - **Contoh:** `<div class="grid grid-auto"><div class="col-2">Kolom 2</div></div>`.

- **Text Styling:**
  - `.txt-left`, `.txt-mid`, `.txt-right`.
  - `.txt-thin`, `.txt-bold`, `.txt-italic`.
  - `.txt-xs`, `.txt-lg`, `.txt-red`, `.txt-white`.
  - **Contoh:** `<p class="txt-bold txt-red">Teks Tebal Merah</p>`.

- **Box dan Layout:**
  - `.box-hold`: Container maksimal lebar.
  - `.box-flat`, `.box-float`, `.box-light`, `.box-dark`.
  - `.pad-mid`, `.pad-top`, `.space-bold`, `.space-auto`.
  - **Contoh:** `<div class="box-float pad-mid">Kotak Mengambang</div>`.

- **Bayangan dan Border:**
  - `.box-shadow-sm`, `.shade-bold`.
  - `.box-line`, `.box-edge`, `.box-round`.
  - **Contoh:** `<div class="box-shadow-md">Elemen dengan Bayangan</div>`.

### 3.3 Animasi
Kode ini menyertakan keyframes untuk efek animasi. Kelas-kelas seperti `.anim-fade-in` menerapkan animasi tersebut.

- **Keyframes Utama:**
  - `fadeAppear`, `fadeDisappear`, `floatRise`, `pulseBeat`, `rotateSpin`, dll.
- **Kelas Animasi:**
  - `.anim-fade-in`: Muncul dengan fade.
  - `.anim-spin`: Rotasi terus-menerus.
  - `.anim-slide-up`, `.anim-blink`, `.anim-glow`.
  - **Contoh:** `<div class="anim-fade-in">Elemen Muncul</div>`.

### 3.4 Komponen UI
- **Navbar:** `.navbar`, `.nav-brand`, `.nav-menu`. Responsif untuk mobile.
  - **Contoh:** `<nav class="navbar">...</nav>`.
- **Form Elements:**
  - `.fieldline`: Input dasar.
  - `.searchframe`: Kotak pencarian.
  - **Contoh:** `<input class="fieldline" type="text">`.
- **Modal:** `.modal`, `.modal-box`. Tampilkan dengan kelas `.active`.
  - **Contoh:** `<div class="modal active">...</div>`.
- **Alert:** `.alert-success`, `.alert-danger`.
  - **Contoh:** `<div class="alert-success">Sukses!</div>`.
- **Tooltip:** `.tooltip`, `.tooltip-text`.
  - **Contoh:** `<span class="tooltip">Teks<span class="tooltip-text">Tooltip</span></span>`.

### 3.5 Responsif Design
Menggunakan media queries:
- `@media (max-width: 1024px)`: Untuk layar besar (lg).
- `@media (max-width: 768px)`: Untuk tablet (md).
- `@media (max-width: 480px)`: Untuk mobile (sm).
- **Contoh:** Kelas seperti `.col-lg-2` berubah menjadi `.col-sm-6` pada layar kecil.

## 4. Contoh Penggunaan
Berikut adalah contoh sederhana dalam HTML untuk menerapkan kode ini.

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contoh Kyrt CSS</title>
    <link rel="stylesheet" href="style.css"> <!-- Ganti dengan file CSS Anda -->
</head>
<body class="bg-body">
    <div class="box-hold">
        <h1 class="txt-bold txt-blue">Selamat Datang di Framework Kyrt</h1>
        
        <!-- Tombol -->
        <button class="btn-default anim-fade-in">Tombol Default</button>
        
        <!-- Grid Layout -->
        <div class="grid grid-auto">
            <div class="col-3 box-flat">Kolom 1</div>
            <div class="col-3 box-flat anim-pulse">Kolom 2</div>
        </div>
        
        <!-- Form -->
        <input class="fieldline" type="text" placeholder="Masukkan teks">
        
        <!-- Navbar -->
        <nav class="navbar">
            <div class="nav-brand">Kyrt</div>
            <div class="nav-menu">
                <a href="#">Home</a>
                <a href="#">About</a>
            </div>
        </nav>
    </div>
</body>
</html>
```

## 5. Catatan Penting
- **Kustomisasi**: Anda bisa mengubah variabel di `:root` untuk menyesuaikan tema.
- **Kompatibilitas**: Pastikan browser mendukung CSS variables dan animasi (sebagian besar browser modern sudah support).
- **Lisensi**: Kode ini tampaknya original; gunakan sesuai kebutuhan Anda.
- **Peningkatan**: Jika Anda ingin menambahkan lebih banyak fitur, pertimbangkan untuk memisahkan kode menjadi modul (misalnya, file terpisah untuk animasi).
