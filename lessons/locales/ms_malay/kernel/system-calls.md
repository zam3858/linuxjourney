# Panggilan Sistem

## Kandungan Pelajaran

Ingat Britney dalam pelajaran sebelumnya? Katakan kita ingin menemuinya dan minum bersama, bagaimana kita boleh sampai dari berdiri di luar dalam kerumunan orang ramai ke dalam lingkaran terdalamnya? Kita akan menggunakan panggilan sistem. Panggilan sistem adalah seperti pas VIP yang membawa anda ke pintu sisi rahsia yang menuju terus ke Britney.

Panggilan sistem (syscall) menyediakan proses ruang pengguna cara untuk meminta kernel melakukan sesuatu untuk kami. Kernel menyediakan perkhidmatan tertentu melalui API panggilan sistem. Perkhidmatan ini membolehkan kami membaca atau menulis ke fail, mengubah suai penggunaan memori, mengubah suai rangkaian kami, dsb. Jumlah perkhidmatan adalah tetap, jadi anda tidak boleh menambah panggilan sistem sewenang-wenangnya, sistem anda sudah mempunyai jadual panggilan sistem yang wujud dan setiap panggilan sistem mempunyai ID yang unik.

Saya tidak akan membincangkan secara spesifik panggilan sistem, kerana itu memerlukan anda mengetahui sedikit tentang C, tetapi asasnya ialah apabila anda memanggil program seperti ls, kod di dalam program ini mengandungi pembungkus panggilan sistem (jadi bukan panggilan sistem sebenar lagi). Di dalam pembungkus ini ia memanggil panggilan sistem yang akan melaksanakan perangkap, perangkap ini kemudiannya ditangkap oleh pengendali panggilan sistem dan kemudian merujuk panggilan sistem dalam jadual panggilan sistem. Katakan kita cuba memanggil panggilan sistem stat(), ia dikenal pasti dengan ID syscall dan tujuan panggilan sistem stat() adalah untuk menanyakan status fail. Sekarang ingat, anda menjalankan program ls dalam mod bukan keistimewaan. Jadi sekarang ia melihat anda cuba membuat syscall, ia kemudian menukar anda ke mod kernel, di sana ia melakukan banyak perkara tetapi yang paling penting ia mencari nombor syscall anda, menemuinya dalam jadual berdasarkan ID syscall dan kemudian melaksanakan fungsi yang anda mahu jalankan. Sebaik sahaja ia selesai, ia akan kembali ke mod pengguna dan proses anda akan menerima status pulangan jika ia berjaya atau jika ia mempunyai ralat. Cara kerja dalaman syscall menjadi sangat terperinci, saya akan mengesyorkan mencari maklumat dalam talian jika anda ingin mengetahui lebih lanjut.

Anda sebenarnya boleh melihat panggilan sistem yang dibuat oleh proses dengan arahan strace. Arahan strace berguna untuk menyahpepijat bagaimana program dilaksanakan.

<pre>$ strace ls</pre>

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Apakah yang digunakan untuk beralih dari mod pengguna ke mod kernel?

## Jawapan Kuiz

panggilan sistem
