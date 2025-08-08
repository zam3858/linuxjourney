# sertai dan pisah

## Kandungan Pelajaran

Perintah sertai membolehkan anda menyertai beberapa fail bersama-sama dengan medan biasa:

Katakan saya mempunyai dua fail yang ingin saya sertai bersama:
<pre>file1.txt
1 John
2 Jane
3 Mary

file2.txt
1 Doe
2 Doe
3 Sue

$ join file1.txt file2.txt
1 John Doe
2 Jane Doe
3 Mary Sue
</pre>

Lihat bagaimana ia menyertai fail saya bersama-sama? Mereka disertai bersama oleh medan pertama secara lalai dan medan mesti sama, jika tidak anda boleh mengisihnya, jadi dalam kes ini fail disertai melalui 1, 2, 3.

Bagaimanakah kita akan menyertai fail berikut?

<pre>file1.txt
John 1
Jane 2
Mary 3

file2.txt
1 Doe
2 Doe
3 Sue
</pre>

Untuk menyertai fail ini anda perlu menentukan medan mana yang anda sertai, dalam kes ini kami mahu medan 2 pada file1.txt dan medan 1 pada file2.txt, jadi arahannya akan kelihatan seperti ini:

<pre>
$ join -1 2 -2 1 file1.txt file2.txt
1 John Doe
2 Jane Doe
3 Mary Sue
</pre>

-1 merujuk kepada file1.txt dan -2 merujuk kepada file2.txt. Cukup kemas. Anda juga boleh memisahkan fail kepada fail yang berbeza dengan arahan pisah:

<pre>$ split somefile</pre>

Ini akan memisahkannya kepada fail yang berbeza, secara lalai ia akan memisahkannya sebaik sahaja ia mencapai had 1000 baris. Fail dinamakan x** secara lalai.

## Latihan

Sertai dua fail dengan bilangan baris yang berbeza dalam setiap fail, apa yang berlaku?

## Soalan Kuiz

Apakah arahan yang akan anda gunakan untuk menyertai fail bernama kucing anjing lembu?

## Jawapan Kuiz

sertai kucing anjing lembu