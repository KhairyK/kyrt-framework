## 🧱 1. Root Variables (`:root{...}`)

Semua variabel global yang dipakai di seluruh framework kamu:

```css
:root {
  --kyrt-primary: #007bff;
  --kyrt-danger: #e63946;
  --kyrt-text-white: #fff;
  --kyrt-radius: 6px;
  --kyrt-transition: 3s ease;
  --primary: #007bff;
  --secondary: #6c757d;
  --success: #28a745;
  --danger: #dc3545;
  --warning: #ffc107;
  --info: #17a2b8;
  --light: #f8f9fa;
  --dark: #212529;
  --shadow: 0 4px 20px #00000026;
  ...
}
```

### Fungsi:

Semacam *“config pusat”* buat semua elemen.
Kalau nanti ganti warna utama framework, tinggal ubah `--kyrt-primary`, langsung keubah semua tombol, border, dan elemen lain yang pakai variabel itu.

---

## 🎨 2. Reset & Global Style

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", "Roboto", sans-serif;
}
```

### Fungsi:

Reset semua elemen agar:

* Tidak ada margin/padding bawaan browser.
* Font default jadi “Poppins / Roboto”.
* Ukuran elemen konsisten dengan `box-sizing: border-box`.

---

## 🔘 3. Buttons (`.button`, `.btn-*`)

Kelas tombol utama KYRT.

Contoh:

```css
.button {
  display: inline-block;
  font-weight: 600;
  padding: 10px 18px;
  border-radius: var(--kyrt-radius);
  border: none;
  cursor: pointer;
  transition: var(--kyrt-transition);
}
```

Lalu ada variasi:

* `.btn-default` → tombol biru utama
* `.btn-red-danger` → tombol merah error
* `.btn-green-success` → tombol hijau sukses
* `.btn-yellow-warning` → tombol kuning peringatan

Ada juga efek `:hover`, `:active`, dan animasi `@keyframes kyrt-blink`.

---

## 🖱️ 4. Cursor Utilities

```css
.cursor-pointer { cursor: pointer; }
.cursor-wait { cursor: wait; }
.cursor-not-allowed { cursor: not-allowed; }
```

### Fungsi:

Utility cepat buat ganti bentuk kursor.

---

## 📐 5. Position & Z-Index Utilities

```css
.pos-relative { position: relative; }
.pos-absolute { position: absolute; }
.top-0 { top: 0; }
.left-0 { left: 0; }
.z-100 { z-index: 100; }
```

### Fungsi:

Utility positioning (buat layout cepat tanpa harus nulis CSS tambahan).

---

## 🧩 6. Display & Flex/Grid Utilities

```css
.dis-flex { display: flex; }
.justify-center { justify-content: center; }
.items-center { align-items: center; }
.grid { display: grid; gap: 1rem; }
.grid-auto { grid-template-columns: repeat(auto-fit,minmax(180px,1fr)); }
```

### Fungsi:

Memudahkan layouting responsif (Flexbox & Grid system mirip Bootstrap).

---

## 🅰️ 7. Text Utilities

```css
.txt-center { text-align: center; }
.txt-bold { font-weight: 700; }
.txt-red { color: #e53935; }
.txt-glow { text-shadow: 0 0 6px #fffc; }
```

### Fungsi:

Utility text lengkap — dari warna, gaya, ukuran, spacing, sampai efek glow/shadow.

---

## 📦 8. Box Utilities

```css
.box-hold { width:100%; max-width:1200px; margin:auto; padding:20px; }
.box-flat { background:#fff; border-radius:6px; padding:15px; box-shadow:0 0 2px #0001; }
.box-float:hover { transform:translateY(-5px); }
```

### Fungsi:

Untuk membuat container & card dengan mudah.

---

## 💡 9. Animation Section (`@keyframes` + `.anim-*`)

Ada **lebih dari 40 animasi** di sini 😳
Contoh:

* `fadeAppear`, `fadeDisappear`
* `floatRise`
* `pulseBeat`
* `shakeFast`
* `slideUp`, `slideDown`, `slideLeft`, `slideRight`
* `twistIn`, `flipFront`, `zoomAppear`, dll.

### Fungsi:

Bisa dipanggil langsung lewat class:

```html
<div class="anim-fade-in"></div>
<div class="anim-spin"></div>
<div class="anim-glow"></div>
```

---

## 🧭 10. Navbar System

```css
.navbar {
  display:flex;
  align-items:center;
  justify-content:space-between;
  background:#0f0f10;
  color:#fff;
  padding:12px 24px;
}
.nav-menu a::after {
  content:"";
  position:absolute;
  bottom:-5px;
  height:2px;
  background:#00d4ff;
  transition:.3s;
}
```

### Fungsi:

Navbar responsif dengan:

* `.nav-toggle` untuk menu hamburger.
* `.nav-menu.show` aktif saat tampilan mobile.

---

## 🔍 11. Form Components (Field & Search)

```css
.fieldline {
  padding:10px 14px;
  border:1px solid #cfcfcf;
  border-radius:6px;
  transition:.3s;
}
.fieldline:focus {
  border-color:#0d6efd;
  box-shadow:0 0 0 3px #0d6efd33;
}
```

Ada juga varian:

* `.fielddark` (tema gelap)
* `.fielderror`, `.fieldokay`
* `.fieldglass` (efek blur transparan)
* `.fieldicon` (input + icon)
* `.fielddisable` (nonaktif)

Dan komponen `searchframe` untuk bar pencarian siap pakai.

---

## 🧊 12. Icon System

```css
.icon-home {
  background: url(/svg_icon/home-icon.svg) no-repeat center/cover;
}
```

### Fungsi:

Sistem ikon berbasis `mask` dan SVG (mirip Material Icons tapi lokal).

---

## 🪟 13. Modal System

```css
.modal {
  position:fixed;
  top:0; left:0;
  width:100%; height:100%;
  display:flex; justify-content:center; align-items:center;
  background:#0009; backdrop-filter:blur(6px);
  opacity:0; visibility:hidden;
  transition:.3s;
}
.modal.active {
  opacity:1; visibility:visible;
}
.modal-box {
  background:#fff; border-radius:12px; padding:25px;
  animation:pop .3s ease;
}
```

### Fungsi:

Komponen modal siap pakai dengan animasi pop-up halus.

---

## 🧯 14. Alerts (Belum selesai di potonganmu)

Mulai dengan:

```css
.alert {
  padding:12px 16px;
  border-radius:8px;
  font-weight:500;
  animation:fadeIn .3s ease;
}
.alert-success { background:#d1fae5; color:#065f... }
```

### Fungsi:

Notifikasi warna-warni seperti success, warning, danger, info.

---

## ✨ Kesimpulan Struktur KYRT v1.1

| Bagian     | Fungsi              | Contoh Class                      |
| ---------- | ------------------- | --------------------------------- |
| Root Vars  | Warna & tema global | `--kyrt-primary`                  |
| Buttons    | Tombol interaktif   | `.btn-default`, `.btn-red-danger` |
| Cursor     | Ubah pointer        | `.cursor-wait`                    |
| Layout     | Posisi & grid       | `.dis-flex`, `.col-6`             |
| Typography | Text styling        | `.txt-bold`, `.txt-center`        |
| Box        | Container/card      | `.box-flat`, `.box-float`         |
| Animation  | Efek visual         | `.anim-glow`, `.anim-fade-in`     |
| Navbar     | Navigasi responsif  | `.navbar`, `.nav-toggle`          |
| Forms      | Input siap pakai    | `.fieldline`, `.searchframe`      |
| Modal      | Popup overlay       | `.modal.active`                   |
| Alerts     | Notifikasi          | `.alert-success`                  |

## Silakan Copy/Paste Ke File HTML Kalian Dan Jalankan

```html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KYRT Framework Demo</title>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/KhairyK/kyrt-framework/kyrt.min.css" type="text/css" media="all" />
</head>
<body class="bg-body font-arial">

<!-- ===== Navbar ===== -->
<nav class="navbar">
  <div class="nav-brand">KYRT Demo</div>
  <div class="nav-toggle" id="navToggle">
    <span></span>
    <span></span>
    <span></span>
  </div>
  <div class="nav-menu" id="navMenu">
    <a href="#">Beranda</a>
    <a href="#">Fitur</a>
    <a href="#">Tentang</a>
    <a href="#">Kontak</a>
  </div>
</nav>

<!-- ===== Buttons ===== -->
<section class="box-hold pad-mid">
  <h2>Tombol</h2>
  <button class="button btn-default">Default</button>
  <button class="button btn-red-danger">Danger</button>
  <button class="button btn-green-success">Success</button>
  <button class="button btn-yellow-warning">Warning</button>
  <button class="button btn-dark-blue">Dark Blue</button>
  <button class="button btn-neon-purple">Neon Purple</button>
  <button class="button btn-solar-yellow">Solar Yellow</button>
</section>

<!-- ===== Input Fields ===== -->
<section class="box-hold pad-mid">
  <h2>Input</h2>
  <input class="fieldline" placeholder="Field line normal"><br><br>
  <input class="fieldglass" placeholder="Glass effect"><br><br>
  <input class="fielddark" placeholder="Dark input"><br><br>
  <input class="fielderror" placeholder="Error"><br><br>
  <input class="fieldokay" placeholder="Success">
</section>

<!-- ===== Alerts ===== -->
<section class="box-hold pad-mid">
  <h2>Alert</h2>
  <div class="alert alert-success">Sukses: Operasi berhasil!</div>
  <div class="alert alert-warning">Peringatan: Periksa input!</div>
  <div class="alert alert-danger">Error: Terjadi kesalahan!</div>
  <div class="alert alert-info">Info: Ini hanya informasi.</div>
</section>

<!-- ===== Tooltip ===== -->
<section class="box-hold pad-mid">
  <h2>Tooltip</h2>
  <span class="tooltip">Hover aku
    <span class="tooltip-text">Ini tooltip text!</span>
  </span>
</section>

<!-- ===== Modal ===== -->
<section class="box-hold pad-mid">
  <h2>Modal</h2>
  <button class="button btn-default" id="openModal">Buka Modal</button>

  <div class="modal" id="myModal">
    <div class="modal-box">
      <h3>Ini Modal</h3>
      <p>Ini konten modal menggunakan KYRT CSS.</p>
      <button class="button btn-red-danger" id="closeModal">Tutup</button>
    </div>
  </div>
</section>

<!-- ===== Scripts ===== -->
<script>
// Navbar toggle
const navToggle = document.getElementById('navToggle');
const navMenu = document.getElementById('navMenu');
navToggle.addEventListener('click', () => {
  navToggle.classList.toggle('active');
  navMenu.classList.toggle('show');
});

// Modal
const modal = document.getElementById('myModal');
document.getElementById('openModal').onclick = () => modal.classList.add('active');
document.getElementById('closeModal').onclick = () => modal.classList.remove('active');
modal.onclick = (e) => { if(e.target===modal) modal.classList.remove('active'); };
</script>

</body>
</html>
```