SEVENZGOD'S SPAR — GITHUB PAGES + FIREBASE

FILE:
- peserta.html  = link peserta
- admin.html    = link admin
- firebase-config.js = config Firebase yang harus diisi
- firestore.rules = aturan keamanan Firestore

1. BUAT PROJECT FIREBASE
- Buka Firebase Console.
- Create project.
- Tambahkan Web App.
- Salin firebaseConfig ke firebase-config.js.
- Dokumentasi resmi: https://firebase.google.com/docs/web/setup

2. AKTIFKAN FIRESTORE
- Firebase Console > Build > Firestore Database > Create database.

3. AKTIFKAN LOGIN ADMIN
- Firebase Console > Build > Authentication > Get started.
- Sign-in providers > Email/Password > Enable.
- Buat 1 akun admin, misalnya email admin milikmu sendiri.
- Ganti GANTI_EMAIL_ADMIN di firestore.rules dengan email admin tersebut.

4. PASANG RULES
- Firebase Console > Firestore Database > Rules.
- Tempel isi firestore.rules.
- Ganti GANTI_EMAIL_ADMIN sebelum Publish.

5. UPLOAD KE GITHUB
Buat repository, lalu upload:
  index.html       (boleh peserta.html diganti nama menjadi index.html)
  peserta.html
  admin.html
  firebase-config.js

Saran struktur:
  /index.html
  /peserta.html
  /admin.html
  /firebase-config.js

6. AKTIFKAN GITHUB PAGES
- Repository > Settings > Pages.
- Source: Deploy from a branch.
- Branch: main / root.
- Simpan.
- GitHub Pages akan memberi URL seperti:
  https://USERNAME.github.io/NAMA-REPO/

7. DUA LINK
Jika file tetap bernama peserta.html dan admin.html:
  Peserta: https://USERNAME.github.io/NAMA-REPO/peserta.html
  Admin:   https://USERNAME.github.io/NAMA-REPO/admin.html

Jika peserta.html dijadikan index.html:
  Peserta: https://USERNAME.github.io/NAMA-REPO/
  Admin:   https://USERNAME.github.io/NAMA-REPO/admin.html

CATATAN KEAMANAN:
- firebase-config.js boleh berada di frontend; API key Firebase Web bukan password rahasia.
- Keamanan admin ditentukan oleh Firebase Authentication + Firestore Rules.
- Jangan memasukkan password admin ke dalam HTML/JavaScript.
