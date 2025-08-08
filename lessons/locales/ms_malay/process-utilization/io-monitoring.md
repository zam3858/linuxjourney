# Pemantauan I/O

## Kandungan Pelajaran

Kita juga boleh memantau penggunaan CPU serta memantau penggunaan cakera dengan alat yang berguna yang dikenali sebagai <b>iostat</b>

<pre>
pete@icebox:~$ iostat
Linux 3.13.0-39-lowlatency (icebox)     01/28/2016      _i686_  (1 CPU)

avg-cpu:  %user   %nice %system %iowait  %steal   %idle
           0.13    0.03    0.50    0.01    0.00   99.33

Device:            tps    kB_read/s    kB_wrtn/s    kB_read    kB_wrtn
sda               0.17         3.49         1.92     385106     212417
</pre>

Bahagian pertama ialah maklumat CPU:

<ul>
<li>%user - Tunjukkan peratusan penggunaan CPU yang berlaku semasa melaksanakan pada peringkat pengguna (aplikasi)</li>
<li>%nice - Tunjukkan peratusan penggunaan CPU yang berlaku semasa melaksanakan pada peringkat pengguna dengan keutamaan nice. penggunaan CPU pengguna dengan keutamaan nice</li>
<li>%system - Tunjukkan peratusan penggunaan CPU yang berlaku semasa melaksanakan pada peringkat sistem (kernel).</li>
<li>%iowait - Tunjukkan peratusan masa CPU atau CPU terbiar semasa sistem mempunyai permintaan I/O cakera yang belum selesai.</li>
<li>%steal - Tunjukkan peratusan masa yang dihabiskan dalam menunggu secara sukarela oleh CPU maya atau CPU semasa hipervisor sedang melayan pemproses maya yang lain.</li>
<li>%idle - Tunjukkan peratusan masa CPU atau CPU terbiar dan sistem tidak mempunyai permintaan I/O cakera yang belum selesai.</li>
</ul>

Bahagian kedua ialah penggunaan cakera:

<ul>
<li>tps - Menunjukkan bilangan pemindahan sesaat yang dikeluarkan kepada peranti. Pemindahan ialah permintaan I/O kepada peranti. Beberapa permintaan logik boleh digabungkan menjadi satu permintaan I/O kepada peranti. Pemindahan adalah saiz yang tidak ditentukan.</li>
<li>kB_read/s - Menunjukkan jumlah data yang dibaca daripada peranti yang dinyatakan dalam kilobait sesaat.</li>
<li>kB_wrtn/s - Menunjukkan jumlah data yang ditulis kepada peranti yang dinyatakan dalam kilobait sesaat.</li>
<li>kB_read - Jumlah kilobait yang dibaca.</li>
<li>kB_wrtn - Jumlah kilobait yang ditulis.</li>
</ul>

## Latihan

Gunakan iostat untuk melihat penggunaan cakera anda.

## Soalan Kuiz

Apakah arahan yang boleh digunakan untuk melihat penggunaan I/O dan CPU?

## Jawapan Kuiz

iostat