# Pemasangan Kernel

## Kandungan Pelajaran

Ok, sekarang kita telah mengetepikan semua perkara yang membosankan itu, mari kita bercakap tentang pemasangan dan pengubahsuaian kernel. Anda boleh memasang beberapa kernel pada sistem anda, ingat dalam pelajaran kita tentang proses but? Dalam menu GRUB kami, kami boleh memilih kernel mana untuk but.

Untuk melihat versi kernel yang anda ada pada sistem anda, gunakan arahan berikut:

<pre>$ uname -r
3.19.0-43-generic</pre>

Perintah uname mencetak maklumat sistem, perintah -r akan mencetak semua versi keluaran kernel.

Anda boleh memasang kernel Linux dengan cara yang berbeza, anda boleh memuat turun pakej sumber dan menyusun dari sumber atau anda boleh memasangnya menggunakan alat pengurusan pakej.

<pre>$ sudo apt install linux-generic-lts-vivid</pre>

dan kemudian but semula ke dalam kernel yang anda pasang. Mudah kan? Agak, anda juga perlu memasang pakej linux lain seperti linux-headers, linux-image-generic, dsb). Anda juga boleh menentukan nombor versi, jadi arahan di atas boleh kelihatan seperti, <b>sudo apt install 3.19.0-43-generic</b>

Sebagai alternatif, jika anda hanya mahukan versi kernel yang dikemas kini, gunakan sahaja dist-upgrade, ia melakukan peningkatan pada semua pakej pada sistem anda:

<pre>$ sudo apt dist-upgrade</pre>

Terdapat banyak versi kernel yang berbeza, sesetengahnya digunakan sebagai LTS (sokongan jangka panjang), sesetengahnya adalah yang terkini dan terhebat, keserasian mungkin sangat berbeza antara versi kernel jadi anda mungkin ingin mencuba kernel yang berbeza.

## Latihan

<ol>
<li>Ketahui versi kernel yang anda ada.</li>
<li>Selidik versi kernel yang berbeza yang tersedia</li>
</ol>

## Soalan Kuiz

Bagaimanakah anda melihat versi kernel sistem anda?

## Jawapan Kuiz

uname -r
