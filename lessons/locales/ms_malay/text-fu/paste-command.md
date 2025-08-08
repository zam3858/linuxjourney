# tampal

## Kandungan Pelajaran

Perintah tampal adalah serupa dengan perintah cat, ia menggabungkan baris bersama-sama dalam fail. Mari kita cipta fail baharu dengan kandungan berikut:

<pre>
sample2.txt
The
quick
brown
fox
</pre>

Mari kita gabungkan semua baris ini menjadi satu baris:

<pre>$ paste -s sample2.txt</pre>

Pembatas lalai untuk tampal ialah TAB, jadi sekarang terdapat satu baris dengan TAB memisahkan setiap perkataan.

Mari kita tukar pembatas ini (-d) kepada sesuatu yang lebih mudah dibaca:

<pre>$ paste -d ' ' -s sample2.txt</pre>

Sekarang semuanya sepatutnya berada pada satu baris yang dibatasi oleh ruang.

## Latihan

Cuba tampal beberapa fail bersama-sama, apa yang berlaku?

## Soalan Kuiz

Apakah bendera yang anda gunakan dengan tampal untuk membuat semuanya menjadi satu baris?

## Jawapan Kuiz

-s