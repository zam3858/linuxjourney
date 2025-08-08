# Keadaan Proses

## Kandungan Pelajaran

Mari kita lihat arahan ps aux sekali lagi:

<pre>$ ps aux</pre>

Dalam lajur STAT, anda akan melihat banyak nilai. Proses linux boleh berada dalam beberapa keadaan yang berbeza. Kod keadaan yang paling biasa anda akan lihat diterangkan di bawah:

<ul>
<li>R: berjalan atau boleh dijalankan, ia hanya menunggu CPU memprosesnya</li>
<li>S: Tidur boleh diganggu, menunggu peristiwa selesai, seperti input dari terminal</li>
<li>D: Tidur tidak boleh diganggu, proses yang tidak boleh dibunuh atau diganggu dengan isyarat, biasanya untuk menghilangkannya anda perlu but semula atau membetulkan isu tersebut</li>
<li>Z: Zombi, kita telah membincangkan dalam pelajaran sebelumnya bahawa zombi ialah proses yang ditamatkan yang sedang menunggu untuk statusnya dikumpulkan</li>
<li>T: Dihentikan, proses yang telah digantung/dihentikan</li>
</ul>

## Latihan

Lihat proses yang sedang berjalan pada sistem anda dan semak keadaan prosesnya.

## Soalan Kuiz

Apakah kod STAT yang digunakan untuk mewakili tidur yang tidak boleh diganggu?

## Jawapan Kuiz

D