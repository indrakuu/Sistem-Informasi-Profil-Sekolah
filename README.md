# <p align="center"><b>SISTEM INFORMASI PROFIL SEKOLAH</b></p>

---

## Daftar Isi

-   [Deskripsi Singkat](#deskripsi-singkat)
-   [Teknologi yang digunakan](#teknologi-yang-digunakan)
-   [Fitur](#fitur)
-   [Fitur Unggulan](#fitur-unggulan)
-   [Persyaratan Sistem](#persyaratan-sistem)
-   [Cara Instalasi](#cara-instalasi)
-   [Akun Pengguna](#akun-pengguna)
-   [Deploy ke Hosting](#deploy-ke-hosting)
-   [Opsional](#opsional)
    -   [Memisahkan Folder Public di public_html](#memisahkan-folder-public-di-public_html)
    -   [Mengubah Nama Folder Public](#mengubah-nama-folder-public)
    -   [Membuat Folder Storage](#membuat-folder-storage)
    -   [Mengaktifkan Recaptcha](#mengaktifkan-recaptcha)
    -   [Mengaktifkan Webmail](#mengaktifkan-webmail)

---

## [Deskripsi Singkat](#deskripsi-singkat)

Sistem Informasi Profil Sekolah adalah sebuah sistem informasi yang digunakan untuk mengelola data profil sekolah. Sistem ini dibuat menggunakan bahasa pemrograman PHP dengan Laravel 9, Javascript dan database MySQL.

---

## [Teknologi yang digunakan](#teknologi-yang-digunakan)
-   PHP 8.0.2 atau lebih baru
-   Framework Laravel 9
-   MySQL
-   Datatables server side processing
-   Template Stisla (sudah dimodifikasi)
-   JavaScript, JQuery, AJAX dan library lainnya


## [Fitur](#fitur)

Sistem Informasi ini memiliki beberapa modul, diantaranya:

1. Dashboard
2. Modul Data Postingan
    - Artikel
    - Kategori
    - Halaman Statis
    - Komentar
    - Carousel
    - Pesan Berjalan
3. Modul Media
    - Album Gambar
    - Dokumen
    - Video
4. Modul Media
    - Album Gambar
    - Dokumen
    - Video
5. Modul Guru dan Staff
    - Daftar Guru dan Staff
    - Daftar Posisi Guru dan Staff</li>
    - Daftar Status Guru dan Staff</li>
    - Daftar Pangkat atau Golongan</li>
6. Modul Bilah Sisi (Untuk menampilkan informasi di sisi kanan halaman)
    - Kata Sambutan
    - Tautan
    - Promosi
7. Pesan Masuk
8. Profil Akun
9. Modul Manajemen Pengguna
    - Daftar Pengguna
    - Daftar Peran / Role Pengguna
10. Modul Pengaturan
    - Informasi Sekolah
    - Media Sosial
    - Webmail
    - Pengaturan Sistem
    - Tata Letak Menu Navigasi
    - Log Viewer
11. Halaman Utama (Frontend) yang responsif
12. Halaman Postingan :
    - Daftar Artikel
    - Detail Artikel
    - Daftar Kategori
    - Detail Halaman Statis
    - Daftar Album Gambar
    - Detail Album Gambar
    - Daftar Dokumen
    - Unduh Dokumen
    - Daftar Video
    - Daftar Guru dan Staff
    - Detail Guru dan Staff
13. Halaman Pencarian
14. Halaman Error
18. Halaman Kontak
15. Halaman Login
16. Halaman Lupa dan Reset Password (Jika Mengaktifkan Fitur Webmail)
17. Dan masih banyak lagi


---

## [Fitur Unggulan](#fitur-unggulan)

1. Menggunakan Laravel 9
2. gambar yang diupload dapat di compress secara otomatis
3. Dapat Mengganti Logo, Favicon, dan Warna Website secara dinamis
4. Terdapat log viewer untuk melihat log sistem
5. Terdapat pengaturan webmail untuk mengirim email (smtp)
6. Terdapat pengaturan recaptcha untuk menghindari spam di komentar dan pesan masuk
7. Terdapat pengaturan tata letak menu navigasi secara dinamis
8. Memiiki manajemen pengguna yang cukup lengkap
9. Terdapat pengaturan manajemen peran / role pengguna 
10. Tampilan yang friendly dan responsif
11. Dapat terindex oleh mesin pencari (SEO Friendly)
12. Dan masih banyak lagi

---

## [Persyaratan Sistem](#persyaratan-sistem)

Sebelum menginstal sistem ini, pastikan server Anda memenuhi persyaratan berikut:

-   PHP >= 8.0.2
-   Database MySQL (Versi Terbaru)
-   Web Server (Apache, Nginx, LiteSpeed, dll)
-   Composer 2.0
-   XAMPP (_Opsional jika menggunakan di localhost_)

---

## [Cara Instalasi](#cara-instalasi)

1. Clone repositori ini atau download repositori ini dalam bentuk zip.
2. Buka terminal atau command prompt, lalu arahkan ke direktori repositori ini.
3. Jalankan perintah `composer install --optimize-autoloader --no-dev` untuk menginstal semua dependensi yang dibutuhkan.
4. Buat database baru di MySQL.
5. Salin file `.env.example` menjadi `.env`.
6. Buka file `.env` dan ubah konfigurasi database sesuai dengan database yang telah dibuat. Contoh:

    ```env
    DB_CONNECTION=mysql
    DB_HOST= [host database]
    DB_PORT= [port database]
    DB_DATABASE= [nama database]
    DB_USERNAME= [username database]
    DB_PASSWORD= [password database]
    ```

7. Jalankan perintah `php artisan key:generate` untuk menghasilkan APP_KEY.
8. Jalankan perintah `php artisan migrate:fresh --seed` untuk menghasilkan tabel-tabel yang dibutuhkan.
9. Terakhir, jalankan perintah `php artisan serve` untuk menjalankan sistem ini di localhost (_default: http://127.0.0.1:8000_) dengan apache dan MySQL aktif.

---

## [Akun Pengguna](#akun-pengguna)

Secara default, sistem ini memiliki akun pengguna berikut:

| Nama Pengguna | Password |
| ------------- | -------- |
| administator  | 12345678 |

---

## [Deploy ke Hosting](#deploy-ke-hosting)

Deploy sudah dicoba di hosting cPanel berikut cara-caranya:

1. Jalankan perintah `composer install --optimize-autoloader --no-dev` untuk menginstal semua dependensi yang dibutuhkan.
2. Jalankan perintah `php artisan optimize:clear` untuk sistem.
3. Backup database yang telah dibuat di localhost (jika ada)
4. Masukkan ke dalama zip file sistem ini termasuk file backup database (jika ada).
5. Upload ke hosting.
6. Buka terminal atau command prompt, lalu arahkan ke direktori repositori ini.
7. Salin file `.env.example` menjadi `.env`.
8. Jalankan perintah `php artisan key:generate` untuk menghasilkan APP_KEY.
9. Sesuaikan konfigurasi database di file `.env` dengan database yang telah dibuat di hosting.
10. Pastikan `APP_ENV` bernilai `production` dan `APP_DEBUG` bernilai `false` di file `.env`.
11. Masih di file `.env` pada bagaian `APP_URL` sesuaikan dengan url hosting.
12. Jalankan perintah `php artisan migrate:fresh --seed` untuk menghasilkan tabel-tabel yang dibutuhkan.
13. Silahkan akses sistem secara online.

---

## [Opsional](#opsional)

---

### [Memisahkan Folder Public di public_html](#memisahkan-folder-public-di-public_html)

Gunakan cara ini jika sudah melakukan deploy ke hosting dengan memisahkan folder public di public_html.

1. Buka file `index.php` di folder `public_html` dan ubah baris berikut:

    ```php
    require __DIR__.'/../vendor/autoload.php';
    ```

    misalnya menjadi:

    ```php
    require __DIR__.'/../{nama_folder_sistem_laravel}/vendor/autoload.php';
    ```

2. Masih di file `index.php` ubah baris berikut:

    ```php
    $app = require_once __DIR__.'/../bootstrap/app.php';
    ```

    misalnya menjadi:

    ```php
    $app = require_once __DIR__.'/../{nama_folder_sistem_laravel}/bootstrap/app.php';
    ```

---

### [Mengubah Tempat Penyimpanan File](#mengubah-tempat-penyimpanan-file)

Gunakan cara ini jika ingin mengubah direktori penyimpanan file yang diupload oleh pengguna ke sistem.

<sub>
Perlu diperhatikan dalam mengubah direktori penyimpanan dilakukan 1 kali saja untuk production, karena jika melakukan perubahan lebih dari 1 kali maka file-file yang telah diupload sebelumnya tidak akan muncul di sistem dan akan menyebabkan sampah serta bahkan bisa mengakibatkan error.
</sub><br><br>

Berikut cara mengubah direktori penyimpanan file:

1. Buka file `config/filesystems.php`.
2. Lihat kode pada baris berikut:

    ```php
    'public' => [
        'driver' => 'local',

        // Folder Public
        'root' => public_path(),
        'url' => env('APP_URL'),

        // Folder Storage
        // 'root' => storage_path('app/public'),
        // 'url' => '/storage',

        'visibility' => 'public',
        'throw' => false,
    ],
    ```

3. Dari kode di atas, pada bagian `root` dan `url` dibawah ini :

    ```php
    'root' => public_path(),
    'url' => env('APP_URL'),
    ```

    merupakan direktori penyimpanan default file dan setiap file yang telah diupload akan disimpan didalam root folder public dengan terdapat folder `uploads` didalamnya.

4. Jika ingin mengubah direktori penyimpanan file maka gantikan posisi komentar ke folder storage pada kode berikut:

    ```php
    'public' => [
        'driver' => 'local',

        // Folder Public
        // 'root' => public_path(),
        // 'url' => env('APP_URL'),

        // Folder Storage
        'root' => storage_path('app/public'),
        'url' => '/storage',

        'visibility' => 'public',
        'throw' => false,
    ],
    ```

5. Berikutnya, jalankan perintah `php artisan storage:link` untuk menghasilkan symbolic link dari folder storage ke folder public.

6. Dengan begitu, file yang diupload oleh pengguna akan disimpan di folder storage dengan terdapat folder `app/public` didalamnya.

7. Jika ingin mengubah kembali ke direktori penyimpanan default, maka gantikan posisi komentar ke folder public pada kode berikut:

    ```php
    'public' => [
        'driver' => 'local',

        // Folder Public
        'root' => public_path(),
        'url' => env('APP_URL'),

        // Folder Storage
        // 'root' => storage_path('app/public'),
        // 'url' => '/storage',

        'visibility' => 'public',
        'throw' => false,
    ],
    ```

8. Lalu hapus folder `storage` yang ada di dalam folder `public`.

---

### [Membuat Folder Storage](#membuat-folder-storage)

Jika telah mengubah direktori penyimpanan di folder storage, maka perlu membuat folder storage di dalam folder public. Tetapi terkadang untuk membuat folder sedikit sulit di shared hosting, maka dari itu dapat menggunakan cara berikut:

1. Melalui Cronjob Hosting :

    - Buka cronjob di hosting.
    - Tambahkan perintah script berikut :

    ```bash
    ln -s /home/{nama_user}/{nama_folder_sistem_laravel}/storage/app/public /home/{nama_user}/public_html/storage
    ```

    - Atur waktu cronjob sesuai kebutuhan.
    - Simpan.
    - Tunggu hingga waktu cronjob berjalan dan folder storage akan terbuat secara otomatis.
    - Hapus cronjob jika folder storage sudah terbuat.

2. Melalui Terminal :

    - Buka terminal di hosting.
    - Tambahkan perintah script berikut :

    ```bash
    ln -s /home/{nama_user}/{nama_folder_sistem_laravel}/storage/app/public /home/{nama_user}/public_html/storage
    ```

    - Tunggu hingga folder storage terbuat secara otomatis.

---

### [Mengaktifkan Recaptcha](#mengaktifkan-recaptcha)

Recaptcha di sistem ini digunakan untuk menghindari spam pada form yang ada di sistem seperti komentar artikel dan pesan kotak. Untuk menggunakan recaptcha, ikuti langkah-langkah berikut:

1. Buka Sistem informasi dan masuk ke halaman `Dashboard > Pengaturan > Informasi Website > ReCaptcha V2`.
2. Aktifkan recaptcha dengan mengubah status menjadi `Aktif`.
3. Sistem meminta `site key` dan `secret key` yang dapat didapatkan di [https://www.google.com/recaptcha/admin](https://www.google.com/recaptcha/admin).

---

### [Mengaktifkan Webmail](#mengaktifkan-webmail)

Webmail di sistem ini digunakan untuk agar admin dapat menerima pesan yang dikirim oleh pengguna melalui halaman `Kontak` ke Pesan Masuk `Email` dan dapat digunakan juga untuk membuka url lupa password (_`/forgot-password`_) yang dikirim ke email pengguna jika terdapat permintaan lupa password. Untuk menggunakan webmail, ikuti langkah-langkah berikut:

1. Buka Sistem informasi dan masuk ke halaman `Dashboard > Pengaturan > Webmail`.
2. Aktifkan webmail dengan mengubah status menjadi `Aktif`.
3. Data yang diperlukan :
    - `Mail Host` : Host email pengirim (_default: `smtp`_).
    - `Mail Port` : Port email pengirim (_default: `587`_).
    - `Mail Username` : Username email pengirim
    - `Mail Password` : Password email pengirim.
    - `Mail Encryption` : Encryption email pengirim.
    - `Mail From Address` : Email pengirim yang akan muncul di email penerima.
    - `Mail From Name` : Nama pengirim yang akan muncul di email penerima.
4. Untuk mendapatkan data-data diatas, diperlukan salah layanan webmail smtp seperti :
    - [Mailtrap](https://mailtrap.io/) (Gratis)
    - [Mailgun](https://www.mailgun.com/) (Gratis)
    - [Sendgrid](https://sendgrid.com/) (Gratis)
    - [Mailjet](https://www.mailjet.com/) (Gratis)
    - [Mailchimp](https://mailchimp.com/) (Gratis)
5. Contoh pengaturan webmail menggunakan Mailtrap :
    - `Mail Host` : smtp.mailtrap.io
    - `Mail Port` : 2525
    - `Mail Username` : 1a2b3c4d5e6f7g
    - `Mail Password` : 1a2b3c4d5e6f7g
    - `Mail Encryption` : tls
    - `Mail From Address` : no-reply@nama_website.com (Email pengirim)
    - `Mail From Name` : Nama Website (bisa Nama Admin)
6. Jika sudah selesai, klik tombol `Simpan` untuk menyimpan pengaturan webmail dan silahkan uji coba mengirim pesan melalui halaman `Kontak` untuk melihat apakah pesan masuk ke email pengirim atau tidak.

---
