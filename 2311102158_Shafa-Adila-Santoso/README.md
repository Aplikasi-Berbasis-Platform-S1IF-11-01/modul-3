<div align="center">

# LAPORAN PRAKTIKUM  
# APLIKASI BERBASIS PLATFORM

## MODUL 2  
## HTML

<img src="assets/logo.jpeg" width="300">

### Disusun Oleh
**Shafa Adila Santoso**  
2311102158  
S1 IF-11-REG01  

### Dosen Pengampu
**Dimas Fanny Hebrasianto Permadi, S.ST., M.Kom**

### Asisten Praktikum
Apri Pandu Wicaksono  
Rangga Pradarrell Fathi  

### LABORATORIUM HIGH PERFORMANCE  
FAKULTAS INFORMATIKA  
UNIVERSITAS TELKOM PURWOKERTO  
2026

</div>

---

<div align="justify">

# 1. Dasar Teori

## 1. Cascading Style Sheets (CSS)

Cascading Style Sheets (CSS) merupakan bahasa yang digunakan untuk mengatur tampilan halaman web yang dibuat menggunakan HTML. CSS berfungsi untuk menentukan bagaimana elemen HTML ditampilkan pada browser, seperti pengaturan warna, ukuran teks, tata letak, dan jarak antar elemen sehingga tampilan website menjadi lebih menarik dan terstruktur. Penulisan CSS terdiri dari selector dan declaration block. Selector digunakan untuk memilih elemen HTML yang akan diberi gaya, sedangkan declaration block berisi property dan value yang menentukan tampilan elemen tersebut.

## 2. Cara Menyimpan CSS

CSS dapat disisipkan ke dalam HTML dengan tiga cara yaitu:

1. External Style Sheet
CSS ditulis dalam file terpisah dengan ekstensi .css kemudian dihubungkan ke file HTML menggunakan tag `<link>` pada bagian `<head>`.

2. Internal Style Sheet
CSS ditulis langsung di dalam file HTML menggunakan tag `<style>` pada bagian `<head>`.

3. Inline Style
CSS ditambahkan langsung pada elemen HTML menggunakan atribut style. Biasanya digunakan untuk memberi gaya pada satu elemen tertentu.

## 3. Selector pada CSS

Selector digunakan untuk menentukan elemen HTML yang akan diberi gaya CSS. Selector dapat berupa nama elemen HTML, atribut id, maupun class. Dengan menggunakan selector, CSS dapat mengatur tampilan elemen secara spesifik sesuai kebutuhan desain halaman web.

## 4. Font Properties

Font properties digunakan untuk mengatur tampilan teks pada halaman web. Beberapa properti yang sering digunakan antara lain:

1. font-family untuk menentukan jenis huruf

2. font-size untuk mengatur ukuran teks

3. font-style untuk menentukan gaya teks seperti italic

4. font-weight untuk mengatur ketebalan teks seperti bold

Penggunaan font properties membantu membuat teks pada website lebih jelas dan menarik.

## 5. List Properties

HTML menyediakan elemen ordered list (`<ol>`) dan unordered list (`<ul>`) untuk membuat daftar. CSS dapat digunakan untuk mengatur tampilan list agar lebih menarik dengan beberapa properti seperti list-style-type, list-style-image, list-style-position, margin, padding, dan background-color.

## 6. Alignment of Text

CSS juga dapat digunakan untuk mengatur perataan teks menggunakan properti text-align. Nilai yang dapat digunakan antara lain left, right, center, dan justify untuk mengatur posisi teks pada halaman web.

## 7. Colors

CSS memungkinkan pengaturan warna pada teks dan latar belakang elemen HTML dengan properti color dan background-color. Penulisan warna dapat menggunakan beberapa format seperti nama warna, RGB, Hexadecimal, HSL, serta RGBA atau HSLA yang mendukung transparansi.

## 8. Span dan Div

Elemen span digunakan untuk memberi gaya pada bagian teks tertentu dalam satu baris, sedangkan div digunakan untuk membuat bagian atau section yang berisi beberapa elemen HTML. Dengan bantuan CSS, elemen tersebut dapat digunakan untuk mengatur tata letak dan tampilan halaman web dengan lebih terstruktur.

---

## UNGUIDED

**Code HTML**

```html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Ucapan Imlek</title>

<link rel="stylesheet" href="style.css">

</head>
<body>

<header>

<h1>Selamat Tahun Baru Imlek</h1>
<p>Gong Xi Fa Cai</p>

</header>


<section class="greeting">

<h2>SHAFA ADILA SANTOSO - 2311102158</h2>

<p>
Semoga tahun baru ini membawa kebahagiaan,
kesehatan, kemakmuran, dan keberuntungan
bagi kita semua.
</p>

</section>


<section class="cards">

<div class="card">
<h3>Keberuntungan</h3>
<p>Semoga keberuntungan selalu menyertai hidupmu.</p>
</div>

<div class="card">
<h3>Kemakmuran</h3>
<p>Semoga rezeki melimpah sepanjang tahun.</p>
</div>

<div class="card">
<h3>Kebahagiaan</h3>
<p>Semoga keluarga selalu diberi kebahagiaan.</p>
</div>

</section>

<footer>

Happy Chinese New Year

</footer>

</body>
</html>
```

Kode HTML tersebut digunakan untuk membuat halaman web sederhana bertema ucapan Tahun Baru Imlek. Struktur halaman dimulai dengan deklarasi `<!DOCTYPE html>` dan elemen `<html>` yang menandakan bahwa dokumen menggunakan HTML5 dengan bahasa Indonesia. Pada bagian `<head>` terdapat pengaturan karakter (UTF-8), viewport untuk tampilan responsif di perangkat mobile, judul halaman, serta pemanggilan file CSS eksternal style.css untuk mengatur desain tampilan. Di dalam `<body>`, terdapat beberapa bagian utama yaitu header yang menampilkan judul “Selamat Tahun Baru Imlek” dan ucapan “Gong Xi Fa Cai”, kemudian section greeting yang berisi nama pembuat dan pesan harapan tahun baru, serta section cards yang menampilkan tiga kartu informasi mengenai harapan seperti keberuntungan, kemakmuran, dan kebahagiaan. Terakhir, terdapat footer yang menampilkan teks “Happy Chinese New Year” sebagai penutup halaman. Struktur ini memanfaatkan elemen semantik HTML seperti header, section, div, dan footer untuk membuat halaman lebih terorganisir dan mudah dipahami.

---

**Code CSS**

```css
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Segoe UI',sans-serif;
}


body{
min-height:100vh;
color:white;
overflow-x:hidden;


background:
radial-gradient(circle at 20% 30%, rgba(255,80,80,0.25), transparent 40%),
radial-gradient(circle at 80% 70%, rgba(255,120,0,0.18), transparent 40%),
radial-gradient(circle at 50% 50%, rgba(255,255,255,0.03), transparent 60%),
linear-gradient(140deg,#4b0f19,#6b0f1c,#4b0f19);

}



body::before{
content:"";
position:fixed;
top:0;
left:0;
width:100%;
height:100%;

background-image:

repeating-radial-gradient(
circle at 0 0,
rgba(255,255,255,0.04) 0px,
rgba(255,255,255,0.04) 1px,
transparent 1px,
transparent 10px
),

repeating-linear-gradient(
120deg,
rgba(255,255,255,0.03) 0px,
rgba(255,255,255,0.03) 1px,
transparent 1px,
transparent 6px
);

mix-blend-mode:overlay;
pointer-events:none;
}



body::after{

content:"";
position:fixed;
width:100%;
height:100%;

background:
radial-gradient(circle, rgba(255,215,0,0.25) 1px, transparent 2px);

background-size:120px 120px;

opacity:0.25;

pointer-events:none;

}


/*HEADER*/

header{

text-align:center;
padding:120px 20px 60px;

}

header h1{

font-size:60px;
color:#ffd700;

text-shadow:
0 0 10px #ffd700,
0 0 30px rgba(255,215,0,0.7);

}

header p{

margin-top:15px;
font-size:22px;
color:#f5e6c4;

}


/*UCAPAN*/

.greeting{

text-align:center;
max-width:800px;
margin:auto;
padding:40px 20px;

}

.greeting h2{

font-size:36px;
color:#ffd700;
margin-bottom:20px;

}

.greeting p{

font-size:18px;
line-height:1.8;
color:#f5e6c4;

}


/*CARDS*/

.cards{

display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:30px;

max-width:1100px;
margin:auto;

padding:60px 20px;

}

.card{

background:rgba(0,0,0,0.35);
border:1px solid rgba(255,215,0,0.5);

border-radius:15px;

padding:30px;

text-align:center;

backdrop-filter:blur(5px);

transition:0.3s;

}

.card:hover{

transform:translateY(-8px);

box-shadow:0 10px 25px rgba(255,215,0,0.4);

}

.card h3{

color:#ffd700;
margin-bottom:10px;

}

.card p{

color:#f5e6c4;

}


/* FOOTER*/

footer{

text-align:center;
margin-top:50px;

padding:30px;

border-top:1px solid rgba(255,215,0,0.5);

color:#f5e6c4;

}
```

Kode CSS tersebut digunakan untuk mengatur tampilan desain halaman web ucapan Tahun Baru Imlek. Pada bagian awal terdapat reset CSS untuk menghilangkan margin dan padding bawaan browser serta mengatur font agar konsisten. Bagian **body** memberikan latar belakang berwarna maroon dengan efek gradient dan tekstur tambahan menggunakan pseudo-element `::before` dan `::after` sehingga terlihat lebih dekoratif. Selanjutnya **header** mengatur tampilan judul dan teks pembuka, **.greeting** menata teks ucapan di tengah halaman, dan **.cards** menggunakan CSS Grid untuk menampilkan beberapa kartu informasi. Setiap **.card** memiliki efek transparan, border emas, dan animasi hover agar terlihat lebih interaktif. Terakhir, **footer** menampilkan teks penutup di bagian bawah halaman.


---

**Output :**

<p align="center">
<img src="assets/ss-hasil.png\" width="1000">
</p>

# 2. REFERENSI

- [Materi Modul 3](https://drive.google.com/file/d/1kd7ogQkR_rsNCnKDcJDmavY8FiOyTLzs/view?usp=sharing)