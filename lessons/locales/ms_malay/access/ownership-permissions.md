# Kebenaran Pemilikan

## Kandungan Pelajaran

Selain mengubah kebenaran pada fail, anda juga boleh mengubah pemilikan kumpulan dan pengguna fail.

<b>Mengubah pemilikan pengguna</b>

<pre>$ sudo chown patty myfile</pre>

Perintah ini akan menetapkan pemilik myfile kepada patty.

<b>Mengubah pemilikan kumpulan</b>

<pre>$ sudo chgrp whales myfile</pre>

Perintah ini akan menetapkan kumpulan myfile kepada whales.

<b>Mengubah pemilikan pengguna dan kumpulan pada masa yang sama</b>
Jika anda menambah titik bertindih dan nama kumpulan selepas pengguna, anda boleh menetapkan kedua-dua pengguna dan kumpulan pada masa yang sama.

<pre>$ sudo chown patty:whales myfile</pre>

## Latihan

Ubah kumpulan dan pengguna beberapa fail ujian. Selepas itu lihat kebenaran dengan ls -l.

## Soalan Kuiz

Perintah apakah yang anda gunakan untuk mengubah pemilikan pengguna?

## Jawapan Kuiz

chown