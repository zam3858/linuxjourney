# CIDR

## Kandungan Pelajaran

CIDR (penghalaan antara domain tanpa kelas) digunakan untuk mewakili topeng subnet dengan cara yang lebih padat. Anda mungkin melihat subnet yang dicatatkan dalam notasi CIDR, di mana subnet seperti 10.42.3.0/255.255.255.0 ditulis sebagai 10.42.3.0/24 yang hanya bermaksud ia merangkumi kedua-dua awalan subnet dan topeng subnet.

Ingat alamat IP terdiri daripada 4 bait atau 32 bit, CIDR menunjukkan jumlah bit yang digunakan sebagai awalan rangkaian. Jadi 123.12.24.0/23 bermakna 23 bit pertama digunakan. Apa maksudnya? Berapa banyak hos itu?

Trik mudah ialah menolak jumlah bit yang boleh dimiliki oleh alamat IP (32) daripada alamat CIDR (23), jadi itu meninggalkan 9 bit, 2^9 = 512, tetapi kita perlu mengalih keluar 2 alamat (alamat subnet dan alamat siaran) jadi kita mempunyai 510 hos yang boleh digunakan.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Tiada soalan, teruskan!

## Jawapan Kuiz