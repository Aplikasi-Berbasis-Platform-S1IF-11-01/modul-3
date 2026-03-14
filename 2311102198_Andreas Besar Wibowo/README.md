<div align="center">
  <br />

  <h1>LAPORAN PRAKTIKUM <br>
  APLIKASI BERBASIS PLATFORM
  </h1>

  <br />

  <h3>MODUL IV <br>
  CSS - Cascading Style Sheet
  </h3>

  <br />

  <img src="Images/Logo Telkom.png" alt="Logo" width="300">

  <br />
  <br />
  <br />

  <h3>Disusun Oleh :</h3>

  <p>
    <strong>Andreas Besar Wibowo</strong><br>
    <strong>2311102198</strong><br>
    <strong>S1 IF-11-REG01</strong>
  </p>

  <br />

  <h3>Dosen Pengampu :</h3>

  <p>
    <strong>Dimas Fanny Hebrasianto Permadi, S.ST., M.Kom</strong>
  </p>
  
  <br />
    <h4>Asisten Praktikum :</h4>
    <strong>Apri Pandu Wicaksono </strong> <br>
    <strong>Rangga Pradarrell Fathi</strong>
  <br />

  <h3>LABORATORIUM HIGH PERFORMANCE
 <br>FAKULTAS INFORMATIKA <br>UNIVERSITAS TELKOM PURWOKERTO <br>2026</h3>
</div>

<hr>

## Dasar Teori

### Pengenalan CSS
Cascading Style Sheets (CSS) merupakan bahasa yang membantu memperindah tampilan dari laman web yang telah dibangun dengan HTML. CSS mendeskripsikan bagaimana bentuk tampilan elemen HTML seharusnya saat ditampilkan pada laman browser.

Selector merupakan elemen HTML yang akan ditambahkan CSS kemudian diikuti dengan declaration block yang terdiri dari property elemen yang akan dirubah beserta value dari property-nya. Setiap deklarasi selector dapat merubah banyak nilai property sekaligus dengan dipisahkan dengan titik koma dan untuk semua declaration block dari satu selector berada di antara kurung kurawal.

#### 1. Cara Menyisipkan CSS
Terdapat tiga cara untuk menyisipkan atau mendefinisikan CSS ke dalam HTML, antara lain:
- External Style Sheet, Eksternal Style Sheet merupakan cara menyisipkan atau mendefinisikan CSS ke dalam HTML denganmemanggil file dengan ekstensi .css ke dalam file HTML. Pemanggilannya diletakkan di antara elemen `<head></head>` dengan menggunakan tag `<link/>`.
```css
<head
    <link rel="stylesheet" type="text/css" href="myStyleSheet.css">
</head>
```
- Internal Style Sheet, Internal Style Sheet merupakan cara menyisipkan atau mendefinisikan CSS ke dalam HTML dengan menggunakan tag `<style> </style>` pada elemen `<head></head>`. Biasanya digunakan ketika satu laman membutuhkan style CSS yang berbeda dari yang telah dipanggil pada Eksternal Style Sheet.
```css
<head>
    <style>
        body {
            background-color: blue;
        }

    h1 {
        color: maroon;
        margin-left: 40px;
    }
    </style>
</head>
```

- Inline Style, Inline Style menyisipkan atau mendefinisikan CSS ke dalam HTML dengan menambahkan atribut style pada elemen yang ingin ditambahkan CSS. Biasanya digunakan hanya untuk satu elemen yang membutuhkan style CSS yang berbeda dari yang telah didefinisikan pada Internal Style atau Eksternal Style.
```css
<h1 style="color:lightblue; font-size:30px;">Praktikum Web Programming< h1>
```

#### 2. Selector
Selector pada CSS digunakan untuk menemukan elemen HTML untuk diberi CSS berdasarkan selector yang didefinisikan. Bentuk selector ada beberapa antara lain nama elemen HTML, atribut ID dan atribut Class.
```css
/* Selector dengan Elemen HTML */
p {
    text-align: center;
    color: red;
}

/* Selector dengan Id Elemen HTML */
#para1 {
    text-align: center;
    color: red;
}

/* Selector dengan Class Elemen HTML */
p.center {
    text-align: center;
    color: red;
}
```
### Font Properties
Sebuah laman web tentunya tidak lepas oleh penggunaan teks, oleh karena itu memiliki tampilan teks yang tepat sangat diperlukan agar sebuah web memiliki tampilan yang baik dan menarik. CSS dapat menangani kebutuhan tampilan teks dengan font properties.

Contoh penerapannya sebagai berikut:
```css
p.example {
    font-family: Arial;
    font-size: 20px;
    color: ligh;
    dddddfont-style: italic;
    font-weight: bold;
}
```
### List Properties
Dalam HTML terdapat elemen yang berguna membuat sebuah list menggunakan simbol dan karakter. Tag yang digunakan adalah tag `<ul></ul>` atau `<ol></ol>`. Tag `<ul>` digunakan ketika akan menggunakan list dengan penanda berupa simbol atau bisa dikatakan unordered list, sedangkan tag `<ol>` digunakan ketika akan menggunakan list dengan penanda karakter yang memiliki urutan atau bisa dikatakan ordered list. Namun di dalam tag tersebut juga harus didefinisikan tag pendukung yaitu `<li></li>` untuk mendefinisikan elemen-elemen list yang akan ditampilkan. Untuk setiap tag ordered list atau unordered list memiliki satu atribut untuk mendefinisikan tipe simbol atau karakter yang akan digunakan yaitu atribut type. Contoh penerapan dan tipe masing-masing tag sebagai berikut:
```css
<h3>List of Property</h3>
<ol type="1">
    <li>
        Indoor
        <ul type="circle">
            <li>Sofa</li>
        </ul>
        <ul type="disc">
            <li>Tanaman Hias</li>
        </ul>
        <ul type="square">
            <li>Lampu Baca</li>
        </ul>
        <ul type="none">
            <li>Rak Buku</li>
        </ul>
    </li>

    <li>
        Outdoor
        <ol type="A">
            <li>Payung Pantai</li>
        </ol>
        <ol type="a">
            <li>Ayunan</li>
        </ol>
        <ol type="I">
            <li>Kursi Taman</li>
        </ol>
        <ol type="i">
            <li>Lampu Taman</li>
        </ol>
    </li>
</ol>
```
Dengan ditambahkan CSS pada elemen list, maka list yang ditampilkan dapat lebih menarik.

Contoh penerapannya sebagai berikut:
```css
Ul.listsatu {
    background-color: tomato;
    margin: 10px 5px 10px 5px;
    list-style-type: lower-alpha;
    list-style-position: inside;
}
ol.listdua {
    background-color: lightblue;
    list-style-type: lower-roman;
    padding: 5px 5px 15px 15px;
    list-style-position: inside;
}
```
### Alignment of Text
Pengaturan alignment pada sebuah teks juga dapat ditangani oleh CSS dengan properties.

Contoh penerapannya :
```css
h1 {
    text-align: center;
}
h2 {
    text-align: left;
}
h3 {
    text-align: right;
}
```
### Colors
Jika berbicara desain antar muka web, permasalahan tentang warna merupakan salah satu hal yang penting. Pada dasarnya Tag HTML dapat menangani pengaturan warna latar belakang atau teks menggunakan atribut dari HTML sendiri, namun CSS dapat menangani lebih baik dengan menawarkan pengaturan yang lebih lengkap.

Contoh penerapannya sebagai berikut :
```css
body {
    background-color: HSL(20%, 40%, 70%);
    color: orange;
}

#teks {
    color: #2F3CDF;
}

/*dengan opacity sebesar 0.5*/
input.text-field {
    background-color: RGBA(32, 55, 122, 0.5);
}
```
### Span & Div
Span merupakan elemen HTML yang dapat menangani perubahan konten elemen pada satu baris. Tag yang digunakan adalah `<span></span>`. Sedangkan Div merupakan elemen HTML yang digunakan untuk membuat section untuk beberapa elemen HTML di dalamnya. Tag yang digunakan yaitu `<div></div>`.

```css
<div class="section1">
    <p>Content of <span class="mark">Property</span></p>
</div>

<!-- CSS Properties -->
<style>
.section1 {
    background-color: lightgrey;
    padding: 10px 5px 10px 5px;
}

.mark {
    background-color: tomato;
    font-style: italic;
    font-weight: bold;
    padding: 10px 10px 10px 10px;
}
</style>
```
## Tugas
### Buat halaman untuk merayakan imlek ("karena bubub gua cina") hanya menggunakan css tanpa library dan tanpa js
```html
<!-- Andreas Besar Wibowo -->
<!-- 2311102198 / IF - 11 - 01 -->
 
<!DOCTYPE html>
<html>

<head>
    <title>Perayaan Imlek</title>

    <style>
        body {
            background: #8B0000;
            color: white;
            text-align: center;
            font-family: Arial;
        }

        .container {
            margin-top: 80px;
        }

        h1 {
            font-size: 60px;
            color: gold;
            text-shadow: 2px 2px 8px black;
        }

        .lampion {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            margin: 20px;
            border: 5px solid gold;
            display: inline-block;
            overflow: hidden;
        }

        .lampion img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .text {
            font-size: 25px;
            margin-top: 20px;
        }

        .gambar {
            width: 250px;
            margin-top: 20px;
            border: 4px solid gold;
            border-radius: 10px;
        }

        .lampion-container {
            margin-top: 30px;
        }
    </style>

</head>

<body>

    <div class="container">

        <h1>Gong Xi Fa Cai</h1>

        <img src="Images/china.png" class="gambar" alt="Dekorasi Imlek">

        <div class="lampion-container">

            <div class="lampion">
                <img src="Images/lampion.png" alt="Lampion 1">
            </div>

            <div class="lampion">
                <img src="Images/lampion.png" alt="Lampion 2">
            </div>

        </div>

        <p class="text">
            Selamat Tahun Baru Imlek<br>
            Semoga Tahun Ini Membawa Keberuntungan dan Rezeki
        </p>

    </div>

</body>

</html>
```
### Hasil
![Ouput 1](Images/Output%20Imlek.png)

Gambar diatas menampilkan halaman web sederhana yang menampilkan Imlek. Halaman ini dihiasi oleh gambar barongsai dan lampion serta menampilkan ucapan selamat tahun baru Imlek.