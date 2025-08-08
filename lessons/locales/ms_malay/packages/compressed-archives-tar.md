# tar dan gzip

## Kandungan Pelajaran

Sebelum kita membincangkan pemasangan pakej dan pengurus yang berbeza, kita perlu membincangkan pengarkiban dan pemampatan fail, kerana kemungkinan besar anda akan menemuinya apabila anda mencari perisian di internet.

Anda mungkin sudah tahu apa itu arkib fail, kemungkinan besar anda pernah menemui jenis fail seperti .rar dan .zip. Ini adalah arkib fail, ia mengandungi banyak fail di dalamnya, tetapi ia datang dalam fail tunggal yang sangat kemas ini yang dikenali sebagai arkib.

<b>Memampatkan fail dengan gzip</b>

gzip ialah program yang digunakan untuk memampatkan fail dalam Linux, ia berakhir dengan sambungan .gz.

Untuk memampatkan fail:
<pre>$ gzip mycoolfile</pre>

Untuk menyahmampat fail:
<pre>$ gunzip mycoolfile.gz</pre>

<b>Mencipta arkib dengan tar</b>
Malangnya, gzip tidak boleh menambah beberapa fail ke dalam satu arkib untuk kami. Nasib baik kita ada program tar yang melakukannya. Apabila anda mencipta arkib menggunakan tar, ia akan mempunyai sambungan .tar.

<pre>$ tar cvf mytarfile.tar mycoolfile1 mycoolfile 2</pre>

<ul>
<li>c - cipta</li>
<li>v - beritahu program untuk menjadi verbose dan biarkan kami melihat apa yang dilakukannya</li>
<li>f - nama fail fail tar mesti datang selepas pilihan ini, jika anda mencipta fail tar, anda perlu memikirkan nama</li>
</ul>

<b>Membongkar arkib dengan tar</b>

Untuk mengekstrak kandungan fail tar, gunakan:

<pre>$ tar xvf mytarfile.tar</pre>

<ul>
<li>x - ekstrak</li>
<li>v - beritahu program untuk menjadi verbose dan biarkan kami melihat apa yang dilakukannya</li>
<li>f - fail yang ingin anda ekstrak</li>
</ul>

<b>Memampatkan/menyahmampat arkib dengan tar dan gzip</b>

Banyak kali anda akan melihat fail tar yang telah dimampatkan seperti: mycompressedarchive.tar.gz, apa yang anda perlu lakukan ialah bekerja dari luar ke dalam, jadi mula-mula keluarkan pemampatan dengan gunzip dan kemudian anda boleh membongkar fail tar. Atau anda boleh menggunakan pilihan <b>z</b> dengan tar, yang hanya memberitahunya untuk menggunakan utiliti gzip atau gunzip.

Cipta fail tar yang dimampatkan:
<pre>$ tar czf myfile.tar.gz</pre>

Nyahmampat dan bongkar:
<pre>$ tar xzf file.tar</pre>

Jika anda memerlukan bantuan, ingat ini: e<b>X</b>tract all <b>Z</b>ee <b>F</b>iles!

tar ialah salah satu arahan yang sangat penting namun anda tidak pernah benar-benar mengingatinya, xkcd yang berkaitan: <a href="https://xkcd.com/1168/">https://xkcd.com/1168/</a>

<b>Utiliti Lain</b>

Sepanjang perjalanan anda menggunakan Linux, anda akan menemui jenis arkib dan pemampatan lain seperti: bzip2, compress, zip, unzip, dsb. Ia kurang biasa, tetapi perlu diingat bahawa utiliti yang berbeza akan memerlukan arahan yang berbeza.

## Latihan

Biasakan diri anda dengan dokumentasi tar dan lihat pilihan lain yang tersedia dalam halaman manual.

## Soalan Kuiz

Apakah bendera tar yang digunakan untuk mencipta arkib?

## Jawapan Kuiz

c