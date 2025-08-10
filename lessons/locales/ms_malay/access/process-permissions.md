# Kebenaran Proses

## Kandungan Pelajaran

Mari kita beralih kepada kebenaran proses sebentar, ingat bagaimana saya memberitahu anda bahawa apabila anda menjalankan perintah passwd dengan bit kebenaran SUID diaktifkan, anda akan menjalankan program sebagai root? Itu benar, tetapi adakah itu bermakna kerana anda sementara menjadi root, anda boleh mengubah kata laluan pengguna lain? Tidak, nasib baik tidak!

Ini kerana banyak UID yang dilaksanakan oleh Linux. Terdapat tiga UID yang berkaitan dengan setiap proses:

Apabila anda melancarkan proses, ia berjalan dengan kebenaran yang sama seperti pengguna atau kumpulan yang menjalankannya, ini dikenali sebagai <b>ID pengguna berkesan</b>. UID ini digunakan untuk memberikan hak akses kepada proses. Jadi secara semula jadi jika Bob menjalankan perintah touch, proses akan berjalan sebagai dia dan mana-mana fail yang dia cipta akan berada di bawah pemilikannya.

Terdapat UID lain, dipanggil <b>ID pengguna sebenar</b> ini adalah ID pengguna yang melancarkan proses. Ini digunakan untuk mengesan siapa pengguna yang melancarkan proses.

UID terakhir adalah <b>ID pengguna tersimpan</b>, ini membolehkan proses beralih antara UID berkesan dan UID sebenar, dan sebaliknya. Ini berguna kerana kita tidak mahu proses kita berjalan dengan keistimewaan yang ditingkatkan sepanjang masa, ia hanya amalan yang baik untuk menggunakan keistimewaan khas pada masa tertentu.

Sekarang mari kita gabungkan semua ini dengan melihat perintah passwd sekali lagi.

Apabila menjalankan perintah passwd, UID berkesan anda adalah ID pengguna anda, katakan ia 500 buat masa ini. Oh tetapi tunggu, ingat perintah passwd mempunyai bit kebenaran SUID diaktifkan. Jadi apabila anda menjalankannya, UID berkesan anda sekarang adalah 0 (0 adalah UID root). Sekarang program ini boleh mengakses fail sebagai root.

Katakan anda mendapat sedikit rasa kuasa dan anda ingin mengubah kata laluan Sally, Sally mempunyai UID 600. Anda tidak akan bernasib baik, nasib baik proses itu juga mempunyai UID sebenar anda dalam kes ini 500. Ia tahu bahawa UID anda adalah 500 dan oleh itu anda tidak boleh mengubah kata laluan UID 600. (Ini sudah tentu sentiasa dipintas jika anda adalah superuser pada mesin dan boleh mengawal dan mengubah segalanya).

Oleh kerana anda menjalankan passwd, ia akan memulakan proses menggunakan UID sebenar anda, dan ia akan menyimpan UID pemilik fail (UID berkesan), jadi anda boleh beralih antara keduanya. Tidak perlu mengubah semua fail dengan akses root jika tidak diperlukan.

Kebanyakan masa UID sebenar dan UID berkesan adalah sama, tetapi dalam kes-kes seperti perintah passwd, ia akan berubah.

## Latihan

Kita belum membincangkan proses lagi, kita masih boleh melihat perubahan ini berlaku dalam masa nyata:

<ol>
<li>Buka satu tetingkap terminal, dan jalankan perintah: <b>watch -n 1 "ps aux | grep passwd"</b>. Ini akan memantau proses passwd.</li>
<li>Buka tetingkap terminal kedua dan jalankan: <b>passwd</b></li>
<li>Lihat pada tetingkap terminal pertama, anda akan melihat proses muncul untuk passwd. Lajur pertama dalam jadual proses adalah ID pengguna berkesan, lihatlah ia adalah pengguna root!</li>
</ol>

## Soalan Kuiz

UID manakah yang menentukan akses yang diberikan?

## Jawapan Kuiz

berkesan
