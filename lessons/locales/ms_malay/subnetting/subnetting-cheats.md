# Penipuan Subnetting

## Kandungan Pelajaran

Saya benci terpaksa menambah bahagian ini, dalam dunia nyata anda kemungkinan besar tidak perlu melakukan matematik subnet dengan tangan, walau bagaimanapun jika anda ditemu duga mengenai perkara ini, anda perlu tahu cara menukar ke dan dari bentuk binari untuk subnetting. Nasib baik terdapat beberapa penipuan aritmetik yang boleh anda hafal.

Mula-mula hafal pengiraan asas-2 anda, lakukannya sahaja:

<ul>
<li>2^1 = 2</li>
<li>2^2 = 4</li>
<li>2^3 = 8</li>
<li>2^4 = 16</li>
<li>2^5 = 32</li>
<li>2^6 = 64</li>
<li>2^7 = 128</li>
<li>2^8 = 256</li>
<li>2^9 = 512</li>
<li>2^10 = 1024</li>
<li>2^11 = 2048</li>
<li>2^12 = 4096</li>
</ul>

<b>Carta Perpuluhan ke Perduaan</b>

<pre>
1   1  1  1  1 1 1 1
128 64 32 16 8 4 2 1
</pre>

Terdapat banyak sebab mengapa carta berikut kelihatan seperti itu, jika anda ingin tahu bagaimana ia berfungsi terdapat banyak sumber dalam talian.

Ok, sudah hafal ini? Mari kita lakukan penukaran perpuluhan ke perduaan pantas:

<b>Tukar 192.168.23.43 kepada Perduaan</b>

Ingat: 128 / 64 / 32 / 16 / 8 / 4 / 2 / 1

Mari kita lalui penukaran oktet pertama kepada perduaan dan anda akan faham bagaimana selebihnya berfungsi.

<ol>
<li>Bolehkah anda menolak 192 - 128? Ya, jadi bit pertama ialah 1</li>
<li>192 - 128 = 64, nombor seterusnya dalam carta ialah 64, bolehkah anda menolak 64 - 64? Ya, jadi bit kedua ialah 1</li>
<li>Kami telah kehabisan nombor untuk ditolak, jadi bentuk perduaan 192 kami ialah 11000000</li>
</ol>

<b>Tukar Perduaan 11000000 kepada Perpuluhan</b>

Untuk penukaran perduaan ke perpuluhan anda menambah nombor yang mempunyai 1, jadi:

128 + 64 + 0 + 0 + 0 + 0 + 0 + 0 = 192!

## Latihan

Lihat alamat IP dan topeng subnet anda dan lihat berapa banyak hos yang boleh anda ada pada subnet anda.

## Soalan Kuiz

Apakah penukaran perduaan bagi 123?

## Jawapan Kuiz

1111011