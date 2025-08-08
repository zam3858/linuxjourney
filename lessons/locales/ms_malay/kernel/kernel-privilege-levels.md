# Tahap Keistimewaan

## Kandungan Pelajaran

Beberapa pelajaran seterusnya menjadi agak teori, jadi jika anda mencari beberapa perkara praktikal, anda boleh melangkau ke hadapan dan kembali kemudian.

Mengapakah kita mempunyai lapisan abstraksi yang berbeza untuk ruang pengguna dan kernel? Mengapakah anda tidak boleh menggabungkan kedua-dua kuasa menjadi satu lapisan? Terdapat sebab yang sangat baik mengapa kedua-dua lapisan ini wujud secara berasingan. Kedua-duanya beroperasi dalam mod yang berbeza, kernel beroperasi dalam mod kernel dan ruang pengguna beroperasi dalam mod pengguna.

Dalam mod kernel, kernel mempunyai akses lengkap kepada perkakasan, ia mengawal segala-galanya. Dalam mod ruang pengguna, terdapat sejumlah kecil memori dan CPU yang selamat yang anda dibenarkan untuk akses. Pada asasnya, apabila kita ingin melakukan apa sahaja yang melibatkan perkakasan, membaca data dari cakera kita, menulis data ke cakera kita, mengawal rangkaian kita, dsb, semuanya dilakukan dalam mod kernel. Mengapakah ini perlu? Bayangkan jika mesin anda dijangkiti perisian intip, anda tidak mahu ia dapat mempunyai akses terus ke perkakasan sistem anda. Ia boleh mengakses semua data anda, kamera web anda, dsb. dan itu tidak baik.

Mod yang berbeza ini dipanggil tahap keistimewaan (dinamakan dengan tepat untuk tahap keistimewaan yang anda dapat) dan sering digambarkan sebagai cincin perlindungan. Untuk menjadikan gambaran ini lebih mudah untuk dilukis, katakan anda mengetahui bahawa Britney Spears berada di bandar di kelab tempatan anda, dia dilindungi oleh peminatnya, kemudian pengawal peribadinya, kemudian penjaga pintu di luar kelab. Anda ingin mendapatkan autografnya (kerana mengapa tidak?), tetapi anda tidak dapat menemuinya kerana dia sangat dilindungi. Cincin berfungsi dengan cara yang sama, cincin paling dalam sepadan dengan tahap keistimewaan tertinggi. Terdapat dua tahap atau mod utama dalam seni bina komputer x86. Cincin #3 ialah keistimewaan yang dijalankan oleh aplikasi mod pengguna, Cincin #0 ialah keistimewaan yang dijalankan oleh kernel. Cincin #0 boleh melaksanakan sebarang arahan sistem dan diberi kepercayaan penuh. Jadi sekarang kita tahu bagaimana tahap keistimewaan itu berfungsi, bagaimana kita boleh menulis apa sahaja pada perkakasan kita? Bukankah kita akan sentiasa berada dalam mod yang berbeza daripada kernel?

Jawabannya adalah dengan panggilan sistem, panggilan sistem membolehkan kita melaksanakan arahan istimewa dalam mod kernel dan kemudian beralih kembali ke mod pengguna.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Apakah nombor cincin yang mempunyai keistimewaan tertinggi?

## Jawapan Kuiz

0
