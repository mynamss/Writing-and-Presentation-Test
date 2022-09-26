# Writing and Presentation Test Week 1

<!-- --- -->

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

   `rm -R` atau `rm -d` - menghapus direktori

## Modul 2 - Git & Github Dasar

1. **Tentang Git dan Github**
   - Git adalah _tools_ yang digunakan dalam memversikan program atau disebut dengan _Version Control System_.
   - Git dapat melacak setiap perubahan yang terjadi pada suatu file atau direktori, termasuk siapa yang mengubahnya.
   - Github adalah sebuah website yang memberikan layanan cloud untuk mengelola dan menyimpan kode suatu project.
   - Local repository adalah istilah untuk direktori penyimpanan yang masih ada di lokal komputer kita.
   - Remote repository adalah istilah untuk direktori penyimpanan yang berada di Github.
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

3.

## Modul 2 - HTML

## Modul 3 - CSS

## Modul 4 - Algoritma

## Modul 5 - JavaScript Dasar

Peserta mampu memahami kenapa Git dan Github tools yang wajib digunakan
Peserta mampu memahami perbedaan antara Git dan Github
Peserta mampu memahami alur kerja dari Git dan Github
Peserta mampu memahami dan membuat Repository Git
Peserta mampu melakukan commit pada Git
Peserta mampu mempublish aplikasi ke Github
Peserta mampu melakukan cloning Github ke local
