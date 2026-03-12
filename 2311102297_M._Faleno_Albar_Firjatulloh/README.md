<div align="center">

# LAPORAN PRAKTIKUM  
## Aplikasi Berbasis Platform

### Modul 3  
### CSS – Cascading Style Sheet

<img src="assets/Logo Tel-u.PNG" alt="Logo Tel-U" width="220">

### Disusun Oleh
**M. Faleno Albar Firjatulloh**  
2311102297  
S1 IF-11-01

### Dosen Pengampu
**Dimas Fanny Hebrasianto Permadi, S.ST., M.Kom**

### Asisten Praktikum
Apri Pandu Wicaksono  
Rangga Pradarrell Fathi

### Laboratorium High Performance  
Fakultas Informatika  
Universitas Telkom Purwokerto  
2026

</div>

---

# 1. Dasar Teori

**CSS (Cascading Style Sheets)** adalah bahasa yang digunakan bersama HTML untuk mengatur tampilan visual pada halaman web.

Jika **HTML** berfungsi sebagai struktur dasar sebuah halaman, maka **CSS** digunakan untuk mengatur berbagai aspek tampilan seperti warna, tata letak, ukuran teks, jarak antar elemen, serta berbagai efek visual lainnya.

CSS bekerja menggunakan **selector** untuk memilih elemen HTML tertentu, kemudian menerapkan aturan gaya berupa berbagai **property** seperti warna, ukuran font, margin, padding, dan lain-lain.

Dengan menggunakan CSS, pengembang dapat **memisahkan struktur (HTML) dan tampilan (CSS)** sehingga kode menjadi lebih:

- Rapi
- Mudah dipahami
- Mudah dikelola
- Lebih fleksibel untuk pengembangan

## Cara Menggunakan CSS

Terdapat **tiga metode utama** dalam menerapkan CSS pada HTML, yaitu:

1. **Inline CSS**  
   CSS ditulis langsung pada elemen HTML menggunakan atribut `style`.

2. **Internal CSS**  
   CSS ditulis di dalam tag `<style>` pada bagian `<head>` dokumen HTML.

3. **External CSS**  
   CSS disimpan pada file terpisah dengan ekstensi `.css` kemudian dihubungkan menggunakan tag `<link>`.  
   Metode ini **paling direkomendasikan** karena membuat struktur kode lebih terorganisir.

---

# 2. Penjelasan Kode

## Source Code (`index.html`)

```html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Selamat Tahun Baru Imlek</title>

<style>
body {
    margin: 0;
    font-family: "Poppins", sans-serif;
    background: radial-gradient(circle, #b30000, #4d0000);
    color: white;
    text-align: center;
}

header {
    padding: 40px 20px;
}

header h1 {
    font-size: 50px;
    color: gold;
    letter-spacing: 3px;
}

header p {
    font-size: 20px;
}

.lampion-container {
    display: flex;
    justify-content: center;
    gap: 60px;
    margin: 40px 0;
}

.lampion {
    width: 80px;
    height: 100px;
    background: red;
    border-radius: 40px;
    position: relative;
    box-shadow: 0 0 15px gold;
}

.lampion::before {
    content: "";
    position: absolute;
    top: -20px;
    left: 35px;
    width: 10px;
    height: 20px;
    background: gold;
}

.lampion::after {
    content: "";
    position: absolute;
    bottom: -25px;
    left: 30px;
    width: 20px;
    height: 25px;
    background: gold;
}

.ucapan {
    max-width: 800px;
    margin: auto;
    padding: 30px;
    background: rgba(0,0,0,0.3);
    border-radius: 15px;
    border: 2px solid gold;
}

.ucapan h2 {
    color: gold;
}

.ucapan p {
    font-size: 18px;
    line-height: 1.6;
}

footer {
    margin-top: 40px;
    padding: 20px;
    font-size: 14px;
    color: #ffd700;
}
</style>
</head>

<body>

<header>
<h1>🧧 Gong Xi Fa Cai 🧧</h1>
<p>Selamat Tahun Baru Imlek</p>
</header>

<div class="lampion-container">
<div class="lampion"></div>
<div class="lampion"></div>
<div class="lampion"></div>
</div>

<div class="ucapan">
<h2>Happy Chinese New Year 🐉</h2>

<p>
Semoga tahun baru Imlek membawa kebahagiaan, kesehatan, dan keberuntungan bagi kita semua.
Mari kita sambut tahun yang baru dengan semangat baru, harapan baru, dan rezeki yang melimpah.
</p>

<p>
恭喜发财 – Semoga semakin makmur dan sukses di tahun ini!
</p>

</div>

<footer>
© 2026 Perayaan Tahun Baru Imlek
</footer>

</body>
</html>
````

---

## Hasil Tampilan

![Hasil Tampilan HTML & CSS](assets/1.PNG)

---

# 3. Penjelasan Program

### Struktur Utama

Program menggunakan struktur **HTML5 semantic** seperti `header`, `div`, dan `footer` untuk membagi konten halaman menjadi beberapa bagian yang terorganisir. Struktur ini membantu membuat halaman lebih mudah dipahami serta meningkatkan keterbacaan kode.

### Pembuatan Lampion dengan CSS

Elemen lampion dibuat **sepenuhnya menggunakan CSS** tanpa menggunakan gambar. Bentuk utama lampion dibuat menggunakan properti `border-radius`, sedangkan bagian gantungan dan hiasan bawah dibuat menggunakan **pseudo-element `::before` dan `::after`**.

### Tampilan Kartu Ucapan

Bagian ucapan berada di tengah halaman dengan desain menyerupai **kartu ucapan**. Elemen ini menggunakan latar belakang transparan (`rgba`) sehingga memberikan efek visual yang menarik serta membuat teks tetap mudah dibaca di atas latar belakang merah.

### Desain Visual

Halaman menggunakan kombinasi warna **merah dan emas** yang identik dengan perayaan Tahun Baru Imlek. Latar belakang dibuat menggunakan **radial gradient** untuk memberikan efek kedalaman warna.

### Tata Letak

Lampion disusun menggunakan **Flexbox (`display: flex`)** sehingga posisi elemen otomatis sejajar di tengah halaman dan tetap terlihat rapi pada berbagai ukuran layar.

---

# Referensi

* [Materi Modul 3](https://drive.google.com/file/d/1kd7ogQkR_rsNCnKDcJDmavY8FiOyTLzs/view?usp=sharing)
