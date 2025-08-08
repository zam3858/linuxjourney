# uniq (Unik)

## Kandungan Pelajaran

Perintah uniq (unik) ialah satu lagi alat yang berguna untuk menghuraikan teks.

Katakan anda mempunyai fail dengan banyak pendua:

<pre>
reading.txt
buku
buku
kertas
kertas
artikel
artikel
majalah
</pre>

Dan anda mahu mengalih keluar pendua, anda boleh menggunakan perintah uniq:

<pre>$ uniq reading.txt
buku
kertas
artikel
majalah</pre>

Mari kita dapatkan kiraan berapa banyak kejadian sesuatu baris:

<pre>$ uniq -c reading.txt
2 buku
2 kertas
2 artikel
1 majalah</pre>

Mari kita dapatkan nilai unik sahaja:

<pre>$ uniq -u reading.txt
majalah</pre>

Mari kita dapatkan nilai pendua sahaja:

<pre>$ uniq -d reading.txt
buku
kertas
artikel
</pre>

<b>Nota</b> : uniq tidak mengesan baris pendua melainkan ia bersebelahan. Contohnya:

Katakan anda mempunyai fail dengan pendua yang tidak bersebelahan:

<pre>
reading.txt
buku
kertas
buku
kertas
artikel
majalah
artikel
</pre>

<pre>$ uniq reading.txt
reading.txt
buku
kertas
buku
kertas
artikel
majalah
artikel</pre>

Hasil yang dikembalikan oleh uniq akan mengandungi semua entri tidak seperti contoh pertama.

Untuk mengatasi batasan uniq ini, kita boleh menggunakan sort dalam kombinasi dengan uniq:

<pre>
$ sort reading.txt | uniq
artikel
buku
majalah
kertas</pre>

## Latihan

Apakah hasil yang akan anda perolehi jika anda mencuba uniq -uc?

## Soalan Kuiz

Apakah arahan yang akan anda gunakan untuk mengalih keluar pendua dalam fail?

## Jawapan Kuiz

uniq
