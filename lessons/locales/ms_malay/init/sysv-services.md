# Perkhidmatan Sistem V

## Kandungan Pelajaran

Terdapat banyak alat baris perintah yang boleh anda gunakan untuk mengurus perkhidmatan Sys V.

<b>Senaraikan perkhidmatan</b>

<pre>$ service --status-all</pre>

<b>Mulakan perkhidmatan</b>

<pre>$ sudo service networking start</pre>

<b>Hentikan perkhidmatan</b>

<pre>$ sudo service networking stop</pre>

<b>Mulakan semula perkhidmatan</b>

<pre>$ sudo service networking restart</pre>

Perintah ini tidak khusus untuk sistem init Sys V, anda boleh menggunakan perintah ini untuk mengurus perkhidmatan Upstart juga. Oleh kerana Linux cuba beralih daripada skrip init Sys V yang lebih tradisional, masih ada perkara yang disediakan untuk membantu peralihan itu.

## Latihan

Urus beberapa perkhidmatan dan ubah keadaannya, apa yang anda perhatikan?

## Soalan Kuiz

Apakah arahan untuk menghentikan perkhidmatan bernama kacang dengan Sys V?

## Jawapan Kuiz

sudo service peanut stop