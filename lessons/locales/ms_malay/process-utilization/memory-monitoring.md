# Pemantauan Memori

## Kandungan Pelajaran

Selain pemantauan CPU dan pemantauan I/O, anda boleh memantau penggunaan memori anda dengan <b>vmstat</b>

<pre>
pete@icebox:~$ vmstat
procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st
 1  0      0 396528  38816 384036    0    0     4     2   38   79  0  0 99  0  0
</pre>

Medan adalah seperti berikut:

<b>procs</b>
<ul>
<li>r - Bilangan proses untuk masa jalan</li>
<li>b - Bilangan proses dalam tidur tidak boleh diganggu</li>
</ul>

<b>memori</b>
<ul>
<li>swpd - Jumlah memori maya yang digunakan</li>
<li>free - Jumlah memori bebas</li>
<li>buff - Jumlah memori yang digunakan sebagai penimbal</li>
<li>cache - Jumlah memori yang digunakan sebagai cache</li>
</ul>

<b>swap</b>
<ul>
<li>si - Jumlah memori yang ditukar masuk dari cakera</li>
<li>so - Jumlah memori yang ditukar keluar ke cakera</li>
</ul>

<b>io</b>
<ul>
<li>bi - Jumlah blok yang diterima masuk dari peranti blok</li>
<li>bo - Jumlah blok yang dihantar keluar ke peranti blok</li>
</ul>

<b>sistem</b>
<ul>
<li>in - Bilangan sampukan sesaat</li>
<li>cs - Bilangan suis konteks sesaat</li>
</ul>

<b>cpu</b>
<ul>
<li>us - Masa yang dihabiskan dalam masa pengguna</li>
<li>sy - Masa yang dihabiskan dalam masa kernel</li>
<li>id - Masa yang dihabiskan terbiar</li>
<li>wa - Masa yang dihabiskan menunggu IO</li>
</ul>

## Latihan

Lihat penggunaan memori anda dengan vmstat.

## Soalan Kuiz

Apakah alat yang digunakan untuk melihat penggunaan memori?

## Jawapan Kuiz

vmstat
