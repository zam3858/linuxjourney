# Gambaran Keseluruhan Systemd

## Kandungan Pelajaran

Systemd perlahan-lahan menjadi standard yang muncul untuk init. Jika anda mempunyai direktori /usr/lib/systemd, kemungkinan besar anda menggunakan systemd.

Systemd menggunakan matlamat untuk menjalankan sistem anda. Pada asasnya anda mempunyai sasaran yang ingin anda capai dan sasaran ini juga mempunyai kebergantungan yang perlu kita capai. Systemd sangat fleksibel dan mantap, ia tidak mengikut urutan yang ketat untuk memulakan proses. Inilah yang berlaku semasa but systemd biasa:

<ol>
<li>Mula-mula, systemd memuatkan fail konfigurasinya, biasanya terletak di /etc/systemd/system atau /usr/lib/systemd/system</li>
<li>Kemudian ia menentukan matlamat butnya, yang biasanya default.target</li>
<li>Systemd memikirkan kebergantungan sasaran but dan mengaktifkannya</l>
</ol>

Sama seperti runlevel Sys V, systemd but ke sasaran yang berbeza:

<ul>
<li>poweroff.target - sistem tutup</li>
<li>rescue.target - mod pengguna tunggal</li>
<li>multi-user.target - berbilang pengguna dengan rangkaian</li>
<li>graphical.target - berbilang pengguna dengan rangkaian dan GUI</li>
<li>reboot.target - mulakan semula</li>
</ul>

Matlamat but lalai default.target biasanya menunjuk ke graphical.target.

Objek utama yang digunakan oleh systemd dikenali sebagai unit. Systemd bukan sahaja menghentikan dan memulakan perkhidmatan, ia boleh melekapkan sistem fail, memantau soket rangkaian anda, dsb dan kerana keteguhan itu ia mempunyai jenis unit yang berbeza yang dikendalikannya. Unit yang paling biasa ialah:

<ul>
<li>Unit perkhidmatan - ini adalah perkhidmatan yang telah kita mulakan dan hentikan, fail unit ini berakhir dengan .service</li>
<li>Unit lekap - Ini melekapkan sistem fail, fail unit ini berakhir dengan .mount</li>
<li>Unit sasaran - Ini mengumpulkan unit lain bersama-sama, fail berakhir dengan .target</li>
</ul>

Sebagai contoh, katakan kita but ke default.target kita, sasaran ini mengumpulkan unit networking.service, unit crond.service, dsb, jadi sebaik sahaja kita mengaktifkan satu unit, semua yang di bawah unit itu akan diaktifkan juga.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Apakah unit yang digunakan untuk mengumpulkan unit lain bersama-sama?

## Jawapan Kuiz

sasaran
