# potong

## Kandungan Pelajaran

Kita akan belajar beberapa arahan berguna yang boleh anda gunakan untuk memproses teks. Sebelum kita bermula, mari kita cipta fail yang akan kita gunakan. Salin dan tampal arahan berikut, sebaik sahaja anda melakukannya tambah TAB di antara malas dan anjing (tahan Ctrl-v + TAB).

<pre>$ echo 'The quick brown; fox jumps over the lazy  dog' > sample.txt</pre>

Perintah pertama yang akan kita pelajari ialah perintah potong. Ia mengekstrak bahagian teks dari fail.

Untuk mengekstrak kandungan dengan senarai aksara:

<pre>$ cut -c 5 sample.txt</pre>

Ini mengeluarkan aksara ke-5 dalam setiap baris fail. Dalam kes ini ia adalah "q", ambil perhatian bahawa ruang juga dikira sebagai aksara.

Untuk mengekstrak kandungan mengikut medan, kita perlu melakukan sedikit pengubahsuaian:

<pre>$ cut -f 2 sample.txt</pre>

Bendera -f atau medan memotong teks berdasarkan medan, secara lalai ia menggunakan TAB sebagai pembatas, jadi semua yang dipisahkan oleh TAB dianggap sebagai medan. Anda akan melihat "anjing" sebagai output anda.

Anda boleh menggabungkan bendera medan dengan bendera pembatas untuk mengekstrak kandungan dengan pembatas tersuai:

<pre>$ cut -f 1 -d ";" sample.txt</pre>

Ini akan menukar pembatas TAB kepada pembatas ";" dan kerana kita memotong medan pertama, hasilnya sepatutnya "The quick brown".

## Latihan

Apakah yang dilakukan oleh arahan berikut? Mengapa?

<pre>$ cut -c 5-10 sample.txt
$ cut -c 5- sample.txt
$ cut -c -5 sample.txt
</pre>

## Soalan Kuiz

Apakah arahan yang akan anda gunakan untuk mendapatkan aksara pertama setiap baris dalam fail?

## Jawapan Kuiz

potong -c 1