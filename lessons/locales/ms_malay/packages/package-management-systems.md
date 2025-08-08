# yum dan apt

## Kandungan Pelajaran

Ah, Batman pengurusan pakej, sistem ini dilengkapi dengan semua pembaikan untuk menjadikan pemasangan, pengalihan dan perubahan pakej lebih mudah, termasuk memasang kebergantungan pakej. Dua sistem pengurusan yang paling popular ialah <b>yum</b> dan <b>apt</b>. Yum adalah eksklusif untuk keluarga Red Hat dan apt adalah eksklusif untuk keluarga Debian.

<b>Pasang pakej dari repositori</b>

<pre>
Debian: $ apt install nama_pakej
RPM: $ yum install nama_pakej
</pre>

<b>Alih keluar pakej</b>

<pre>
Debian: $ apt remove nama_pakej
RPM: $ yum erase nama_pakej
</pre>

<b>Mengemas kini pakej untuk repositori</b>

Amalan terbaik sentiasa mengemas kini repositori pakej anda supaya ia terkini sebelum anda memasang dan mengemas kini pakej.

<pre>
Debian: apt update; apt upgrade
RPM: yum update
</pre>

<b>Dapatkan maklumat tentang pakej yang dipasang</b>

<pre>
Debian: apt show nama_pakej
RPM: yum info nama_pakej
</pre>

## Latihan

Jalankan setiap arahan pakej ini dan lihat output yang anda terima.

## Soalan Kuiz

Apakah arahan yang digunakan untuk menunjukkan maklumat pakej pada sistem Debian?

## Jawapan Kuiz

apt show
