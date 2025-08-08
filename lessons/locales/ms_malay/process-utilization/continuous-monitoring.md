# Pemantauan Berterusan

## Kandungan Pelajaran

Alat pemantauan ini bagus untuk dilihat apabila mesin anda menghadapi masalah, tetapi bagaimana pula dengan mesin yang menghadapi masalah apabila anda tidak melihat. Untuk itu, anda perlu menggunakan alat pemantauan berterusan, sesuatu yang akan mengumpul, melaporkan dan menyimpan maklumat aktiviti sistem anda. Dalam pelajaran ini kita akan membincangkan alat yang hebat untuk digunakan <b>sar</b>.

<b>Memasang sar</b>
Sar ialah alat yang digunakan untuk melakukan analisis sejarah pada sistem anda, mula-mula pastikan anda telah memasangnya dengan memasang pakej sysstat <b>sudo apt install sysstat</b>.

<b>Menyediakan pengumpulan data</b>
Biasanya sebaik sahaja anda memasang sysstat, sistem anda akan mula mengumpul data secara automatik, jika tidak, anda boleh mendayakannya dengan mengubah suai medan ENABLED dalam /etc/default/sysstat.

<b>Menggunakan sar</b>

<pre>$ sudo sar -q</pre>

Perintah ini akan menyenaraikan butiran dari awal hari.

<pre>$ sudo sar -r</pre>

Ini akan menyenaraikan butiran penggunaan memori dari awal hari.

<pre>$ sudo sar -P</pre>

Ini akan menyenaraikan butiran penggunaan CPU.

Untuk melihat paparan hari yang berbeza, anda boleh pergi ke /var/log/sysstat/saXX di mana XX ialah hari yang ingin anda lihat.

<pre>$sar -q /var/log/sysstat/sa02</pre>

## Latihan

Pasang sar pada sistem anda dan mula mengumpul dan menganalisis penggunaan sumber sistem anda.

## Soalan Kuiz

Apakah alat yang baik untuk digunakan untuk memantau sumber sistem?

## Jawapan Kuiz

sar
