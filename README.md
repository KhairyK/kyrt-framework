
````markdown
# KYRT Framework

**Write Less, Style More.**  
KYRT adalah mini CSS framework futuristik buatan **Sholehuddin Khairy**, dirancang agar developer bisa membuat tampilan web modern hanya dengan sedikit kode. Framework ini ringan, cepat, dan kaya fitur utility seperti Tailwind — tapi tetap punya sentuhan khas KYRT.

---

## 🚀 Fitur Utama

- 🎨 **Design System Modern** — menggunakan variabel CSS global seperti `--kyrt-primary`, `--kyrt-danger`, `--bg-alt`, dan banyak lagi.
- ⚡ **Utility Classes Lengkap** — mulai dari layout, typography, grid, animasi, hingga efek glow & shadow.
- 🧩 **Komponen Siap Pakai** — tombol, navbar, alert, field input, modal, dan search bar.
- 🌙 **Mode Gelap & Transparan (Glass UI)** — tinggal tambahkan kelas seperti `.searchglass` atau `.fieldglass`.
- 💫 **Animasi Built-in** — fade, slide, bounce, glow, shimmer, twist, flip, dan lain-lain.

---

## 📦 Instalasi

Kamu bisa pakai KYRT dengan dua cara:

### 1. CDN
```html
<link rel="stylesheet" href="https://kyrt.my.id/kyrt.css">
````

### 2. Download Manual

Clone repositori ini dan tambahkan file CSS-nya:

```bash
git clone https://github.com/KhairyK/kyrt-framework.git
```

Lalu import ke dalam HTML kamu:

```html
<link rel="stylesheet" href="./kyrt.css">
```

---

## 🧠 Contoh Penggunaan

### Tombol

```html
<button class="button btn-default">Primary</button>
<button class="button btn-red-danger">Danger</button>
<button class="button btn-green-success">Success</button>
<button class="button btn-yellow-warning">Warning</button>
```

### Grid Layout

```html
<div class="grid grid-auto">
  <div class="box-float col-3">Item 1</div>
  <div class="box-float col-3">Item 2</div>
  <div class="box-float col-3">Item 3</div>
</div>
```

### Search Frame

```html
<div class="searchframe">
  <input type="text" placeholder="Search..." />
  <button>Go</button>
</div>
```

---

## 🎛️ Utilitas yang Tersedia

* **Position:** `.pos-relative`, `.pos-fixed`, `.pos-center`, dll.
* **Flex & Grid:** `.dis-flex`, `.justify-center`, `.items-center`, `.grid-auto`, `.col-6`, dll.
* **Text:** `.txt-bold`, `.txt-italic`, `.txt-upper`, `.txt-center`, `.txt-glow`.
* **Box & Padding:** `.box-float`, `.pad-mid`, `.space-y`, `.shade-mid`.
* **Animasi:** `.anim-fade-in`, `.anim-slide-up`, `.anim-spin`, `.anim-glow`, `.anim-bounce`.

---

## 🌈 Tema & Warna Global

Semua warna didefinisikan dalam `:root`, seperti:

```css
--kyrt-primary: #007bff;
--kyrt-danger: #e63946;
--kyrt-text-white: #fff;
--bg-alt: #f5f6f8;
--shadow: 0 4px 20px #00000026;
```

---

## 🧩 Komponen Tambahan

* `.navbar` — navigasi responsif dengan hamburger menu
* `.modal` — popup interaktif
* `.alert` — notifikasi dengan warna sesuai status (`.alert-success`, `.alert-danger`, dll)
* `.fieldline`, `.fieldglass` — input modern
* `.icon-*` — mendukung ikon berbasis SVG mask

---

## 🧠 Filosofi KYRT

> “KYRT dibuat untuk developer muda yang ingin membuat web cepat, bersih, dan penuh gaya — tanpa perlu ribuan baris CSS.”

---

## 💡 Info Tambahan

* Versi: **v1.1 (Beta)**
* Pembuat: **Sholehuddin Khairy (11 Tahun, Indonesia)**
* Website: [https://kyrt.my.id](https://kyrt.my.id)
* Lisensi: MIT License

---

## ❤️ Kontribusi

Pull request sangat diterima!
Silakan buat **issue** jika kamu menemukan bug atau ide fitur baru di:
👉 [https://github.com/KhairyK/kyrt-framework/issues](https://github.com/KhairyK/kyrt-framework/issues)

---

© 2025 KYRT Framework — *Made with 💙 by Khairy*
