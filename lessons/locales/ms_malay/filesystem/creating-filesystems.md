# Mencipta Sistem Fail

## Kandungan Pelajaran

Sekarang anda telah benar-benar memetakan cakera, mari kita cipta sistem fail!

<pre>$ sudo mkfs -t ext4 /dev/sdb2</pre>

Semudah itu! Alat <b>mkfs</b> (make filesystem) membolehkan kita menentukan jenis sistem fail yang kita mahu dan di mana kita mahukannya. Anda hanya perlu mencipta sistem fail pada cakera yang baru dipetakan atau jika anda memetakan semula yang lama. Anda kemungkinan besar akan meninggalkan sistem fail anda dalam keadaan rosak jika anda cuba mencipta satu di atas yang sedia ada.

## Latihan

Buat sistem fail ext4 pada pemacu USB.

## Soalan Kuiz

Apakah arahan yang digunakan untuk mencipta sistem fail?

## Jawapan Kuiz

mkfs