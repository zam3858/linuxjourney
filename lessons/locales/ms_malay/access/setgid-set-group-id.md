# Setgid

## Kandungan Pelajaran

Serupa dengan bit kebenaran set ID pengguna, terdapat bit kebenaran set ID kumpulan (SGID). Bit ini membolehkan program berjalan seolah-olah ia adalah ahli kumpulan tersebut.

Mari lihat satu contoh:

<pre>$ ls -l /usr/bin/wall
-rwxr-sr-x 1 root tty 19024 Dec 14 11:45 /usr/bin/wall
</pre>

Kita boleh lihat sekarang bahawa bit kebenaran berada dalam set kebenaran kumpulan.

<b>Mengubah SGID</b>

<pre>$ sudo chmod g+s myfile
$ sudo chmod 2555 myfile
</pre>

Perwakilan angka untuk SGID adalah 2.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Nombor apakah yang mewakili SGID?

## Jawapan Kuiz

2