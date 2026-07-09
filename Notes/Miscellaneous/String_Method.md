## 47 Method String di Python
Python menyediakan banyak method bawaan untuk memanipulasi string. Berikut rangkuman 47 method yang paling umum digunakan, dikelompokkan berdasarkan fungsinya.

### Catatan penting
Semua method string di Python **tidak mengubah string asli** (karena string bersifat immutable), melainkan selalu mengembalikan string/nilai baru sebagai hasilnya.

### 1. Mengubah huruf besar/kecil
| Method | Kegunaan | Contoh |
|---|---|---|
| `upper()` | Ubah semua jadi huruf besar | `"halo".upper()` → `"HALO"` |
| `lower()` | Ubah semua jadi huruf kecil | `"HALO".lower()` → `"halo"` |
| `capitalize()` | Huruf pertama besar, sisanya kecil | `"halo dunia".capitalize()` → `"Halo dunia"` |
| `title()` | Huruf pertama tiap kata jadi besar | `"halo dunia".title()` → `"Halo Dunia"` |
| `swapcase()` | Tukar besar↔kecil | `"Halo".swapcase()` → `"hALO"` |
| `casefold()` | Lowercase versi agresif (untuk perbandingan teks) | `"STRASSE".casefold()` → `"strasse"` |

### 2. Mencari & menghitung
| Method | Kegunaan | Contoh |
|---|---|---|
| `find()` | Cari index kemunculan pertama, `-1` jika tidak ada | `"halo".find("l")` → `2` |
| `rfind()` | Cari index kemunculan terakhir | `"halo".rfind("l")` → `2` |
| `index()` | Sama seperti `find()`, tapi error jika tidak ketemu | `"halo".index("a")` → `1` |
| `rindex()` | Sama seperti `rfind()`, tapi error jika tidak ketemu | `"halo".rindex("a")` → `1` |
| `count()` | Hitung jumlah kemunculan substring | `"halo".count("l")` → `1` |
| `startswith()` | Cek apakah diawali substring tertentu | `"halo".startswith("ha")` → `True` |
| `endswith()` | Cek apakah diakhiri substring tertentu | `"halo".endswith("lo")` → `True` |

### 3. Cek jenis karakter (is...)
| Method | Kegunaan | Contoh |
|---|---|---|
| `isalpha()` | Semua karakter huruf? | `"halo".isalpha()` → `True` |
| `isdigit()` | Semua karakter angka? | `"123".isdigit()` → `True` |
| `isdecimal()` | Semua karakter desimal? | `"123".isdecimal()` → `True` |
| `isnumeric()` | Semua karakter numerik (termasuk simbol angka lain)? | `"½".isnumeric()` → `True` |
| `isalnum()` | Gabungan huruf & angka saja? | `"halo123".isalnum()` → `True` |
| `isspace()` | Semua karakter spasi/whitespace? | `"   ".isspace()` → `True` |
| `islower()` | Semua huruf kecil? | `"halo".islower()` → `True` |
| `isupper()` | Semua huruf besar? | `"HALO".isupper()` → `True` |
| `istitle()` | Format sudah title case? | `"Halo Dunia".istitle()` → `True` |
| `isidentifier()` | Valid sebagai nama variabel Python? | `"nama_1".isidentifier()` → `True` |
| `isprintable()` | Semua karakter bisa dicetak (tidak ada `\n`, dll)? | `"halo".isprintable()` → `True` |
| `isascii()` | Semua karakter termasuk ASCII? | `"halo".isascii()` → `True` |

### 4. Whitespace & perataan (padding)
| Method | Kegunaan | Contoh |
|---|---|---|
| `strip()` | Hapus spasi di awal & akhir | `"  halo  ".strip()` → `"halo"` |
| `lstrip()` | Hapus spasi di awal saja | `"  halo".lstrip()` → `"halo"` |
| `rstrip()` | Hapus spasi di akhir saja | `"halo  ".rstrip()` → `"halo"` |
| `center()` | Ratakan tengah dengan lebar tertentu | `"hi".center(6, "*")` → `"**hi**"` |
| `ljust()` | Ratakan kiri dengan lebar tertentu | `"hi".ljust(5, "-")` → `"hi---"` |
| `rjust()` | Ratakan kanan dengan lebar tertentu | `"hi".rjust(5, "-")` → `"---hi"` |
| `zfill()` | Tambah `0` di depan hingga lebar tertentu | `"7".zfill(3)` → `"007"` |
| `expandtabs()` | Ubah tab (`\t`) jadi spasi | `"a\tb".expandtabs(4)` → `"a   b"` |

### 5. Split, join, & partition
| Method | Kegunaan | Contoh |
|---|---|---|
| `split()` | Pecah string jadi list berdasarkan pemisah | `"a,b,c".split(",")` → `['a','b','c']` |
| `rsplit()` | Sama seperti `split()`, tapi mulai dari kanan | `"a,b,c".rsplit(",", 1)` → `['a,b','c']` |
| `splitlines()` | Pecah string berdasarkan baris baru | `"a\nb".splitlines()` → `['a','b']` |
| `join()` | Gabungkan list jadi string dengan pemisah | `",".join(['a','b','c'])` → `"a,b,c"` |
| `partition()` | Pecah jadi 3 bagian di kemunculan pertama | `"a=b=c".partition("=")` → `('a','=','b=c')` |
| `rpartition()` | Sama seperti `partition()`, tapi dari kanan | `"a=b=c".rpartition("=")` → `('a=b','=','c')` |

### 6. Mengganti isi
| Method | Kegunaan | Contoh |
|---|---|---|
| `replace()` | Ganti substring dengan substring lain | `"halo".replace("a", "e")` → `"helo"` |
| `removeprefix()` | Hapus awalan tertentu jika ada | `"halo_dunia".removeprefix("halo_")` → `"dunia"` |
| `removesuffix()` | Hapus akhiran tertentu jika ada | `"file.txt".removesuffix(".txt")` → `"file"` |
| `translate()` | Ganti karakter sesuai tabel mapping | `"halo".translate(str.maketrans("a","e"))` → `"helo"` |
| `maketrans()` | Buat tabel mapping untuk `translate()` | `str.maketrans("ab", "xy")` |

### 7. Format teks
| Method | Kegunaan | Contoh |
|---|---|---|
| `format()` | Sisipkan nilai ke dalam string pakai `{}` | `"Halo {}".format("Dika")` → `"Halo Dika"` |
| `format_map()` | Sama seperti `format()`, tapi input berupa dictionary | `"Halo {nama}".format_map({"nama":"Dika"})` → `"Halo Dika"` |
| `encode()` | Ubah string jadi bytes | `"halo".encode()` → `b'halo'` |