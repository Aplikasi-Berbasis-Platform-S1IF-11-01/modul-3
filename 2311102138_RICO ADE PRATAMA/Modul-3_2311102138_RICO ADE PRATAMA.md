<div align="center">
   <h2>LAPORAN PRAKTIKUM<br>APLIKASI BERBASIS PLATFORM</h2>
   <h>
   <br>
   <h4>MODUL 3<br>CSS - Cascading Style Sheet</h4>
   <br>
   <img src="assets/logotelu.png" alt="Logo Telkom" width="200">
   <br><br>
 
**Disusun Oleh :**<br>
RICO ADE PRATAMA<br>
2311102138<br>
PS1IF-11-REG01
<br><br>
 
**Dosen Pengampu :**<br>
Dimas Fanny Hebrasianto Permadi, S.ST., M.Kom
<br><br>
 
**Assisten Praktikum :**<br>
Apri Pandu Wicaksono
<br>Rangga Pradarrell Fathi
<br><br>
 
PROGRAM STUDI S1 TEKNIK INFORMATIKA<br>
FAKULTAS INFORMATIKA<br>
UNIVERSITAS TELKOM PURWOKERTO<br>
2026

</div>

---

## 1. Dasar Teori

**Cascading Style Sheets (CSS)** merupakan bahasa yang membantu memperindah tampilan dari laman web yang telah dibangun dengan HTML. CSS mendeskripsikan bagaimana bentuk tampilan elemen HTML seharusnya saat ditampilkan pada laman browser. Dengan CSS, dapat mengatur berbagai aspek visual seperti warna, ukuran teks, posisi, hingga animasi halaman web agar lebih menarik.

**Selector** merupakan elemen HTML yang akan ditambahkan CSS kemudian diikuti dengan declaration block yang terdiri dari property elemen yang akan dirubah beserta value dari property-nya. Setiap deklarasi selector dapat merubah banyak nilai property sekaligus dengan dipisahkan titik koma dan untuk semua declaration block dari satu selector berada di antara kurung kurawal. Selector pada CSS digunakan untuk menemukan elemen HTML untuk diberi CSS berdasarkan selector yang didefinisikan. Bentuk selector ada beberapa antara lain nama elemen HTML, atribut ID dan atribut Class.

**Penyisipan CSS** terdapat tiga cara untuk menyisipkan atau mendefinisikan CSS ke dalam HTML, antara lain:
<br>a. **Eksternal Style Sheet**, merupakan cara menyisipkan atau mendefinisikan CSS ke dalam HTML dengan memanggil file dengan ekstensi .css ke dalam file HTML. Pemanggilannya diletakkan di antara elemen
"head" "/head" dengan menggunakan tag "link/".
<br>b. **Internal Style Sheet**, merupakan cara menyisipkan atau mendefinisikan CSS ke dalam HTML dengan menggunakan tag "style" "/style" pada elemen "head""/head". Biasanya digunakan ketika satu laman membutuhkan style CSS yang berbeda dari yang telah dipanggil pada Eksternal Style Sheet.
<br>c. **Inline Style**, menyisipkan atau mendefinisikan CSS ke dalam HTML dengan menambahkan atribut style pada elemen yang ingin ditambahkan CSS. Biasanya digunakan hanya untuk satu elemen yang membutuhkan style CSS yang berbeda dari yang telah didefinisikan pada Internal Style atau Eksternal Style.

**Font Properties** Mengatur jenis ("font-family"), ukuran ("font-size"), gaya ("font-style"), dan ketebalan ("font-weight") teks.

**List Properties** Memperindah elemen list ("ul" untuk simbol, "ol" untuk karakter berurutan, dan "li" untuk elemennya). Propertinya mencakup "list-style-image", "list-style-position", "list-style-type", serta pengaturan latar dan jarak ("background-color", "padding", "margin").

**Alignment of Text** Mengatur rata teks dengan properti "text-align" yang bernilai "center" (tengah), "left" (kiri), "right" (kanan), atau "justify" (rata kiri-kanan).

**Colors** Mengatur warna elemen melalui "background-color" (latar belakang) dan "color" (teks). Nilai warnanya dapat berupa nama warna, RGB, Hex, HSL, RGBA, atau HSLA.

**Span & Div** Elemen "span" menangani perubahan konten pada satu baris , sedangkan "div" membuat section untuk mengelompokkan beberapa elemen HTML di dalamnya.

## 2. Kode Program HTML

Tugas 3, Buat halaman untuk merayakan imlek ("karena bubub gua cina") hanya menggunakan css tanpa library dan tanpa js

### Kode HTML (imlek.html)

```
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tugas 3 - Imlek Untuk Bubub</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="lantern-left">🏮</div>
    <div class="lantern-right">🏮</div>
    <div class="angpao-float1">🧧</div>
    <div class="angpao-float2">🧧</div>
    <div class="card">
        <div class="content">
            <p class="text-top">🎉 Selamat Tahun Baru Imlek 2026 🎉</p>
            <h1 class="title">Gong Xi Fa Cai</h1>
            <p class="mandarin">恭喜发财</p>
            <h2 class="subtitle">For Bubub Cina Tersayang ♡</h2>
            <p class="pesan-label">Pesan</p>
            <p class="message">
                Selamat tahun baru imlek ya sayang semoga kamu diberi keberuntungan, rezeki, dan sehat selalu, serta apa diinginkan tersampaikan.
            </p>
            <button class="btn-angpao">
                Open Angpao 🧧
            </button>
            <div class="footer">
                <p class="footer-label">Ucapan dari :</p>
                <p class="footer-name">Rico Ade Pratama</p>
                <p class="footer-nim">2311102138</p>
            </div>
        </div>
    </div>
</body>
</html>
```

### Kode CSS (style.css)

```
/* RICO ADE PRATAMA */
/* 2311102138 */

/_ TEMA BACKGROUND _/
body {
margin: 0;
padding: 0;
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
background: radial-gradient(circle, #8a0303 0%, #2e0000 100%);
display: flex;
justify-content: center;
align-items: center;
min-height: 100vh;
overflow: hidden;
position: relative;
}
.lantern-left, .lantern-right {
position: absolute;
top: -20px;
font-size: 100px;
filter: drop-shadow(0 10px 15px rgba(0,0,0,0.5));
animation: swing 3s ease-in-out infinite alternate;
transform-origin: top center;
z-index: 0;
}
.lantern-left {
left: 8%;
animation-delay: 0s;
}
.lantern-right {
right: 8%;
animation-delay: -1.5s;
}
.angpao-float1, .angpao-float2 {
position: absolute;
font-size: 50px;
filter: drop-shadow(0 5px 10px rgba(0,0,0,0.4));
animation: float 4s ease-in-out infinite;
z-index: 0;
opacity: 0.7;
}
.angpao-float1 {
bottom: 15%;
left: 12%;
transform: rotate(-15deg);
animation-delay: 0s;
}
.angpao-float2 {
top: 20%;
right: 15%;
transform: rotate(25deg);
animation-delay: -2s;
}

/_ Animasi Lampion Bergoyang dan Angpao Mengambang_/
@keyframes swing {
0% { transform: rotate(-8deg); }
100% { transform: rotate(8deg); }
}
@keyframes float {
0% { transform: translateY(0) rotate(-15deg); }
50% { transform: translateY(-20px) rotate(-5deg); }
100% { transform: translateY(0) rotate(-15deg); }
}
/_2311102138_RICO ADE PRATAMA_/
/_ CONTAINER KARTU MERAH _/
.card {
background: linear-gradient(145deg, #e31818, #aa0000);
width: 380px;
padding: 40px 30px;
border-radius: 15px;
border: 6px solid #ffcc00;
box-shadow: 0 20px 40px rgba(0, 0, 0, 0.6), 0 0 25px rgba(255, 204, 0, 0.3);
text-align: center;
position: relative;
overflow: hidden;
z-index: 10;
}

/_ Kalimat Selamat _/
.text-top {
color: white;
font-size: 18px;
font-weight: bold;
margin: 0 0 10px 0;
}

/_ Judul Utama _/
.title {
color: #ffcc00;
font-family: 'Times New Roman', Times, serif;
font-size: 42px;
font-weight: bold;
margin: 0 0 5px 0;
letter-spacing: 1.5px;
text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

/_ Tulisan Mandarin _/
.mandarin {
color: #ffcc00;
font-size: 24px;
margin: 0 0 20px 0;
letter-spacing: 4px;
text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
font-weight: bold;
}

/_ Subjudul Bubub _/
.subtitle {
color: #ff99cc;
font-family: 'Comic Sans MS', 'Marker Felt', cursive, sans-serif;
font-size: 18px;
margin: 0 0 20px 0;
font-weight: bold;
text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
}

/_ Teks Pesan Paragraf _/
.pesan-label {
color: white;
font-size: 15px;
font-weight: bold;
margin: 0 0 5px 0;
}
.message {
color: white;
font-size: 12px;
line-height: 1.6;
margin: 0 0 20px 0;
padding: 0 12px;
}
/_2311102138_RICO ADE PRATAMA_/
/_ Tombol Buka Angpao _/
.btn-angpao {
background-color: #ffcc00;
color: #d31010;
border: none;
padding: 12px 25px;
border-radius: 25px;
font-size: 15px;
font-weight: bold;
cursor: pointer;
box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
transition: transform 0.2s, background-color 0.2s;
margin-bottom: 30px;
display: inline-flex;
align-items: center;
gap: 8px;
}
.btn-angpao:hover {
transform: scale(1.05);
background-color: #ffe066;
}
/_2311102138_RICO ADE PRATAMA_/
/_ Ucapan Dari _/
.footer {
color: #ffcc00;
}
.footer p {
margin: 3px 0;
}
.footer-label {
font-size: 12px;
color: white;
}
.footer-name {
font-size: 16px;
font-weight: bold;
}
.footer-nim {
font-size: 14px;
}

```

### Hasil Output

![Gambar Hasil tabel](assets/hasil.png)

### Penjelasan Kode HTML

Kode Pertama ada HTML yang merupakan kerangka untuk sebuah halaman web kartu ucapan Tahun Baru Imlek 2026 yang dibangun dengan memanfaatkan elemen div untuk mengelompokkan berbagai bagian tata letaknya, seperti dekorasi lampion, angpao, dan area konten utama kartu. Pada bagian head, kode ini menerapkan metode External Style Sheet dengan memanggil file style.css melalui tag "link" agar desain visualnya dapat diatur secara terpisah. Isi dari kartu tersebut disusun rapi di dalam tag body menggunakan berbagai elemen teks seperti heading (h1, h2) dan paragraf (p) untuk menampilkan pesan ucapan personal, dilengkapi dengan sebuah tombol interaktif "Open Angpao", serta bagian footer yang memuat nama dan NIM Anda sebagai pembuat tugas tersebut. Lebih Jelasnya seperti pada gambar diatas.

Sedangkan Kode Kedua ada CSS yang bertugas untuk mendesain dan memberikan animasi pada kartu ucapan Imlek yang kerangkanya dibuat pada HTML sebelumnya. Elemen body diberi latar belakang gradasi merah gelap untuk menciptakan nuansa Imlek yang kental, sambil mengatur tata letak dengan Flexbox agar kartu berada tepat di tengah layar. Kode ini juga mendefinisikan animasi keyframe bernama swing untuk membuat elemen lampion bergoyang layaknya tertiup angin dan float agar ornamen angpao terlihat melayang secara dinamis di latar belakang. Pada bagian utama kartu (.card), CSS memberikan warna dasar merah terang dengan border kuning keemasan, efek bayangan, serta mengatur tipografi untuk teks ucapan, judul "Gong Xi Fa Cai", dan pesan personal agar terlihat kontras dan menarik. Terakhir, kode ini mempercantik tombol "Open Angpao" dengan warna kuning, sudut melengkung, serta efek hover yang membuatnya sedikit membesar saat diarahkan kursor, sekaligus menata bagian footer untuk menampilkan nama dan NIM dengan jelas.

## 3. Kesimpulan dan Penutup

Modul ini menjelaskan tentang konsep dasar dan implementasi CSS (Cascading Style Sheets) yang berfungsi untuk memperindah dan mengatur bentuk tampilan elemen pada laman web yang telah dibangun dengan HTML , dengan pengaturan font, list, perataan teks, dan warna sebagai fokus materi utamanya. Cocok sebagai panduan pembelajaran awal pada praktikum pemrograman web bagi mahasiswa Teknik Informatika.

<br>Ngabuburit di daerah Baturraden,
<br>Sama kawan-kawan dengan motoran.
<br>Tugas Modul 3 Rico sudah absen,
<br>Siap di-push ke GitHub sebagai laporan.

## 4. Referensi

- [Materi Modul 3](https://drive.google.com/file/d/1YZ4-EXXFpIfaoV6P8ZpeixciZLjrFiy5/view)
