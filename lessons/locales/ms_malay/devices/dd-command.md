# dd

## Kandungan Pelajaran

Alat dd sangat berguna untuk menukar dan menyalin data. Ia membaca input daripada fail atau strim data dan menulisnya ke fail atau strim data.

Pertimbangkan arahan berikut:

<pre>$ dd if=/home/pete/backup.img of=/dev/sdb bs=1024 </pre>

Perintah ini menyalin kandungan backup.img ke /dev/sdb. Ia akan menyalin data dalam blok 1024 bait sehingga tiada lagi data untuk disalin.

<ul>
<li>if=fail - Fail input, baca daripada fail dan bukannya input standard</li>
<li>of=fail - Fail output, tulis ke fail dan bukannya output standard</li>
<li>bs=bait - Saiz blok, ia membaca dan menulis bait data ini pada satu masa. Anda boleh menggunakan metrik saiz yang berbeza dengan menandakan saiz dengan k untuk kilobait, m untuk megabait, dsb, jadi 1024 bait ialah 1k</li>
<li>kiraan=nombor - Bilangan blok untuk disalin.</li>
</ul>

Anda akan melihat beberapa arahan dd yang menggunakan pilihan kiraan, biasanya dengan dd jika anda ingin menyalin fail yang bersaiz 1 megabait, anda biasanya ingin melihat fail itu sebagai 1 megabait apabila ia selesai disalin. Katakan anda menjalankan arahan berikut:

<pre>$ dd if=/home/pete/backup.img of=/dev/sdb bs=1M count=2</pre>

Fail backup.img kami ialah 10M, walau bagaimanapun, kami mengatakan dalam arahan ini untuk menyalin lebih 1M 2 kali, jadi hanya 2M yang disalin, meninggalkan data salinan kami tidak lengkap. Kiraan boleh berguna dalam banyak situasi, tetapi jika anda hanya menyalin data, anda boleh meninggalkan kiraan dan juga bs. Jika anda benar-benar ingin mengoptimumkan pemindahan data anda, maka anda perlu mula menggunakan pilihan tersebut.

dd sangat berkuasa, anda boleh menggunakannya untuk membuat sandaran apa sahaja, termasuk keseluruhan pemacu cakera, memulihkan imej cakera dan banyak lagi. Berhati-hati, alat yang berkuasa itu boleh datang dengan harga jika anda tidak pasti apa yang anda lakukan.

## Latihan

Gunakan arahan dd untuk membuat sandaran pemacu anda dan tetapkan output kepada fail .img.

## Soalan Kuiz

Apakah pilihan dd untuk saiz blok?

## Jawapan Kuiz

bs