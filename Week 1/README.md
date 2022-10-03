# Writing and Presentation Test Week 1

## Modul 1 - Unix Command Line

Secara umum, agar pengguna atau **_user_** bisa berinteraksi dengan sistem operasi komputer, ada program yang disebut dengan **_shell_**. Lalu, apa itu shell ? Ada berapa macamnya ? dan bagaimana cara mengaksesnya ?

1. **Tentang Shell**

   - Shell adalah program yang digunakan untuk berkomunikasi antara pengguna dengan sistem operasi komputer.  
     ![Shell](images/shell.png)
   - Shell dibagi menjadi dua berdasarkan tampilan _interface_-nya, yaitu

     1. GUI (_Graphical User Interface_) adalah tampilan antarmuka berbentuk grafis atau objek yang merepresentasikan perintah untuk menampilkan sesuatu. Contoh : File Explorer di Windows.
     2. CLI (_Command Line Interface_) adalah tampilan antarmuka berupa _terminal_ yang berbasis baris teks untuk memberikan perintah menjalankan suatu program, mengelola file, dan berinteraksi dengan komputer. Contoh : sh, bash, zsh, cmd.  
        ![GUIvsCLI](images/guiCli.png)

2. **Cara untuk mengakses CLI dan menggunakan terminal**
   - Untuk mengakses CLI, kita bisa menggunakan Terminal Emulator seperti CMD, Windows Powershell, Git Bash, dan lain - lain. Agar lebih mudah kedepannya, di sini kita akan menggunakan **Git Bash**.  
     ![search Git](images/gitBashLogo.jpg)
   - Git bisa di-_download_ melalui situs resminya [di sini](https://git-scm.com/downloads). Tutorial instalasi juga bisa ditemukan di internet. Ada banyak sekali website dan video di Youtube yang membahasnya.
   - Setelah di-_download_ dan _install_, buka Git Bash dengan mengetikkan `git bash` di kotak pencarian windows.  
     ![search Git](images/gitBash.png)
   - Selanjutnya akan terbuka jendela baru yang merupakan jendela dari Git Bash. Sampai proses ini kita sudah siap untuk menggunkan Git Bash.  
     ![Bash](images/tampilanCLI.png)
3. **File System**
   - _File system_ adalah sebuah cara untuk mengatur bagaimana data disimpan di dalam sebuah sistem.
   - Pada sistem operasi Windows dan UNIX-like, file dan direktori disusun menggunakan struktur yang bentuknya seperti _tree_.
     ![File System Structure](images/fileSystemStruct.png)
   - Biasanya, _root directory_ adalah direktori yang berada di tingkat paling atas.
   - Di OS Windows, _root_-nya adalah Local disk C: atau D:\. Sementara itu, untuk tampilan CLI, _root directory_ adalah tanda titik (`.`).
4. **Command untuk Navigasi**  
   `pwd` - melihat nama direktori kita berada saat ini.

   `ls` - melihat isi dari direktori.

   `cd` - berpindah ke direktori lain.

5. **Command untuk membuat file dan direktori**  
   `touch` - membuat sebuah file.

   `mkdir` - membuat sebuah direktori/folder.

6. **Command untuk melihat isi file**  
   `cat` - melihat isi sebuah file.

   `head` - melihat beberapa baris awal dari sebuah file.

   `tail` - melihat beberapa baris akhir dari sebuah file.

7. **Command untuk menyalin, memindah, me-_rename_, dan menghapus file dan direktori**  
   `cp` - menyalin file.

   `cp -R` - menyalin direktori.

   `mv` - memindahkan file ke direktori lain.

   `mv -R` - memindahkan direktori.

   `rm` - menghapus file.

   `rm -R` atau `rm -d` - menghapus direktori.

## Modul 2 - Git & Github Dasar

1. **Tentang Git dan Github**
   - Git adalah _tools_ yang digunakan dalam memversikan program atau disebut dengan _Version Control System_.
   - Git dapat melacak setiap perubahan yang terjadi pada suatu file atau direktori, termasuk siapa yang mengubahnya.
   - Github adalah sebuah website yang memberikan layanan cloud untuk mengelola dan menyimpan kode suatu project.
   - **Local repository** adalah istilah untuk direktori penyimpanan yang masih ada di lokal komputer kita.
   - **Remote repository** adalah istilah untuk direktori penyimpanan yang berada di Github.
   - Git dan Github adalah tools yang wajib digunakan khususnya oleh programmer karena bisa bekerja sama dalam sebuah tim tanpa menunggu rekan satu tim menyelesaikan suatu program terlebih dahulu. Seperti pepatah :
     > Sepandai apapun seorang programmer, tidak akan bisa bekerja sendirian selamanya
2. **Setup Awal Git**

   - Konfigurasi Git  
     `git config --global user.name "Nunung Ali Maulana"` untuk menambahkan _username_.

     `git config --global user.email nunungalimaulana@students.unnes.ac.id` untuk menambahkan email.  
     \* Pastikan email yang ditambahkan sama dengan email yang didaftarkan ke Github.  
     `git config --list` untuk mengecek apakah setup berhasil.

   - 3 stage di Git  
     ![3 stage git](images/stageGit.png)

   - Membuat repository Git  
     Buat sebuah folder yang akan menyimpan projek kita. Klik kanan dan pilih `Git Bash Here` untuk membuka Git Bash.  
     `git init` untuk membuat repository git dengan nama **.git**.
   - `git status` untuk melihat ada tidaknya perubahan pada direktori projek.
   - `git add <nama file>` atau `git add .` untuk menambahkan perubahan(_tracking_) dari **Working Directory** ke **Staging Area** pada Git.
   - `git commit -m "pesan commit"` untuk menyimpan perubahan ke **Git Repository**.
   - `git log` untuk melihat catatan commit yang pernah dilakukan.
   - `git log --oneline` untuk melihat catatan commit dalam satu baris.

3. **Push ke Github**
   - Membuat repository di Github
     1. Buka situs Github di <https://github.com/>. Pastikan untuk masuk ke Github dengan _login_ atau _sign up_ jika belum memilik akun.
     2. Setelah masuk, pada bagian kiri klik _new_ untuk membuat repository baru.  
        ![New Repo Github](images/newRepo.png)
     3. Isi nama repository dan deskripsi singkatnya, pilih visibilty(public/private), dan terakhir klik **Create repository**
   - `git branch -M main` untuk mengubah branch master menjadi branch main.
   - `git remote add origin <link>` untuk menghubungkan _local repository_ dan _github repository_.
   - `git push -u origin main` untuk melakukan push dari _local reposiroty_ ke _github repository_.
4. **Cloning Github ke local**
   - Melakukan clone repository dari Github ke local menggunakan command `git clone <link repository>`

## Modul 3 - HTML Dasar

- HTML adalah singkatan dari Hipertext Markup Language.
- HTML bukanlah bahasa pemrograman. Namun, berfungsi untuk membuat kerangka dari website dan menampilkan konten didalamnya.
- Tools utama untuk menggunakan HTML, yaitu :
  1. Browser, seperti Google Chrome, Mozilla Firefox, Opera, Safari.
  2. Code Editor, seperti Visual Studio Code, Sublime Text, Vim, dll.
- Untuk menjalankan file HTML secara manual dapat dengan membuka langsung file HTML via Google Chrome
- Untuk menjalankan file HTML secara otomatis dapat menggunakan ekstensi _live server_ yang ada di VS Code.
- Beberapa ekstensi untuk mempermudah dalam membuat isi file HTML di VS Code diantaranya :
  1. Live server
  2. Prettier
  3. Auto CLose Tag
  4. Auto Rename Tag
- HTML Structure :
  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Website Nunung</title>
    </head>
    <body>
      <h1 class="header">Halo ! Ini adalah Website pertamaku</h1>
      <p>Namaku Nunung Ali Maulana</p>
    </body>
  </html>
  ```
- HTML elements terdiri dari 3 bagian utama, yaitu opening tag, content, dan closing tag.
- HTML attributes adalah properti dari sebuah HTML element. Misalnya id, src, href, dll.
- HTML comment berfungsi untuk memberikan penjelasan maksud dari baris kode yang kita buat. Comment ini tidak akan dieksekusi oleh sistem. Cara membuatnya dengan `<!--(isi comment) -->`.
- Ada 2 jenis tag di HTMl, yaitu :  
  _**Single tag**_ (tidak memiliki tag penutup) seperti tag `<br/>`, `<img src="" alt=""/>`.

  _**Double tag**_ (memilik tag penutup) seperti tag `<h1> </h1>`, `<p> </p>`, `<b> </b>`.

- Tag populer yang sering digunakan di HTML diantaranya tag `<img src="" alt=""/>`, `<video></video>`, `<table></table>`, `<form></form>`,dan lain lain.
- Semantic HTML adalah menggunakan dan menempatkan content sesuai dengan posisi dan kebutuhannya.

  ```html
  <body>
    <header>
      <h1>Website Nunung Ali Maulana</h1>
    </header>

    <nav>
      <a href="#">Home</a> | <a href="#">About</a> |
      <a href="#">Contact Us</a>
    </nav>

    <article>
      <h1>Halo ! Ini adalah website pertamaku</h1>
      <p>Saya Nunung Ali Maulana dari Universitas Negeri Semarang</p>
    </article>

    <footer>Copyright &copy; 2022 by nunungalimaulana_</footer>
  </body>
  ```

- Agar website yang sudah kita buat bisa diakses oleh orang lain melalui internet, maka harus dilakukan publish atau deploy ke sebuah layanan hosting. Ada layanan yang gratis dan juga berbayar. Untuk menggunakan layanan gratis, salah satunya dapat menggunakan sebuah situs bernama [Netlify](https://www.netlify.com/). Setelah mendaftar dan masuk ke menu _site_, kita dapat mengupload repository dari website kita yang ada di Github ke Netlify. Selanjutnya, setelah terdeploy, kita bisa mengubah nama domain melalui menu _setting_.

## Modul 4 - CSS Dasar

- CSS adalah kepanjangan dari Cascading Style Sheets.
- CSS adalah bahasa yang digunakan untuk mendesain halaman website agar terlhat lebih berwarna dan menarik.
- Dengan CSS, kita bisa mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya.
- Struktur CSS :
  ```css
  .selector {
    property: value;
  }
  ```
- CSS comment dapat memberikan penjelasan maksud dari baris kode yang kita kerjakan. Comment ini tidak akan dieksekusi oleh sistem.
- 3 cara menyisipkan CSS ke HTML :
  1. Inline styles adalah menambahkan CSS pada attribute element HTML.
  2. Internal styles adalah menambahkan CSS dengan tag `<styles></styles>` pada head.
  3. Eksternal styles adalah menambahkan CSS dari luar file HTML. Cara memanggilnya dengan menggunakan tag `<link />`.
- Cara menerapkan styling CSS di HTML :
  - Tag name yang akan mempengaruhi semua elemen yang memiliki tag yang sama.
    ```css
    h1 {
      color: red;
    }
    ```
  - Class name yang akan mempengaruhi elemen HTML dengan nama class yang dimaksud. Tanda titik(**.**) digunakan untuk memanggil nama class.
    ```css
    .title {
      color: blue;
    }
    ```
  - ID name bersifat unik dan hanya ada 1 saja di elemen HTML. Gunakan tanda pagar(**#**)saat memanggil element ID HTML pada CSS.
    ```css
    #nav-bar {
      display: inline;
    }
    ```
  - !important CSS berada di level paling atas dari ID dan Class.
- Flexbox
  - Flexbox adalah cara untuk mengatur layout atau tata letak.
  - Konsepnya sederhana, Flexbox memiliki 1 _parent/container_ dan bisa beberapa _child/item_.
  - _flex-direction_ digunakan untuk mengatur letak item _child_. ada 4 value flex-direction, yaitu row, row-reverse, column, column-reverse.
  - _flex-wrap_ digunakan untuk membatasi jumlah item children dalam 1 line.
  - _flex-flow_ digunakan sebagai _shortcut_ untuk set up flex-direction dan flex-wrap bersamaan.
  - _order_ pada flex berfungsi untuk ordering item mana yang ingin kita atur posisinya berdasarkan urutan order.
  - _justify-content_ digunakan untuk mengatur tata letak dan space antar item child secara horizontal atau main axis.
  - _align-items_ digunakan untuk mengatur align dari item child secara vertikal atau cross axis.
  - _align-self_ digunakan untuk mengatur align item pada masing-masing item.
  - _align-content_ digunakan untuk mengatur tata letak dan space antar item child secara vertikal atau cross axis.
  - _flex-grow_ dapat mengatur size suatu item child pada flexbox.
  - _flex-shrink_ adalah properti yang membuat size suatu item child mengecil secara relatif terhadap item child yang lainnya.
  - _flex-basis_ mengatur width dari setiap item child.

## Modul 5 - Algoritma

- Pemrograman itu adalah Algoritma dan Struktur Data.
- Struktur data adalah cara penyimpanan, penyusunan dan pengaturan data di dalam media penyimpanan komputer.
- Algoritma adalah urutan langkah logis tertentu untuk memecahkan suatu masalah. - "Microsoft Press Computer and Internet Dictionary (1998)".
- Manfaat Struktur data yaitu untuk mengelola/manajemen sebuah data. Sementara itu, Algoritma yang akan menyelesaikan suatu permasalahan menggunakan data tersebut.
- Algoritma sangat penting bagi programmer karena merupakan pemeran utama. Bahasa pemrograman hanyalah pemeran pendamping.
- Ciri ciri algoritma :
  1. Memiliki 0 atau lebih inputan.
  2. Memiliki minimal 1 buah output.
  3. Instruksi jelas dan tidak ambigu.
  4. Memiliki titik berhenti.
  5. Sebisa mungkin tepat sasaran dan efisien.
- Jenis proses Algoritma :
  1. Sequence - instruksi dijalankan secara berurutan.
  2. Selection - instruksi dijalankan jika memenuhi kondisi.
  3. Iteration - instruksi berulang kali dijalankan selama memenuhi suatu kondisi.
  4. Concurrent - instruksi dijalankan secara bersamaan.
- Penyajian Algoritma :
  1. Deksriptif
  2. Flow Chart
  3. Pesudocode  
     ![Jenis](images/jenisAlgoritma.png)
- Contoh algoritma sederhana :
  > Cara membersihkan piring :
  >
  > 1. Ambil piring kotor
  > 2. Bawa ke tempat cuci piring
  > 3. Gosok piring dengan spons yang bersabun
  > 4. Bilas dengan air
- Contoh permasalahan nyata berbentuk algoritma untuk diselesaikan dengan program :  
  ![Contoh Algoritma1](images/contohMasalahAlgoritma.png)
- Contoh algoritma untuk diselesaikan dengan JavaScript :  
  ![Contoh Algoritma2](images/ganjilgenap.png)

## Modul 6 - Intro to JavaScript

- Javascript adalah bahasa pemograman yang sangat powerful yang digunakan untuk membuat sebuah website menjadi interaktif dan dinamis.
- Untuk menjalankan JavaScript, kita tidak bisa secara langsung menjalankannya di browser atau Code Editor(kecuali pakai _extentions_). Namun,untuk menjalankannya ada beberapa cara, yaitu :
  - Inline : Buat tag `<script></script>` secara langsung di file HTML.
  - Eksternal : Buat file yang berformat `.js`, lalu memanggilnya dengan menggunakan tag `<script src=""></script>` di file HTML.
- Ada 6 macam tipe data di JavaScript, yaitu :

  - **number** = tipe data yang mengandung semua angka termasuk angka desimal. Contoh : 2, 4, 10, 3.14
  - **string** = tipe data grup karakter yang ada pada keyboard laptop (letters/huruf), number/angka, spasi, symbol, dll. Contoh : "Skilvul01", "Indonesia123".
  - **boolean** = tipe data yang hanya mempunyai _dua_ buah nilai, yaitu TRUE atau FALSE.
  - **null** = tipe data yang berarti sebuah variable/data tidak memiliki nilai.
  - **undefined** = tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai(_error_).
  - **object** = koleksi data yang saling berhubungan (related). Contoh :
    ```javascript
    let orang = {
      nama: "Ali",
      usia: 20,
    };
    ```

- **Variabel** merupakan wadah atau tempat untuk menyimpan sebuah nilai.
- Ada 3 cara mendefinisikan variabel :

  - var
  - let
  - const (tidak bisa diubah nilainya).

- Operator :
  - Assignment Operator ( = ) digunakan untuk menyimpan sebuah nilai pada variabel. Contoh : `let namaSaya = "Nunung Ali Maulana"`;
  - Mathematical Assignment Operator. Contoh :
    ```javascript
    let a = 10;
    a = a + 1;
    console.log(a);
    ```
  - Increment dan Decrement
    ```javascript
    let b = 5;
    let c = 6;
    b++;
    c--;
    console.log(b);
    console.log(c);
    ```
  - Arithmetic Operator adalah operator yang melibatkan operasi matematika.
    - Tambah (+)
    - Kuramg (-)
    - Perkalian (\*)
    - Pembagian (/)
    - Modulus (%)
  - Comparison Operator adalah adalah operator yang membandingkan satu nilai dengan nilai lainnya.
    - Lebih kecil dari : **<**
    - Lebih besar dari: **>**
    - Lebih kecil atau sama dengan: **<=**
    - Lebih besar atau sama dengan: **>=**
    - Sama dengan: **===**
    - Tidak sama dengan: **!==**
  - Logical Operator digunakan untuk sebuah CONDITIONAL pada pemograman.
    - AND operator : **&&**
    - OR operator: **||**
    - NOT operator: **!**
- CONDITIONAL

  - Conditional merupakan statement percabangan yang menggambarkan suatu kondisi.
  - Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut. Yang akan dicek dan dijalankan adalah ketika kondisi TRUE.
  - **IF Statement**
  - Contoh :
    ```javascript
    let nilai = 5;
    if (nilai === 5) {
      console.log("Nilai adalah 5");
    }
    ```
  - **IF..ELSE Statement**
  - Contoh :

    ```javascript
    let lapar = false;
    if (lapar == true) {
      console.log("Makan nasi");
    } else {
      console.log("Tidak makan");
    }
    ```

  - **IF...ELSE IF Statement**
  - Contoh :
    ```javascript
    let lampu = "kuning";
    if (lampu === "merah") {
      console.log("Berhenti");
    } else if (lampu === "kuning") {
      console.log("Hati-hati");
    } else if (lampu === "hijau") {
      console.log("Jalan");
    } else {
      console.log("Salah perintah");
    }
    ```
  - **SWITCH CASE Statement**
  - Contoh :

    ```javascript
    let warna = "coklat";
    switch (warna) {
      case "hitam":
        console.log("warna kuning");
        break;
      case "merah":
        console.log("warna coklat");
        break;
      case "hijau":
        console.log("warna abu-abu");
        break;
      default:
        console.log("warna tidak terdeteksi");
    }
    ```

  - **Ternary Operator merupakan _short-syntax_ dari statement if ... else**
  - Contoh :
    ```javascript
    let mandi = true;
    mandi ? console.log("Sudah mandi") : console.log("Belum mandi");
    ```

- LOOPING
  - Looping merupakan statement yang mengulang suatu instruksi hingga kondisi terpenuhi atau jika kondisi berhenti.
  - Ada 3 macam looping yaitu :
    - For Loop
    - While Loop
    - Nested Loop
  - FOOR LOOP : digunakan jika kita tahu pasti seberapa banyak pengulangan yang ingin dilakukan.
  - Contoh :
    ```javascript
    for (let nilai = 1; nilai <= 10; nilai++) {
      console.log(nilai);
    }
    ```
  - WHILE LOOP : digunakan jika kita belum tahu seberapa banyak pengulangan yang akan dilakukan.
  - Contoh :
    ```javascript
    let sum = 1;
    while (sum < 5) {
      console.log(sum);
      sum++;
    }
    ```
  - DO WHILE LOOP :
  - Contoh :
    ```javascript
    checkNum = 1;
    do {
      console.log(checkNum);
      checkNum++;
    } while (checkNum <= 10);
    ```
