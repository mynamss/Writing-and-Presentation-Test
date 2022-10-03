# Writing and Presentation Test Week 2

## JavaScript Dasar

**Scope dan Function**

- Scope adalah konsep dalam flow data variable yang menentukan suatu variable bisa diakses pada scope tertentu atau tidak.
- Blocks adalah kode yang berada di dalam _curly braces_ `{}`. Contohnya adalah _conditional_, _function_, dan _looping_.
- Scope ada dua macam yaitu,

  - Global scope , yaitu variabel yang dibuat bisa diakses dimanapun dalam suatu file. Letaknya yaitu berada di luar blocks.

  ```javascript
  let city = "Semarang";

  function bigCity() {
    return city; // Semarang
  }
  console.log(city); // Semarang
  ```

  \*Dari kode di atas, variabel `city` merupakan global scope sehingga bisa diakses dari manapun (dalam ataupun luar blocks).

  - Local scope, yaitu mendeklarasikan variabel di dalam block yang mana variabel hanya bisa diakses di dalam blocks saja.

  ```javascript
  function heroName() {
    let hero = "Jendral Soedirman";
    return hero; //
  }
  console.log(heroName()); // Jendral Soedirman
  console.log(hero); // ReferenceError: hero is not defined because local scope
  ```

  \*Dari kode di atas, variabel hero bisa diakses dari dalam function. Namun, error ketika diakses dari luar function.

- Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/ 1 fitur.
- Membuat Function :
  ```javascript
  function ucapan() {
    return "Selamat Datang";
  }
  ```
- Memanggil function
  Untuk memanggil function dan memunculkan output yaitu dengan memanggil nama function-nya.
  ```javascript
  ucapan();
  console.log(ucapan());
  ```
- Paramater Function
  Dengan paramater, function dapat menerima inputan dannmenggunakannya untuk melakukan task/tugas.
  ```javascript
  function luasPersegi(sisi) {
    return sisi * sisi;
  }
  ```
- Argumen Function
  Argumen adalah nilai yang digunakan saat memanggil function. Jumlah argumen harus sama dengan jumlah paramaternya.
  ```javascript
  function luasPersegi(sisi) {
    return sisi * sisi;
  }
  console.log(luasPersegi(8));
  ```
- Default paramater digunakan untuk memberikan nilai awal pada paramater function. Tujuannya adalah agar function tidak erro saat dipanggil tanpa argumen.
- Kita bisa menggunakan function yang sudah dibuat pada function lain.
- Arrow function adalah cara lain menuliskan function. Fitur ini adaalah fitur baru yang ada di ES6.

**Data Types Built in Prototype and Methods**

- Tipe data adalah jenis-jenis data yang bisa kita simpan di dalam variabel.
- Di JavaScript ada 6 jenis tipe data, yaitu
  - String
  - Number
  - Boolean
  - Null
  - Undefined
  - Object
- JavaScript akan otomatis mengenali tipe data yang diberikan pada suatu variabel.
- Property dan Methods adalah tambahan yang ada di setiap tipe data yang disediakan oleh JavaScript untuk memudahkan proses development.
- Cara untuk memanggil property dan methods yaitu dengan menambahkan titik setelah nama variabel, maka sesuai tipe datanya akan muncul berbagai property dan methods sesuai tipe datanya.
- Khusus tipe data string, hanya memiliki 1 property yaitu `string.length` yang digunakan untuk mengetahui panjang karakter dari string.
  ```javascript
  let laptop = "Lenovo";
  laptop.length; // 6
  ```
  **DOM HTML dan JavaScript**
- DOM adalah kepanjangan dari Document Object Model.
- DOM merupakan cara memanipulasi HTML agar website terlihat lebih dinamis dan interaktif.
- Cara memanggil DOM yaitu
  - memanggil element HTML berdasarkan ID
    `document.getElementById("check")`
  - memanggil element HTML berdasarkan Class Name
    `document.getElementsByClassName("text-color-red")`
  - memanggil element HTML berdasarkan Query selector
    `document.querySelector("#check")`
    `document.querySelectorAll(".example")`
- Cara memanipulasi konten :

1. Membuat file HTML dan JavaScript. Lalu hubungkan keduanya.
2. Setelah itu, buat sebuah element, header misalnya dan tambahkan id ke dalam element tersebut.  
   index.html :
   ```html
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <meta http-equiv="X-UA-Compatible" content="IE=edge" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>Document</title>
     </head>
     <body>
       <header id="header">Header Websiteku</header>
       <script src="script.js"></script>
     </body>
   </html>
   ```
   script.js
   ```javascript
   document.getElementById("header").textContent = "Ini Heading Web";
   ```
3. Hasilnya, yang awalnya konten di header adalah "Header Websiteku" berubah menjadi "Ini Heading Web".

- Selain contoh di atas,masih ada banyak hal yang bisa dilakukan oleh DOM, seperti
  - membuat element : `document.createElement("p")`
  - membuat child ke dalam parent : `app.append(p)`
  - menghapus element : `end.remove()`
  - menambahkan atribut : `link.getAttribute("href")`
  - memberikan style : `link.style.color = "black"`
  - mendapatkan style dari element : `getComputedStyle(coba)`
  - dan masih banyak lagi.

**DOM Events & Forms**

- DOM Events merupakan objek model yang berfungsi untuk membantu interaksi user dengan document HTML.
- Macam macam HTML DOM Events :

  - Click
  - Scroll
  - Change
  - Focus
  - Hover
  - Submit
  - Blur

- Untuk menangkap interaksi user dapat menggunakan :

  - Element.addEventListener("event")
  - Element.onevent

- 3 cara memberikan event :

  - HTML Attributes
  - Event Property
  - addEventListener()

- Contoh EventListener

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta http-equiv="X-UA-Compatible" content="IE=edge" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Document</title>
    </head>
    <body>
      <button id="btn-hello">Coba</button>

      <script>
        let button = document.getElementById("btn-hello");
        button.onclick = function () {
          alert("Halo Skilvul");
        };
      </script>
    </body>
  </html>
  ```

  Note : Ketika tombol "Coba' di atas di klik, maka akan menampilkan pop up dengan tulisan "Halo Skilvul".

- Form

  - Misalkan terdapat beberapa input dalam sebuah form `<input name="email"/>` dan `<input type="password" name="pass"/>`
  - Untuk mendapatkan isi dari kedua inputan tersebut terdapat 2 cara :
    - Memasang event listener di kedua input dan tombol submit, lalu saat tombol diklik, baca value dari kedua input tersebut
    - Memasang event listener di form, lalu gunakan FormData untuk menggambil data dari masing-masing input

  ```javascript
  const form = document.getElementById("form")

  form.addEventListener("submit", function(event)){
  event.preventDefault()

  const formData = new FormData(form)
  const values = Object.fromEntries(formData) {
    email: ....
    }
  }
  ```