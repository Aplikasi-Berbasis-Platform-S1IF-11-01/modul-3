<div align="center">
  <br />
  <h1>LAPORAN PRAKTIKUM <br>APLIKASI BERBASIS PLATFORM</h1>
  <br />
  <h3>MODUL 3 <br> CSS - CASCADING STYLE SHEET</h3>
  <br />
  <br />
  <img src="Telkom.png" alt="Logo" width="300"> 
  <br />
  <br />
  <br />
  <br />
  <h3>Disusun Oleh :</h3>
  <p>
    <strong>Bayu Kuncoro Adi</strong><br>
    <strong>2311102031</strong><br>
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

**CSS (Cascading Style Sheets)** adalah bahasa yang digunakan bersamaan dengan HTML untuk mengatur tampilan visual pada halaman web. Apabila HTML berfungsi sebagai struktur atau kerangka dasar dari sebuah halaman, maka CSS berperan untuk mempercantik tampilannya, seperti mengatur warna, tata letak, ukuran elemen, hingga berbagai aspek dekoratif lainnya.

CSS bekerja dengan cara memilih elemen HTML menggunakan **selector**, seperti tag, *class*, atau *id*, lalu menerapkan aturan gaya melalui berbagai properti, misalnya warna, ukuran teks, jarak antar elemen, dan lain sebagainya. Dengan penerapan CSS, struktur konten (HTML) dapat dipisahkan dari tampilan visualnya (CSS). Pemisahan ini membuat kode menjadi lebih rapi, terstruktur, serta memudahkan proses pengelolaan dan pembaruan pada halaman web.

Secara umum terdapat tiga metode untuk menambahkan CSS ke dalam dokumen HTML, yaitu:

1. **Inline CSS**  
   Gaya dituliskan langsung pada elemen HTML menggunakan atribut `style`.

2. **Internal CSS**  
   Aturan CSS ditulis di dalam tag `<style>` yang ditempatkan pada bagian `<head>` dokumen HTML.

3. **External CSS**  
  Aturan CSS umumnya disimpan dalam file terpisah yang memiliki ekstensi `.css`, kemudian dihubungkan dengan file HTML menggunakan tag `<link>`. Metode ini menjadi praktik yang paling direkomendasikan dalam pengembangan web karena membantu menjaga kerapian dan struktur kode. Selain itu, pemisahan file CSS dari HTML juga memudahkan pengelolaan dan pemeliharaan kode, terutama ketika digunakan pada proyek web yang lebih besar dan kompleks.


## 2. Penjelasan Kode HTML dan CSS

Berikut ini adalah implementasi desain kartu ucapan yang digabungkan antara struktur kerangka dasar HTML murni dan desain modern visual yang diambil dari *External CSS*, beserta hasil tampilannya.

### Kode HTML (`imlek.html`)

```html
<!DOCTYPE html>
<html lang="id">
<head>

<meta charset="UTF-8">
<title>Chinese New Year Celebration</title>

<link rel="stylesheet" href="style.css">

</head>
<body>

<!-- Background effect -->
<div class="glow glow1"></div>
<div class="glow glow2"></div>

<!-- Lampion -->
<div class="lantern l1"></div>
<div class="lantern l2"></div>
<div class="lantern l3"></div>

<!-- Konten utama -->
<div class="card">

<h1>恭喜发财</h1>

<h2>Happy Chinese New Year</h2>

<p class="message">
Semoga tahun baru ini membawa keberuntungan,
kesehatan, kebahagiaan, dan rezeki yang melimpah
bagi kita semua.
</p>

<div class="divider"></div>

<p class="author">
Ucapan dari <br>
<b>Bayu Kuncoro Adi</b><br>
2311102031 • IF 11 01
</p>

</div>

</body>
</html>
```

### Kode CSS (`style.css`)

```css
body{
margin:0;
height:100vh;
overflow:hidden;
font-family:'Segoe UI',sans-serif;
background:#0f0f14;
color:white;
display:flex;
justify-content:center;
align-items:center;
}

/* glowing background */

.glow{
position:absolute;
width:500px;
height:500px;
border-radius:50%;
filter:blur(150px);
opacity:0.5;
}

.glow1{
background:#ff003c;
top:-150px;
left:-150px;
}

.glow2{
background:#ffb300;
bottom:-200px;
right:-150px;
}

/* card modern */

.card{

width:420px;
padding:40px;

background:rgba(255,255,255,0.05);
backdrop-filter:blur(10px);

border-radius:20px;
border:1px solid rgba(255,255,255,0.1);

text-align:center;

box-shadow:
0 0 30px rgba(255,0,0,0.3);
}

/* heading */

h1{
font-size:64px;
margin:0;
color:#ffd700;
letter-spacing:4px;
}

h2{
margin-top:10px;
font-weight:300;
color:#ff4d4d;
}

/* pesan */

.message{
margin-top:20px;
line-height:1.6;
color:#ddd;
}

/* divider */

.divider{
width:60%;
height:1px;
background:linear-gradient(to right,transparent,gold,transparent);
margin:25px auto;
}

/* author */

.author{
font-size:14px;
color:#bbb;
}

.author b{
color:gold;
font-size:18px;
}

/* lantern modern */

.lantern{
position:absolute;
width:40px;
height:60px;

background:linear-gradient(#ff0000,#b30000);

border-radius:50% 50% 40% 40%;

box-shadow:
0 0 20px red,
0 0 40px red;

animation:float 4s ease-in-out infinite;
}

.lantern::after{
content:"";
width:3px;
height:30px;
background:gold;
position:absolute;
bottom:-30px;
left:50%;
transform:translateX(-50%);
}

.l1{
top:80px;
left:10%;
}

.l2{
top:60px;
right:15%;
animation-delay:1s;
}

.l3{
top:120px;
right:40%;
animation-delay:2s;
}

/* animasi */

@keyframes float{

0%{
transform:translateY(0);
}

50%{
transform:translateY(-15px);
}

100%{
transform:translateY(0);
}

}
```

### Hasil Tampilan (Screenshot)

![Hasil Tampilan HTML & CSS](assets/1.jpeg)
### Penjelasan Code

#### 1. HTML

Program HTML di atas digunakan untuk membuat sebuah halaman web sederhana yang menampilkan ucapan perayaan Tahun Baru Imlek dengan tampilan modern. Pada **baris pertama** terdapat deklarasi `<!DOCTYPE html>` yang berfungsi untuk memberi tahu browser bahwa dokumen tersebut menggunakan standar **HTML5**. Selanjutnya pada **tag `<html lang="id">`** ditentukan bahwa bahasa utama yang digunakan pada halaman tersebut adalah **Bahasa Indonesia**, sehingga browser maupun mesin pencari dapat mengenali bahasa yang digunakan pada konten halaman.

Bagian **`<head>`** berisi informasi dasar mengenai halaman web. Di dalamnya terdapat **`<meta charset="UTF-8">`** yang berfungsi untuk mengatur sistem pengkodean karakter agar halaman dapat menampilkan berbagai jenis karakter dengan benar, termasuk karakter khusus seperti huruf Mandarin yang digunakan pada judul halaman. Kemudian terdapat **`<title>`** yang berfungsi untuk menentukan judul halaman yang akan ditampilkan pada tab browser, yaitu *“Chinese New Year Celebration”*. Selain itu, terdapat juga tag **`<link rel="stylesheet" href="style.css">`** yang digunakan untuk menghubungkan dokumen HTML dengan file CSS eksternal bernama **style.css**, sehingga seluruh pengaturan tampilan dan desain visual halaman akan diatur melalui file CSS tersebut.

Bagian **`<body>`** merupakan bagian utama yang berisi seluruh elemen yang akan ditampilkan pada halaman web. Pada bagian awal terdapat dua elemen `<div>` dengan kelas **`glow glow1`** dan **`glow glow2`** yang berfungsi sebagai elemen dekoratif untuk menampilkan efek cahaya pada latar belakang halaman. Efek ini biasanya diatur melalui CSS untuk menciptakan nuansa visual yang lebih menarik dan modern.

Setelah itu terdapat beberapa elemen `<div>` dengan kelas **`lantern`**, yaitu **`lantern l1`**, **`lantern l2`**, dan **`lantern l3`**. Elemen-elemen ini digunakan untuk menampilkan dekorasi **lampion khas perayaan Imlek**. Setiap lampion diberi kelas tambahan (`l1`, `l2`, `l3`) agar dapat diatur posisinya secara berbeda melalui CSS, sehingga tampilan halaman menjadi lebih dinamis dan tidak monoton.

Bagian berikutnya merupakan **konten utama halaman** yang dibungkus dalam elemen `<div>` dengan kelas **`card`**. Elemen ini berfungsi sebagai wadah utama yang menampilkan pesan ucapan Tahun Baru Imlek dalam bentuk sebuah kartu modern di tengah halaman. Di dalamnya terdapat tag **`<h1>`** yang menampilkan tulisan Mandarin **“恭喜发财”**, yang merupakan ucapan populer dalam perayaan Imlek yang berarti harapan agar seseorang memperoleh kemakmuran dan keberuntungan. Kemudian terdapat tag **`<h2>`** yang menampilkan terjemahan ucapan tersebut dalam bahasa Inggris, yaitu **“Happy Chinese New Year”**.

Selanjutnya terdapat elemen **`<p class="message">`** yang berisi pesan ucapan Tahun Baru Imlek dalam bentuk paragraf. Pesan ini menyampaikan harapan agar tahun baru membawa keberuntungan, kesehatan, kebahagiaan, dan rezeki yang melimpah bagi semua orang. Setelah pesan tersebut, terdapat elemen **`<div class="divider">`** yang berfungsi sebagai garis pemisah visual antara isi ucapan dengan informasi pembuat halaman. Elemen ini biasanya digunakan untuk memperjelas struktur tampilan pada halaman.

Pada bagian akhir kartu terdapat elemen **`<p class="author">`** yang berisi informasi mengenai pembuat ucapan tersebut. Di dalamnya terdapat teks **“Ucapan dari”** yang diikuti dengan nama pembuat yaitu **Bayu Kuncoro Adi**, yang ditandai menggunakan tag **`<b>`** agar tampil lebih menonjol. Di bawahnya juga dicantumkan **NIM 2311102031** serta **kelas IF 11 01**, yang menunjukkan identitas pembuat halaman sebagai bagian dari tugas atau proyek yang dikerjakan.

Secara keseluruhan, struktur HTML pada program ini berfungsi sebagai **kerangka dasar halaman web** yang menampilkan ucapan Tahun Baru Imlek dengan elemen dekoratif seperti efek cahaya latar belakang dan lampion. Sementara itu, seluruh pengaturan tampilan visual seperti warna, posisi elemen, animasi, dan efek dekoratif lainnya diatur melalui file **CSS eksternal**, sehingga struktur HTML tetap rapi dan mudah untuk dipahami serta dikelola.


#### 2. Styling CSS (`style.css`)

Kode CSS di atas digunakan untuk mengatur tampilan visual halaman web yang menampilkan ucapan Tahun Baru Imlek dengan gaya modern. Pada bagian awal terdapat aturan untuk elemen **`body`** yang berfungsi sebagai wadah utama seluruh konten halaman. Properti `margin:0` digunakan untuk menghilangkan jarak bawaan dari browser sehingga tampilan halaman menjadi penuh dari tepi ke tepi. Kemudian `height:100vh` membuat tinggi halaman mengikuti tinggi layar perangkat. Properti `overflow:hidden` digunakan agar elemen dekoratif yang berada di luar area layar tidak memunculkan scroll bar. Jenis huruf halaman diatur menggunakan `font-family:'Segoe UI', sans-serif` agar tampilan teks terlihat modern dan mudah dibaca. Warna latar belakang halaman diatur menggunakan `background:#0f0f14`, yaitu warna gelap yang memberikan nuansa elegan dan kontras dengan elemen dekoratif lainnya. Warna teks utama ditentukan dengan `color:white`. Selain itu, halaman menggunakan `display:flex` dengan `justify-content:center` dan `align-items:center` agar konten utama dapat berada tepat di tengah layar baik secara horizontal maupun vertikal.

Bagian berikutnya adalah aturan untuk kelas **`.glow`** yang digunakan untuk membuat efek cahaya pada latar belakang halaman. Elemen ini diposisikan menggunakan `position:absolute` sehingga dapat ditempatkan bebas di halaman tanpa memengaruhi tata letak elemen lain. Properti `width` dan `height` masing-masing diatur sebesar `500px` untuk membentuk area cahaya yang besar, kemudian `border-radius:50%` digunakan agar bentuknya menjadi lingkaran. Efek cahaya lembut dihasilkan menggunakan `filter:blur(150px)` sehingga warna lingkaran tampak menyebar seperti cahaya. Transparansi cahaya diatur dengan `opacity:0.5` agar tidak terlalu terang dan tetap menyatu dengan latar belakang. Kelas **`.glow1`** dan **`.glow2`** merupakan variasi dari elemen glow yang berfungsi mengatur posisi serta warna masing-masing cahaya. Pada `.glow1` digunakan warna merah terang (`#ff003c`) yang ditempatkan di bagian kiri atas halaman dengan properti `top:-150px` dan `left:-150px`. Sementara `.glow2` menggunakan warna emas (`#ffb300`) yang ditempatkan di bagian kanan bawah halaman menggunakan `bottom:-200px` dan `right:-150px`.

Selanjutnya terdapat aturan untuk kelas **`.card`** yang berfungsi sebagai wadah utama konten ucapan Tahun Baru Imlek. Elemen ini memiliki lebar `420px` dengan jarak dalam `padding:40px` agar isi kartu tidak terlalu menempel dengan tepinya. Tampilan kartu dibuat semi transparan menggunakan `background:rgba(255,255,255,0.05)` sehingga sedikit memperlihatkan latar belakang di belakangnya. Efek kaca buram atau **glassmorphism** dibuat menggunakan `backdrop-filter:blur(10px)` sehingga bagian belakang kartu terlihat samar. Bentuk sudut kartu dibuat melengkung dengan `border-radius:20px`, kemudian diberi garis tepi halus menggunakan `border:1px solid rgba(255,255,255,0.1)`. Teks di dalam kartu disejajarkan ke tengah dengan `text-align:center`. Selain itu, kartu juga memiliki efek bayangan menggunakan `box-shadow:0 0 30px rgba(255,0,0,0.3)` untuk memberikan kesan bercahaya yang selaras dengan tema perayaan Imlek.

Pada bagian pengaturan **heading**, elemen **`h1`** digunakan untuk menampilkan teks utama yaitu tulisan Mandarin. Ukuran huruf dibuat besar menggunakan `font-size:64px` agar menjadi fokus utama halaman. Properti `margin:0` digunakan untuk menghilangkan jarak bawaan dari elemen heading. Warna teks diatur menggunakan `color:#ffd700`, yaitu warna emas yang identik dengan simbol kemakmuran dalam budaya Tiongkok. Selain itu, `letter-spacing:4px` digunakan untuk memberikan jarak antar huruf sehingga tampilan teks terlihat lebih elegan. Untuk elemen **`h2`**, digunakan `margin-top:10px` untuk memberi sedikit jarak dari judul utama, `font-weight:300` agar ketebalan teks terlihat lebih ringan, serta `color:#ff4d4d` yang memberikan nuansa merah khas perayaan Imlek.

Selanjutnya terdapat pengaturan untuk kelas **`.message`** yang digunakan pada paragraf ucapan. Properti `margin-top:20px` memberikan jarak dari elemen sebelumnya, sedangkan `line-height:1.6` digunakan agar jarak antar baris teks lebih nyaman dibaca. Warna teks diatur dengan `color:#ddd` sehingga tidak terlalu terang namun tetap kontras dengan latar belakang gelap.

Untuk memperjelas pemisahan antara pesan ucapan dan identitas pembuat, digunakan elemen **`.divider`**. Elemen ini memiliki lebar `60%` dari kontainer dengan tinggi `1px` sehingga membentuk garis tipis. Garis ini diberi efek gradasi menggunakan `background:linear-gradient(to right, transparent, gold, transparent)` sehingga bagian tengah tampak berwarna emas sementara sisi kiri dan kanan memudar. Posisi garis berada di tengah kartu dengan `margin:25px auto`.

Bagian berikutnya adalah aturan untuk kelas **`.author`** yang menampilkan identitas pembuat ucapan. Ukuran teks dibuat lebih kecil menggunakan `font-size:14px` dengan warna abu-abu terang `color:#bbb` agar terlihat lebih halus dibandingkan teks utama. Namun, pada elemen **`.author b`** digunakan warna emas `color:gold` serta ukuran huruf yang lebih besar `font-size:18px` agar nama pembuat lebih menonjol dibandingkan informasi lainnya.

Selanjutnya terdapat pengaturan untuk elemen **`.lantern`** yang berfungsi sebagai dekorasi lampion khas perayaan Imlek. Lampion diposisikan secara bebas menggunakan `position:absolute` sehingga dapat ditempatkan di berbagai bagian halaman. Ukuran lampion dibuat menggunakan `width:40px` dan `height:60px`. Warna lampion dibuat menggunakan gradasi merah `background:linear-gradient(#ff0000,#b30000)` yang memberikan efek pencahayaan. Bentuk lampion dibuat menyerupai lampion tradisional menggunakan `border-radius:50% 50% 40% 40%`. Lampion juga memiliki efek cahaya menggunakan `box-shadow:0 0 20px red, 0 0 40px red` sehingga terlihat bercahaya. Untuk memberikan efek hidup, lampion dianimasikan menggunakan `animation:float 4s ease-in-out infinite` yang membuat lampion bergerak naik turun secara perlahan.

Bagian **`.lantern::after`** merupakan pseudo-element yang digunakan untuk membuat tali lampion. Elemen ini tidak memerlukan tag HTML tambahan karena dibuat langsung melalui CSS. Lebarnya `3px` dengan tinggi `30px` dan berwarna emas (`gold`). Posisi tali ditempatkan di bagian bawah lampion menggunakan `bottom:-30px` serta disejajarkan ke tengah menggunakan `left:50%` dan `transform:translateX(-50%)`.

Kemudian terdapat kelas **`.l1`**, **`.l2`**, dan **`.l3`** yang digunakan untuk mengatur posisi masing-masing lampion di halaman. Lampion pertama (`.l1`) ditempatkan di bagian kiri atas menggunakan `top:80px` dan `left:10%`. Lampion kedua (`.l2`) ditempatkan di bagian kanan atas dengan `top:60px` dan `right:15%`, serta diberi `animation-delay:1s` agar animasi bergeraknya tidak bersamaan dengan lampion lain. Lampion ketiga (`.l3`) ditempatkan sedikit lebih ke tengah menggunakan `top:120px` dan `right:40%` dengan `animation-delay:2s`.

Terakhir terdapat definisi **`@keyframes float`** yang digunakan untuk membuat animasi lampion. Animasi ini memiliki tiga tahap utama. Pada kondisi awal (`0%`) lampion berada pada posisi normal menggunakan `transform:translateY(0)`. Pada tahap tengah (`50%`) lampion bergerak naik sebesar `-15px` menggunakan `transform:translateY(-15px)`, sehingga terlihat seperti mengambang. Pada tahap akhir (`100%`) lampion kembali ke posisi awal. Animasi ini berlangsung selama 4 detik dengan pola gerakan halus (`ease-in-out`) dan diulang terus menerus (`infinite`), sehingga lampion tampak bergerak lembut seperti tertiup angin.

Secara keseluruhan, kode CSS ini berfungsi untuk menciptakan **tampilan halaman ucapan Tahun Baru Imlek yang modern**, dengan kombinasi latar belakang gelap, efek cahaya berwarna merah dan emas, kartu bergaya glassmorphism, tipografi elegan, serta dekorasi lampion yang dianimasikan agar halaman terlihat lebih hidup dan menarik.


## Refrensi
- [Materi Modul 3](https://drive.google.com/file/d/1kd7ogQkR_rsNCnKDcJDmavY8FiOyTLzs/view?usp=sharing)