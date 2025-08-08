# Jenis Sistem Fail

## Kandungan Pelajaran

Terdapat banyak pelaksanaan sistem fail yang berbeza. Sesetengahnya lebih pantas daripada yang lain, sesetengah menyokong storan kapasiti yang lebih besar dan yang lain hanya berfungsi pada storan kapasiti yang lebih kecil. Sistem fail yang berbeza mempunyai cara yang berbeza untuk menyusun data mereka dan kami akan membincangkan secara terperinci tentang jenis sistem fail yang ada. Oleh kerana terdapat begitu banyak pelaksanaan yang berbeza, aplikasi memerlukan cara untuk menangani operasi yang berbeza. Jadi ada sesuatu yang dipanggil lapisan abstraksi Sistem Fail Maya (VFS). Ia adalah lapisan antara aplikasi dan jenis sistem fail yang berbeza, jadi tidak kira apa sistem fail yang anda ada, aplikasi anda akan dapat berfungsi dengannya.

Anda boleh mempunyai banyak sistem fail pada cakera anda, bergantung pada cara ia dipetakan dan kami akan melaluinya dalam pelajaran yang akan datang.

<b>Penjurnalan</b>

Penjurnalan datang secara lalai pada kebanyakan jenis sistem fail, tetapi sekiranya tidak, anda harus tahu apa yang dilakukannya. Katakan anda sedang menyalin fail yang besar dan tiba-tiba anda kehilangan kuasa. Jika anda menggunakan sistem fail bukan jurnal, fail itu akan rosak dan sistem fail anda akan tidak konsisten dan kemudian apabila anda but semula, sistem anda akan melakukan pemeriksaan sistem fail untuk memastikan semuanya ok. Walau bagaimanapun, pembaikan boleh mengambil sedikit masa bergantung pada saiz sistem fail anda.

Sekarang jika anda menggunakan sistem berjurnal, sebelum mesin anda mula menyalin fail, ia akan menulis apa yang akan anda lakukan dalam fail log (jurnal). Sekarang apabila anda benar-benar menyalin fail, sebaik sahaja ia selesai, jurnal menandakan tugas itu sebagai selesai. Sistem fail sentiasa dalam keadaan konsisten kerana ini, jadi ia akan tahu di mana anda berhenti jika mesin anda tiba-tiba ditutup. Ini juga mengurangkan masa but kerana bukannya memeriksa keseluruhan sistem fail, ia hanya melihat jurnal anda.

<b>Jenis Sistem Fail Desktop Biasa</b>

<ul>
<li>ext4 - Ini ialah versi paling terkini bagi sistem fail Linux asli. Ia serasi dengan versi ext2 dan ext3 yang lebih lama. Ia menyokong volum cakera sehingga 1 eksabait dan saiz fail sehingga 16 terabait dan banyak lagi. Ia adalah pilihan standard untuk sistem fail Linux.</li>
<li>Btrfs - "Better or Butter FS" ia adalah sistem fail baharu untuk Linux yang disertakan dengan gambar petikan, sandaran tambahan, peningkatan prestasi dan banyak lagi. Ia tersedia secara meluas, tetapi belum begitu stabil dan serasi.</li>
<li>XFS - Sistem fail penjurnalan berprestasi tinggi, bagus untuk sistem dengan fail besar seperti pelayan media.</li>
<li>NTFS dan FAT - Sistem fail Windows</li>
<li>HFS+ - Sistem fail Macintosh</li>
</ul>

Semak sistem fail apa yang ada pada mesin anda:

<pre>
pete@icebox:~$ df -T
Filesystem     Type     1K-blocks    Used Available Use% Mounted on
/dev/sda1      ext4       6461592 2402708   3707604  40% /
udev           devtmpfs    501356       4    501352   1% /dev
tmpfs          tmpfs       102544    1068    101476   2% /run
/dev/sda6      xfs       13752320  460112  13292208   4% /home
</pre>

Perintah <b>df</b> melaporkan penggunaan ruang cakera sistem fail dan butiran lain tentang cakera anda, kami akan membincangkan lebih lanjut tentang alat ini kemudian.

## Latihan

Lakukan sedikit penyelidikan dalam talian tentang jenis sistem fail lain: ReiserFS, ZFS, JFS dan lain-lain yang boleh anda temui.

## Soalan Kuiz

Apakah jenis sistem fail Linux yang biasa?

## Jawapan Kuiz

ext4