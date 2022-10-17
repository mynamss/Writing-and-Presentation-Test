# Writing Test Week 3

**Asynchronous**

- Javascript adalah bahasa pemrograman _single-thread_ yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa disebut **_synchronous_**.
- Pada konsep pemrograman (web development pada case kita) dikenal istilah **_Asynchronous_**.
- Asynchronous mengizinkan komputer memproses task yang lain sambil menunggu proses yang masih berlangsung.
- Ada 3 teknik yang digunakan untuk menghandle proses asynchronous pada JavaScript:
  - Callback
  - Promise
  - Async Await
- Callback Function

  - Callback function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya.
  - Contoh :

    ```javascript
    const notify = () => {
      console.log("Download complete!");
    };
    const download = (url, callback) => {
      console.log(`Downloading from ${url}....`);
      callback();
    };
    const url = "https://brachio.site/download";
    download(url, notify);
    //Output :
    //Downloading from https://brachio.site/download.... -->
    //Download complete!
    ```

- Promise

  - Promise bisa dikatakan sebagai object yang menyimpan hasil dari sebuah operasi asynchronous baik itu hasil yang diinginkan (resolved value) atau alasan kenapa operasi itu gagal (failure reason).
  - Sebuah Promise berada di salah satu diantara 3 kondisi(state):
    - pending, operasi sedang berlangsung
    - fulfilled, operasi selesai dan berhasil
    - rejected, operasi selesai namun gagal
  - Contoh :

    ```javascript
    let progress = 100;
    const download = new Promise((resolve, reject) => {
      if (progress === 100) {
        resolve("Download complete");
      } else {
        reject("Download failed");
      }
    });
    ```

    - resolve(value) adalah callback function yang dieksekusi jika operasi yang dijalankan oleh executor berhasil(fulfilled)
    - reject(error) adalah callback function yang akan dieksekusi jika operasi gagal (rejected)
    - Untuk merespon hasilnya (baik berupa value atau error) kita perlu menambahkan handler.
    - Handler biasanya berupa function dan ditempatkan di dalam method bernama then() untuk value yang berhasil.
    - untuk merespon error kita bisa tambahkan method catch().

  - Async Await
    - Async/Await diperkenalkan di ES8 / ES2017 untuk menghandle operasi asynchronous dengan syntax yang lebih mirip dengan synchronous.
  - Contoh :
    ```javascript
    async function hello() {
      result = await doAsync();
      console.log(result);
    }
    ```
    - Keterangan :
    - async → mengubah function menjadi asynchronous
    - await → menunda eksekusi hingga proses asynchronous selesai, dari kode di atas berarti console.log(result) tidak akan di eksekusi sebelum prose doAsyncA() selesai. await juga bisa digunakan berkali-kali di dalam function

- Cara mengambil data dari API di JavaScript

  - Fetch API memungkinkan kita untuk mengambil atau meminta sumber daya secara asynchronous.
  - Contoh

    ```javascript
    fetch("https://digimon-api.vercel.app/api/digimon")
      .then((result) => {
        result.json();
      }) //butuh waktu untuk membuka
      .then((resultJson) => {
        console.log(resultJson);
      })
      // Jika API mati, tangani dengan catch
      .catch((result) => {
        console.log(result);
      });
    ```

    atau

    ```javascript
    let containerDigimon = document.getElementById("list-digimon");
    let getDataDigimon = async () => {
      let response = await fetch("https://digimon-api.vercel.app/api/digimon");
      let digimons = await response.json();
      console.log(digimons);

      digimons.slice(0, 10).forEach((item, index) => {
        // if (index < 4) {
        containerDigimon.innerHTML += `<div>
            <img src="${item.img}" alt="image" width="200"> 
            <h3>${item.name}</h3
            </div>
            `;
        // }
      });
      console.log(item);
      // slice dan if untuk membatasi output
    };

    getDataDigimon();
    ```

**Git dan Github Lanjutan**

- Branch adalah sebuah cabang pada Git.
- Secara default, branch utama adalah master.
- Git branch memilik beberapa keuntungan, diantaranya :
  - Memungkinkan pengembangan fitur baru bagi aplikasi tanpa menganggu pengembangan di branch utama.
  - Memungkinkan pembuatan branch-branch pengembangan berbeda yang dapat berpusat di satu repositori.
- Beriku beberapa perintah atau _command_ pada git:
  - `git branch` = melihat semua branch
  - `git branch [branch_baru]` = untuk membuat branch baru
  - `git branch -d <branch>` = untuk menghapus branch
  - `git checkout <branch>` = untuk berpindah ke branch yang dituju.
  - `git merge <branch>` = untuk menggabungkan
  -

**Responsive Web Design**

- Responsive Web Design (RWD) adalah suatu tampilan website yang dapat menyesuaikan dengan perangkat yang digunakan.
- Device yang umumnya digunakan adalah laptop/PC, smartphone, dan tablet.
- Setiap developer wajib menggunakan tools bawaan browser yang memudahkan proses development website.
- Di Google Chrome, tools itu disebut dengan **Chrome Dev Tools**.
- Untuk mengakses Chrome Dev Tools di Windows,

  - _pertama_, buka Google Chrome
  - _kedua_, gunakan shortcut :

    > `Ctrl` + `Shift` + `J`

    atau bisa dengan klik kanan pada viewport dan klik _`inspect`_.

- Agar bisa menggunakan RWD, pada code HTML perlu ditambahkan _viewport_ sehingga tampilan website dapat diatur untuk menyesuaikan dengan berbagai device.
- Berikut ini adalah tag meta yang berisi viewport

  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  ```

- CSS Unit adalah satuan untuk menentukan ukuran dari suatu elemen atau kontennya.
- Relative unit berguna untuk mendesain website yang responsif karena ukurannya bisa berubah relatif terhadap parent atau ukuran layar.
- Berikut adalah macam macam CSS Unit :

  - **%**: Ukurannya relatif terhadap parent element
  - **em**: Ukurannya relatif terhadap font-size dari elemen saat ini
  - **rem**: Ukurannya relatif terhadap font-size root elemen (<html>). "rem" = "root em"
  - **ch**: Ukurannya mengikuti jumlah karakter (1 karakter sama dengan lebar dari karakter 0/nol font yang sedang aktif)
  - **vh**: Ukurannya relatif terhadap tinggi viewport (ukuran jendela tau aplikasi), 1vh = 1/100 dari tinggi viewport
  - **vw**: Ukurannya relatif terhadap lebar dari viewport. 1vw = 1/100 lebar viewport
  - **vmin**: Ukurannya relatif terhadap ukuran viewport yang lebih kecil (misalnya diorientasi portrait, lebar akan lebih kecil daripada tinggi). 1vmin = 1/100 dari ukuran viewport yang lebih kecil.
  - **vmax**: Sama dengan vmin, dia akan melihat ukuran viewport yang lebih besar
  - **ex**: Ukurannya relatif terhadap tinggi dari karakter "x" kecil font yang sedang aktif.
  - Contoh penggunaan :

    ```css
    .child {
      margin: 10%;
    }

    .header {
      font-size: 2rem;
    }
    ```

- Media Query
  - RWD akan lebih mudah ketika menggunakan _meida query_.
  - Media query digunakan untuk membuat beberapa styles tergantung pada jenis device.
  - Ada 2 cara menggunakan media query :
    - Membuat file CSS berbeda di masing-masing device
    - Menggabungkan 1 file CSS untuk setting styling berbagai device.
  - Jenis :
    - min-width
    - max-width
  - Setting up Media Query di file css:
    ```css
    @media screen and (min-width: your-px) {
      /* isi dengan selector html dan CSS*/
    }
    ```
- Breakpoint adalah perubahan yang terjadi pada tampilan saat berganti ukuran width pada device.
- Jika kita menginginkan tampilan yang ingin diterapkan pada range ukuran device tertentu, maka bisa menggunakan _range media query_.
- Contoh :

  ```css
  body {
    background-color: blue;
  }

  @media screen and (min-width: 500px) and (max-width: 700px) {
    body {
      background-color: #fff;
    }
  }
  ```

- Flexbox adalah sebuah display yang bertujuan untuk membuat wbsite yang lebih efisien dalam mengatur dan menata element yang ada didalamnya sekalipun ukurannya tidak diketahui atau dinamis.
- Caranya yaitu dengan menggunakan display :flex.
- Flexbox properties :
  - Flex direction : menetapkan sumbu utama item, sehingga menentukan arah item fleksibel ditempatkan di wadah fleksibel.
    - Row : Kiri ke kanan
    - Row-Reverse : Kanan ke kiri
    - Column : Atas ke bawah
    - Column-Reverse : Bawah ke atas
  - Flex Wrap : Secara default, semua item atau element pada flexbox akan mencoba berada dalam satu baris. Namun, dengan flex wrap kita bisa mengubah hal tersebut.
    - nowrap : semua item flex akan berada dalam satu baris
    - wrap : item fkex akan membungkus ke beberapa baris, dari atas ke bawah.
    - wrap-reverse :item flex akan membungkus beberapa baris dari bawah ke atas.
  - Flex flow : cara singkat untuk properti flex-direction dan flex-wrap. Nilai default adalah baris nowrap.
- Grid adalah sistem tata letak pada tampilan web yang berbasis dua dimenis.
- Ada 2 jenis grid, yaitu grid container dan grid item.

**Bootsrap 5**

- Bootstrap adalah salah satu framework untuk HTML dan CSS yang bisa digunakan untuk membuat webiste yang responsif.
- Komponen utama Bootstrap yaitu `bootstrap.css` dan `bootsrap.js`.
- Bootsrap digunakan ketika kita ingin membuat website sederhana dan tidak membutuhkan load yang lama.
- Layout bootstrap :
  - Breakpoints, ada 5 yaitu `sm, md, lg, xl dan xxl`.
  - Setiap breakpoint dipilih untuk menampung container yang lebarnya 12 sehingga tersusun rapi. Breakpoint juga mewakili subset ukuran perangkat umum dan dimensi area pandang.
- Container adalah blok dasar untuk pembungkus bootstrap yang terdiri dari contain, pad dan align yang menyelaraskan konten website dalam perangkat.
- Component di Bootstrap ada 4, yaitu
  - Alert
    - alert-secondary
    - alert-success
    - alert-danger
    - alert-warning
    - alert-info
    - alert-light
    - alert-dark
  - Badges
  - Breadcrumb (untuk navigasi)
  - Buttons
- Secara default, Grid system di Bootstrap dibagi menjadi 12 kolom.
- Grid system pada bootstrap menggunakan container,baris dan kolom untuk menata dan menyelaraskan konten,yang dibangun menggunakan flexbox dan itu sudah responsive.
- Grid system bootstrap :
  - .col-lg digunakan untuk mengatur grid pada ukuran monitor yang besar
  - .col-md digunakan pada monitor komputer berukuran sedang
  - col-sm digunakan untuk mengatur monitor pada tablet
  - .col-xs digunakan untuk mengatur monitor pada handphone
