# Gambaran Keseluruhan Sistem V

## Kandungan Pelajaran

Tujuan utama init adalah untuk memulakan dan menghentikan proses penting pada sistem. Terdapat tiga pelaksanaan utama init dalam Linux, Sistem V, Upstart dan systemd. Dalam pelajaran ini, kita akan membincangkan versi init yang paling tradisional, init Sistem V atau Sys V (disebut sebagai 'Sistem Lima').

Untuk mengetahui sama ada anda menggunakan pelaksanaan init Sys V, jika anda mempunyai fail /etc/inittab, kemungkinan besar anda menjalankan Sys V.

Sys V memulakan dan menghentikan proses secara berurutan, jadi katakan jika anda ingin memulakan perkhidmatan bernama foo-a, sebelum foo-b boleh berfungsi, anda perlu memastikan foo-a sudah berjalan. Sys V melakukannya dengan skrip, skrip ini memulakan dan menghentikan perkhidmatan untuk kami, kami boleh menulis skrip kami sendiri atau kebanyakannya menggunakan yang sudah dibina dalam sistem pengendalian dan digunakan untuk memuatkan perkhidmatan penting.

Kelebihan menggunakan pelaksanaan init ini, ialah ia agak mudah untuk menyelesaikan kebergantungan, kerana anda tahu foo-a datang sebelum foo-b, walau bagaimanapun prestasi tidak hebat kerana biasanya satu perkara bermula atau berhenti pada satu masa.

Apabila menggunakan Sys V, keadaan mesin ditakrifkan oleh runlevel yang ditetapkan dari 0 hingga 6. Mod yang berbeza ini akan berbeza-beza bergantung pada pengedaran, tetapi kebanyakannya akan kelihatan seperti berikut:

<ul>
<li>0: Tutup</li>
<li>1: Mod Pengguna Tunggal</li>
<li>2: Mod berbilang pengguna tanpa rangkaian</li>
<li>3: Mod berbilang pengguna dengan rangkaian</li>
<li>4: Tidak digunakan</li>
<li>5: Mod berbilang pengguna dengan rangkaian dan GUI</li>
<li>6: But semula</li>
</ul>

Apabila sistem anda dimulakan, ia melihat runlevel mana anda berada dan melaksanakan skrip yang terletak di dalam konfigurasi runlevel itu. Skrip terletak di <b>/etc/rc.d/rc[nombor runlevel].d/</b> atau <b>/etc/init.d</b>. Skrip yang bermula dengan S(mula) atau K(bunuh) akan berjalan semasa permulaan dan penutupan, masing-masing. Nombor di sebelah aksara ini ialah urutan ia berjalan.

Sebagai contoh:

<pre>
pete@icebox:/etc/rc.d/rc0.d$ ls
K10updates  K80openvpn
</pre>

Kita lihat apabila kita beralih ke runlevel 0 atau mod tutup, mesin kita akan cuba menjalankan skrip untuk membunuh perkhidmatan kemas kini dan kemudian openvpn. Untuk mengetahui runlevel mana mesin anda but, anda boleh melihat runlevel lalai dalam fail /etc/inittab. Anda juga boleh menukar runlevel lalai anda dalam fail ini juga.

Satu perkara yang perlu diberi perhatian, Sistem V perlahan-lahan digantikan, mungkin bukan hari ini, atau bahkan bertahun-tahun dari sekarang. Walau bagaimanapun, anda mungkin melihat runlevel muncul dalam pelaksanaan init lain, ini terutamanya untuk menyokong perkhidmatan yang hanya dimulakan atau dihentikan menggunakan skrip init Sistem V.

## Latihan

Jika anda menjalankan Sistem V, tukar runlevel lalai mesin anda kepada sesuatu yang lain dan lihat apa yang berlaku.

## Soalan Kuiz

Runlevel manakah yang biasanya digunakan untuk penutupan?

## Jawapan Kuiz

0
