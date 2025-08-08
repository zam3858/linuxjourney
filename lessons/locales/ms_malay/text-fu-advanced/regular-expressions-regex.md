# regex (Ungkapan Nalar)

## Kandungan Pelajaran

Ungkapan nalar ialah alat yang berkuasa untuk melakukan pemilihan berasaskan corak. Ia menggunakan notasi khas yang serupa dengan yang telah kita temui seperti kad bebas *.

Kami akan meneliti beberapa ungkapan nalar yang paling biasa, ini hampir universal dengan mana-mana bahasa pengaturcaraan.

Baiklah gunakan frasa ini sebagai rentetan ujian kami:
<pre>
sally sells seashells
by the seashore
</pre>

<b>1. Permulaan baris dengan ^</b>

<pre>
<b>^</b>by
akan sepadan dengan baris "by the seashore"
</pre>

<b>2. Penghujung baris dengan $</b>

<pre>
seashore<b>$</b>
akan sepadan dengan baris "by the seashore"
</pre>

<b>3. Memadankan sebarang aksara tunggal dengan .</b>

<pre>
b<b>.</b>
akan sepadan dengan by
</pre>

<b>4. Notasi kurungan dengan [] dan ()</b>

Ini boleh menjadi sedikit rumit, kurungan membolehkan kita menentukan aksara yang terdapat di dalam kurungan.

<pre>
d<b>[iou]</b>g
akan sepadan dengan: dig, dog, dug
</pre>

Tag sauh ^ sebelum ini apabila digunakan dalam kurungan bermaksud apa sahaja kecuali aksara di dalam kurungan.

<pre>
d<b>[^i]</b>g
akan sepadan dengan: dog dan dug tetapi bukan dig
</pre>

Kurungan juga boleh menggunakan julat untuk meningkatkan jumlah aksara yang ingin anda gunakan.

<pre>
d<b>[a-c]</b>g
akan sepadan dengan corak seperti dag, dbg, dan dcg
</pre>

Berhati-hati kerana kurungan adalah peka huruf besar-kecil:

<pre>
d<b>[A-C]</b>g
akan sepadan dengan dAg, dBg dan dCg tetapi bukan dag, dbg dan dcg
</pre>

Dan itu adalah beberapa ungkapan nalar asas.

## Latihan

Cuba gabungkan ungkapan nalar dengan grep dan cari melalui beberapa fail.

<pre>
grep [regular expression here] [file]

## Soalan Kuiz

Apakah ungkapan nalar yang akan anda gunakan untuk memadankan satu aksara?

## Jawapan Kuiz

.