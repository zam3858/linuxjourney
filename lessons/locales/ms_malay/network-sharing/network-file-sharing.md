# Gambaran Keseluruhan Perkongsian Fail

## Kandungan Pelajaran

Anda biasanya bukan satu-satunya komputer dalam rangkaian anda, ini terutamanya berlaku jika anda bekerja dalam persekitaran komersial. Apabila kita ingin memindahkan data dari satu mesin ke mesin lain, kadang-kadang lebih mudah untuk menyambungkan pemacu USB dan menyalinnya secara manual. Tetapi kebanyakannya, jika anda bekerja dengan mesin pada rangkaian yang sama, cara untuk memindahkan data adalah melalui perkongsian fail rangkaian.

Dalam kursus ini kita akan membincangkan beberapa kaedah yang berbeza untuk menyalin data ke dan dari mesin yang berbeza pada rangkaian anda. Kita akan membincangkan beberapa salinan fail mudah, kemudian kita akan bercakap tentang melekapkan keseluruhan direktori pada mesin anda yang bertindak sebagai pemacu yang berasingan.

Satu alat perkongsian fail yang mudah ialah arahan <b>scp</b>. Arahan scp adalah singkatan untuk salinan selamat, ia berfungsi sama seperti arahan cp, tetapi membolehkan anda menyalin dari satu hos ke hos lain pada rangkaian yang sama. Ia berfungsi melalui ssh jadi semua tindakan anda menggunakan pengesahan dan keselamatan yang sama seperti ssh.

<b>Untuk menyalin fail dari hos tempatan ke hos jauh</b>

<pre>$ scp myfile.txt username@remotehost.com:/remote/directory</pre>

<b>Untuk menyalin fail dari hos jauh ke hos tempatan anda</b>

<pre>$ scp username@remotehost.com:/remote/directory/myfile.txt /local/directory</pre>

<b>Untuk menyalin direktori dari hos tempatan anda ke hos jauh</b>

<pre>$ scp -r mydir username@remotehost.com:/remote/directory</pre>

## Latihan

Cuba salin fail dengan scp dari satu mesin ke mesin lain.

## Soalan Kuiz

Apakah arahan yang boleh anda gunakan untuk menyalin fail dengan selamat dari satu hos ke hos lain?

## Jawapan Kuiz

scp
