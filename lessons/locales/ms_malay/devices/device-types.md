# jenis peranti

## Kandungan Pelajaran

Sebelum kita berbual tentang cara peranti diuruskan, mari kita lihat beberapa peranti.

<pre>$ ls -l /dev
brw-rw----   1 root disk      8,   0 Dec 20 20:13 sda
crw-rw-rw-   1 root root      1,   3 Dec 20 20:13 null
srw-rw-rw-   1 root root           0 Dec 20 20:13 log
prw-r--r--   1 root root           0 Dec 20 20:13 fdata
</pre>

Lajur adalah seperti berikut dari kiri ke kanan:

<ul>
<li>Kebenaran</li>
<li>Pemilik</li>
<li>Kumpulan</li>
<li>Nombor Peranti Utama</li>
<li>Nombor Peranti Kecil</li>
<li>Cap Masa</li>
<li>Nama Peranti</li>
</ul>

Ingat dalam arahan ls anda boleh melihat jenis fail dengan bit pertama pada setiap baris. Fail peranti ditandakan seperti berikut:

<ul>
<li>c - aksara</li>
<li>b - blok</li>
<li>p - paip</li>
<li>s - soket</li>
</ul>

<b>Peranti Aksara</b>

Peranti ini memindahkan data, tetapi satu aksara pada satu masa. Anda akan melihat banyak peranti pseudo (/dev/null) sebagai peranti aksara, peranti ini tidak benar-benar disambungkan secara fizikal ke mesin, tetapi ia membolehkan sistem pengendalian berfungsi dengan lebih baik.

<b>Peranti Blok</b>

Peranti ini memindahkan data, tetapi dalam blok bersaiz tetap yang besar. Anda akan paling biasa melihat peranti yang menggunakan blok data sebagai peranti blok, seperti cakera keras, sistem fail, dsb.

<b>Peranti Paip</b>

Paip bernama membolehkan dua atau lebih proses berkomunikasi antara satu sama lain, ini serupa dengan peranti aksara, tetapi bukannya output dihantar ke peranti, ia dihantar ke proses lain.

<b>Peranti Soket</b>

Peranti soket memudahkan komunikasi antara proses, serupa dengan peranti paip tetapi ia boleh berkomunikasi dengan banyak proses sekaligus.

<b>Pencirian Peranti</b>

Peranti dicirikan menggunakan dua nombor, <b>nombor peranti utama</b> dan <b>nombor peranti kecil</b>. Anda boleh melihat nombor ini dalam contoh ls di atas, ia dipisahkan dengan koma. Sebagai contoh, katakan peranti mempunyai nombor peranti: <b>8, 0</b>:

Nombor peranti utama mewakili pemacu peranti yang digunakan, dalam kes ini 8, yang selalunya nombor utama untuk peranti blok sd. Nombor kecil memberitahu kernel peranti unik mana dalam kelas pemacu ini, dalam kes ini 0 digunakan untuk mewakili peranti pertama (a).

## Latihan

Lihat direktori /dev anda dan ketahui jenis peranti yang boleh anda lihat.

## Soalan Kuiz

Apakah simbol untuk peranti aksara dalam arahan ls -l?

## Jawapan Kuiz

c