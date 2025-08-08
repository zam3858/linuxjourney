# NFS

## Kandungan Pelajaran

Perkongsian fail rangkaian yang paling standard untuk Linux ialah NFS (Network File System), NFS membolehkan pelayan berkongsi direktori dan fail dengan satu atau lebih klien melalui rangkaian.

Kami tidak akan membincangkan butiran cara membuat pelayan NFS kerana ia boleh menjadi rumit, walau bagaimanapun kami akan membincangkan penyediaan klien NFS.

<b>Menyediakan klien NFS</b>

<pre>$ sudo service nfsclient start
$ sudo mount server:/directory /mount_directory</pre>

<b>Pemasangan automatik</b>

Katakan anda sering menggunakan pelayan NFS dan anda ingin mengekalkannya dilekapkan secara kekal, biasanya anda fikir anda akan mengedit fail /etc/fstab, tetapi anda mungkin tidak sentiasa mendapat sambungan ke pelayan dan itu boleh menyebabkan isu semasa but. Sebaliknya apa yang anda mahu lakukan ialah menyediakan pemasangan automatik supaya anda boleh menyambung ke pelayan NFS apabila anda perlu. Ini dilakukan dengan alat <b>automount</b> atau dalam versi Linux terkini <b>amd</b>. Apabila fail diakses dalam direktori yang ditentukan, automount akan mencari pelayan jauh dan melekapkannya secara automatik.

## Latihan

Baca halaman manual untuk NFS untuk mengetahui lebih lanjut.

## Soalan Kuiz

Apakah alat yang digunakan untuk mengurus titik lekap secara automatik?

## Jawapan Kuiz

automount