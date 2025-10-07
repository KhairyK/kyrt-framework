
````markdown
# 🌐 Kyrt UI Framework

**Kyrt UI** adalah mini CSS framework buatan Khairy yang ringan, cepat, dan fleksibel — dirancang untuk mempercepat pembuatan tampilan web modern tanpa perlu bergantung pada library besar seperti Bootstrap atau Tailwind.

Framework ini berfokus pada:
- 🎨 Desain minimalis dengan warna dinamis
- ⚡ Kinerja cepat tanpa JavaScript tambahan
- 🧩 Utilitas siap pakai (layout, grid, animasi, form)
- 💎 Komponen serbaguna (button, navbar, searchbox, field, dll)

---

## 🚀 Fitur Utama

### 🎨 Desain Modern
Gunakan variabel warna dan radius global agar tampilan konsisten di seluruh komponen:
```css
:root {
  --kyrt-primary: #007bff;
  --kyrt-danger: #e63946;
  --kyrt-text-white: #fff;
  --kyrt-radius: 6px;
  --kyrt-transition: .3s ease;
}
````

---

### 🧱 Utility Class

Banyak class utilitas siap pakai untuk posisi, display, margin, padding, grid, dan lainnya.

| Class         | Fungsi                         |
| ------------- | ------------------------------ |
| `.pos-center` | Posisi absolut di tengah       |
| `.dis-flex`   | Flexbox display                |
| `.grid-3`     | Membagi layout menjadi 3 kolom |
| `.pad-mid`    | Padding sedang                 |
| `.txt-mid`    | Teks rata tengah               |

Contoh:

```html
<div class="dis-flex justify-center items-center pad-mid">
  <p>Halo Dunia</p>
</div>
```

---

### 🔘 Tombol (Buttons)

Tersedia banyak varian tombol dengan warna berbeda:

| Class                 | Warna / Fungsi             |
| --------------------- | -------------------------- |
| `.btn-default`        | Tombol biru utama          |
| `.btn-red-danger`     | Tombol merah (hapus/error) |
| `.btn-green-success`  | Tombol hijau (berhasil)    |
| `.btn-yellow-warning` | Tombol kuning (peringatan) |

Contoh:

```html
<button class="button btn-default">Primary</button>
<button class="button btn-red-danger">Delete</button>
```

---

### 🪟 Box & Card

Gunakan `.box-float`, `.box-light`, `.box-shadow-md`, dan lainnya untuk membuat container atau card.

```html
<div class="box-float box-light txt-mid pad-mid">
  <h3>Card Title</h3>
  <p>Isi dari box ini terlihat elegan dan bersih.</p>
</div>
```

---

### ⚡ Animasi Siap Pakai

Lebih dari **30 animasi built-in**, termasuk:

* `.anim-fade-in`
* `.anim-slide-up`
* `.anim-glow`
* `.anim-shake`
* `.anim-zoom-in`
* `.anim-blur-in`

```html
<div class="anim-fade-in">Fade In Effect</div>
```

---

### 🧠 Input & Field

Desain form yang modern dan fleksibel:

```html
<input class="fieldline" placeholder="Masukkan Nama">
<input class="fieldokay" placeholder="Valid Input">
<input class="fielderror" placeholder="Error Input">
```

Atau gunakan versi dengan ikon:

```html
<div class="fieldicon">
  <i class="icon-user"></i>
  <input class="fieldline" placeholder="Username">
</div>
```

---

### 🔍 Search Box

Komponen kotak pencarian yang responsif:

```html
<div class="searchframe">
  <input type="text" placeholder="Cari...">
  <button><i class="icon-search"></i></button>
</div>
```

---

### 🧭 Navbar Responsive

Struktur navbar sederhana dan fleksibel:

```html
<nav class="navline">
  <div class="navbrand">Kyrt UI</div>
  <div class="navtoggle"><span></span><span></span><span></span></div>
  <div class="navmenu">
    <a href="#" class="navitem">Home</a>
    <a href="#" class="navitem">Docs</a>
    <a href="#" class="navitem">About</a>
  </div>
</nav>
```

---

## 🧰 Instalasi

### 💾 Cara Cepat (CDN)

Tambahkan ini di `<head>` HTML kamu:

```html
<link rel="stylesheet" href="https://phpin.kesug.com/kyrt/kyrt.min.css">
```

Atau gunakan file lokal:

```html
<link rel="stylesheet" href="kyrt.min.css">
```

---

## 📘 Contoh Penggunaan

```html
<button class="button btn-default anim-pop">Klik Aku!</button>

<div class="box-float box-light anim-fade-in">
  <h3>Hello Kyrt UI</h3>
  <p>Framework ringan buatan Khairy.</p>
</div>
```
