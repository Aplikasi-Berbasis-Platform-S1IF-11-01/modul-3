

<div align="center">
  <br />
  <h1>LAPORAN PRAKTIKUM <br>APLIKASI BERBASIS PLATFORM</h1>
  <br />
  <h3>MODUL 3 <br> CSS</h3>
  <br />
  <img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2F1.bp.blogspot.com%2F-vb7jyBjK-sM%2FXXfKp51LrjI%2FAAAAAAAACts%2FEjcXzlgZwSswNWXsBHMyX-6aav1mjA77QCPcBGAYYCw%2Fs1600%2FLogo_Telkom_University_potrait.png&f=1&nofb=1&ipt=9d030d54102ea96369d39fe491220e0536195abc8ee443279c1a420302206400" alt="Logo Telkom" width="300"> 
  <br /><br /><br />
  
  <h3>Disusun Oleh :</h3>
  <p>
    <strong>Didik Setiawan</strong><br>
    <strong>2311102030</strong><br>
    <strong>IF-11-REG-01</strong>
  </p>
  <br />
  
  <h3>Dosen Pengampu :</h3>
  <p><strong>Dimas Fanny Hebrasianto Permadi, S.ST., M.Kom</strong></p>
  <br />
  
  <h4>Asisten Praktikum :</h4>
  <strong>Apri Pandu Wicaksono</strong> <br>
  <strong>Rangga Pradarrell Fathi</strong>
  <br />
  
  <h3>LABORATORIUM HIGH PERFORMANCE<br>FAKULTAS INFORMATIKA<br>UNIVERSITAS TELKOM PURWOKERTO<br>2026</h3>
</div>

---

## DASAR TEORI

CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mengatur tampilan halaman web yang dibuat dengan HTML, seperti warna, jenis dan ukuran teks, posisi elemen, serta tata letak agar website terlihat lebih menarik dan rapi. CSS bekerja menggunakan aturan gaya yang terdiri dari selector untuk memilih elemen HTML dan declaration yang berisi properti serta nilainya. CSS dapat diterapkan dengan tiga cara yaitu inline, internal, dan external, di mana external CSS paling efisien karena dapat digunakan pada banyak halaman. Beberapa properti yang sering digunakan antara lain font-family, font-size, font-style, dan font-weight untuk mengatur tampilan teks agar lebih mudah dibaca dan menarik.



## UNGUIDED

### kode html



```bash
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gong Xi Fa Cai 2026</title>
  <link rel="stylesheet" href="imlek.css">
</head>
<body>

  <!-- Lanterns -->
  <div class="lantern l1">
    <div class="lantern-string"></div>
    <div class="lantern-body">福</div>
    <div class="lantern-tassel"></div>
  </div>
  <div class="lantern l2">
    <div class="lantern-string"></div>
    <div class="lantern-body">福</div>
    <div class="lantern-tassel"></div>
  </div>
  <div class="lantern l3">
    <div class="lantern-string"></div>
    <div class="lantern-body">福</div>
    <div class="lantern-tassel"></div>
  </div>
  <div class="lantern l4">
    <div class="lantern-string"></div>
    <div class="lantern-body">福</div>
    <div class="lantern-tassel"></div>
  </div>

  <!-- Falling angpao -->
  <div class="angpao a1">福</div>
  <div class="angpao a2">喜</div>
  <div class="angpao a3">财</div>
  <div class="angpao a4">禄</div>
  <div class="angpao a5">福</div>
  <div class="angpao a6">喜</div>
  <div class="angpao a7">财</div>

  <!-- Main content -->
  <div class="stage">
    <div class="year-badge">Tahun Baru Imlek 2026 · 蛇年</div>

    <h1 class="main-title">Gong Xi Fa Cai</h1>
    <div class="cjk-title">恭喜发财</div>

    <div class="divider"></div>

    <p class="subtitle">
      Selamat Merayakan Tahun Baru Imlek 🧧<br>
      Semoga tahun baru dipenuhi keberuntungan,<br>
      kedamaian, dan kebahagiaan.
    </p>

    <div class="blessings">
      <div class="blessing-item b1">
        <span class="blessing-char">福</span>
        <span class="blessing-label">Berkah</span>
      </div>
      <div class="blessing-item b2">
        <span class="blessing-char">禄</span>
        <span class="blessing-label">Rezeki</span>
      </div>
      <div class="blessing-item b3">
        <span class="blessing-char">寿</span>
        <span class="blessing-label">Panjang Umur</span>
      </div>
      <div class="blessing-item b4">
        <span class="blessing-char">喜</span>
        <span class="blessing-label">Bahagia</span>
      </div>
    </div>
  </div>

</body>
</html>
```



##### penjelasan
File ini adalah kerangka halaman. Di bagian <head> ada link ke Google Fonts dan ke file imlek.css. Di dalam <body> ada tiga kelompok elemen utama.
Pertama adalah empat lantern, masing-masing terdiri dari tiga div yaitu string (tali), body (badan berisi karakter 福), dan tassel (rumbai bawah). Kedua adalah tujuh angpao dengan karakter berbeda (福喜财禄) yang akan jatuh dari atas. Ketiga adalah .stage yang berisi seluruh konten tengah, mulai dari badge tahun, judul utama, karakter Mandarin, garis pembatas, teks subtitle, hingga empat karakter blessing di bagian bawah.


### kode css

```bash
@import url('https://fonts.googleapis.com/css2?family=Ma+Shan+Zheng&family=Noto+Serif+SC&display=swap');

:root {
  --gold: #f5c518;
  --gold-light: #ffe87c;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  overflow: hidden;
  background: radial-gradient(ellipse at top, #8b0000, #3d0000 50%, #0f0000);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Noto Serif SC', serif;
  color: var(--gold);
}

/* ── Lanterns ── */
.lantern {
  position: fixed;
  top: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  transform-origin: top center;
  animation: swing 4s ease-in-out infinite;
}

.lantern-string {
  width: 2px;
  height: 40px;
  background: var(--gold);
}

.lantern-body {
  width: 50px;
  height: 75px;
  background: radial-gradient(ellipse at 40% 35%, #ff4444, #aa0000 60%, #600000);
  border-radius: 50% / 40%;
  border: 2px solid var(--gold);
  box-shadow: 0 0 20px rgba(255, 80, 0, 0.6);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Ma Shan Zheng', cursive;
  font-size: 26px;
  color: var(--gold-light);
  text-shadow: 0 0 8px var(--gold);
}

.lantern-tassel {
  width: 2px;
  height: 25px;
  background: linear-gradient(to bottom, var(--gold), transparent);
}

.l1 { left: 10%; animation-delay: 0s; }
.l2 { left: 25%; animation-delay: 0.8s; }
.l3 { right: 25%; animation-delay: 0.4s; }
.l4 { right: 10%; animation-delay: 1.2s; }

@keyframes swing {
  0%, 100% { transform: rotate(-10deg); }
  50%       { transform: rotate( 10deg); }
}

/* ── Falling angpao ── */
.angpao {
  position: fixed;
  top: -70px;
  width: 42px;
  height: 58px;
  background: linear-gradient(135deg, #e00020, #8a0010);
  border: 2px solid var(--gold);
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Ma Shan Zheng', cursive;
  font-size: 22px;
  color: var(--gold);
  animation: fall linear infinite;
}

@keyframes fall {
  0%   { transform: translateY(0) rotate(-10deg); opacity: 0; }
  10%  { opacity: 1; }
  100% { transform: translateY(110vh) rotate(20deg); opacity: 0.7; }
}

.a1 { left:  5%; animation-duration: 7s; animation-delay: 0.0s; }
.a2 { left: 18%; animation-duration: 9s; animation-delay: 1.5s; }
.a3 { left: 32%; animation-duration: 6s; animation-delay: 3.0s; }
.a4 { left: 50%; animation-duration: 8s; animation-delay: 0.5s; }
.a5 { left: 65%; animation-duration: 7s; animation-delay: 2.0s; }
.a6 { left: 80%; animation-duration: 9s; animation-delay: 1.0s; }
.a7 { left: 93%; animation-duration: 6s; animation-delay: 4.0s; }

/* ── Centre content ── */
.stage {
  text-align: center;
  z-index: 5;
  padding: 40px 50px;
}

.year-badge {
  display: inline-block;
  font-size: 13px;
  letter-spacing: 4px;
  color: rgba(245, 197, 24, 0.6);
  border: 1px solid rgba(245, 197, 24, 0.25);
  padding: 3px 16px;
  border-radius: 20px;
  margin-bottom: 20px;
}

.main-title {
  font-family: 'Ma Shan Zheng', cursive;
  font-size: 72px;
  color: var(--gold-light);
  animation: glow 3s ease-in-out infinite alternate;
  letter-spacing: 4px;
}

.cjk-title {
  font-family: 'Ma Shan Zheng', cursive;
  font-size: 44px;
  letter-spacing: 10px;
  opacity: 0.8;
  margin-top: 6px;
}

@keyframes glow {
  from { text-shadow: 0 0 15px rgba(255,180,0,0.6), 0 0 40px rgba(255,80,0,0.3); }
  to   { text-shadow: 0 0 30px rgba(255,220,0,1),   0 0 80px rgba(255,60,0,0.6); }
}

.divider {
  width: 160px;
  height: 1px;
  background: linear-gradient(to right, transparent, var(--gold), transparent);
  margin: 20px auto;
}

.subtitle {
  font-size: 16px;
  color: #fff8e7;
  opacity: 0.7;
  line-height: 1.9;
}

.blessings {
  display: flex;
  justify-content: center;
  gap: 24px;
  margin-top: 24px;
}

.blessing-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
}

.blessing-char {
  font-family: 'Ma Shan Zheng', cursive;
  font-size: 34px;
  animation: float 4s ease-in-out infinite;
}

.blessing-label {
  font-size: 10px;
  letter-spacing: 2px;
  opacity: 0.5;
  text-transform: uppercase;
}

.b1 .blessing-char { animation-delay: 0.0s; }
.b2 .blessing-char { animation-delay: 0.4s; }
.b3 .blessing-char { animation-delay: 0.8s; }
.b4 .blessing-char { animation-delay: 1.2s; }

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50%       { transform: translateY(-6px); }
}

@media (max-width: 600px) {
  .main-title { font-size: 46px; }
  .cjk-title  { font-size: 28px; }
  .stage      { padding: 30px 20px; }
}

```
#### penjelasan
File ini mengatur tampilan dan animasi semua elemen. Di bagian atas ada :root dengan dua variabel warna emas yang dipakai berulang di seluruh file. Lalu body menggunakan radial-gradient untuk background merah gelap, dengan flexbox untuk memusatkan konten.
Lantern diberi position: fixed agar menempel di atas layar, dan animasi swing membuatnya berayun kiri-kanan lewat rotate. Body lantern menggunakan radial-gradient untuk efek cahaya dari dalam, sementara border-radius: 50% / 40% memberi bentuk oval khas lampion.
Angpao juga position: fixed dengan top: -70px sebagai titik mulai, lalu animasi fall menggerakkannya ke bawah lewat translateY(110vh) sambil sedikit berotasi dan memudar. Setiap angpao punya animation-duration dan animation-delay yang berbeda agar jatuhnya tidak bersamaan.
Di bagian konten, .main-title punya animasi glow yang mengubah intensitas text-shadow secara bergantian untuk efek berpendar. Empat karakter blessing masing-masing bergerak naik-turun lewat animasi float dengan animation-delay berbeda agar gerakannya tampak hidup dan tidak sinkron.
![Alt 1](https://raw.githubusercontent.com/didiksetia1/asset/refs/heads/main/Screenshot%202026-03-13%20224439.png)