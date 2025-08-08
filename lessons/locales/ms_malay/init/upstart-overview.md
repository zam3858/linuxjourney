# Gambaran Keseluruhan Upstart

## Kandungan Pelajaran

Upstart dibangunkan oleh Canonical, jadi ia adalah pelaksanaan init pada Ubuntu untuk seketika, walau bagaimanapun pada pemasangan Ubuntu moden systemd kini digunakan. Upstart dicipta untuk memperbaiki isu dengan Sys V, seperti proses permulaan yang ketat, penyekatan tugas, dsb. Model pacuan peristiwa dan kerja Upstart membolehkannya bertindak balas terhadap peristiwa semasa ia berlaku.

Untuk mengetahui sama ada anda menggunakan Upstart, jika anda mempunyai direktori /usr/share/upstart itu adalah penunjuk yang cukup baik.

Kerja ialah tindakan yang dilakukan oleh Upstart dan peristiwa ialah mesej yang diterima daripada proses lain untuk mencetuskan kerja. Untuk melihat senarai kerja dan konfigurasinya:

<pre>
pete@icebox:~$ ls /etc/init
acpid.conf                   mountnfs.sh.conf
alsa-restore.conf            mtab.sh.conf
alsa-state.conf              networking.conf
alsa-store.conf              network-interface.conf
anacron.conf                 network-interface-container.conf
</pre>

Di dalam konfigurasi kerja ini, ia akan menyertakan maklumat tentang cara memulakan kerja dan bila untuk memulakan kerja.

Sebagai contoh, dalam fail networking.conf, ia boleh mengatakan sesuatu yang semudah:
<pre>
start on runlevel [235]
stop on runlevel [0]
</pre>

Ini bermakna ia akan mula menyediakan rangkaian pada runlevel 2, 3 atau 5 dan akan menghentikan rangkaian pada runlevel 0. Terdapat banyak cara untuk menulis fail konfigurasi dan anda akan menemuinya apabila anda melihat konfigurasi kerja yang berbeza yang tersedia.

Cara Upstart berfungsi ialah:

<ol>
<li>Mula-mula, ia memuatkan konfigurasi kerja dari /etc/init</li>
<li>Sebaik sahaja peristiwa permulaan berlaku, ia akan menjalankan kerja yang dicetuskan oleh peristiwa itu.</li>
<li>Kerja-kerja ini akan membuat peristiwa baharu dan kemudian peristiwa itu akan mencetuskan lebih banyak kerja</li>
<li>Upstart terus melakukan ini sehingga ia melengkapkan semua kerja yang diperlukan</li>
</ol>

## Latihan

Jika anda menjalankan Upstart, lihat jika anda boleh memahami konfigurasi kerja dalam /etc/init.

## Soalan Kuiz

Apakah pelaksanaan init yang digunakan oleh Ubuntu?

## Jawapan Kuiz

upstart
