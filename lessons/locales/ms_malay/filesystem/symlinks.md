# pautan simbolik

## Kandungan Pelajaran

Mari kita gunakan contoh maklumat inod sebelum ini:

<pre>
pete@icebox:~$ ls -li
140 drwxr-xr-x 2 pete pete 6 Jan 20 20:13 Desktop
141 drwxr-xr-x 2 pete pete 6 Jan 20 20:01 Documents
</pre>

Anda mungkin perasan bahawa kita telah mengabaikan medan ketiga dalam arahan ls, medan itu ialah kiraan pautan. Kiraan pautan ialah jumlah pautan keras yang dimiliki oleh fail, baik itu tidak bermakna apa-apa kepada anda sekarang. Jadi mari kita bincangkan pautan terlebih dahulu.

<b>Pautan Simbolik</b>

Dalam sistem pengendalian Windows, terdapat perkara yang dikenali sebagai pintasan, pintasan hanyalah alias kepada fail lain. Jika anda melakukan sesuatu pada fail asal, anda berpotensi memecahkan pintasan itu. Dalam Linux, yang setara dengan pintasan ialah pautan simbolik (atau pautan lembut atau pautan simbolik). Pautan simbolik membolehkan kita memaut ke fail lain dengan nama failnya. Jenis pautan lain yang terdapat dalam Linux ialah pautan keras, ini sebenarnya fail lain dengan pautan ke inod. Mari kita lihat apa yang saya maksudkan dalam amalan bermula dengan pautan simbolik.

<pre>
pete@icebox:~/Desktop$ echo 'myfile' > myfile
pete@icebox:~/Desktop$ echo 'myfile2' > myfile2
pete@icebox:~/Desktop$ echo 'myfile3' > myfile3

pete@icebox:~/Desktop$ ln -s myfile myfilelink
pete@icebox:~/Desktop$ ls -li
total 12
  151 -rw-rw-r-- 1 pete pete 7 Jan 21 21:36 myfile
93401 -rw-rw-r-- 1 pete pete 8 Jan 21 21:36 myfile2
93402 -rw-rw-r-- 1 pete pete 8 Jan 21 21:36 myfile3
93403 lrwxrwxrwx 1 pete pete 6 Jan 21 21:39 myfilelink -> myfile
</pre>

Anda boleh lihat bahawa saya telah membuat pautan simbolik bernama myfilelink yang menunjuk ke myfile. Pautan simbolik ditandakan dengan ->. Perhatikan bagaimana saya mendapat nombor inod baharu, pautan simbolik hanyalah fail yang menunjuk ke nama fail. Apabila anda mengubah suai pautan simbolik, fail itu juga akan diubah suai. Nombor inod adalah unik untuk sistem fail, anda tidak boleh mempunyai dua nombor inod yang sama dalam satu sistem fail, bermakna anda tidak boleh merujuk fail dalam sistem fail yang berbeza dengan nombor inodnya. Walau bagaimanapun, jika anda menggunakan pautan simbolik, ia tidak menggunakan nombor inod, ia menggunakan nama fail, jadi ia boleh dirujuk merentasi sistem fail yang berbeza.

<b>Pautan Keras</b>

Mari kita lihat contoh pautan keras:

<pre>
pete@icebox:~/Desktop$ ln myfile2 myhardlink
pete@icebox:~/Desktop$ ls -li
total 16
  151 -rw-rw-r-- 1 pete pete 7 Jan 21 21:36 myfile
93401 -rw-rw-r-- 2 pete pete 8 Jan 21 21:36 myfile2
93402 -rw-rw-r-- 1 pete pete 8 Jan 21 21:36 myfile3
93403 lrwxrwxrwx 1 pete pete 6 Jan 21 21:39 myfilelink -> myfile
93401 -rw-rw-r-- 2 pete pete 8 Jan 21 21:36 myhardlink
</pre>

Pautan keras hanya mencipta fail lain dengan pautan ke inod yang sama. Jadi jika saya mengubah suai kandungan myfile2 atau myhardlink, perubahan itu akan dilihat pada kedua-duanya, tetapi jika saya memadam myfile2, fail itu masih boleh diakses melalui myhardlink. Di sinilah kiraan pautan kami dalam arahan ls dimainkan. Kiraan pautan ialah bilangan pautan keras yang dimiliki oleh inod, apabila anda mengalih keluar fail, ia akan mengurangkan kiraan pautan itu. Inod hanya dipadam apabila semua pautan keras ke inod telah dipadamkan. Apabila anda mencipta fail, kiraan pautannya ialah 1 kerana ia adalah satu-satunya fail yang menunjuk ke inod itu. Tidak seperti pautan simbolik, pautan keras tidak merentangi sistem fail kerana inod adalah unik untuk sistem fail.

<b>Mencipta pautan simbolik</b>

<pre>
$ ln -s myfile mylink</pre>

Untuk mencipta pautan simbolik, anda menggunakan arahan ln dengan -s untuk simbolik dan anda menentukan fail sasaran dan kemudian nama pautan.

<b>Mencipta pautan keras</b>

<pre>
$ ln somefile somelink</pre>

Sama seperti penciptaan pautan simbolik, kecuali kali ini anda meninggalkan -s.

## Latihan

Bermain-main dengan membuat pautan simbolik dan pautan keras, padam beberapa dan lihat apa yang berlaku.

## Soalan Kuiz

Apakah arahan yang digunakan untuk membuat pautan simbolik?

## Jawapan Kuiz

ln -s
