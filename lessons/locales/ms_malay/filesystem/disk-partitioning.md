# Pemetakan Cakera

## Kandungan Pelajaran

Mari kita lakukan beberapa perkara praktikal dengan sistem fail dengan melalui proses pada pemacu USB. Jika anda tidak mempunyainya, jangan risau, anda masih boleh mengikuti beberapa pelajaran seterusnya.

Mula-mula kita perlu memetakan cakera kita. Terdapat banyak alat yang tersedia untuk melakukan ini:

<ul>
<li>fdisk - alat pemetakan baris perintah asas, ia tidak menyokong GPT</li>
<li>parted - ini ialah alat baris perintah yang menyokong pemetakan MBR dan GPT</li>
<li>gparted - ini ialah versi GUI parted</li>
<li>gdisk - fdisk, tetapi ia tidak menyokong MBR sahaja GPT</li>
</ul>

Mari kita gunakan parted untuk melakukan pemetakan kita. Katakan saya menyambungkan peranti USB dan kita melihat nama peranti ialah /dev/sdb2.

<b>Lancarkan parted</b>

<pre>$ sudo parted</pre>

Anda akan dimasukkan ke dalam alat parted, di sini anda boleh menjalankan arahan untuk memetakan peranti anda.

<b>Pilih peranti</b>

<pre>pilih /dev/sdb2</pre>

Untuk memilih peranti yang akan anda gunakan, pilihnya dengan nama perantinya.

<b>Lihat jadual partition semasa</b>

<pre>
(parted) print
Model: Seagate (scsi)
Disk /dev/sda: 21.5GB
Sector size (logical/physical): 512B/512B
Partition Table: msdos

Number  Start   End     Size    Type      File system     Flags
 1      1049kB  6860MB  6859MB  primary   ext4            boot
 2      6861MB  21.5GB  14.6GB  extended
 5      6861MB  7380MB  519MB   logical   linux-swap(v1)
 6      7381MB  21.5GB  14.1GB  logical   xfs
</pre>

Di sini anda akan melihat partition yang tersedia pada peranti. Titik <b>mula</b> dan <b>akhir</b> ialah tempat partition mengambil ruang pada cakera keras, anda perlu mencari lokasi mula dan akhir yang baik untuk partition anda.

<b>Petakan peranti</b>

<pre>mkpart primary 123 4567</pre>

Sekarang pilih sahaja titik mula dan akhir dan buat partition, anda perlu menentukan jenis partition bergantung pada jadual yang anda gunakan.

<b>Ubah saiz partition</b>

Anda juga boleh mengubah saiz partition jika anda tidak mempunyai ruang.

<pre>ubah saiz 2 1245 3456</pre>

Pilih nombor partition dan kemudian titik mula dan akhir tempat anda mahu mengubah saiznya.

Parted ialah alat yang sangat berkuasa dan anda harus berhati-hati semasa memetakan cakera anda.

## Latihan

Petakan pemacu USB dengan separuh pemacu sebagai ext4 dan separuh lagi sebagai ruang kosong.

## Soalan Kuiz

Apakah arahan parted untuk membuat partition?

## Jawapan Kuiz

mkpart