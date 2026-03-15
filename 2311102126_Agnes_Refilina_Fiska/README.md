<div align="center">
  <br />
  <h1>LAPORAN PRAKTIKUM <br>APLIKASI BERBASIS PLATFORM</h1>
  <br />
  <h3>MODUL 3 <br> CSS - CASCADING STYLE SHEET</h3>
  <br />
  <br />
  <img src="assets/logo.jpeg" alt="Logo" width="300"> 
  <br />
  <br />
  <br />
  <br />
  <h3>Disusun Oleh :</h3>
  <p>
    <strong>Agnes Refilina Fiska</strong><br>
    <strong>2311102126</strong><br>
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

**CSS (Cascading Style Sheets)** adalah bahasa desain yang berfungsi sebagai pendamping HTML untuk mengelola aspek visual sebuah situs web. Jika kita mengibaratkan HTML sebagai kerangka atau fondasi bangunan, maka CSS berperan sebagai elemen arsitektur dan interiornya—seperti pemilihan warna cat, penyusunan tata letak perabotan, penentuan ukuran jendela, hingga berbagai dekorasi artistik lainnya.

Mekanisme kerja CSS mengandalkan **selector** (pemilih) untuk membidik elemen HTML tertentu—baik melalui label tag, class, maupun id—yang kemudian diberikan aturan gaya khusus, seperti jenis fon, skema warna, hingga pengaturan jarak antar elemen. Keuntungan utama menggunakan CSS adalah adanya pemisahan yang jelas antara struktur data (HTML) dan estetika (CSS), sehingga kode program menjadi lebih rapi, efisien, dan mudah dimodifikasi di masa depan.

Dalam implementasinya, terdapat tiga teknik utama untuk menyematkan CSS ke dalam dokumen HTML:

1. **Inline CSS**  
   Gaya visual disisipkan secara spesifik langsung di dalam tag HTML melalui atribut `style`. Metode ini biasanya hanya digunakan untuk perubahan kecil yang bersifat mendesak.

2. **Internal CSS**  
   Seluruh aturan gaya dikumpulkan di dalam satu blok tag <style> yang diletakkan pada bagian <head> dokumen. Teknik ini efektif untuk mengatur tampilan satu halaman web secara mandiri.

3. **External CSS**  
   Aturan desain disimpan dalam berkas terpisah berformat .css dan dipanggil ke dalam HTML menggunakan tag <link>. Metode ini adalah standar industri dan praktik terbaik (best practice) karena memungkinkan pengembang untuk mengelola tampilan banyak halaman sekaligus hanya dari satu berkas pusat.

## 2. Penjelasan Kode HTML dan CSS

Berikut ini adalah implementasi desain kartu ucapan yang digabungkan antara struktur kerangka dasar HTML murni dan desain modern visual yang diambil dari *External CSS*, beserta hasil tampilannya.

### Kode HTML (`Tugas3.html`)

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lunar Elegance for Bubub</title>
    <style>
        /* --- CSS SETUP --- */
        :root {
            --bg-color: #4a0000;
            --card-bg: #5c0000;
            --gold: #d4af37;
            --gold-light: #f9e297;
            --text-white: #fdfdfd;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: radial-gradient(circle at center, #630000 0%, #2b0000 100%);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Georgia', serif;
            color: var(--gold);
            overflow: hidden;
        }

        /* --- BACKGROUND ANIMATION (PURE CSS) --- */
        .petal {
            position: absolute;
            background-color: #ffc0cb;
            border-radius: 150% 0 150% 0;
            opacity: 0.3;
            top: -10%;
            animation: drift linear infinite;
        }

        @keyframes drift {
            0% { transform: translateY(0) rotate(0deg); opacity: 0; }
            10% { opacity: 0.4; }
            90% { opacity: 0.4; }
            100% { transform: translateY(110vh) rotate(720deg); opacity: 0; }
        }

        /* Kelopak dengan variasi posisi & durasi manual (Tanpa JS) */
        .p1 { left: 10%; width: 10px; height: 12px; animation-duration: 7s; }
        .p2 { left: 30%; width: 15px; height: 18px; animation-duration: 10s; animation-delay: 2s; }
        .p3 { left: 55%; width: 8px; height: 10px; animation-duration: 8s; animation-delay: 4s; }
        .p4 { left: 80%; width: 12px; height: 14px; animation-duration: 12s; animation-delay: 1s; }

        /* --- MAIN CARD --- */
        .elegant-card {
            position: relative;
            width: 400px;
            padding: 60px 40px;
            background: var(--card-bg);
            border: 1px solid var(--gold);
            text-align: center;
            box-shadow: 0 25px 50px rgba(0,0,0,0.6);
            z-index: 5;
        }

        /* Border Dalam Ganda */
        .elegant-card::before {
            content: "";
            position: absolute;
            top: 15px;
            bottom: 15px;
            left: 15px;
            right: 15px;
            border: 1px solid var(--gold);
            opacity: 0.5;
            pointer-events: none;
        }

        .mandarin-title {
            font-size: 3.5rem;
            font-weight: normal;
            margin-bottom: 20px;
            letter-spacing: 10px;
            display: block;
            background: linear-gradient(to bottom, var(--gold-light), var(--gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        h1 {
            font-size: 1.2rem;
            font-weight: 300;
            text-transform: uppercase;
            letter-spacing: 5px;
            margin-bottom: 40px;
            color: var(--gold-light);
        }

        .message {
            font-size: 1.05rem;
            line-height: 1.8;
            color: var(--text-white);
            font-style: italic;
            border-top: 1px solid rgba(212, 175, 55, 0.3);
            border-bottom: 1px solid rgba(212, 175, 55, 0.3);
            padding: 25px 0;
            margin-bottom: 30px;
        }

        .gold-seal {
            width: 50px;
            height: 50px;
            margin: 0 auto;
            border: 2px solid var(--gold);
            transform: rotate(45deg);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .gold-seal span {
            transform: rotate(-45deg);
            font-size: 1.2rem;
            font-weight: bold;
        }

        .footer {
            margin-top: 40px;
            font-size: 0.75rem;
            letter-spacing: 2px;
            opacity: 0.6;
            text-transform: uppercase;
        }

        /* Simpul Tali (CSS Art) */
        .knot {
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            color: var(--gold);
            font-size: 2rem;
        }
    </style>
</head>
<body>

    <div class="petal p1"></div>
    <div class="petal p2"></div>
    <div class="petal p3"></div>
    <div class="petal p4"></div>

    <div class="elegant-card">
        <div class="knot">◈</div>
        
        <span class="mandarin-title">新年快乐</span>
        <h1>Happy Lunar New Year</h1>

        <div class="message">
            "Semoga kemakmuran dan kedamaian menyelimuti langkahmu di tahun yang baru ini. Selamat merayakan Imlek, Bubub tersayang. Terima kasih telah menjadi cahaya yang paling indah."
        </div>

        <div class="gold-seal">
            <span>福</span>
        </div>

        <div class="footer">
            2026 — Year of the Horse
        </div>
    </div>

</body>
</html>
```

### Hasil Tampilan (Screenshot)

![Hasil Tampilan HTML & CSS](assets/1.jpeg)
### Penjelasan Code

#### 1. Struktur Dan Metadata

- Pada bagian <head>, tag <meta charset="UTF-8"> digunakan agar halaman dapat menampilkan karakter khusus (seperti aksara Mandarin) dengan baik, sedangkan tag <meta name="viewport"> berfungsi supaya tampilan website tetap responsif dan proporsional saat dibuka di berbagai ukuran layar.

- Tag <title> dipakai untuk memberi judul "Lunar Elegance for Bubub" pada tab browser, dan bagian <style> digunakan untuk mendefinisikan seluruh estetika visual secara internal tanpa memerlukan file CSS eksternal.

#### 2. Styling CSS

- Pada bagian :root, didefinisikan variabel warna seperti merah tua (--bg-color) dan emas (--gold) untuk menciptakan tema Imlek yang mewah dan konsisten di seluruh elemen.

- Selector `body` menggunakan properti `radial-gradient` untuk menciptakan efek pencahayaan dari pusat layar, sementara kelas .petal dipadukan dengan `@keyframes drift` untuk menciptakan animasi kelopak bunga yang jatuh berguguran secara otomatis.

- Bagian .`elegant-card` menggunakan `box-shadow` untuk memberikan efek kedalaman dan `border` ganda guna menciptakan bingkai kartu ucapan yang terlihat eksklusif dan elegan.

#### 3. Styling HTML

- Di dalam <body>, terdapat beberapa elemen <div> dengan kelas petal yang berfungsi sebagai objek animasi dekoratif di latar belakang halaman.

- Elemen <span class="mandarin-title"> digunakan untuk menampilkan ucapan "Xin Nian Kuai Le" dengan efek gradasi emas yang mencolok sebagai poin utama visual.

- Bagian <div class="message"> berisi teks ucapan personal yang dibungkus dengan garis tepi halus (border-top dan border-bottom) untuk memisahkan pesan inti dari elemen dekorasi lainnya.

- Tag <div class="gold-seal"> menampilkan karakter "Fu" (Keberuntungan) di dalam kotak yang diputar 45 derajat, menciptakan simbol segel tradisional Tiongkok sebagai penutup kartu.

- Terakhir, bagian <div class="footer"> berfungsi untuk menampilkan keterangan tahun 2026 sebagai "Year of the Horse" dengan format teks yang tipis dan elegan.

## Refrensi
- [Materi Modul 3](https://drive.google.com/file/d/1kd7ogQkR_rsNCnKDcJDmavY8FiOyTLzs/view?usp=sharing)