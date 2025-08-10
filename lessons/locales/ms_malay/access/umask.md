# Umask

## Kandungan Pelajaran

Setiap fail yang dicipta datang dengan set kebenaran lalai. Jika anda ingin mengubah set kebenaran lalai itu, anda boleh melakukannya dengan perintah umask. Perintah ini mengambil set kebenaran 3 bit yang kita lihat dalam kebenaran angka.

Tetapi bukannya menambah kebenaran ini, umask mengambil kebenaran ini.

<pre>$ umask 021</pre>

Dalam contoh di atas, kita menyatakan bahawa kita mahu kebenaran lalai fail baru untuk membolehkan pengguna mengakses semuanya, tetapi untuk kumpulan kita mahu mengambil kebenaran tulis mereka dan untuk orang lain kita mahu mengambil kebenaran boleh laksana mereka. Umask lalai pada kebanyakan pengedaran adalah 022, bermakna semua akses pengguna, tetapi tiada akses tulis untuk kumpulan dan pengguna lain.

Apabila anda menjalankan perintah umask ia akan memberikan set kebenaran lalai pada mana-mana fail baru yang anda buat. Walau bagaimanapun, jika anda mahu ia berterusan, anda perlu mengubah fail permulaan anda (.profile), tetapi kita akan membincangkan itu dalam pelajaran kemudian.

## Latihan

<ol>
<li>Cipta fail baru, kemudian perhatikan kebenaran fail tersebut.</li>
<li>Ubah umask dan kemudian cipta fail baru yang lain.</li>
<li>Periksa kebenaran sekali lagi pada fail baru, apa yang anda jangka untuk lihat?</li>
</ol>

## Soalan Kuiz

Perintah apakah yang digunakan untuk mengubah kebenaran fail lalai?

## Jawapan Kuiz

umask