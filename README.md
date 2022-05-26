# Teknik Komputasi kelompok 10

Achmat Sodikkun

Ahmad Syafi'i

M. Hafidz Amanullah Abyan

# Bahasa Javanglish

Javanglish merupakan bahasa pemrograman baru modifikasi dari bahasa Python, menggunakan bahasa Jawa, Indonesia, dan Inggris sebagai perintahnya.

# Peringatan

Proyek ini hanya untuk bersenang-senang, saya tidak ingin menyakiti siapa pun. Hanya dari ide "bagaimana jika bahasa jawa adalah bahasa pemrograman" dan membuatnya menjadi kenyataan. Proyek ini hanya untuk tujuan pendidikan, bukan untuk produksi siap dan terinspirasi dari **Jaksel Script**.

# Menggunakan Bahasa javanglish

Cara menggunakan Bahasa javanglish adalah dengan menggunakan perintah **"python shell.py"** pada terminal atau langsung menjalankan file **"shell.py"**,
Ketika perintah dibaca, interpreter dikatakan dalam mode interaktif. Dalam mode ini ia meminta perintah berikutnya dengan prompt utama, ditandai dengan javanglish tanda lebih besar (javanglish > ).
```ruby
$ python shell.py
javanglish >
```
sebagai contoh untuk mencetak "Hello world" pada javanglish sebagai berikut:
```ruby
javanglish > TULIS("Hello world")
Hello world
```
# Perintah dasar javanglish

Beberapa perintah javanglish sederhana. Jalankan interpreter dan tunggu prompt utama, **javanglish >**. (Seharusnya tidak butuh waktu lama.)

## Angka

Interpreter bertindak sebagai kalkulator sederhana: Anda dapat mengetikkan ekspresi padanya dan itu akan menulis nilainya. Sintaks ekspresi sangat mudah: operator +, -, \* dan / bekerja seperti kebanyakan bahasa lain (misalnya, Pascal atau C); tanda kurung (()) dapat digunakan untuk pengelompokan. Sebagai contoh:

```ruby
javanglish > 2 + 2
4
javanglish > 50 - 5*6
20
javanglish > (50 - 5*6) / 4
5.0
javanglish > 8 / 5
1.6
```
> note:
pembagian selalu mengembalikan angka floating point

Pada javanglish menggunakan simbol ^ untuk menghitung pangkat:

```ruby
javanglish > 5 ^ 2
25
javanglish > 2 ^ 7
128
```

## Variabel

Pendefinisian variabel pada javanglish diawali dengan perintah **MISAL** atau pada bahasa pemrograman lain dikenal sebagai **"var"** atau **"let"** lalu diikuti dengan nama variabel lalu tanda sama dengan (=) digunakan untuk memberikan nilai pada variabel. Setelah itu, hasil ditampilkan sebelum prompt interaktif berikutnya:
```ruby
javanglish > width = 20
20
javanglish > height = 5*9
45
javanglish > width*height
900
```
Jika suatu variabel tidak "didefinisikan" (diberi nilai), mencoba menggunakannya akan memberi Anda kesalahan:
```ruby
javanglish > n
Traceback (paling anyar call terakhir):
File <stdin>, line 1, in <program>
Kesalahan Runtime: 'n' is not defined
n
^
```
Ada dukungan penuh untuk floating point; operator dengan operan tipe campuran mengubah operan integer menjadi floating point:
```ruby
javanglish > 4 \* 3.75 - 1
14.0
```
## String

Selain angka dan variabel, javanglish juga dapat memanipulasi string, yang dapat diekspresikan dalam beberapa cara. Mereka dapat diapit dalam tanda kutip ganda **("...")** dengan hasil yang sama. \ dapat digunakan untuk menghindari tanda kutip:
```ruby
javanglish > "Aku"
"Aku"
javanglish > "doesn\'t"
"doesn't"
```
String dapat digabungkan (direkatkan) dengan operator +, dan diulang dengan \*:
```ruby
javanglish > "aku" + "kamu"  
"akukamu"
javanglish > "iloveyou" \* 3  
"iloveyouiloveyouiloveyou"
```
## Percabangan If

Penulisan statements if, if-else, if-elif-else pada javanglish adalah sebagai berikut:
```ruby
javanglish > YEN 5 == 5 DADI 123
123
javanglish > YEN 5 == 6 DADI 123 LIYANE 234
234
javanglish > MISAL a = 5
5
javanglish > YEN a == 6 DADI 123 YENLIYANE a == 5 DADI 456 LIYANE 789
456
```
> note: 
> - YEN = if
> - DADI = then
> - LIYANE = else
> - YENLIYANE = elif

## Perulangan For

Penulisan statements for pada javanglish adalah sebagai berikut:
```ruby
javanglish > KANGGO i = 1 NGANTI 6 DADI i + 1
[2, 3, 4, 5, 6]
javanglish > KANGGO i = 1 NGANTI 6 DADI i _ 1
[1, 2, 3, 4, 5]
javanglish > KANGGO i = 5 NGANTI 1 NJANGKAH -1 DADI i _ 1
[5, 4, 3, 2]
```
> note:
> - KANGGO = for
> - NGANTI = to
> - DADI = then
> - NJANGKAH = step

## Perulangan Hhile

Penulisan statements while pada javanglish adalah sebagai berikut:
```ruby
javanglish > NALIKA i < 5 DADI MISAL i = i + 1
[3, 4, 5]
```
> note:
> - NALIKA = while
> - DADI = then

## Function

Penulisan function pada javanglish diawali dengan **MIGUNANI** atau sama dengan perintah **function** adalah sebagai berikut:
```ruby
javanglish > MIGUNANI tambah(a, b) -> a + b
<function tambah>
javanglish > tambah(2, 4)
6
```
Akan muncul eror ketika masukan tidak sesuai dengan yang didefinisikan pada function:
```ruby
javanglish > tambah(2, 4, 6)
Traceback (paling anyar call terakhir):
File <stdin>, line 1, in <program>
Kesalahan Runtime: 1 kakehan args liwati menyang <function tambah>
tambah(2, 4, 6)
^^^^^^^^^^^^^^
```
## List

Penulisan list pada javanglish menggunakan perintah **[]** sebagai berikut:
```ruby
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
```
## Append, Pop dan Extend

Penulisan append, pop dan extend pada javanglish adalah sebagai berikut:
```ruby
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
```
> note:
> - APPEND = menambah item pada akhir list.
> - POP = mengambil item pada list sesuai posisi.
> - EXTEND = menambah list dengan append semua list item.

##  Input dan Print

Penulisan input pada javanglish menggunakan perintah **MASUKNA()** untuk tipe data string dan **MASUKNA_INT()** untuk tipe data iteger:
```ruby
javanglish > MISAL nama = MASUKNA()
sayang
"sayang"
javanglish > nama
"sayang"
javanglish > MISAL umur = MASUKNA_INT()
aku
'aku' kudu integer. Coba maneh!
19
19
javanglish > umur
19
```
Penulis print pada javanglish menggunakan perintah **TULIS()** sebagai berikut:
```ruby
javanglish > TULIS("HELLO WORlD")
HELLO WORlD
```
## Penulisan Multiline
Penulisan multiline pada javanglish ditandai dengan perintah **;** untuk mengganti baris, sebagai contoh:
```ruby
javanglish > 1 + 2; 3 + 4
[3, 7] 
```
### Penulisan pada percabangan if
contoh single line:
```ruby
javanglish > MISAL nilai = YEN 7 == 7 DADI "lolos" LIYANE "gagal"
"lolos"
javanglish > nilai
"lolos"
```
contoh multi line:
```ruby
javanglish > YEN 7 == 7 DADI; TULIS("lolos"); TULIS("selamat") 
LIYANE TULIS("gagal")
lolos
selamat
```
## Return, Break dan Continue
Penulisan return pada javanglish menggunakan perintah **BALIK** sebagai berikut:
```ruby
javanglish > MIGUNANI contoh(); MISAL absen = 5; BALIK absen; AKHIR
<function contoh>
javanglish > contoh()
5
```
Penulisan continue pada javanglish menggunakan perintah **LANJUT** dan break menggunakan perintah **MANDEK** sebagai berikut:
```ruby
javanglish > MISAL a = []
[]
javanglish > KANGGO i = 0 NGANTI 10 DADI; YEN i == 4 DADI LANJUT YENLIYANE i == 8 DADI MANDEK; MISAL a = a + i; AKHIR
javanglish > a
[0, 1, 2, 3, 5, 6, 7]
```
> note:
> - BALIK = return
> - LANJUT = continue
> - MANDEK = break

## Menjalankan file javanglish
Ekstensi file javanglish adalah **.jvl** untuk menjalankannya menggunakan perintah **COBA("")** diikuti dengan nama file, sudah disediakan file dengan ekstensi **.jvl** dengan nama **test**:
```ruby
javanglish > COBA("test.jvl")
Hello World
Ini adalah bahasa javanglish
```
## membersihkan terminal
Perintah untuk membersihkan terminal pada javanglish ada dua cara, **HAPUS()** dan **HPS()**
```ruby
javanglish > HAPUS()
javanglish > HPS()
```
