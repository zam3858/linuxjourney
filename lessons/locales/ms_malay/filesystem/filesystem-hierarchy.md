# Hierarki Sistem Fail

## Kandungan Pelajaran

Pada ketika ini, anda mungkin sudah biasa dengan struktur direktori sistem anda, jika tidak, anda akan mengetahuinya tidak lama lagi. Sistem fail boleh berbeza-beza dari segi strukturnya, tetapi kebanyakannya harus mematuhi Piawaian Hierarki Sistem Fail.

Teruskan dan lakukan <b>ls -l /</b> untuk melihat direktori yang disenaraikan di bawah direktori akar, direktori anda mungkin kelihatan berbeza daripada saya, tetapi kebanyakannya direktori harus kelihatan seperti berikut:

<ul>
<li>/ - Direktori akar bagi keseluruhan hierarki sistem fail, semuanya terletak di bawah direktori ini.</li>
<li>/bin - Program sedia untuk dijalankan yang penting (binari), termasuk arahan paling asas seperti ls dan cp.</li>
<li>/boot - Mengandungi fail pemuat but kernel.</li>
<li>/dev - Fail peranti.</li>
<li>/etc - Direktori konfigurasi sistem teras, hanya perlu menyimpan fail konfigurasi dan bukan sebarang binari.</li>
<li>/home - Direktori peribadi untuk pengguna, menyimpan dokumen, fail, tetapan anda, dsb.</li>
<li>/lib - Menyimpan fail perpustakaan yang boleh digunakan oleh binari.</li>
<li>/media - Digunakan sebagai titik lampiran untuk media boleh tanggal seperti pemacu USB.</li>
<li>/mnt - Sistem fail yang dilekapkan buat sementara waktu.</li>
<li>/opt - Pakej perisian aplikasi pilihan.</li>
<li>/proc - Maklumat tentang proses yang sedang berjalan.</li>
<li>/root - Direktori rumah pengguna akar.</li>
<li>/run - Maklumat tentang sistem yang berjalan sejak but terakhir.</li>
<li>/sbin - Mengandungi binari sistem penting, biasanya hanya boleh dijalankan oleh akar.</li>
<li>/srv - Data khusus tapak yang dilayan oleh sistem.</li>
<li>/tmp - Storan untuk fail sementara</li>
<li>/usr - Ini malangnya dinamakan, selalunya ia tidak mengandungi fail pengguna dalam erti kata folder rumah. Ini bertujuan untuk perisian dan utiliti yang dipasang pengguna, namun itu tidak bermakna anda tidak boleh menambah direktori peribadi di sana. Di dalam direktori ini terdapat sub-direktori untuk /usr/bin, /usr/local, dsb.</li>
<li>/var - Direktori pembolehubah, ia digunakan untuk pengelogan sistem, penjejakan pengguna, cache, dsb. Pada asasnya apa sahaja yang tertakluk kepada perubahan sepanjang masa.</li>
</ul>

## Latihan

Lihat di dalam direktori /usr anda, apakah jenis maklumat yang terdapat di sana?

## Soalan Kuiz

Direktori manakah yang digunakan untuk menyimpan log?

## Jawapan Kuiz

/var