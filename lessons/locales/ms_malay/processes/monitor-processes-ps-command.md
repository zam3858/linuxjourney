# ps (Proses)

## Kandungan Pelajaran

Proses ialah program yang sedang berjalan pada mesin anda. Ia diuruskan oleh kernel dan setiap proses mempunyai ID yang dikaitkan dengannya yang dipanggil <b>ID proses (PID).</b> PID ini diberikan mengikut urutan proses dicipta.

Teruskan dan jalankan arahan ps untuk melihat senarai proses yang sedang berjalan:

<pre>$ ps

PID        TTY     STAT   TIME          CMD
41230    pts/4    Ss        00:00:00     bash
51224    pts/4    R+        00:00:00     ps
</pre>

Ini menunjukkan kepada anda gambaran ringkas tentang proses semasa:

<ul>
<li>PID: ID Proses</li>
<li>TTY: Terminal kawalan yang dikaitkan dengan proses (kita akan membincangkan secara terperinci tentang ini kemudian)</li>
<li>STAT: Kod status proses</li>
<li>TIME: Jumlah masa penggunaan CPU</li>
<li>CMD: Nama boleh laksana/perintah</li>
</ul>

Jika anda melihat halaman manual untuk ps anda akan melihat bahawa terdapat banyak pilihan arahan yang boleh anda lalui, ia akan berbeza-beza bergantung pada pilihan yang ingin anda gunakan - BSD, GNU atau Unix. Pada pendapat saya gaya BSD lebih popular untuk digunakan, jadi kita akan menggunakannya. Jika anda ingin tahu perbezaan antara gaya ialah jumlah sengkang yang anda gunakan dan benderanya.

<pre>$ ps aux</pre>

<b>a</b> memaparkan semua proses yang sedang berjalan, termasuk yang dijalankan oleh pengguna lain. <b>u</b> menunjukkan lebih banyak butiran tentang proses. Dan akhirnya <b>x</b> menyenaraikan semua proses yang tidak mempunyai TTY yang dikaitkan dengannya, program ini akan menunjukkan ? dalam medan TTY, ia paling biasa dalam proses daemon yang dilancarkan sebagai sebahagian daripada permulaan sistem.

Anda akan perasan anda melihat lebih banyak medan sekarang, tidak perlu menghafal kesemuanya, dalam kursus kemudian mengenai proses lanjutan, kami akan membincangkan beberapa daripadanya sekali lagi:

<ul>
<li>USER: Pengguna yang berkesan (yang aksesnya kami gunakan)</li>
<li>PID: ID Proses</li>
<li>%CPU: Masa CPU yang digunakan dibahagikan dengan masa proses telah berjalan</li>
<li>%MEM: Nisbah saiz set pemastautin proses kepada memori fizikal pada mesin</li>
<li>VSZ: Penggunaan memori maya bagi keseluruhan proses</li>
<li>RSS: Saiz set pemastautin, memori fizikal yang tidak ditukar yang telah digunakan oleh tugas</li>
<li>TTY: Terminal kawalan yang dikaitkan dengan proses</li>
<li>STAT: Kod status proses</li>
<li>START: Masa mula proses</li>
<li>TIME: Jumlah masa penggunaan CPU</li>
<li>COMMAND: Nama boleh laksana/perintah</li>
</ul>

Arahan ps boleh menjadi sedikit kemas untuk dilihat, buat masa ini medan yang akan kita lihat paling banyak ialah PID, STAT dan COMMAND.

Satu lagi arahan yang sangat berguna ialah arahan <b>top</b>, top memberikan anda maklumat masa nyata tentang proses yang berjalan pada sistem anda dan bukannya gambar ringkas. Secara lalai anda akan mendapat penyegaran setiap 10 saat. Top ialah alat yang sangat berguna untuk melihat proses mana yang menggunakan banyak sumber anda.

<pre>$ top</pre>

## Latihan

Gunakan arahan ps dengan bendera yang berbeza dan lihat bagaimana output berubah.

## Soalan Kuiz

Apakah bendera ps yang digunakan untuk melihat maklumat terperinci tentang proses?

## Jawapan Kuiz

u