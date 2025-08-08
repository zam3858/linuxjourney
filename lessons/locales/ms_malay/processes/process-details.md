# Butiran Proses

## Kandungan Pelajaran

Sebelum kita membincangkan aplikasi proses yang lebih praktikal, kita perlu terlebih dahulu memahami apa itu dan bagaimana ia berfungsi. Bahagian ini boleh menjadi mengelirukan kerana kita menyelami selok-beloknya, jadi jangan ragu untuk kembali ke pelajaran ini jika anda tidak mahu belajar mengenainya sekarang.

Proses seperti yang kita katakan sebelum ini ialah program yang sedang berjalan pada sistem, lebih tepat lagi ia adalah sistem yang memperuntukkan memori, CPU, I/O untuk menjalankan program. Proses ialah contoh program yang sedang berjalan, teruskan dan buka 3 tetingkap terminal, dalam dua tetingkap, jalankan arahan <b>cat</b> tanpa melepasi sebarang pilihan (proses cat akan tetap terbuka sebagai proses kerana ia menjangkakan stdin). Sekarang dalam tetingkap ketiga jalankan: <b>ps aux | grep cat</b>. Anda akan melihat bahawa terdapat dua proses untuk cat, walaupun ia memanggil program yang sama.

Kernel bertanggungjawab ke atas proses, apabila kita menjalankan program, kernel memuatkan kod program dalam memori, menentukan dan memperuntukkan sumber dan kemudian menjejaki setiap proses, ia tahu:

<ul>
<li>Status proses</li>
<li>Sumber yang digunakan dan diterima oleh proses</li>
<li>Pemilik proses</li>
<li>Pengendalian isyarat (lebih lanjut mengenai itu kemudian)</li>
<li>Dan pada asasnya segala-galanya</li>
</ul>

Semua proses cuba merasai pai sumber yang manis itu, tugas kernel adalah untuk memastikan proses mendapat jumlah sumber yang betul bergantung pada permintaan proses. Apabila proses berakhir, sumber yang digunakannya kini dibebaskan untuk proses lain.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Apakah yang mengurus dan mengawal proses?

## Jawapan Kuiz

kernel