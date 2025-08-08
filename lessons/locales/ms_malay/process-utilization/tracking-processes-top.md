# Menjejaki proses: atas

## Kandungan Pelajaran

Dalam kursus ini, kita akan membincangkan cara membaca dan menganalisis penggunaan sumber pada sistem anda, pelajaran ini menunjukkan beberapa alat hebat untuk digunakan apabila anda perlu menjejaki apa yang dilakukan oleh sesuatu proses.

<b>atas</b>

Kami telah membincangkan tentang atas sebelum ini, tetapi kami akan mendalami secara spesifik tentang apa yang sebenarnya dipaparkannya. Ingat atas ialah alat yang kami gunakan untuk mendapatkan paparan masa nyata penggunaan sistem oleh proses kami:

<pre>
top - 18:06:26 up 6 days,  4:07,  2 users,  load average: 0.92, 0.62, 0.59
Tasks: 389 total,   1 running, 387 sleeping,   0 stopped,   1 zombie
%Cpu(s):  1.8 us,  0.4 sy,  0.0 ni, 97.6 id,  0.1 wa,  0.0 hi,  0.0 si,  0.0 st
KiB Mem:  32870888 total, 27467976 used,  5402912 free,   518808 buffers
KiB Swap: 33480700 total,    39892 used, 33440808 free. 19454152 cached Mem

  PID USER      PR  NI    VIRT    RES    SHR S  %CPU %MEM     TIME+ COMMAND
 6675 patty    20   0 1731472 520960  30876 S   8.3  1.6 160:24.79 chrome
 6926 patty    20   0  935888 163456  25576 S   4.3  0.5   5:28.13 chrome
</pre>

Mari kita lihat apa maksud output ini, anda tidak perlu menghafalnya, tetapi kembali ke sini apabila anda memerlukan rujukan.

<b>Baris pertama: Ini adalah maklumat yang sama yang akan anda lihat jika anda menjalankan arahan uptime (banyak lagi yang akan datang)</b>

Medan adalah dari kiri ke kanan:
<ol>
<li>Masa semasa</li>
<li>Berapa lama sistem telah berjalan</li>
<li>Berapa ramai pengguna yang sedang log masuk</li>
<li>Purata beban sistem (banyak lagi yang akan datang)</li>
</ol>

<b>Baris ke-2: Tugas yang sedang berjalan, tidur, dihentikan dan zombi</b>

<b>Baris ke-3: Maklumat CPU</b>

<ol>
<li>us: masa CPU pengguna - Peratusan masa CPU yang dihabiskan untuk menjalankan proses pengguna yang tidak dinice.</li>
<li>sy: masa CPU sistem - Peratusan masa CPU yang dihabiskan untuk menjalankan kernel dan proses kernel</li>
<li>ni: masa CPU nice - Peratusan masa CPU yang dihabiskan untuk menjalankan proses yang dinice</li>
<li>id: masa terbiar CPU - Peratusan masa CPU yang dihabiskan terbiar</li>
<li>wa: tunggu I/O - Peratusan masa CPU yang dihabiskan menunggu I/O. Jika nilai ini rendah, masalahnya mungkin bukan I/O cakera atau rangkaian</li>
<li>hi: sampukan perkakasan - Peratusan masa CPU yang dihabiskan untuk melayan sampukan perkakasan</li>
<li>si: sampukan perisian - Peratusan masa CPU yang dihabiskan untuk melayan sampukan perisian</li>
<li>st: masa curi - Jika anda menjalankan mesin maya, ini ialah peratusan masa CPU yang dicuri daripada anda untuk tugas lain</li>
</ol>

<b>Baris ke-4 dan ke-5: Penggunaan Memori dan Penggunaan Swap</b>

<b>Senarai Proses yang Sedang Digunakan</b>

<ol>
<li>PID: Id proses</li>
<li>USER: pengguna yang merupakan pemilik proses</li>
<li>PR: Keutamaan proses</li>
<li>NI: Nilai nice</li>
<li>VIRT: Memori maya yang digunakan oleh proses</li>
<li>RES: Memori fizikal yang digunakan daripada proses</li>
<li>SHR: Memori kongsi proses</li>
<li>S: Menunjukkan status proses: S=tidur, R=berjalan, Z=zombi,D=tidak boleh diganggu,T=dihentikan</li>
<li>%CPU - ini ialah peratus CPU yang digunakan oleh proses ini</li>
<li>%MEM - peratusan RAM yang digunakan oleh proses ini</li>
<li>TIME+ - jumlah masa aktiviti proses ini</li>
<li>COMMAND - nama proses</li>
</ol>

Anda juga boleh menentukan ID proses jika anda hanya ingin menjejaki proses tertentu:

<pre>$ top -p 1</pre>

## Latihan

Bermain-main dengan arahan atas dan lihat proses mana yang menggunakan sumber paling banyak.

## Soalan Kuiz

Apakah arahan yang memaparkan output yang sama dengan baris pertama di atas?

## Jawapan Kuiz

uptime