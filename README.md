# Group7-Komdat-P1

<h1 align="center"><img src="Dokumentasi/Cover.jpg"></h1>

[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Hosting](#hosting) | [Konfigurasi](#konfigurasi) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)
:---:|:---:|:---:|:---:|:---:|:---:|:---:

Akses I-Course Center melalui : `https://komdat7jaya.000webhostapp.com/`

# Sekilas Tentang
[`^ Back to Top ^`](#)

**I-Course Center** merupakan platform berupa WebApps yang diperuntukan untuk mahasiswa IPB University dalam mempertimbangkan pengambilan keputusan memilih SC/MBKM dengan adanya referensi yang disajikan dan forum diskusi antar mahasiswa. I-Course Center dirancang sebagai web application dengan menggunakan HTML, CSS, PHP, JavaScript, MySQL, XAMPP, serta framework Laravel dan Bootstrap. Fitur-fitur yang disediakan meliputi pencarian referensi SC/MBKM tambahan, preview mata kuliah, dan fasilitas diskusi untuk semua user. 

Akses I-Course Center melalui : `https://komdat7jaya.000webhostapp.com/`

# Instalasi
[`^ Back to Top ^`](#)

#### Kebutuhan Sistem :
1.  Sistem Operasi: Unix/Linux atau Windows Server.
2.  Web Server: Apache (disarankan) atau Nginx.
3.  PHP: Versi 7.4+ dengan ekstensi yang diperlukan.
4.  Database: MySQL 5.7+ (disarankan) atau alternatif lainnya.
5.  Composer: Instal Composer di server.
6.  Memory (RAM): Minimal 512MB.
7.  Storage: Cukup ruang penyimpanan.
8.  SSL Certificate: Disarankan untuk HTTPS.
9.  Caching: Redis/memcached untuk kinerja.
10.  Keamanan: Firewall dan praktik keamanan.

#### Proses Instalasi Perangkat Lunak :
1. Unduh atau clone **I-Course Center** ke dalam direktori kita. Jalankan perintah di bawah ini pada command prompt atau terminal:
    ```
    git clone https://github.com/shishimeow/proyek-akhir-rpl-kel4.git
    ```
2. Setelah diekstrak, kita perlu membuat file `.env` berdasarkan dari file `.env.example`, caranya jalankan perintah:
    ```
    copy .env.example .env
    ```
3. Instal package-package yang diinstal dalam composer di mana package tersebut akan disimpan dalam folder vendor. Jalankan
   perintah berikut di dalam command prompt atau terminal:
   ```
   composer install
   ```
   Setelah berhasil membuat file `.env`, berikutnya jalankan perintah berikut:
   ```
   php artisan key:generate
   ```
4. Kemudian sesuaikan nama database, username, dan password database di file `.env` 
   Jalankan perintah berikut di dalam command prompt atau terminal:
   ```
   php artisan migrate --seed
   ```
   Biasanya, aplikasi yang sudah jadi tidak hanya menyediakan file-file migrations tapi juga file-file seeder untuk data table yang ada di folder database/seeds sehingga 
   kita perlu memasukkannya ke dalam table dengan perintah:
   ```
   php artisan db:seed
   ```
5. Terakhir, untuk membukanya di web browser, jalankan perintah:
   ```
   php artisan serve
   ```
# Hosting
[`^ Back to Top ^`](#)

**Layanan hosting yang digunakan:** 000webhost powered by hostinger 

**Setting I-Course Center pada 000webhost:**
1. Buat akun dan registrasi melalui website https://www.000webhost.com/
2. Pada tampilan dashboard pilih section pada menu `File` dan klik `File Manager`. Kemudian upload seluruh file project I-Course Center
   ![Image](Dokumentasi/Filemanager.jpeg) 
3. Pindahkan semua file dan folder yang harus diakses oleh publik ke dalam folder `public_html`. Untuk source code atau file yang tidak perlu diakses secara langsung, buat folder baru di luar `public_html` dengan nama "laravel" dan letakkan file-file tersebut di sana. Pada contoh di bawah ini merupakan setting pada folder public_html file index.php /index.html
   ![Image](Dokumentasi/Connect1.jpeg)
   
5. Pada file `.env` yang berisi berbagai pengaturan penting seperti informasi database, pengaturan cache, pengaturan email, dan banyak lagi dilakukan setting seperti:  
   a. Ganti `APP_URL` dengan URL hosting.    
   b. Sesuaikan `DB_HOST` dengan alamat server database (biasanya "localhost" jika di server yang sama).  
   c. Sesuaikan `DB_DATABASE` dengan nama database.  
   d. Sesuaikan `DB_PASSWORD` dengan kata sandi database.
   ![Image](Dokumentasi/Connect2.jpeg)

**Setting database I-Course Center**
1. Klik Database Manager: Untuk mengatur database, klik "Database Manager".
2. Ekspor Database Lokal: Sebelumnya, ekspor database yang sudah ada di localhost.
3. Buat Database Baru: Buat database baru dengan memasukkan nama, username, dan password. Ingat dan catat informasi ini.
4. Set Database Baru: Klik "phpmyadmin" untuk mengatur database yang baru
   ![Image](Dokumentasi/Database1.jpeg)  
6. Impor Database: Import database yang telah Anda ekspor ke database baru
   ![Image](Dokumentasi/Phpmyadmin1.jpeg)

# Konfigurasi
[`^ Back to Top ^`](#)

- Untuk melihat banyaknya dari segi user maupun SC/MBKM dapat melalui `Dashboard admin` yang dapat diakses melalui akun admin
  ![Image](Dokumentasi/Dashboardadmin.jpg)
- Untuk memperbaiki informasi atau Create, Read, Update, and Delete (CRUD)  baik dari SC/MBKM dapat melalui menu `Supporting Course (SC)` ataupun `Merdeka Bejalar Kampus Merdeka (MBKM)`
  ![Image](Dokumentasi/SC.jpg)
- Untuk memperbaiki informasi atau Create, Read, Update, and Delete (CRUD) dari Fakultas dapat melalui menu `Fakultas`
  ![Image](Dokumentasi/Fakultas.jpg)
- Untuk Create, Read, Update, and Delete (CRUD) user dapat melalui menu `List Akun`
  ![Image](Dokumentasi/Listakun.jpg)

# Maintenance
[`^ Back to Top ^`](#)

Beberapa maintenance dilakukan pada I-Course Center:

**1. Optimisasi Database:**

Tujuan: Meningkatkan performa dan efisiensi database untuk mempercepat respon aplikasi dan mengurangi beban server.

Langkah-langkah:
- Mengidentifikasi query SQL yang lambat dan mengoptimasinya.
- Memeriksa dan mengindeks kolom yang sering digunakan dalam query.
- Menghapus data yang tidak diperlukan atau cadangan yang sudah usang.
- Melakukan monitoring penggunaan sumber daya server dan melakukan tuning jika diperlukan.

**2. Adress Link Backup:**

Tujuan: Memastikan ketersediaan data dan konfigurasi aplikasi dalam kasus kegagalan atau kehilangan data.

Langkah-langkah:
- Melakukan backup rutin data dan file konfigurasi aplikasi.
- Menyimpan cadangan di server terpisah atau layanan penyimpanan awan yang aman.
- Mengatur jadwal backup otomatis yang konsisten.
- Menguji pemulihan dari cadangan secara berkala untuk memastikan keberfungsian backup.

# Cara Pemakaian
[`^ kembali ke atas ^`](#)
Cara pemakaian sangatlah mudah, berikut penjelasannya:


# Pembahasan
[`^ kembali ke atas ^`](#)

# Referensi
[`^ kembali ke atas ^`](#)
- [Cara menjalankan aplikasi laravel](https://www.cafeteria.id/2018/08/cara-menjalankan-aplikasi-laravel-hasil.html)

