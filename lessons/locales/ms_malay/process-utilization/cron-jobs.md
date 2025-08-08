# Kerja Cron

## Kandungan Pelajaran

Walaupun kita telah bercakap tentang penggunaan sumber, saya fikir ini adalah masa yang baik untuk menyebut alat yang kemas dalam Linux yang digunakan untuk menjadualkan tugas menggunakan cron. Terdapat perkhidmatan yang menjalankan program untuk anda pada bila-bila masa yang anda jadualkan. Ini sangat berguna jika anda mempunyai skrip yang ingin anda jalankan sekali sehari yang perlu melaksanakan sesuatu untuk anda.

Sebagai contoh, katakan saya mempunyai skrip yang terletak di /home/pete/scripts/change_wallpaper. Saya menggunakan skrip ini setiap pagi untuk menukar gambar yang saya gunakan untuk kertas dinding saya, tetapi setiap pagi saya perlu melaksanakan skrip ini secara manual. Sebaliknya apa yang boleh saya lakukan ialah membuat kerja cron yang melaksanakan skrip saya melalui cron. Saya boleh menentukan masa yang saya mahu kerja cron ini dijalankan dan melaksanakan skrip saya.

<pre>30 08 * * * /home/pete/scripts/change_wallpaper</pre>

Medan adalah seperti berikut dari kiri ke kanan:
<ul>
<li>Minit - (0-59)</li>
<li>Jam - (0-23)</li>
<li>Hari dalam bulan - (1-31)</li>
<li>Bulan - (1-12)</li>
<li>Hari dalam minggu - (0-7). 0 dan 7 ditandakan sebagai Ahad</li>
</ul>

Tanda bintang dalam medan bermaksud untuk memadankan setiap nilai. Jadi dalam contoh saya di atas, saya mahu ini berjalan setiap hari dalam setiap bulan pada jam 8:30 pagi.

Untuk membuat kerja cron, hanya edit fail crontab:

<pre>crontab -e</pre>

## Latihan

Buat kerja cron yang ingin anda jalankan pada masa yang dijadualkan.

## Soalan Kuiz

Apakah arahan untuk mengedit kerja cron anda?

## Jawapan Kuiz

crontab -e