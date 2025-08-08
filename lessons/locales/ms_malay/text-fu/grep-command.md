# grep

## Kandungan Pelajaran

Perintah grep mungkin merupakan perintah pemprosesan teks yang paling biasa anda akan gunakan. Ia membolehkan anda mencari fail untuk aksara yang sepadan dengan corak tertentu. Bagaimana jika anda ingin tahu sama ada fail wujud dalam direktori tertentu atau jika anda ingin melihat sama ada rentetan ditemui dalam fail? Anda pastinya tidak akan menggali setiap baris teks, anda akan menggunakan grep!

Mari kita gunakan fail sample.txt kami sebagai contoh:

<pre>$ grep fox sample.txt</pre>

Anda akan melihat bahawa grep menemui musang dalam fail sample.txt.

Anda juga boleh grep corak yang tidak peka huruf besar-kecil dengan bendera -i:

<pre>$ grep -i somepattern somefile</pre>

Untuk menjadi lebih fleksibel dengan grep anda boleh menggabungkannya dengan arahan lain dengan |.

<pre>$ env | grep -i User</pre>

Seperti yang anda lihat grep agak serba boleh. Anda juga boleh menggunakan ungkapan nalar dalam corak anda:

<pre>$ ls /somedir | grep '.txt$'</pre>

Sepatutnya mengembalikan semua fail yang berakhir dengan .txt dalam somedir.

## Latihan

Anda mungkin pernah mendengar tentang egrep atau fgrep, ini adalah panggilan grep yang tidak digunakan lagi dan telah digantikan oleh grep -E dan grep -F. Baca halaman manual grep untuk mengetahui lebih lanjut.

## Soalan Kuiz

Apakah arahan yang anda gunakan untuk mencari corak tertentu?

## Jawapan Kuiz

grep