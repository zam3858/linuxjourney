# Kebenaran Fail

## Kandungan Pelajaran

Seperti yang telah kita pelajari sebelum ini, fail mempunyai kebenaran atau mod fail yang berbeza. Mari lihat contoh:

<pre>$ ls -l Desktop/
drwxr-xr-x 2 pete penguins 4096 Dec 1 11:45 .
</pre>

Terdapat empat bahagian untuk kebenaran fail. Bahagian pertama ialah jenis fail, yang ditandakan oleh aksara pertama dalam kebenaran, dalam kes kita kerana kita melihat direktori ia menunjukkan <b>d</b> untuk jenis fail. Paling biasa anda akan melihat <b>-</b> untuk fail biasa.

Tiga bahagian seterusnya mod fail adalah kebenaran sebenar. Kebenaran dikumpulkan kepada 3 bit setiap satu. 3 bit pertama adalah kebenaran pengguna, kemudian kebenaran kumpulan dan kemudian kebenaran lain. Saya telah menambah paip untuk memudahkan pembezaan.

<pre>d | rwx | r-x | r-x </pre>

Setiap aksara mewakili kebenaran yang berbeza:
<ul>
<li>r: boleh dibaca</li>
<li>w: boleh ditulis</li>
<li>x: boleh dilaksanakan (pada asasnya program yang boleh dilaksanakan)</li>
<li>-: kosong</li>
</ul>

Jadi dalam contoh di atas, kita lihat bahawa pengguna pete mempunyai kebenaran baca, tulis dan laksana pada fail tersebut. Kumpulan penguins mempunyai kebenaran baca dan laksana. Dan akhirnya, pengguna lain (semua orang lain) mempunyai kebenaran baca dan laksana.

## Latihan

Gunakan perintah ls -l pada beberapa fail dan sebutkan kebenaran, pengguna dan kumpulan mereka.

## Soalan Kuiz

Bit kebenaran apakah yang digunakan untuk boleh dilaksanakan?

## Jawapan Kuiz

x