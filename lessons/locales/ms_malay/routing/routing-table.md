# Jadual Penghalaan

## Kandungan Pelajaran

Lihat jadual penghalaan mesin anda:

<pre>
pete@icebox:~$ sudo route -n
Kernel IP routing table
Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
0.0.0.0         192.168.224.2   0.0.0.0         UG    0      0        0 eth0
192.168.224.0   0.0.0.0         255.255.255.0   U     1      0        0 eth0
</pre>

<b>Destinasi</b>

Dalam medan pertama, kami mempunyai alamat IP destinasi 192.168.224.0, ini mengatakan bahawa mana-mana paket yang cuba pergi ke rangkaian ini, keluar melalui kabel Ethernet saya (eth0). Jika saya 192.168.224.5 dan ingin ke 192.168.224.7, saya hanya akan menggunakan antara muka rangkaian eth0 secara terus.

Perhatikan bahawa kami mempunyai alamat <b>0.0.0.0</b> ini bermakna tiada alamat yang dinyatakan atau ia tidak diketahui. Jadi jika sebagai contoh, saya ingin menghantar paket ke alamat IP 151.123.43.6, jadual penghalaan kami tidak tahu ke mana ia pergi, jadi ia menandakannya sebagai 0.0.0.0 dan oleh itu menghalakan paket kami ke Get Laluan.

<b>Get Laluan</b>

Jika kami menghantar paket yang tidak berada pada rangkaian yang sama, ia akan dihantar ke alamat Get Laluan ini. Yang dinamakan dengan tepat sebagai Get Laluan ke rangkaian lain.

<b>Genmask</b>

Ini ialah topeng subnet, digunakan untuk mengetahui alamat IP mana yang sepadan dengan destinasi mana.

<b>Bendera</b>

<ul>
<li>UG - Rangkaian sedang Aktif dan merupakan Get Laluan</li>
<li>U - Rangkaian sedang Aktif</li>
</ul>

<b>Iface</b>

Ini ialah antara muka yang akan dilalui oleh paket kami, eth0 biasanya bermaksud peranti Ethernet pertama pada sistem anda.

## Latihan

Lihat jadual penghalaan anda dan lihat ke mana paket anda boleh pergi.

## Soalan Kuiz

Ke manakah paket dihalakan jika jadual penghalaan kami tidak tahu?

## Jawapan Kuiz

Get Laluan