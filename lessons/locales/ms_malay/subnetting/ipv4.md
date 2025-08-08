# IPv4

## Kandungan Pelajaran

Jadi kita tahu bahawa hos rangkaian mempunyai alamat unik yang boleh ditemui. Alamat ini dikenali sebagai alamat IP. Alamat IPv4 kelihatan seperti ini:

<pre>204.23.124.23</pre>

Alamat ini sebenarnya mengandungi dua bahagian, bahagian rangkaian yang memberitahu kita rangkaian mana ia berada dan bahagian hos yang memberitahu kita hos mana pada rangkaian itu. Untuk kursus ini kita kebanyakannya akan membincangkan alamat IPv4, yang biasa anda lihat apabila merujuk kepada alamat IP.

Alamat IP dipisahkan kepada oktet oleh noktah. Jadi terdapat 4 oktet dalam alamat IPv4. Jika anda tahu sedikit tentang sains komputer, oktet ialah 8 bit dan 8 bit sebenarnya bersamaan dengan 1 bait, jadi kami juga merujuk kepada alamat IPv4 sebagai mempunyai 4 bait. Kami kerap menggunakan bit apabila berurusan dengan subnet dan alamat IP.

Anda boleh melihat alamat IP anda dengan arahan ifconfig -a:

<pre>
pete@icebox:~$ ifconfig -a
eth0      Link encap:Ethernet  HWaddr 1d:3a:32:24:4d:ce
          inet addr:192.168.1.129  Bcast:192.168.1.255  Mask:255.255.255.0
          inet6 addr: fd60::21c:29ff:fe63:5cdc/64 Scope:Link
</pre>

Seperti yang anda lihat alamat IPv4 saya ialah: 192.168.1.129

## Latihan

Cari alamat IP anda dengan ifconfig.

## Soalan Kuiz

Berapa banyak bait dalam alamat IPv4?

## Jawapan Kuiz

4