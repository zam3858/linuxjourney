# Lokasi Kernel

## Kandungan Pelajaran

Apa yang berlaku apabila anda memasang kernel baharu? Sebenarnya ia menambah beberapa fail pada sistem anda, fail ini biasanya ditambahkan pada direktori /boot.

Anda akan melihat beberapa fail untuk versi kernel yang berbeza:

<ul>
<li>vmlinuz - ini ialah kernel linux sebenar</li>
<li>initrd - seperti yang telah kita bincangkan sebelum ini, initrd digunakan sebagai sistem fail sementara, digunakan sebelum memuatkan kernel</li>
<li>System.map - jadual carian simbolik</li>
<li>config - tetapan konfigurasi kernel, jika anda menyusun kernel anda sendiri, anda boleh menetapkan modul mana yang boleh dimuatkan</li>
</ul>

Jika direktori /boot anda kehabisan ruang, anda sentiasa boleh memadam versi lama fail ini atau hanya menggunakan pengurus pakej, tetapi berhati-hati semasa melakukan penyelenggaraan dalam direktori ini dan jangan padam kernel yang sedang anda gunakan secara tidak sengaja.

## Latihan

Pergi ke direktori but anda dan lihat fail apa yang ada di sana.

## Soalan Kuiz

Apakah nama imej kernel dalam /boot?

## Jawapan Kuiz

vmlinuz