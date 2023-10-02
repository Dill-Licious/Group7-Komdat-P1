# Group7-Komdat-P1

<h1 align="center"><img src="Dokumentasi/Cover.jpg"></h1>

[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Hosting](#hosting) | [Konfigurasi](#konfigurasi) | [Otomatisasi](#otomatisasi) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)
:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:


# Sekilas Tentang
[`^ kembali ke atas ^`](#)

**I-Course Center** merupakan platform berupa WebApps yang diperuntukan untuk mahasiswa IPB University dalam mempertimbangkan pengambilan keputusan memilih SC/MBKM dengan adanya referensi yang disajikan dan forum diskusi antar mahasiswa. I-Course Center dirancang sebagai web application dengan menggunakan HTML, CSS, PHP, JavaScript, MySQL, XAMPP, serta framework Laravel dan Bootstrap. Fitur-fitur yang disediakan meliputi pencarian referensi SC/MBKM tambahan, preview mata kuliah, dan fasilitas diskusi untuk semua user. 

# Instalasi
[`^ kembali ke atas ^`](#)

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
10. Scheduled Tasks: Konfigurasi tugas cron.
11. Keamanan: Firewall dan praktik keamanan.
12. Logging dan Monitoring: Konfigurasi logging dan pemantauan.

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

   Biasanya, aplikasi yang sudah jadi tidak hanya menyediakan file-file migrations tapi juga file-file seeder untuk data table yang ada di folder database/seeds sehingga kita perlu memasukkannya ke dalam table dengan perintah:
   ```
   php artisan db:seed
   ```

5. Terakhir, untuk membukanya di web browser, jalankan perintah:
   ```
   php artisan serve
   ```

# Hosting
[`^ kembali ke atas ^`](#)

Belom dirapihin ya
1. buat akun di website 00Webhosting.
2. upload file projet di file manager
3. untuk folder public_html, berisikam file folder public, dan file-file lainnya dibuat folder baru diluar public_html. //dicontohkan nama folder diluar public_html diberi nama "laravel"
4. dilakukan setting pada file env, 
	a. mengganti app_url = url dari hosting 
	a. mengganti DB_Host = localhost
	b. DB_database = disesuaikan nama databasenya
	c. DB_password = disesuaikan pw databasenya
5.dilakukan setting pada folder public_html file index.php /index.html
	a. menambahkan nama folder "laravel"

======== bagian database ===========
1. click database manager untuk setting database
1. melakukan ekspor terlebih dahulu database yang sudah dibuat di localhost.
2. buat new database, masukan input nama database, username database, dan password database *harus dingat/dicatat.
3. setelah membuat database baru click phpmyadmin untuk setting database barunya
3. lakukan import di database yang baru/telah dibuat.

# Konfigurasi
[`^ kembali ke atas ^`](#)

# Maintenance
[`^ kembali ke atas ^`](#)

# Otomatisasi
[`^ kembali ke atas ^`](#)

# Cara Pemakaian
[`^ kembali ke atas ^`](#)

# Pembahasan
[`^ kembali ke atas ^`](#)

# Referensi
[`^ kembali ke atas ^`](#)


