# Teknik Komputasi kelompok 10

Achmat Sodikkun
Ahmad Syafi'i
M. Hafidz Amanullah Abyan

# Bahasa Javanglish (Jawa + English)

# Menggunakan Bahasa javanglish

Cara menggunakan Bahasa javanglish adalah dengan menggunakan perintah "python shell.py" pada terminal atau langsung menjalankan file "shell.py",
Ketika perintah dibac, interpreter dikatakan dalam mode interaktif. Dalam mode ini ia meminta perintah berikutnya dengan prompt utama, ditandai dengan javanglish tanda lebih besar (javanglish > ).

$ python shell.py

javanglish >

sebagai contoh untuk mencetak "Hello world" pada javanglish sebagai berikut:

javanglish > TULIS("Hello world")
Hello world

# javanglish sebagai kalkulator

Beberapa perintah javanglish sederhana. Jalankan interpreter dan tunggu prompt utama, javanglish >. (Seharusnya tidak butuh waktu lama.)

## Angka

Interpreter bertindak sebagai kalkulator sederhana: Anda dapat mengetikkan ekspresi padanya dan itu akan menulis nilainya. Sintaks ekspresi sangat mudah: operator +, -, \* dan / bekerja seperti kebanyakan bahasa lain (misalnya, Pascal atau C); tanda kurung (()) dapat digunakan untuk pengelompokan. Sebagai contoh:

javanglish > 2 + 2
4
javanglish > 50 - 5*6
20
javanglish > (50 - 5*6) / 4
5.0
javanglish > 8 / 5
1.6

note:
pembagian selalu mengembalikan angka floating point

Pada javanglish menggunakan simbol ^ untuk menghitung pangkat:

javanglish > 5 ^ 2
25
javanglish > 2 ^ 7
128

## Variabel

Pendefinisian variabel pada javanglish diawali dengan perintah "MISAL" atau pada bahasa pemrograman lain dikenal sebagai "var" atau "let" lalu diikuti dengan nama variabel lalu tanda sama dengan (=) digunakan untuk memberikan nilai pada variabel. Setelah itu, hasil ditampilkan sebelum prompt interaktif berikutnya:

javanglish > width = 20
20
javanglish > height = 5*9
45
javanglish > width*height
900

Jika suatu variabel tidak "didefinisikan" (diberi nilai), mencoba menggunakannya akan memberi Anda kesalahan:

javanglish > n
Traceback (paling anyar call terakhir):
File <stdin>, line 1, in <program>
Kesalahan Runtime: 'n' is not defined

n
^
Ada dukungan penuh untuk floating point; operator dengan operan tipe campuran mengubah operan integer menjadi floating point:

javanglish > 4 \* 3.75 - 1
14.0

## String

Selain angka dan variabel, javanglish juga dapat memanipulasi string, yang dapat diekspresikan dalam beberapa cara. Mereka dapat diapit dalam tanda kutip ganda ("...") dengan hasil yang sama. \ dapat digunakan untuk menghindari tanda kutip:

javanglish > "Aku"
"Aku"
javanglish > "doesn\'t"
"doesn't"

String dapat digabungkan (direkatkan) dengan operator +, dan diulang dengan \*:

javanglish > "aku" + "kamu"  
"akukamu"
javanglish > "iloveyou" \* 3  
"iloveyouiloveyouiloveyou"

## percabangan if

Penulisan statements if, if-else, if-elif-else pada javanglish adalah sebagai berikut:

javanglish > YEN 5 == 5 DADI 123
123
javanglish > YEN 5 == 6 DADI 123 LIYANE 234
234
javanglish > MISAL a = 5
5
javanglish > YEN a == 6 DADI 123 YENLIYANE a == 5 DADI 456 LIYANE 789
456

note:
YEN = if
DADI = then
LIYANE = else
YENLIYANE = elif

## perulangan for

Penulisan statements for pada javanglish adalah sebagai berikut:

javanglish > KANGGO i = 1 NGANTI 6 DADI i + 1
[2, 3, 4, 5, 6]
javanglish > KANGGO i = 1 NGANTI 6 DADI i _ 1
[1, 2, 3, 4, 5]
javanglish > KANGGO i = 5 NGANTI 1 NJANGKAH -1 DADI i _ 1
[5, 4, 3, 2]

note:
KANGGO = for
NGANTI = to
DADI = then
NJANGKAH = step

## perulangan while

Penulisan statements while pada javanglish adalah sebagai berikut:

javanglish > NALIKA i < 5 DADI MISAL i = i + 1
[3, 4, 5]

note:
NALIKA = while
DADI = then

## Function

Penulisan function pada javanglish diawali dengan "MIGUNANI" atau sama dengan perintah "function" adalah sebagai berikut:

javanglish > MIGUNANI tambah(a, b) -> a + b
<function tambah>
javanglish > tambah(2, 4)
6

akan muncul eror ketika masukan tidak sesuai dengan yang didefinisikan pada function:

javanglish > tambah(2, 4, 6)
Traceback (paling anyar call terakhir):
File <stdin>, line 1, in <program>
Kesalahan Runtime: 1 kakehan args liwati menyang <function tambah>

tambah(2, 4, 6)
^^^^^^^^^^^^^^

## list

Penulisan list pada javanglish menggunakan perintah "[]" sebagai berikut:

javanglish > []
[]
javanglish > [1, 2, 3]  
[1, 2, 3]
javanglish > [1, 2, 3] + 4
[1, 2, 3, 4]
javanglish > [1, 2, 3] \* [3, 4, 5]
[1, 2, 3, 3, 4, 5]
javanglish > [1, 2, 3] / 0  
1
javanglish > [1, 2, 3] / 1
2
javanglish > [1, 2, 3] / 5
Traceback (paling anyar call terakhir):
File <stdin>, line 1, in <program>
Kesalahan Runtime: Unsur ing indeks iki oga bisa dijupuk saka list amarga indeks metu saka batas

[1, 2, 3] / 5
^
javanglish > KANGGO i = 1 NGANTI 9 DADI 2 ^ i
[2, 4, 8, 16, 32, 64, 128, 256]

## append, pop dan extend

Penulisan append, pop dan extend pada javanglish adalah sebagai berikut:

javanglish > MISAL list = [1, 2, 3]
[1, 2, 3]
javanglish > APPEND(list, 4)
0
javanglish > list
[1, 2, 3, 4]
javanglish > POP(list, 3)  
4
javanglish > list
[1, 2, 3]
javanglish > EXTEND(list, [4, 5, 6])
0
javanglish > list
[1, 2, 3, 4, 5, 6]

note:
APPEND = menambah item pada akhir list.
POP = mengambil item pada list sesuai posisi.
EXTEND = menambah list dengan append semua list item.

## append, pop dan extend

Penulisan append, pop dan extend pada javanglish adalah sebagai berikut:

javanglish > MISAL list = [1, 2, 3]
[1, 2, 3]
javanglish > APPEND(list, 4)
0
javanglish > list
[1, 2, 3, 4]
javanglish > POP(list, 3)  
4
javanglish > list
[1, 2, 3]
javanglish > EXTEND(list, [4, 5, 6])
0
javanglish > list
[1, 2, 3, 4, 5, 6]

note:
APPEND = menambah item pada akhir list.
POP = mengambil item pada list sesuai posisi.
EXTEND = menambah list dengan append semua list item.

## return, break dan continue

Penulisan return, break, continue pada javanglish adalah sebagai berikut:

javanglish > NALIKA i < 5 DADI MISAL i = i + 1
[3, 4, 5]

note:
BALIK = return
LANJUT = continue
MANDEK = break
