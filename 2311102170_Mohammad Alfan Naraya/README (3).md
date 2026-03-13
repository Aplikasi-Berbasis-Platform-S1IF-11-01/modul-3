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
    <strong>Mohammad Alfan Naraya</strong><br>
    <strong>2311102170</strong><br>
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

**CSS (Cascading Style Sheets)** adalah bahasa yang digunakan bersama HTML untuk mengatur tampilan visual pada halaman web. Jika HTML berfungsi sebagai struktur atau kerangka dasar sebuah halaman, maka CSS berperan dalam mempercantik tampilannya, seperti mengatur warna, tata letak, ukuran elemen, hingga berbagai dekorasi visual lainnya.

Cara kerja CSS adalah dengan memilih elemen HTML menggunakan selector, seperti tag, class, atau id, kemudian menerapkan aturan gaya melalui berbagai properti, misalnya warna, ukuran teks, jarak antar elemen, dan sebagainya. Dengan penggunaan CSS, struktur konten (HTML) dapat dipisahkan dari pengaturan tampilannya (CSS), sehingga kode menjadi lebih rapi, mudah dipelihara, dan lebih mudah diperbarui.

Secara umum terdapat tiga metode untuk menambahkan CSS ke dalam dokumen HTML, yaitu:

1. **Inline CSS**  
  Gaya CSS dituliskan langsung pada elemen HTML melalui atribut style.

2. **Internal CSS**  
  Aturan CSS ditulis di dalam tag <style> yang ditempatkan pada bagian <head> dalam dokumen HTML.

3. **External CSS**  
   Aturan CSS disimpan dalam file terpisah dengan ekstensi .css, lalu dihubungkan ke file HTML menggunakan tag <link>. Metode ini paling direkomendasikan dalam pengembangan web karena membuat pengelolaan kode lebih terstruktur, terutama untuk proyek yang lebih besar.
   
## 2. Penjelasan Kode HTML dan CSS

Berikut ini adalah implementasi desain kartu ucapan yang digabungkan antara struktur kerangka dasar HTML murni dan desain modern visual yang diambil dari *External CSS*, beserta hasil tampilannya.

### Kode HTML (`modul3.html`)

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ucapan Selamat Tahun Baru Imlek</title>
    <style>
        :root {
            --red: #d32f2f;
            --gold: #ffd700;
            --dark-red: #8b0000;
            --cream: #fff5e6;
        }

        body {
            margin: 0;
            padding: 0;
            background-color: var(--dark-red);
            font-family: 'Georgia', serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
            color: var(--gold);
        }

        /* Dekorasi Tirai/Bingkai Samping */
        body::before, body::after {
            content: '';
            position: absolute;
            top: 0;
            width: 40px;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,215,0,0.1), transparent);
            border-left: 2px solid var(--gold);
            border-right: 2px solid var(--gold);
            z-index: 1;
        }
        body::before { left: 20px; }
        body::after { right: 20px; }

        /* Container Ucapan */
        .card {
            text-align: center;
            max-width: 600px;
            padding: 40px;
            border: 2px solid var(--gold);
            background: rgba(0, 0, 0, 0.3);
            position: relative;
            box-shadow: 0 0 50px rgba(0,0,0,0.5);
            animation: fadeIn 2s ease-out;
        }

        /* Ornamen Sudut */
        .card::before {
            content: '🧧';
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 2rem;
        }

        .chinese-main {
            font-size: 5rem;
            margin: 0;
            display: block;
            filter: drop-shadow(0 0 10px var(--gold));
            animation: glow 3s infinite alternate;
        }

        h1 {
            font-size: 2.5rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            margin: 20px 0;
            border-bottom: 1px solid var(--gold);
            padding-bottom: 10px;
            display: inline-block;
        }

        .message {
            font-size: 1.2rem;
            line-height: 1.8;
            color: var(--cream);
            font-style: italic;
        }

        /* Animasi Lampion Kecil di Pojok */
        .mini-lantern {
            position: absolute;
            top: 20px;
            font-size: 2rem;
            animation: swing 4s ease-in-out infinite;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.9); }
            to { opacity: 1; transform: scale(1); }
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 5px var(--gold)); }
            to { filter: drop-shadow(0 0 20px #fff); }
        }

        @keyframes swing {
            0%, 100% { transform: rotate(-10deg); }
            50% { transform: rotate(10deg); }
        }

        /* Responsif untuk HP */
        @media (max-width: 480px) {
            .chinese-main { font-size: 3.5rem; }
            h1 { font-size: 1.5rem; }
            .card { margin: 20px; padding: 20px; }
            body::before, body::after { display: none; }
        }
    </style>
</head>
<body>

    <div class="mini-lantern" style="left: 10%;">🏮</div>
    <div class="mini-lantern" style="right: 10%; animation-delay: 1s;">🏮</div>

    <div class="card">
        <span class="chinese-main">恭贺新禧</span>
        <h1>Gong Xi Fa Cai</h1>
        
        <div class="message">
            <p>Di ambang tahun yang baru ini,</p>
            <p>Semoga setiap langkah kita dipenuhi keberuntungan,<br>
               setiap usaha membuahkan kemakmuran,<br>
               dan setiap hari berlimpah kebahagiaan.</p>
            <p style="color: var(--gold); font-weight: bold; margin-top: 30px;">
                Selamat Tahun Baru Imlek 2026
            </p>
        </div>
    </div>

</body>
</html>
```

### Hasil Tampilan (Screenshot)

![Hasil Tampilan HTML & CSS](assets/output.png)
### Penjelasan Code

###  1. Struktur HTML 
Elemen di dalam `<body>` disusun secara berlapis untuk menciptakan kedalaman visual:

* **`mini-lantern`**: Menggunakan emoji 🏮 yang diposisikan secara **absolut** di kiri dan kanan atas sebagai pemanis tampilan.
* **`card`**: Kontainer utama ucapan yang berfungsi sebagai titik fokus. Di dalamnya terdapat:
    * **`chinese-main`**: Teks Mandarin `恭贺新禧` (*Gōng hè xīn xǐ*) yang berarti "Selamat menyambut tahun baru yang penuh keberuntungan".
    * **`h1`**: Judul utama "Gong Xi Fa Cai".
    * **`message`**: Paragraf berisi doa, harapan, dan ucapan tulus.

---

###  2. CSS Styling
Teknik CSS yang digunakan bertujuan untuk menciptakan keindahan halaman html:

* **CSS Variables (`:root`)**: Digunakan untuk menyimpan palet warna inti (merah, emas, krem). Hal ini memudahkan manajemen warna (tema) di seluruh dokumen secara konsisten.
* **Latar Belakang & Bingkai (`body::before/after`)**: 
    * Garis vertikal di sisi kiri dan kanan dibuat menggunakan *pseudo-elements*.
    * `linear-gradient` memberikan efek cahaya halus agar bingkai terlihat lebih dinamis dan tidak kaku.
* **Efek Kartu (`.card`)**:
    * `background: rgba(0, 0, 0, 0.3)`: Menciptakan latar belakang hitam transparan sehingga warna merah dasar tetap terlihat tembus (*glassmorphism* ringan).
    * `box-shadow`: Memberikan efek bayangan dalam agar kartu terlihat "timbul" dari latar belakang.

---

###  3. Animasi
Halaman ini menggunakan tiga animasi utama agar tidak terlihat statis:

1.  **`fadeIn`**: Membuat kartu muncul perlahan (transparan ke jelas) dan sedikit membesar saat halaman dimuat pertama kali.
2.  **`glow`**: Mengubah intensitas `drop-shadow` pada teks Mandarin secara terus-menerus untuk efek "pijar" lampu neon emas.
3.  **`swing`**: Menggerakkan lampion (🏮) dengan mengubah rotasi (`rotate`) dari -10° ke 10°, meniru gerakan lampion yang tertiup angin.

---

## Refrensi
- [Materi Modul 3](https://drive.google.com/file/d/1kd7ogQkR_rsNCnKDcJDmavY8FiOyTLzs/view?usp=sharing)
