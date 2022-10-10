# Writing Test Week 3

**Array dan Multidimensional Array**

- Array adalah tipe data list order yang banyak menyimpan tipe data apapun didalamnya, seperti string, number, boolean, dan lain lain.
- Contoh array :

  ```javascript
  let namaOrang = ["Nunung", "Ali", "Maulana"];
  console.log(namaOrang);
  ```

- Array didefinisikan menggunakan Square brackets `[]`.
- Array pada javascript dihitung dari index data ke-0.
- Contoh mengakses array :
  ```javascript
  let namaOrang = ["Nunung", "Ali", "Maulana"];
  console.log(namaOrang[2]); //output = Ali
  ```
- Untuk meng-_update_ data pada array dengan cara : namaArray\[index] = "newData";
  Contoh:

  ```javascript
  let namaOrang = ["Nunung", "Ali", "Maulana"];
  namaOrang[0] = "Sugeng";
  console.log(namaOrang[0]); //output : Sugeng
  ```

- Const in Array
  - Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain.
  - Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
  - Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const.
- Array Properties  
  Array memiliki 5 properti yang sering dipakai, yaitu **constructor, lenght, index, input, dan prototype**. Contoh :

  ```javascript
  let namaOrang = ["Sugeng", "Ali", "Maulana"];

  console.log(namaOrang.length); //output : 3
  ```

- Array method

  - Array memiliki method atau biasa disebut built-in methods.
  - Contoh method push() :

    ```javascript
    let namaOrang = ["Sugeng", "Ali", "Maulana"];

    namaOrang.push("Dendi");
    console.log(namOrang); //output : "Sugeng", "Ali", "Maulana", "Dendi"
    ```

  - Method lain yang sering digunakan :
    - push()
    - pop()
    - shift()
    - unshift()
    - sort()
  - Looping pada Array dengan built-in method;

    - .map() untuk melakukan looping dengan membuat array baru.

      ```javascript
      let namaBarang = ["Kulkas", "TV", "Pot Bunga"];

      let arrBarang = namaBarang.map((barang) => {
        return barang;
      });
      ```

    - .forEach() untuk melakukan looping pada setiap elemen array.

      ```javascript
      let namaOrang = ["Sugeng", "Ali", "Maulana"];

      namaOrang.forEach((element) => {
        console.log(element); //output : "Sugeng", "Ali", "Maulana"
      });
      ```

- Multidimensional Array

  - Multidimensional Array bisa dianalogikan dengan array of array.
  - Ada array didalam array.

    ```javascript
    let isiLemari = [
      ["Baju batik", 5],
      ["Kaos polos", 8],
      ["Celana pendek", 3],
      ["Celana panjang", 4],
    ];

    console.log(isiLemari);
    ```

  - Multidimensional ini seperti table.
  - Baris pada table menunjukkan jumlah array.
  - Column pada table menunjukkan isi dari tiap array.

  - Sama seperti array satu dimensi, multidimensional array juga dapat menggunakan Property dan Method built-in Array.

  ```javascript
  let isiLemari = [
    ["Baju batik", 5],
    ["Kaos polos", 8],
    ["Celana pendek", 3],
    ["Celana panjang", 4],
  ];

  isiLemari.map((data) => {
    let jumlah = 100 - data[1];
    data[2] = jumlah;
  });
  console.log(isiLemari);
  ```

  - Operasi menggunakan map di Multidimensional Array

    ```javascript
    let inventory = [
      ["Kaos Polos", 10],
      ["Jaket", 5],
      ["Topi", 12],
      ["Celana", 4],
    ];

    inventory.map((dataInventory) => {
      let terjual = 100 - dataInventory[1];
      dataInventory[2] = terjual;
    });
    console.table(inventory);
    ```

**Object dan Array of Object**

- Object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method).
- Properti adalah data lengkap dari sebuah object.
- Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.
- Membuat , mengakses, update, delete object dan property
  ```javascript
  let siswa = {
    nama: "Nunung Ali Maulana",
    umur: 20,
    jurusan: "Ilmu Komputer",
  };
  //mengakses object
  console.log(siswa);
  //mengakses property
  console.log(siswa.nama);
  console.log(siswa["umur"]);
  //update object
  siswa.NIM = 4611420011;
  console.log(siswa.NIM);
  // delete object
  delete siswa.jurusan;
  console.log(siswa);
  ```
- Object method adalah value yang dimasukkan pada property berupa _function_.
- Nested Object berarti di dalam object ada object lain
  ```javascript
  let siswa = {
    nama: "Nunung Ali Maulana",
    umur: 20,
    jurusan: "Ilmu Komputer",
    hobby: {
      hobby1: "Sepak bola",
      hobby2: "Membaca",
    },
  };
  ```
- Passed by reference adalah mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function.
- Looping pada object bisa untuk menampilkan seluruh object property.

  ```javascript
  let siswa = {
    nama: "Nunung Ali Maulana",
    umur: 20,
    jurusan: "Ilmu Komputer",
    hobby: {
      hobby1: "Sepak bola",
      hobby2: "Membaca",
    },
  };

  for (let key in siswa) {
    console.log(siswa.key);
  }
  ```

- Array of object digunakan untuk data yang lebih dari satu.
- Caranya yaitu dengan memasukkan object ke dalam array dengan square bracket yang menutupi object.

**Modules dan Recursive**

- Modules memungkinkan untuk memecah kode menjadi file terpisah sehingga mempermudah untuk maintain code
- JavaScript Module bergantung pada pernyataan impor dan ekspor.
- Recursive adalah fungsi yang memanggil dirinya sendiri sampai suatu kondisi tertentu terpenuhi
- A new paradigm :
  - Procedural
  - Conditional
  - Looping
  - Modular (function)
  - Recursive
- Ciri dari recursive:
- Fungsi recursive memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti.
- Fungsi recursive selalu memaanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya.
- Contoh mencari nilai pangkat dengan rekursif
  ```javascript
  function pow(x, n) {
    if ((n = 1)) {
      return x;
    } else {
      return x * pow(x, n - 1);
    }
  }
  console.log(pow(2, 3)); // 8
  ```
**Asynchronous**
- Asynchronous sebuah teknik yang menyelesaikan fungsi secara paralel.
- Penggunaan asynchronous dapat dilakukan jika kita ingin mengambil data dari database.
- Asynchronous dibutuhkan ketika ada proses yangg membutuhkan waktu lama. Jadi kita bisa mengerjakan proses yg lain secara paralel.
- Callbacks adalah suatu function namun cara pengeksekusiannya yang berbeda yaitu hanya mengeksekusi pada point tertentu.
- Salah satu function yang digunakan untuk mengatur penjadwalan asynchronous adalah setTimeout function.
- Blocking = proses yang tidak boleh diselak/diganti yang lain dulu
- Non-blocking = proses yang bisa di ganti oleh yang lain dulu
- Synchronous = proses yang urut
- Asynchronous = proses yang tidak urut dan mendahulukan yang cepat
- JS Async ada 3 proses utama :
  - callback  -> function yang dijadikan sebagai argumen.
  - promises 
  - async await
  
- Contoh penggunaan asynchronous :
  ```javascript
  function tugas1() {
    console.log("tugas 1 selesai");
  }
  function tugas2() {
    setTimeout(function () {
      console.log("tugas 2 selesai");
    }, 2000);
  }
  function tugas3() {
    console.log("tugas 3 selesai");
  }
  p1();
  p2();
  p3();

  /*
  output : 
  tugas 1 selesai
  tugas 3 selesai
  tugas 2 selesai
  */
  ```
- Contoh penggunaan Callback 
  ```javascript
  const mainFunc = (num1, num2, callBack) => {
    console.log(num1 + num2)
    callBack()
  }

  const myCalBack = () => {
    console.log("Done")
  }

  mainFunc(1,2,myCallBack) //Output: 3 Done
  ```
- setTimeout digunakan untuk simulasi asynchronous. Karena sebenarnya kita tidak bisa membuat proses asynchronous murni.
- Promise adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API.
- Dalam pengambilan data, promise memiliki 3 kemungkinan state.
  - Pending(sedang dalam proses)
  - Fulfilled (berhasil)
  - Rejected (gagal)
- 

**Web Storage**

- Sebelum **HTML5**, data disimpan di sebuah penyimpanan bernama _cookies_.
- Pada HTML5, Web storage digunakan untuk menggantikan _cookies_.
- Web Storage adalah sebuah penyimpanan pada website atu browser yag menyimpan data pada sisi klien (_client side_).
- Web Storage merupakan salah satu WEB API.
- Web Storage dibagi menjadi 2 tipe, yaitu
  - Session Storage
  - Local Storage
- Session storage adalah penyimpanan website pada sisi klien yang digunakan untuk menyimpan data selama web browser atau tab yang memuat halaman belum ditutup.
- Local Storage adalah penyimpanan web yang memungkinkan situs menyimpan dan mengakses data langsung di browser tanpa kadaluwarsa. Artinya, data yang disimpan pada webbrowser akan tetap ada bahkan setelah jendela web browser ditutup.
- Cara menyimpan data pada local storage
  ```javascript
  let nama = "namaku Panjang" //key
  localStorage.setItem("nama", nama);
  ```
- Cara mengambil data
  ```javascript
  localstorage.getItem("nama", nama);
  console.log(localStorage.getItem('nama");
  ```
- Cara menghapus data
  ```javascript
  localStorage.removeItem("token")
  ```
