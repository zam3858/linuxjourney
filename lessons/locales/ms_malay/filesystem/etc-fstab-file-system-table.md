# /etc/fstab

## Kandungan Pelajaran

Apabila kita ingin melekapkan sistem fail secara automatik semasa permulaan, kita boleh menambahkannya ke fail yang dipanggil /etc/fstab (disebut "eff es tab" bukan "eff stab") singkatan untuk jadual sistem fail. Fail ini mengandungi senarai kekal sistem fail yang dilekapkan.

<pre>
pete@icebox:~$ cat /etc/fstab
UUID=130b882f-7d79-436d-a096-1e594c92bb76 /               ext4    relatime,errors=remount-ro 0       1
UUID=78d203a0-7c18-49bd-9e07-54f44cdb5726 /home           xfs     relatime        0       2
UUID=22c3d34b-467e-467c-b44d-f03803c2c526 none            swap    sw              0       0
</pre>

Setiap baris mewakili satu sistem fail, medannya ialah:

<ul>
<li>UUID - Pengecam peranti</li>
<li>Titik lekap - Direktori tempat sistem fail dilekapkan</li>
<li>Jenis sistem fail</li>
<li>Pilihan - pilihan lekap lain, lihat halaman manual untuk butiran lanjut</li>
<li>Buang - digunakan oleh utiliti buang untuk memutuskan bila hendak membuat sandaran, anda hanya perlu lalai kepada 0</li>
<li>Lulus - Digunakan oleh fsck untuk memutuskan susunan sistem fail yang perlu diperiksa, jika nilainya 0, ia tidak akan diperiksa</li>
</ul>

Untuk menambah entri, hanya ubah suai fail /etc/fstab secara terus menggunakan sintaks entri di atas. Berhati-hati semasa mengubah suai fail ini, anda berpotensi menjadikan hidup anda lebih sukar jika anda mengacaukannya.

## Latihan

Tambah pemacu USB yang telah kita kerjakan sebagai entri dalam /etc/fstab, apabila anda but semula anda masih akan melihatnya dilekapkan.

## Soalan Kuiz

Apakah fail yang digunakan untuk menentukan cara sistem fail harus dilekapkan?

## Jawapan Kuiz

/etc/fstab