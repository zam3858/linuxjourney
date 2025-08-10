# Bit Lekat

## Kandungan Pelajaran

Satu lagi bit kebenaran khas yang ingin saya bincangkan adalah bit lekat (sticky bit).

Bit kebenaran ini, "melekatkan fail/direktori" ini bermakna hanya pemilik atau pengguna root sahaja yang boleh menghapus atau mengubah fail tersebut. Ini sangat berguna untuk direktori yang dikongsi. Lihat contoh di bawah:

<pre>$ ls -ld /tmp
drwxrwxrwxt 6 root root 4096 Dec 15 11:45 /tmp
</pre>

Anda akan melihat bit kebenaran khas di akhir sini <b>t</b>, ini bermakna semua orang boleh menambah fail, menulis fail, mengubah fail dalam direktori /tmp, tetapi hanya root boleh menghapus direktori /tmp.

<b>Mengubah bit lekat</b>

<pre>$ sudo chmod +t mydir

$ sudo chmod 1755 mydir</pre>

Perwakilan angka untuk bit lekat adalah <b>1</b>

## Latihan

Fail dan direktori lain manakah yang anda fikir mempunyai bit lekat diaktifkan?

## Soalan Kuiz

Simbol apakah yang mewakili bit lekat?

## Jawapan Kuiz

t