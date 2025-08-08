# Menyusun Kod Sumber

## Kandungan Pelajaran

Selalunya anda akan menemui pakej yang tidak jelas yang hanya datang dalam bentuk kod sumber tulen. Anda perlu menggunakan beberapa arahan untuk menyusun dan memasang pakej kod sumber itu pada sistem anda.

Pertama sekali, anda perlu mempunyai perisian untuk memasang alat yang akan membolehkan anda menyusun kod sumber.

<pre>$ sudo apt install build-essential</pre>

Sebaik sahaja anda melakukannya, ekstrak kandungan fail pakej, kemungkinan besar fail .tar.gz.

<pre>$ tar -xzvf package.tar.gz</pre>

Sebelum anda melakukan apa-apa, lihat fail README atau INSTALL di dalam pakej. Kadang-kadang akan ada arahan pemasangan khusus.

Bergantung pada kaedah penyusunan yang digunakan oleh pembangun, anda perlu menggunakan arahan yang berbeza, seperti cmake atau sesuatu yang lain.

Walau bagaimanapun, yang paling biasa anda akan lihat ialah penyusunan make asas, jadi kita akan membincangkannya:

Di dalam kandungan pakej akan ada skrip konfigurasi, skrip ini memeriksa kebergantungan pada sistem anda dan jika anda kehilangan apa-apa, anda akan melihat ralat dan anda perlu membetulkan kebergantungan tersebut.

<pre>$ ./configure</pre>

<b>./</b> membolehkan anda melaksanakan skrip dalam direktori semasa.

<pre>$ make</pre>

Di dalam kandungan pakej, terdapat fail yang dipanggil Makefile yang mengandungi peraturan untuk membina perisian. Apabila anda menjalankan arahan make, ia melihat fail ini untuk membina perisian.

<pre>$ sudo make install</pre>

Perintah ini sebenarnya memasang pakej, ia akan menyalin fail yang betul ke lokasi yang betul pada komputer anda.

Jika anda ingin menyahpasang pakej, gunakan:

<pre>$ sudo make uninstall</pre>

Berhati-hati apabila menggunakan make install, anda mungkin tidak menyedari betapa banyak yang sebenarnya berlaku di latar belakang. Jika anda memutuskan untuk mengalih keluar pakej ini, anda mungkin tidak benar-benar mengalih keluar semuanya kerana anda tidak menyedari apa yang telah ditambahkan pada sistem anda. Sebaliknya lupakan semua tentang make install yang baru saya terangkan kepada anda dan gunakan arahan <b>checkinstall</b>. Perintah ini akan membuat fail .deb untuk anda yang boleh anda pasang dan nyahpasang dengan mudah.

<pre>$ sudo checkinstall</pre>

Perintah ini pada asasnya akan "make install" dan membina pakej .deb dan memasangnya. Ini memudahkan untuk mengalih keluar pakej kemudian.

## Latihan

Cari program kod sumber (dari tapak yang dipercayai) dan pasang dari sumber.

## Soalan Kuiz

Apakah yang perlu anda gunakan dan bukannya make install SENTIASA?

## Jawapan Kuiz

checkinstall
