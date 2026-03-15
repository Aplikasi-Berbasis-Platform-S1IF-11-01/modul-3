<div align="center">
  <br />
  <h1>LAPORAN PRAKTIKUM <br>APLIKASI BERBASIS PLATFORM</h1>
  <br />
  <h3>MODUL 3 <br> CSS - CASCADING STYLE SHEET</h3>
  <br />
  <br />
  <img src="logo.jpeg" alt="Logo" width="300"> 
  <br />
  <br />
  <br />
  <br />
  <h3>Disusun Oleh :</h3>
  <p>
    <strong>Yoga Hogantara</strong><br>
    <strong>2311102153</strong><br>
    <strong>S1 IF-11-REG01</strong>
  </p>
  <br />
  <h3>Dosen Pengampu :</h3>
  <p>
    <strong>Dimas Fanny Hebrasianto Permadi, S.ST., M.Kom</strong>
  </p>
  <br />
  <br />
    <h4>Asisten Praktikum :</h4>
    <strong> Apri Pandu Wicaksono </strong> <br>
    <strong>Rangga Pradarrell Fathi</strong>
  <br />
  <h3>LABORATORIUM HIGH PERFORMANCE
 <br>FAKULTAS INFORMATIKA <br>UNIVERSITAS TELKOM PURWOKERTO <br>2026</h3>
</div>

---

## 1. Dasar Teori

**CSS (Cascading Style Sheets)** adalah bahasa yang dirancang khusus untuk mempercantik tampilan halaman web. Jika kita mengibaratkan HTML sebagai kerangka atau struktur bangunan, maka CSS berperan sebagai desain interiornya mulai dari pemilihan warna cat, pengaturan tata letak furnitur, hingga dekorasi visual lainnya agar halaman terlihat lebih estetik dan profesional.

Prinsip kerja CSS adalah dengan menargetkan elemen HTML menggunakan **selector** (seperti tag, *class*, atau *id*), lalu memberikan instruksi gaya melalui berbagai properti, misalnya mengatur ukuran teks, memberikan jarak antar elemen, hingga menentukan skema warna. Pemisahan antara struktur (HTML) dan desain (CSS) ini sangat penting karena membuat kode lebih rapi, terorganisir, dan mudah dimodifikasi di kemudian hari.

Dalam penerapannya, ada tiga cara utama untuk menyisipkan CSS ke dalam dokumen HTML:

1.  **Inline CSS** Metode ini dilakukan dengan menuliskan langsung aturan gaya pada elemen HTML tertentu menggunakan atribut `style`. Biasanya cara ini hanya digunakan untuk perubahan kecil yang sangat spesifik.

2.  **Internal CSS** Aturan gaya dikumpulkan di dalam tag `<style>` yang diletakkan pada bagian `<head>` dokumen HTML. Metode ini sangat praktis untuk mengatur tampilan satu halaman penuh dalam satu file tunggal.

3.  **External CSS** Gaya desain disimpan dalam file terpisah dengan format `.css`, kemudian dipanggil ke file HTML melalui tag `<link>`. Ini adalah metode yang paling direkomendasikan dalam pengembangan web profesional karena memungkinkan satu file CSS digunakan untuk banyak halaman sekaligus, sehingga pengelolaan proyek besar menjadi jauh lebih efisien.

## 2. Penjelasan Kode 

### Kode 

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>新年快乐</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #aa0000; 
            color: #ffd700; 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
            overflow: hidden;
            position: relative; 
        }

        .container {
            border: 5px solid #ffd700;
            padding: 50px;
            border-radius: 20px;
            background-color: #8b0000;
            box-shadow: 0 0 20px #ffd700;
            animation: glow 2s infinite alternate;
            position: relative; 
            z-index: 1; 
        }

        h1 {
            font-size: 3.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px #000;
        }

        p {
            font-size: 1.5em;
            font-weight: bold;
            color: #ffebcd;
        }

        .lantern {
            font-size: 60px;
            display: inline-block;
            margin: 0 20px;
            animation: swing 2s infinite ease-in-out alternate;
            transform-origin: top center;
        }

        .firework {
            position: absolute;
            width: 20px; 
            height: 20px;
            background-color: #ffd700; 
            border-radius: 70%; 
            box-shadow: 0 0 10px #ffd700; 
            opacity: 0;
            pointer-events: none; 
        }

        @keyframes fireworkBurst {
            0% { transform: scale(0); opacity: 0; }
            15% { transform: scale(1); opacity: 1; }
            75% { transform: scale(1.5); opacity: 1; }
            100% { transform: scale(25); opacity: 0; } 
        }

        .fw1 {
            top: 20px; left: 20px;
            animation: fireworkBurst 3s infinite ease-out;
        }
        .fw2 {
            top: 30px; right: 30px;
            animation: fireworkBurst 3.5s infinite ease-out;
            animation-delay: 1.5s;
        }
        .fw3 {
            bottom: 20px; right: 20px;
            animation: fireworkBurst 3.2s infinite ease-out;
            animation-delay: 0.8s;
        }
        .fw4 {
            bottom: 30px; left: 30px;
            animation: fireworkBurst 3.8s infinite ease-out;
            animation-delay: 2.2s;
        }

        @keyframes glow {
            from { box-shadow: 0 0 10px #ffd700; }
            to { box-shadow: 0 0 40px #ffd700, 0 0 15px #ff0000 inset; }
        }

        @keyframes swing {
            from { transform: rotate(-15deg); }
            to { transform: rotate(15deg); }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="firework fw1"></div>
        <div class="firework fw2"></div>
        <div class="firework fw3"></div>
        <div class="firework fw4"></div>

        <div class="lantern">🏮</div>
        <div class="lantern">🏮</div>
        <h1>Gong Xi Fa Cai</h1>
        <p>新年快乐!</p>
        <p style="font-size: 1.2em; font-weight: normal;">Yoga Hogantara-2311102153</p>
    </div>
</body>
</html>
```

### Hasil Tampilan (Screenshot)

![Hasil Tampilan HTML & CSS](1.PNG)
### Penjelasan Code
### A. Struktur HTML (`imlek.html`)
* **Viewport Metadata**: Penggunaan `<meta name="viewport" content="width=device-width, initial-scale=1.0">` memastikan tampilan kartu tetap proporsional dan tidak terpotong saat dibuka di perangkat *mobile*.
* **Elemen Kontainer**: Seluruh konten dibungkus dalam `<div class="container">` yang berfungsi sebagai bingkai utama kartu.
* **Komponen Dekoratif**:
    * **Kembang Api**: Empat elemen `<div>` dengan *class* `firework` (fw1-fw4) diletakkan di dalam kontainer sebagai media untuk menampilkan animasi ledakan cahaya.
    * **Lampion**: Dua emoji lampion (`🏮`) dimasukkan sebagai elemen teks yang kemudian diberikan animasi ayunan melalui CSS.
* **Identitas Penulis**: Nama **Yoga Hogantara** dan NIM **2311102153** diletakkan di bagian paling bawah kontainer menggunakan tag `<p>` untuk menunjukkan kepemilikan proyek.

### B. Analisis Styling CSS
Penerapan CSS pada kode ini berfokus pada penggunaan **Flexbox** untuk tata letak dan **Keyframes** untuk menghidupkan suasana kartu:

* **Pusat Tata Letak (Flexbox)**:
    Pada selektor `body`, diterapkan `display: flex`, `justify-content: center`, dan `align-items: center`. Hal ini membuat kartu ucapan selalu berada tepat di tengah layar secara otomatis.
* **Animasi Lampion (Swing)**:
    Melalui animasi `@keyframes swing`, lampion diberikan efek gerak melengkung. Penggunaan `transform-origin: top center` membuat lampion seolah-olah memiliki poros di bagian atas, sehingga ayunannya terlihat lebih natural.
* **Efek Ledakan Kembang Api**:
    Animasi `@keyframes fireworkBurst` mengatur perubahan skala dari `scale(0)` menjadi `scale(25)` dan transparansi (`opacity`). Perbedaan `animation-delay` pada tiap elemen kembang api menciptakan efek ledakan yang muncul secara bergantian di sudut-sudut kartu.
* **Efek Cahaya Dinamis (Glow)**:
    Kontainer diberikan efek pendaran emas menggunakan animasi `@keyframes glow` pada properti `box-shadow`. Ini memberikan kesan bahwa kartu tersebut memancarkan cahaya secara berkala.
* **Palet Warna dan Tipografi**:
    Pemilihan warna merah (`#8b0000`) dan emas (`#ffd700`) memperkuat identitas budaya Imlek, sementara penggunaan `text-shadow` pada judul memberikan efek kedalaman agar teks lebih mudah dibaca di atas latar belakang yang gelap.

## Refrensi
- [Materi Modul 3](https://drive.google.com/file/d/1kd7ogQkR_rsNCnKDcJDmavY8FiOyTLzs/view?usp=sharing)