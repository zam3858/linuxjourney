# swap

## Kandungan Pelajaran

Dalam contoh kami sebelum ini, saya menunjukkan kepada anda cara melihat jadual partition anda, mari kita lawati semula contoh itu, lebih khusus baris ini:

<pre>
Number  Start   End     Size    Type      File system     Flags
 5      6861MB  7380MB  519MB   logical   linux-swap(v1)
</pre>

Apakah partition swap ini? Swap ialah apa yang kita gunakan untuk memperuntukkan memori maya kepada sistem kita. Jika anda kekurangan memori, sistem menggunakan partition ini untuk "menukar" kepingan memori proses terbiar ke cakera, jadi anda tidak terbeban untuk memori.

<b>Menggunakan partition untuk ruang swap</b>

Katakan kita mahu menetapkan partition /dev/sdb2 kita untuk digunakan untuk ruang swap.

<ol>
<li>Mula-mula pastikan kita tidak mempunyai apa-apa pada partition</li>
<li>Jalankan: mkswap /dev/sdb2 untuk memulakan kawasan swap</li>
<li>Jalankan: swapon /dev/sdb2 ini akan mendayakan peranti swap</li>
<li>Jika anda mahu partition swap berterusan semasa but, anda perlu menambah entri pada fail /etc/fstab. sw ialah jenis sistem fail yang akan anda gunakan.</li>
<li>Untuk mengalih keluar swap: swapoff /dev/sdb2</li>
</ol>

Secara amnya anda harus memperuntukkan kira-kira dua kali lebih banyak ruang swap daripada memori yang anda ada. Tetapi sistem moden hari ini biasanya cukup berkuasa dan mempunyai RAM yang mencukupi.

## Latihan

Bahagikan ruang kosong dalam pemacu USB untuk ruang swap.

## Soalan Kuiz

Apakah arahan untuk mendayakan ruang swap pada peranti?

## Jawapan Kuiz

swapon
