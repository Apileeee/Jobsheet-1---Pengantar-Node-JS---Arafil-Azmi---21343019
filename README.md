# Job Sheet 1 - Pengantar Node JS - Pemrograman Berbasis Jaringan Menggunakan Node.js

## Konsep Pemmograman Berbasis Jaringan Node.js

Konsep-konsep utama yang dicakup dalam kursus ini meliputi:

- **Arsitektur Klien-Pelayan (Client-Server Architecture):** Paradigma dasar yang menginspirasi pemrograman berbasis jaringan, melibatkan peran klien dan pelayan untuk distribusi tugas yang efisien dan pemanfaatan sumber daya.

- **Protokol Jaringan:** Aturan dan konvensi yang mengatur pertukaran data di antara entitas dalam jaringan, seperti HTTP dan SMTP.

- **Soket:** Antarmuka pemrograman yang memfasilitasi interaksi jaringan, dengan variasi seperti soket aliran (stream) dan soket datagram.

- **Pemrograman Sinkron dan Asinkron:** Pilihan antara menunggu operasi jaringan selesai (sinkron) atau memungkinkan aplikasi melanjutkan eksekusi tanpa menunggu (asinkron).

## Node.js dan Perannya

Node.js berfungsi sebagai lingkungan runtime untuk mengeksekusi kode JavaScript di sisi server, meningkatkan pemrograman berbasis jaringan dengan pendekatan asinkron dan event-driven. Node.js sangat efektif dalam menangani operasi dengan potensi latensi, seperti permintaan jaringan atau akses ke penyimpanan.

## Panduan Instalasi

Ikuti langkah-langkah berikut untuk menyiapkan lingkungan pengembangan:

### Visual Studio Code:

1. Unduh Visual Studio Code dari [sini](https://code.visualstudio.com/).
2. Jalankan installer (VSCodeUserSetup-{versi}.exe).
3. Secara default, VS Code diinstal di `C:\Users\{Username}\AppData\Local\Programs\Microsoft VS Code`.

### Node.js:

1. Kunjungi situs resmi Node.js di [https://nodejs.org/](https://nodejs.org/).
2. Unduh versi sesuai dengan sistem operasi Anda (Windows, macOS, atau Linux).
3. Ikuti langkah-langkah instalasi, termasuk pemilihan direktori instalasi dan persetujuan terhadap syarat dan ketentuan.

4. Setelah instalasi, buka terminal atau command prompt dan jalankan `node -v` untuk memeriksa instalasi Node.js. Jalankan juga `npm -v` untuk memastikan bahwa npm (Node Package Manager) juga terinstal.

5. Jika Node.js tidak terdeteksi, atur PATH untuk Node.js dalam variabel lingkungan. Gunakan perintah: `SET PATH=C:\Program Files\Nodejs;%PATH%` di command prompt.

6. Alternatifnya, buka pengaturan Environment Variables melalui Control Panel -> System and Security -> System -> Advanced System Settings -> Environment Variables. Edit variabel pengguna dan sistem untuk menyertakan direktori instalasi Node.js (misalnya, C:\Program Files\nodejs).

### Membuat Program Uji Coba Node.js :

### Buat Folder Proyek:

1. Buat folder dengan nama "PBJ1" (atau nama yang Anda pilih) dan simpan di direktori yang diinginkan. Hindari menggunakan spasi dalam nama folder.

### Buka di Visual Studio Code:

- Buka Visual Studio Code dan muat folder yang telah Anda buat.

### Buat Folder Uji:

- Dalam folder yang dibuka, buat folder baru dengan nama "testground" menggunakan Visual Studio Code.

### Buat dan Jalankan Program Sederhana:

1. Buat file baru dengan nama "hello.js" di dalam folder "testground" dan masukkan kode berikut:

    ```javascript
    console.log('Welcome to Node.js!');
    ```

2. Jalankan file tersebut dan perhatikan keluarannya. Gunakan terminal di Visual Studio Code dengan perintah:

    ```bash
    node hello.js
    ```

### Buat Program Berbasis Jaringan:

1. Buat file lain dengan nama "hello-world.js" di folder yang sama dan masukkan kode berikut:

    ```javascript
    const http = require('http');

    const server = http.createServer((req, res) => {
      res.writeHead(200, { 'Content-Type': 'text/plain' });
      res.end('Hello, World!\n');
    });

    server.listen(3000, '127.0.0.1');
    console.log('Server berjalan di http://127.0.0.1:3000/');
    ```

2. Jalankan program dan Anda akan melihat pesan "Server berjalan di http://127.0.0.1:3000/" di konsol.

3. Buka URL yang disediakan di browser untuk melihat pesan "Hello, World!"
