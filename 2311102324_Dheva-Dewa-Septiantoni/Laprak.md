<div align="center">
  <h3>LAPORAN PRAKTIKUM<br>APLIKASI BERBASIS PLATFORM</h3>
  <h>
  <br>
  <h3>MODUL 3<br>HTML & CSS</h3>
  <br>
  <img src="assets/logotelu.png" alt="Logo Telkom" width="200">
  <br>
  <br>

**Disusun Oleh :**<br>
Dheva Dewa Septiantoni<br>
2311102324<br>
IF-11-01
<br>
<br>

**Dosen Pengampu :**<br>
Dimas Fanny Hebrasianto Permadi, S.ST., M.Kom
<br>
<br>

**Assisten Praktikum :**<br>
Apri Pandu Wicaksono<br>
Rangga Pradarrell Fathi
<br>
<br>

PROGRAM STUDI S1 TEKNIK INFORMATIKA<br>
FAKULTAS INFORMATIKA<br>
UNIVERSITAS TELKOM PURWOKERTO<br>
2026

</div>

---

## 1. Dasar Teori

**HTML (HyperText Markup Language)** merupakan bahasa markah standar web yang digunakan untuk membuat dan menyusun struktur sebuah halaman website. HTML bekerja menggunakan sederet tag bersarang (*nested element*) untuk memberi tahu *web browser* bagaimana cara menampilkan elemen teks, gambar, maupun layout secara keseluruhan di layar.

Dalam pembuatan struktur tabel murni menggunakan HTML (tanpa bantuan *Cascading Style Sheets* atau CSS), digunakan format elemen `<table>` yang didukung oleh tag pendukungnya:
- `<thead>` — mengelompokkan baris header tabel.
- `<tbody>` — mengelompokkan baris isi data tabel.
- `<tr>` — mendefinisikan satu baris dalam tabel.
- `<th>` — mendefinisikan sel header (teks tebal dan rata tengah secara default).
- `<td>` — mendefinisikan sel data biasa.

HTML juga menyediakan atribut `rowspan` untuk menggabungkan beberapa baris secara vertikal dan `colspan` untuk menggabungkan beberapa kolom secara horizontal. Atribut presentasi lama yang masih sering diajarkan meliputi `border`, `cellpadding`, dan `cellspacing` pada tag `<table>`, serta tag `<center>` untuk meratakan konten ke tengah layar.

---

## 2. Penjelasan Kode HTML

Berikut ini adalah implementasi tabel berdasarkan struktur dasar HTML murni beserta hasil tampilannya.

### Kode HTML (`table.html`)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tabel Dasar</title>
</head>
<body>
        <table border="1" align="center">
    <tr>
        <th>NIM</th>
        <th>Nama</th>
        <th>Status</th>
    </tr>
    <tr>
        <td>2311102324</td>
        <td>Dheva Dewa Septiantoni</td>
        <td>Saya</td>
    </tr>
    <tr>
        <td>2312345678</td>
        <td>Cristiano Ronaldo</td>
        <td>My Goat</td>
    </tr>
    <tr>
        <td>2323456789</td>
        <td>Lionel Messi</td>
        <td>My Goat Also</td>
    </tr>
</table>
</body>
</html>
```

### Hasil Tampilan (Screenshot)

![Tabel HTML](assets/image.png)

### Penjelasan code:

- Tag Utama: `<table border="1" align="center">`
Ini adalah "kerangka" utamanya.<br>
`border="1"`: Tanpa CSS, tabel secara default tidak punya garis. Atribut ini memberikan bingkai setebal 1 pixel agar kotak-kotak tabelnya terlihat. <br>
`align="center"`: Inilah kunci dari permintaanmu. Atribut ini memerintahkan browser untuk meletakkan seluruh blok tabel tepat di tengah secara horizontal terhadap lebar layar.

2. Baris Judul: `<tr>` dan `<th>`
`<tr>` (Table Row): Digunakan untuk membuat satu baris baru dalam tabel.<br>
`<th>` (Table Header): Digunakan untuk sel judul. Secara default, teks di dalam `<th>` akan otomatis menjadi tebal (bold) dan posisinya di tengah (center) di dalam sel tersebut.
3. Baris Data: `<td>`
`<td>` (Table Data): Ini adalah isi sel biasa. Berbeda dengan `<th>`, teks di sini akan rata kiri dan tidak tebal.

## Refrensi
- [Materi Modul 2](https://drive.google.com/file/d/1Gcsi-U4rzqU0GC6dYTlzO7KUthrGoL8q/view?usp=sharing)
- [MDN Web Docs — HTML Table Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)
- [MDN Web Docs — rowspan & colspan](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td#attributes)