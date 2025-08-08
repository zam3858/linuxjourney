# stdout (Output Standard)

## Kandungan Pelajaran

Sekarang, kita telah biasa dengan banyak arahan dan outputnya dan itu membawa kita ke subjek seterusnya iaitu strim I/O (input/output). Mari kita jalankan arahan berikut dan kita akan bincangkan bagaimana ia berfungsi.

<pre>$ echo Hello World > peanuts.txt</pre>

Apa yang baru berlaku? Periksa direktori tempat anda menjalankan arahan itu dan lihatlah anda akan melihat fail yang dipanggil peanuts.txt, lihat di dalam fail itu dan anda akan melihat teks Hello World. Banyak perkara baru berlaku dalam satu arahan jadi mari kita pecahkannya.

Mula-mula mari kita pecahkan bahagian pertama:

<pre>$ echo Hello World</pre>

Kita tahu ini mencetak Hello World ke skrin, tetapi bagaimana? Proses menggunakan strim I/O untuk menerima input dan mengembalikan output. Secara lalai, arahan echo mengambil input (input standard atau stdin) dari papan kekunci dan mengembalikan output (output standard atau stdout) ke skrin. Jadi itulah sebabnya apabila anda menaip echo Hello World dalam shell anda, anda mendapat Hello World pada skrin. Walau bagaimanapun, pengalihan semula I/O membolehkan kita mengubah tingkah laku lalai ini yang memberi kita fleksibiliti fail yang lebih besar.

Mari kita teruskan ke bahagian seterusnya arahan:

<pre> > </pre>

> ialah operator pengalihan semula yang membolehkan kita menukar ke mana output standard pergi. Ia membolehkan kita menghantar output echo Hello World ke fail dan bukannya skrin. Jika fail itu belum wujud, ia akan menciptanya untuk kita. Walau bagaimanapun, jika ia wujud, ia akan menimpanya (anda boleh menambah bendera shell untuk mengelakkan ini bergantung pada shell yang anda gunakan).

Dan itulah pada asasnya bagaimana pengalihan semula stdout berfungsi!

Baiklah, katakan saya tidak mahu menimpa peanuts.txt saya, nasib baik ada operator pengalihan semula untuk itu juga, >>:

<pre>$ echo Hello World >> peanuts.txt</pre>

Ini akan menambahkan Hello World pada penghujung fail peanuts.txt, jika fail itu belum wujud, ia akan menciptanya untuk kita seperti yang dilakukannya dengan pengalih hala >!


## Latihan

Cuba beberapa arahan:

<pre>
$ ls -l /var/log > myoutput.txt
$ echo Hello World > rm
$ > somefile.txt
</pre>

## Soalan Kuiz

Apakah pengalih hala yang anda gunakan untuk menambahkan output pada fail?

## Jawapan Kuiz

>>