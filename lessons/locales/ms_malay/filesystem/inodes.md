# Inod

## Kandungan Pelajaran

Ingat bagaimana sistem fail kita terdiri daripada semua fail sebenar kita dan pangkalan data yang menguruskan fail-fail ini? Pangkalan data ini dikenali sebagai jadual inod.

<b>Apakah itu inod?</b>

Inod (nod indeks) ialah entri dalam jadual ini dan terdapat satu untuk setiap fail. Ia menerangkan segala-galanya tentang fail, seperti:

<ul>
<li>Jenis fail - fail biasa, direktori, peranti aksara, dsb</li>
<li>Pemilik</li>
<li>Kumpulan</li>
<li>Kebenaran akses</li>
<li>Cap masa - mtime (masa pengubahsuaian fail terakhir), ctime (masa perubahan atribut terakhir), atime (masa akses terakhir)</li>
<li>Bilangan pautan keras ke fail</li>
<li>Saiz fail</li>
<li>Bilangan blok yang diperuntukkan kepada fail</li>
<li>Penunjuk ke blok data fail - paling penting!</li>
</ul>

Pada asasnya inod menyimpan segala-galanya tentang fail, kecuali nama fail dan fail itu sendiri!

<b>Bilakah inod dicipta?</b>

Apabila sistem fail dicipta, ruang untuk inod juga diperuntukkan. Terdapat algoritma yang berlaku untuk menentukan berapa banyak ruang inod yang anda perlukan bergantung pada volum cakera dan banyak lagi. Anda mungkin pernah melihat ralat untuk isu kehabisan ruang cakera pada satu ketika dalam hidup anda. Perkara yang sama boleh berlaku untuk inod juga (walaupun kurang biasa), anda boleh kehabisan inod dan oleh itu tidak dapat mencipta lebih banyak fail. Ingat storan data bergantung pada kedua-dua data dan pangkalan data (inod).

Untuk melihat berapa banyak inod yang tinggal pada sistem anda, gunakan arahan <b>df -i</b>

<b>Maklumat Inod</b>

Inod dikenal pasti dengan nombor, apabila fail dicipta ia diberikan nombor inod, nombor itu diberikan dalam urutan berurutan. Walau bagaimanapun, anda kadang-kadang mungkin perasan apabila anda mencipta fail baharu, ia mendapat nombor inod yang lebih rendah daripada yang lain, ini kerana apabila inod dipadam, ia boleh digunakan semula oleh fail lain. Untuk melihat nombor inod jalankan <b>ls -li</b>:

<pre>
pete@icebox:~$ ls -li
140 drwxr-xr-x 2 pete pete 6 Jan 20 20:13 Desktop
141 drwxr-xr-x 2 pete pete 6 Jan 20 20:01 Documents
</pre>

Medan pertama dalam arahan ini menyenaraikan nombor inod.

Anda juga boleh melihat maklumat terperinci tentang fail dengan stat, ia memberitahu anda maklumat tentang inod juga.

<pre>
pete@icebox:~$ stat ~/Desktop/
  File: ‘/home/pete/Desktop/’
  Size: 6               Blocks: 0          IO Block: 4096   directory
Device: 806h/2054d      Inode: 140         Links: 2
Access: (0755/drwxr-xr-x)  Uid: ( 1000/   pete)   Gid: ( 1000/   pete)
Access: 2016-01-20 20:13:50.647435982 -0800
Modify: 2016-01-20 20:13:06.191675843 -0800
Change: 2016-01-20 20:13:06.191675843 -0800
 Birth: -
</pre>


<b>Bagaimanakah inod mencari fail?</b>

Kita tahu data kita ada di luar sana pada cakera di suatu tempat, malangnya ia mungkin tidak disimpan secara berurutan, jadi kita perlu menggunakan inod. Inod menunjuk ke blok data sebenar fail anda. Dalam sistem fail biasa (tidak semua berfungsi sama), setiap inod mengandungi 15 penunjuk, 12 penunjuk pertama menunjuk terus ke blok data. Penunjuk ke-13, menunjuk ke blok yang mengandungi penunjuk ke lebih banyak blok, penunjuk ke-14 menunjuk ke blok bersarang penunjuk yang lain, dan penunjuk ke-15 menunjuk sekali lagi ke blok penunjuk yang lain! Mengelirukan, saya tahu! Sebab ini dilakukan dengan cara ini adalah untuk mengekalkan struktur inod yang sama untuk setiap inod, tetapi dapat merujuk fail dengan saiz yang berbeza. Jika anda mempunyai fail kecil, anda boleh menemuinya dengan lebih cepat dengan 12 penunjuk langsung pertama, fail yang lebih besar boleh ditemui dengan sarang penunjuk. Sama ada cara struktur inod adalah sama.

## Latihan

Perhatikan beberapa nombor inod untuk fail yang berbeza, yang manakah biasanya dicipta dahulu?

## Soalan Kuiz

Bagaimanakah anda melihat berapa banyak inod yang tinggal pada sistem anda?

## Jawapan Kuiz

df -i