# rsync

## Kandungan Pelajaran

Alat lain yang digunakan untuk menyalin data dari hos yang berbeza ialah rsync (singkatan untuk penyegerakan jauh). Rsync sangat serupa dengan scp, tetapi ia mempunyai perbezaan besar. Rsync menggunakan algoritma khas yang memeriksa terlebih dahulu jika sudah ada data yang anda salin dan hanya akan menyalin perbezaannya. Sebagai contoh, katakan anda sedang menyalin fail dan rangkaian anda terganggu, oleh itu salinan anda berhenti di tengah jalan. Daripada menyalin semula semua dari awal, rsync hanya akan menyalin bahagian yang tidak disalin.

Ia juga mengesahkan integriti fail yang anda salin dengan checksum. Pengoptimuman kecil ini membolehkan fleksibiliti pemindahan fail yang lebih besar dan menjadikan rsync sesuai untuk penyegerakan direktori dari jauh dan tempatan, sandaran data, pemindahan data yang besar dan banyak lagi.

Beberapa pilihan rsync yang biasa digunakan:

<ul>
<li>v - output verbose</li>
<li>r - rekursif ke dalam direktori</li>
<li>h - output yang boleh dibaca manusia</li>
<li>z - dimampatkan untuk pemindahan yang lebih mudah, bagus untuk sambungan yang perlahan</li>
</ul>

<b>Salin/segerakkan fail pada hos yang sama</b>

<pre>$ rsync -zvr /my/local/directory/one /my/local/directory/two</pre>

<b>Salin/segerakkan fail ke hos tempatan dari hos jauh</b>

<pre>$ rsync /local/directory username@remotehost.com:/remote/directory</pre>

<b>Salin/segerakkan fail ke hos jauh dari hos tempatan</b>

<pre>$ rsync username@remotehost.com:/remote/directory /local/directory</pre>

## Latihan

Gunakan rsync untuk menyegerakkan direktori ke direktori lain, pastikan tidak menimpa direktori penting!

## Soalan Kuiz

Apakah arahan yang berguna untuk sandaran data?

## Jawapan Kuiz

rsync