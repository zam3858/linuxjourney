# stdin (Input Standard)

## Kandungan Pelajaran

Dalam pelajaran kita sebelum ini kita belajar bahawa kita mempunyai strim stdout yang berbeza yang boleh kita gunakan, seperti fail atau skrin. Terdapat juga strim input standard (stdin) yang berbeza yang boleh kita gunakan juga. Kita tahu bahawa kita mempunyai stdin dari peranti seperti papan kekunci, tetapi kita boleh menggunakan fail, output dari proses lain dan terminal juga, mari kita lihat contoh.

Mari kita gunakan fail peanuts.txt dalam pelajaran sebelumnya untuk contoh ini, ingat ia mempunyai teks Hello World di dalamnya.

<pre>$ cat <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt </pre>

Sama seperti kita mempunyai <b>&gt;</b> untuk pengalihan semula stdout, kita boleh menggunakan <b>&lt;</b> untuk pengalihan semula stdin.

Biasanya dalam arahan cat, anda menghantar fail kepadanya dan fail itu menjadi stdin, dalam kes ini, kami menghalakan semula peanuts.txt menjadi stdin kami. Kemudian output cat peanuts.txt yang akan menjadi Hello World dialihkan semula ke fail lain yang dipanggil banana.txt.

## Latihan

Cuba beberapa arahan:
<pre>
$ echo <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ ls <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ pwd <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
</pre>

## Soalan Kuiz

Apakah pengalih hala yang anda gunakan untuk menghalakan semula stdin?

## Jawapan Kuiz

<