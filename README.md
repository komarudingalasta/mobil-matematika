# MATH RACE 8-BIT — Online GitHub Pages

Game balapan matematika retro berwarna dengan:
- Mode Guru/Admin
- Sandi guru saat membuat ruang
- Kode ruang 6 karakter untuk siswa
- Siswa mengisi nama dan memilih mobil
- Pengaturan waktu, nyawa, dan poin
- Guru mengontrol MULAI/SELESAIKAN
- Soal matematika
- Skor dan nyawa tersinkron antar perangkat melalui Firebase Realtime Database

## Penting
GitHub Pages sendiri adalah hosting statis. Agar guru dan banyak HP siswa dapat berada di ruang yang sama, project ini menggunakan Firebase Realtime Database.

## Setup singkat
1. Buat project di Firebase Console.
2. Aktifkan Realtime Database.
3. Buat Web App dan salin konfigurasi Firebase.
4. Ganti isi `firebase-config.example.js` menjadi `firebase-config.js`.
5. Terapkan rules dari `database.rules.json` untuk uji coba.
6. Upload `index.html`, `firebase-config.js`, lalu aktifkan GitHub Pages.

## Keamanan
Rules contoh di atas terbuka untuk prototype. Untuk penggunaan sekolah sungguhan, rules sebaiknya diperketat dan autentikasi guru/siswa digunakan. Sandi di antarmuka ini adalah mekanisme aplikasi, bukan pengganti Firebase Authentication.

## Cara bermain
Guru:
MODE GURU → masukkan sandi → atur waktu/nyawa/poin → BUAT RUANG.

Siswa:
MODE SISWA → masukkan kode → nama → pilih mobil → GABUNG.

Guru menekan MULAI. Saat balapan, siswa menekan ENTER untuk memunculkan soal. Jawaban benar memberi poin; jawaban salah mengurangi nyawa. Tidak ada timer khusus soal, dan waktu permainan tetap berjalan.
