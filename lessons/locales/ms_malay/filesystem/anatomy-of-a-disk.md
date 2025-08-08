# Anatomi Cakera

## Kandungan Pelajaran

Cakera keras boleh dibahagikan kepada partition, pada asasnya membuat beberapa peranti blok. Ingat contoh seperti, /dev/sda1 dan /dev/sda2, /dev/sda ialah keseluruhan cakera, tetapi /dev/sda1 ialah partition pertama pada cakera itu. Partition amat berguna untuk mengasingkan data dan jika anda memerlukan sistem fail tertentu, anda boleh membuat partition dengan mudah dan bukannya menjadikan keseluruhan cakera satu jenis sistem fail.

<b>Jadual Partition</b>

Setiap cakera akan mempunyai jadual partition, jadual ini memberitahu sistem bagaimana cakera itu dipetakan. Jadual ini memberitahu anda di mana partition bermula dan berakhir, partition mana yang boleh dibut, sektor cakera mana yang diperuntukkan kepada partition mana, dsb. Terdapat dua skema jadual partition utama yang digunakan, Master Boot Record (MBR) dan GUID Partition Table (GPT).

<b>Partition</b>

Cakera terdiri daripada partition yang membantu kita menyusun data kita. Anda boleh mempunyai beberapa partition pada cakera dan ia tidak boleh bertindih antara satu sama lain. Jika terdapat ruang yang tidak diperuntukkan kepada partition, maka ia dikenali sebagai ruang bebas. Jenis partition bergantung pada jadual partition anda. Di dalam partition, anda boleh mempunyai sistem fail atau mendedikasikan partition untuk perkara lain seperti swap (kita akan membincangkannya tidak lama lagi).

<i>MBR</i>

<ul>
<li>Jadual partition tradisional, digunakan sebagai standard</li>
<li>Boleh mempunyai partition primer, lanjutan dan logik</li>
<li>MBR mempunyai had empat partition primer</li>
<li>Partition tambahan boleh dibuat dengan menjadikan partition primer sebagai partition lanjutan (hanya boleh ada satu partition lanjutan pada cakera). Kemudian di dalam partition lanjutan anda menambah partition logik. Partition logik digunakan sama seperti partition lain. Saya tahu ia kedengaran pelik.</li>
<li>Menyokong cakera sehingga 2 terabait</li>
</ul>

<i>GPT</i>

<ul>
<li>Jadual Partition GUID (GPT) menjadi standard baharu untuk pemetakan cakera</li>
<li>Hanya mempunyai satu jenis partition dan anda boleh membuat banyak daripadanya</li>
<li>Setiap partition mempunyai ID unik global (GUID)</li>
<li>Digunakan kebanyakannya bersama dengan but berasaskan UEFI (kita akan membincangkan butiran dalam kursus lain)</li>
</ul>

<b>Struktur Sistem Fail</b>

Kita tahu dari pelajaran kita sebelum ini bahawa sistem fail ialah koleksi fail dan direktori yang teratur. Dalam bentuk yang paling mudah, ia terdiri daripada pangkalan data untuk mengurus fail dan fail sebenar itu sendiri, namun kita akan pergi ke butiran yang lebih terperinci.

<ul>
<li>Blok but - Ini terletak di beberapa sektor pertama sistem fail, dan ia tidak begitu digunakan oleh sistem fail. Sebaliknya, ia mengandungi maklumat yang digunakan untuk membut sistem pengendalian. Hanya satu blok but diperlukan oleh sistem pengendalian. Jika anda mempunyai beberapa partition, ia akan mempunyai blok but, tetapi kebanyakannya tidak digunakan.</li>
<li>Blok super - Ini ialah blok tunggal yang datang selepas blok but, dan ia mengandungi maklumat tentang sistem fail, seperti saiz jadual inod, saiz blok logik dan saiz sistem fail.</li>
<li>Jadual inod - Anggap ini sebagai pangkalan data yang mengurus fail kita (kita ada pelajaran keseluruhan tentang inod, jadi jangan risau). Setiap fail atau direktori mempunyai entri unik dalam jadual inod dan ia mempunyai pelbagai maklumat tentang fail itu.</li>
<li>Blok data - Ini ialah data sebenar untuk fail dan direktori.</li>
</ul>

Mari kita lihat jadual partition yang berbeza. Di bawah ialah contoh partition menggunakan jadual partition MBR (msdos). Anda boleh melihat partition primer, lanjutan dan logik pada mesin.

<pre>
pete@icebox:~$ sudo parted -l
Model: Seagate (scsi)
Disk /dev/sda: 21.5GB
Sector size (logical/physical): 512B/512B
Partition Table: msdos

Number Start End Size Type File system Flags
 1 1049kB 6860MB 6859MB primary ext4 boot
 2 6861MB 21.5GB 14.6GB extended
 5 6861MB 7380MB 519MB logical linux-swap(v1)
 6 7381MB 21.5GB 14.1GB logical xfs
</pre>


Contoh ini ialah GPT, hanya menggunakan ID unik untuk partition.

<pre>
Model: Thumb Drive (scsi)
Disk /dev/sdb: 4041MB
Sector size (logical/physical): 512B/512B
Partition Table: gpt

Number Start End Size File system Name Flags
 1 17.4kB 1000MB 1000MB first
 2 1000MB 4040MB 3040MB second
</pre>

## Latihan

Jalankan <b>parted -l</b> pada mesin anda dan nilaikan hasilnya.

## Soalan Kuiz

Apakah jenis partition yang digunakan untuk mencipta lebih daripada 4 partition dalam skema partition MBR?

## Jawapan Kuiz

lanjutan
