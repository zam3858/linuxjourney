# lekap dan nyahlekap

## Kandungan Pelajaran

Sebelum anda boleh melihat kandungan sistem fail anda, anda perlu melekapkannya. Untuk melakukannya, saya memerlukan lokasi peranti, jenis sistem fail dan titik lekap, titik lekap ialah direktori pada sistem di mana sistem fail akan dilampirkan. Jadi pada asasnya kita mahu melekapkan peranti kita ke titik lekap.

Mula-mula cipta titik lekap, dalam kes kami <b>mkdir /mydrive</b>

<pre>$ sudo mount -t ext4 /dev/sdb2 /mydrive</pre>

Semudah itu! Sekarang apabila kita pergi ke /mydrive kita boleh melihat kandungan sistem fail kita, <b>-t</b> menentukan jenis sistem fail, kemudian kita mempunyai lokasi peranti, kemudian titik lekap.

Untuk menyahlekap peranti dari titik lekap:

<pre>$ sudo umount /mydrive
atau
$ sudo umount /dev/sdb2</pre>

Ingat bahawa kernel menamakan peranti mengikut urutan ia menemuinya. Bagaimana jika nama peranti kita berubah atas sebab tertentu selepas kita melekapkannya? Mujurlah, anda boleh menggunakan ID unik universal (UUID) peranti dan bukannya nama.

Untuk melihat UUIDS pada sistem anda untuk peranti blok:

<pre>
pete@icebox:~$ sudo blkid
/dev/sda1: UUID="130b882f-7d79-436d-a096-1e594c92bb76" TYPE="ext4"
/dev/sda5: UUID="22c3d34b-467e-467c-b44d-f03803c2c526" TYPE="swap"
/dev/sda6: UUID="78d203a0-7c18-49bd-9e07-54f44cdb5726" TYPE="xfs"
</pre>

Kita boleh melihat nama peranti kita, jenis sistem fail yang sepadan dan UUIDnya. Sekarang apabila kita mahu melekapkan sesuatu, kita boleh menggunakan:

<pre>$ sudo mount UUID=130b882f-7d79-436d-a096-1e594c92bb76 /mydrive</pre>

Kebanyakan masa anda tidak perlu melekapkan peranti melalui UUID mereka, lebih mudah menggunakan nama peranti dan selalunya sistem pengendalian akan tahu untuk melekapkan peranti biasa seperti pemacu USB. Jika anda perlu melekapkan sistem fail secara automatik semasa permulaan walaupun seperti jika anda menambah cakera keras kedua, anda akan mahu menggunakan UUID dan kami akan membincangkannya dalam pelajaran seterusnya.

## Latihan

Lihat halaman manual untuk lekap dan nyahlekap dan lihat pilihan lain yang boleh anda gunakan.

## Soalan Kuiz

Apakah arahan yang digunakan untuk melampirkan sistem fail?

## Jawapan Kuiz

lekap