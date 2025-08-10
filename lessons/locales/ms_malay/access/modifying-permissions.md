# Mengubah Kebenaran

## Kandungan Pelajaran

Mengubah kebenaran boleh dilakukan dengan mudah menggunakan perintah <b>chmod</b>.

Pertama, pilih set kebenaran yang ingin anda ubah, pengguna, kumpulan atau lain-lain. Anda boleh menambah atau menghapus kebenaran dengan <b>+</b> atau <b>-</b>, mari lihat beberapa contoh.

<b>Menambah bit kebenaran pada fail</b>
<pre>$ chmod u+x myfile</pre>

Perintah di atas dibaca seperti ini: ubah kebenaran pada myfile dengan menambah bit kebenaran boleh laksana pada set pengguna. Jadi sekarang pengguna mempunyai kebenaran boleh laksana pada fail ini!

<b>Menghapus bit kebenaran pada fail</b>
<pre>$ chmod u-x myfile</pre>

<b>Menambah beberapa bit kebenaran pada fail</b>
<pre>$ chmod ug+w</pre>

Terdapat cara lain untuk mengubah kebenaran menggunakan format angka. Kaedah ini membolehkan anda mengubah kebenaran sekaligus. Bukannya menggunakan r, w, atau x untuk mewakili kebenaran, anda akan menggunakan perwakilan angka untuk satu set kebenaran. Jadi tidak perlu menentukan kumpulan dengan g atau pengguna dengan u.

Perwakilan angka adalah seperti berikut:

<ul>
<li>4: kebenaran baca</li>
<li>2: kebenaran tulis</li>
<li>1: kebenaran laksana</li>
</ul>

Mari lihat contoh:

<pre>$ chmod 755 myfile</pre>

Bolehkah anda meneka kebenaran apa yang kita berikan kepada fail ini? Mari kita pecahkan, jadi sekarang 755 meliputi kebenaran untuk semua set. Nombor pertama (7) mewakili kebenaran pengguna, nombor kedua (5) mewakili kebenaran kumpulan dan 5 terakhir mewakili kebenaran lain.

Tunggu sebentar, 7 dan 5 tidak disenaraikan di atas, dari mana kita mendapat nombor-nombor ini? Ingat kita menggabungkan semua kebenaran menjadi satu nombor sekarang, jadi anda perlu melibatkan sedikit matematik.

7 = 4 + 2 + 1, jadi 7 adalah kebenaran pengguna dan ia mempunyai kebenaran baca, tulis dan laksana

5 = 4 + 1, kumpulan mempunyai kebenaran baca dan laksana

5 = 4 + 1, dan semua pengguna lain mempunyai kebenaran baca dan laksana

Satu perkara yang perlu diperhatikan: bukan idea yang baik untuk mengubah kebenaran sesuka hati, anda berpotensi mendedahkan fail sensitif untuk diubah oleh semua orang, namun banyak kali anda sah ingin mengubah kebenaran, hanya berhati-hati ketika menggunakan perintah chmod.

## Latihan

Ubah beberapa kebenaran fail teks asas dan lihat bit berubah semasa anda melakukan ls -l.

## Soalan Kuiz

Nombor apakah yang mewakili kebenaran baca apabila menggunakan format angka?

## Jawapan Kuiz

4