# Mengawal Terminal

## Kandungan Pelajaran

Kami membincangkan bagaimana terdapat medan TTY dalam output ps. TTY ialah terminal yang melaksanakan arahan.

Terdapat dua jenis terminal, <b>peranti terminal</b> biasa dan <b>peranti pseudoterminal</b>. Peranti terminal biasa ialah peranti terminal asli yang boleh anda taip dan hantar output ke sistem anda, ini kedengaran seperti aplikasi terminal yang telah anda lancarkan untuk sampai ke shell anda, tetapi bukan.

Kami akan beralih supaya anda dapat melihat tindakan ini, teruskan dan taip Ctrl-Alt-F1 untuk masuk ke TTY1 (konsol maya pertama), anda akan perasan bagaimana anda tidak mempunyai apa-apa kecuali terminal, tiada grafik, dsb. Ini dianggap sebagai peranti terminal biasa, anda boleh keluar dari ini dengan Ctrl-Alt-F7.

Pseudoterminal ialah apa yang anda biasa gunakan, ia meniru terminal dengan tetingkap terminal shell dan ditandakan dengan PTS . Jika anda melihat ps sekali lagi, anda akan melihat proses shell anda di bawah pts/*.

Ok, sekarang kembali ke terminal kawalan, proses biasanya terikat pada terminal kawalan. Sebagai contoh, jika anda menjalankan program pada tetingkap shell anda seperti find dan anda menutup tetingkap, proses anda juga akan turut serta.

Terdapat proses seperti proses daemon, yang merupakan proses khas yang pada asasnya memastikan sistem berjalan. Ia selalunya bermula semasa but sistem dan biasanya ditamatkan apabila sistem ditutup. Ia berjalan di latar belakang dan kerana kami tidak mahu proses khas ini ditamatkan, ia tidak terikat pada terminal kawalan. Dalam output ps, TTY disenaraikan sebagai <b>?</b> yang bermaksud ia tidak mempunyai terminal kawalan.

## Latihan

Lihat output ps anda dan senaraikan semua nilai TTY yang unik.

## Soalan Kuiz

Apakah nilai yang diberikan untuk proses yang tidak mempunyai terminal kawalan?

## Jawapan Kuiz

?