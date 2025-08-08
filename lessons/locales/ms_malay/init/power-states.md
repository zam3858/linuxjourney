# Keadaan Kuasa

## Kandungan Pelajaran

Sukar untuk percaya kita sebenarnya belum membincangkan cara untuk mengawal keadaan sistem anda melalui baris perintah, tetapi apabila bercakap tentang init, kita bukan sahaja bercakap tentang mod yang membolehkan kita memulakan sistem kita, tetapi juga yang menghentikan sistem kita.

Untuk mematikan sistem anda:

<pre>$ sudo shutdown -h now</pre>

Ini akan menghentikan sistem (mematikannya), anda juga mesti menentukan masa bila anda mahu ini berlaku. Anda boleh menambah masa dalam minit yang akan mematikan sistem dalam jumlah masa itu.

<pre>$ sudo shutdown -h +2</pre>

Ini akan mematikan sistem anda dalam dua minit. Anda juga boleh memulakan semula dengan arahan shutdown:

<pre>$ sudo shutdown -r now</pre>

Atau gunakan sahaja arahan but semula:

<pre>$ sudo reboot</pre>

## Latihan

Apa yang anda fikir berlaku dengan init apabila anda mematikan mesin anda?

## Soalan Kuiz

Apakah arahan untuk mematikan sistem anda dalam 4 minit?

## Jawapan Kuiz

sudo shutdown -h +4