# Subnet

## Kandungan Pelajaran

Bagaimanakah saya boleh tahu jika saya berada pada rangkaian yang sama dengan Patty? Kita boleh lihat sahaja pada subnet singkatan untuk subnetwork. Subnet ialah sekumpulan hos dengan alamat IP yang serupa dalam cara tertentu. Hos ini biasanya berada di lokasi yang berdekatan antara satu sama lain dan anda boleh menghantar data ke dan dari hos pada subnet yang sama dengan mudah. Fikirkan ia seperti menghantar mel dalam poskod yang sama, ia lebih mudah daripada menghantar mel ke negeri yang berbeza.

Sebagai contoh, semua hos dengan alamat IP yang bermula dengan 123.45.67 akan berada pada subnet yang sama. Hos saya mempunyai IP 123.45.67.8 dan Patty mempunyai IP 123.45.67.9. Nombor biasa ialah awalan rangkaian saya dan 8 dan 9 ialah hos kami, oleh itu rangkaian saya sama dengan Patty. Subnet dibahagikan kepada awalan rangkaian, seperti 123.45.67.0 dan topeng subnet.

<b>Topeng Subnet</b>

Topeng subnet menentukan bahagian mana alamat IP anda ialah bahagian rangkaian dan bahagian mana ialah bahagian hos.

Topeng subnet biasa boleh kelihatan seperti ini:

<pre>255.255.255.0</pre>

Bahagian 255 sebenarnya adalah topeng kami. Untuk menjadikan ini lebih mudah difahami, ingat bagaimana kita merujuk setiap oktet sebagai 8 bit? Dalam sains komputer, bit ditandakan dengan 0 atau 1 dalam bentuk binari. Apabila nombor binari digunakan, 1 bermaksud hidup dan 0 bermaksud mati. Jadi apakah persamaan 8 0 atau 1?

Masukkan ke dalam Google "kalkulator binari ke perpuluhan" dan tukar 11111111 ke dalam bentuk perpuluhan. Apa yang anda dapat? 255! Jadi oktet berjulat dari 0 hingga 255. Jadi jika kita mempunyai topeng subnet 255.255.255.0, dan alamat IP 192.168.1.0, berapa banyak hos pada subnet itu? Kita akan mengetahui jawapannya dalam pelajaran matematik subnet kita.

Juga apabila kita bercakap tentang subnet kita, kita biasanya menandakannya dengan awalan rangkaian diikuti dengan topeng subnet:

<pre>123.234.0.0/255.255.0.0</pre>

<b>Mengapa?</b>

Mengapakah kita membuat subnet? Subnetting digunakan untuk mensegmenkan rangkaian dan mengawal aliran trafik dalam rangkaian itu. Jadi hos pada satu subnet tidak boleh berinteraksi dengan hos lain pada subnet yang berbeza.

Tetapi tunggu sebentar, bagaimana jika saya ingin menyambung ke hos lain seperti yahoo.com? Kemudian anda perlu menyambungkan subnet bersama-sama. Untuk menyambungkan subnet anda hanya perlu mencari hos yang disambungkan ke lebih daripada satu subnet. Sebagai contoh, jika hos saya di 192.168.1.129 disambungkan ke rangkaian tempatan 192.168.1.129/24 ia boleh mencapai mana-mana hos pada rangkaian itu. Untuk mencapai hos di seluruh Internet, ia perlu berkomunikasi melalui penghala. Secara tradisinya, pada kebanyakan rangkaian dengan topeng subnet 255.255.255.0, penghala biasanya berada di alamat 1 subnet, jadi 192.168.1.1. Sekarang penghala itu akan mempunyai port yang menyambungkannya ke subnet lain (lebih lanjut dalam kursus Penghalaan). Alamat IP tertentu (rangkaian peribadi) tidak dapat dilihat oleh internet, dan kami mempunyai perkara seperti NAT (lebih lanjut mengenai ini kemudian).

## Latihan

Gunakan ifconfig untuk melihat topeng subnet anda.

## Soalan Kuiz

Benar atau salah, subnet terdiri daripada topeng subnet dan awalan rangkaian.

## Jawapan Kuiz

Benar