# Penggunaan Cakera

## Kandungan Pelajaran

Terdapat beberapa alat yang boleh anda gunakan untuk melihat penggunaan cakera anda:

<pre>
pete@icebox:~$ df -h
Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/sda1       6.2G  2.3G  3.6G  40% /
</pre>

Perintah df menunjukkan kepada anda penggunaan sistem fail yang sedang anda lekapkan. Bendera -h memberikan anda format yang boleh dibaca manusia. Anda boleh melihat peranti itu, dan berapa banyak kapasiti yang digunakan dan tersedia.

Katakan cakera anda semakin penuh dan anda ingin tahu fail atau direktori mana yang menggunakan ruang itu, untuk itu anda boleh menggunakan perintah <b>du</b>.

<pre>$ du -h</pre>

Ini menunjukkan kepada anda penggunaan cakera bagi direktori semasa anda berada, anda boleh melihat direktori akar dengan <b>du -h /</b> tetapi itu boleh menjadi sedikit bersepah.

Kedua-dua arahan ini sangat serupa dalam sintaks sehingga sukar untuk mengingati yang mana satu untuk digunakan, untuk memeriksa berapa banyak <b>cakera</b> anda yang <b>bebas</b> gunakan df. Untuk memeriksa <b>penggunaan cakera</b>, gunakan du.

## Latihan

Lihat penggunaan cakera dan ruang kosong anda dengan kedua-dua du dan df.

## Soalan Kuiz

Apakah arahan yang digunakan untuk menunjukkan berapa banyak ruang yang bebas pada cakera anda?

## Jawapan Kuiz

df
