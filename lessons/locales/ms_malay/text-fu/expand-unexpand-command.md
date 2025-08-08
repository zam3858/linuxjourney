# kembangkan dan nyahkembangkan

## Kandungan Pelajaran

Dalam pelajaran kita mengenai arahan potong, kita mempunyai fail sample.txt kita yang mengandungi tab. Biasanya TAB akan menunjukkan perbezaan yang ketara tetapi sesetengah fail teks tidak menunjukkannya dengan cukup baik. Mempunyai TAB dalam fail teks mungkin bukan jarak yang anda inginkan. Untuk menukar TAB anda kepada ruang, gunakan arahan kembangkan.

<pre>$ expand sample.txt</pre>

Perintah di atas akan mencetak output dengan setiap TAB ditukar kepada sekumpulan ruang. Untuk menyimpan output ini dalam fail, gunakan pengalihan semula output seperti di bawah.

<pre>$ expand sample.txt > result.txt</pre>

Bertentangan dengan kembangkan, kita boleh menukar kembali setiap kumpulan ruang kepada TAB dengan arahan nyahkembangkan:

<pre>$ unexpand -a result.txt</pre>

## Latihan

Apa yang berlaku jika anda hanya menaip kembangkan tanpa input fail?

## Soalan Kuiz

Apakah arahan yang digunakan untuk menukar TAB kepada ruang?

## Jawapan Kuiz

kembangkan
