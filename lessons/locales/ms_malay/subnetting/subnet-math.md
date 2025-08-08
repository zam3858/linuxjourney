# Matematik Subnet

## Kandungan Pelajaran

Ok, kita tahu bahawa topeng subnet penting untuk mengetahui berapa banyak hos yang boleh kita ada pada subnet kita. Jadi berapa banyak hos yang akan ada?

Katakan saya mempunyai alamat IP <b>192.168.1.0</b> dan topeng subnet <b>255.255.255.0</b>, sekarang mari kita susun nombor ini dalam bentuk binari. Buat masa ini gunakan kalkulator dalam talian untuk menukar nilai ini dari perpuluhan ke binari.

<pre>
192.168.1.165  = 11000000.10101000.00000001.10100101
255.255.255.0  = 11111111.11111111.11111111.00000000
</pre>

Alamat IP ditopeng oleh topeng subnet kami, apabila anda melihat 1, ia ditopeng dan kami berpura-pura seperti kami tidak melihatnya. Jadi satu-satunya hos yang mungkin kita ada adalah dari rantau 00000000. Ingat 11111111 dalam bentuk binari bersamaan dengan 255, kita juga mengira 0 sebagai nombor hos, jadi terdapat 256 pilihan yang mungkin. Walau bagaimanapun, ia mungkin kelihatan seperti kita mempunyai 256 pilihan yang mungkin, tetapi kita sebenarnya menolak 2 hos kerana kita perlu mengambil kira alamat siaran dan alamat subnet, meninggalkan kita dengan 254 hos yang mungkin pada subnet kita. Jadi kita tahu bahawa kita boleh mempunyai hos dengan alamat IP antara 192.168.1.1 - 192.168.1.254.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Apakah persamaan binari bagi 255?

## Jawapan Kuiz

11111111