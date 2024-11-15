<h1>APLIKASI LMS BERBASIS DJANGO DAN MENGGUNAKAN POSTGRESQL</h1>
<h2>Aplikasi LMS Untuk Tujuan Pembelajaran Backend Yakni Matkul PSS , aplikasi ini bisa menggunakan docker karena ada docker compose di dalam nya</h2>
<br>
<h2>Langkah-Langkah nya Menjalankannya di Docker Container</h2>
<ul>
  <li>Pasang Docker Jika Belum Ada. Jika Sudah, Aktifkan Docker Machine</li>
  <li>Unduh file zip proyek ini, lalu ekstrak di komputer Anda</li>
  <li>Sebelum menjalankan apa pun, saya sarankan untuk memasang ekstensi Docker (oleh Microsoft) dan PostgreSQL (oleh Weijan Chen) jika Anda menggunakan VSCode sebagai IDE</li>
  <li>Buka terminal baru, lalu jalankan perintah berikut</li>
  <li><code>docker compose up -d --build</code></li>
  <li>Proses ini akan memakan waktu beberapa menit untuk menyusun container</li>
  <li>Setelah berjalan, buka ekstensi Docker di VSCode untuk melihat container yang sedang aktif</li>
  <li>Klik kanan pada "docker-lms-django" dan pilih "Attach Shell" untuk membuka terminal baru di dalam Docker</li>
  <li>Sebelum menjalankan perintah lain, Anda harus terhubung ke PostgreSQL terlebih dahulu</li>
  <li>Buka ekstensi PostgreSQL Anda, lalu buat koneksi baru</li>
  <li>Isi nama database, pengguna database, dan kata sandi sesuai dengan file settings.py. Cari file tersebut, lalu gulir ke bagian databases</li>
  <li>Setelah koneksi dibuat, lanjutkan ke langkah berikutnya</li>
  <li>Jalankan perintah-perintah di bawah ini</li>
  <li><code>python manage.py makemigrations</code></li>
  <li><code>python manage.py migrate</code></li>
  <li>Perintah ini akan membuat migrasi untuk membuat tabel di PostgreSQL</li>
  <li>Untuk memeriksa tabelnya, gunakan ekstensi PostgreSQL lagi dan cek tabel user, coursecontent, coursemember, course, dan comment</li>
  <li>Setelah itu, buka terminal Docker dan ketik perintah berikut</li>
  <li><code>python manage.py runserver 0.0.0.0:8000</code></li>
  <li>Untuk melihat data, cukup akses URL yang sudah ditetapkan di urls.py</li>
</ul>
