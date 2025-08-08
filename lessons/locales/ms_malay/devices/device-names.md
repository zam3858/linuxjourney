# Nama Peranti

## Kandungan Pelajaran

Berikut ialah nama peranti paling biasa yang akan anda temui:

<b>Peranti SCSI</b>

Jika anda mempunyai sebarang jenis storan massa pada mesin anda, kemungkinan besar ia menggunakan protokol SCSI (disebut "scuzzy"). SCSI adalah singkatan untuk Antara Muka Sistem Komputer Kecil, ia adalah protokol yang digunakan untuk membenarkan komunikasi antara cakera, pencetak, pengimbas dan peranti lain ke sistem anda. Anda mungkin pernah mendengar tentang peranti SCSI yang sebenarnya tidak digunakan dalam sistem moden, walau bagaimanapun sistem Linux kami memadankan cakera SCSI dengan pemacu cakera keras dalam /dev. Ia diwakili oleh awalan sd (cakera SCSI):

Fail peranti SCSI biasa:

<ul>
<li>/dev/sda - Cakera keras pertama</li>
<li>/dev/sdb - Cakera keras kedua</li>
<li>/dev/sda3 - Partition ketiga pada cakera keras pertama</li>
</ul>

<b>Peranti Pseudo</b>

Seperti yang kita bincangkan sebelum ini, peranti pseudo tidak benar-benar disambungkan secara fizikal ke sistem anda, peranti pseudo yang paling biasa ialah peranti aksara:

<ul>
<li>/dev/zero - menerima dan membuang semua input, menghasilkan strim berterusan bait NULL (nilai sifar)</li>
<li>/dev/null - menerima dan membuang semua input, tidak menghasilkan output</li>
<li>/dev/random - menghasilkan nombor rawak</li>
</ul>

<b>Peranti PATA</b>

Kadang-kadang dalam sistem yang lebih lama anda mungkin melihat pemacu keras dirujuk dengan awalan hd:

<ul>
<li>/dev/hda - Cakera keras pertama</li>
<li>/dev/hdd2 - Partition kedua pada cakera keras ke-4</li>
</ul>

## Latihan

Tulis kepada peranti pseudo dan lihat apa yang berlaku, berhati-hati untuk tidak menulis cakera anda kepada peranti tersebut!

## Soalan Kuiz

Apakah nama peranti yang biasa untuk partition pertama pada cakera SCSI kedua?

## Jawapan Kuiz

sdb1