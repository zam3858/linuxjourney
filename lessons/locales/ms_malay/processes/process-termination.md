# Penamatan Proses

## Kandungan Pelajaran

Sekarang kita tahu apa yang berlaku apabila proses dicipta, apa yang berlaku apabila kita tidak memerlukannya lagi? Berhati-hatilah, kadang-kadang Linux boleh menjadi sedikit gelap...

Proses boleh keluar menggunakan panggilan sistem _exit, ini akan membebaskan sumber yang digunakan oleh proses itu untuk peruntukan semula. Jadi apabila proses sedia untuk ditamatkan, ia memberitahu kernel mengapa ia ditamatkan dengan sesuatu yang dipanggil status penamatan. Paling biasa status 0 bermakna proses itu berjaya. Walau bagaimanapun, itu tidak cukup untuk menamatkan proses sepenuhnya. Proses induk perlu mengakui penamatan proses anak dengan menggunakan panggilan sistem tunggu dan apa yang dilakukannya ialah ia memeriksa status penamatan proses anak. Saya tahu ia mengerikan untuk difikirkan, tetapi panggilan tunggu adalah satu keperluan, lagipun ibu bapa mana yang tidak mahu tahu bagaimana anak mereka meninggal dunia?

Terdapat cara lain untuk menamatkan proses dan itu melibatkan penggunaan isyarat, yang akan kita bincangkan tidak lama lagi.

<b>Proses Yatim Piatu</b>

Apabila proses induk mati sebelum proses anak, kernel tahu bahawa ia tidak akan mendapat panggilan tunggu, jadi sebaliknya ia menjadikan proses ini "yatim piatu" dan meletakkannya di bawah jagaan init (ingat ibu kepada semua proses). Init akhirnya akan melakukan panggilan sistem tunggu untuk anak yatim ini supaya mereka boleh mati.

<b>Proses Zombi</b>

Apa yang berlaku apabila anak ditamatkan dan proses induk belum memanggil tunggu lagi? Kita masih mahu dapat melihat bagaimana proses anak ditamatkan, jadi walaupun proses anak selesai, kernel menukar proses anak menjadi proses zombi. Sumber yang digunakan oleh proses anak masih dibebaskan untuk proses lain, walau bagaimanapun masih terdapat entri dalam jadual proses untuk zombi ini. Proses zombi juga tidak boleh dibunuh, kerana ia secara teknikalnya "mati", jadi anda tidak boleh menggunakan isyarat untuk membunuhnya. Akhirnya jika proses induk memanggil panggilan sistem tunggu, zombi akan hilang, ini dikenali sebagai "menuai". Jika induk tidak melakukan panggilan tunggu, init akan mengambil alih zombi dan secara automatik melakukan tunggu dan mengalih keluar zombi. Ia boleh menjadi perkara yang buruk untuk mempunyai terlalu banyak proses zombi, kerana ia mengambil ruang pada jadual proses, jika ia penuh ia akan menghalang proses lain daripada berjalan.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Apakah status penamatan yang paling biasa untuk proses yang berjaya?

## Jawapan Kuiz

0