## Tuple (`tuple`)

`Tuple` di Python adalah tipe data koleksi yang digunakan untuk menyimpan beberapa nilai (elemen) dalam satu variabel, mirip dengan `list`. Bedanya, tuple bersifat **immutable** — sekali dibuat, isinya tidak bisa diubah. Tuple ditulis menggunakan tanda kurung `()`, dengan tiap elemen dipisahkan koma.

```python
koordinat = (10, 20)
print(koordinat)   # Output: (10, 20)
```

### Sifat Tuple

| Sifat       | Nilai     | Keterangan                                                  |
|-------------|-----------|---------------------------------------------------------------|
| Ordered     | ✅ True   | Elemen memiliki posisi/indeks tetap sesuai urutan input        |
| Mutable     | ❌ False  | Isi **tidak** bisa diedit, ditambah, atau dihapus setelah dibuat |
| Heterogen   | ✅ True   | Bisa menyimpan berbagai tipe data sekaligus dalam satu tuple    |
| Duplicate   | ✅ True   | Boleh berisi elemen dengan nilai yang sama                     |
| Size        | Tetap     | Panjang tuple tidak berubah setelah dibuat                     |

### Contoh: Immutable

```python
angka = (1, 2, 3)
angka[0] = 99   # Error!
# Output: TypeError: 'tuple' object does not support item assignment
```

### Contoh: Heterogen

```python
data_diri = ("Dika", 20, True)
print(data_diri)   # Output: ('Dika', 20, True)
```

### Contoh: Ordered & Duplicate

```python
angka = (5, 1, 5, 3)
print(angka[0])   # Output: 5   (elemen pertama, indeks 0)
print(angka[2])   # Output: 5   (nilai duplikat, tetap diizinkan)
```

### Tuple dengan satu elemen

Perlu tanda koma `,` di belakang elemen, kalau tidak, Python akan menganggapnya bukan tuple.

```python
bukan_tuple = (5)
print(type(bukan_tuple))    # Output: <class 'int'>

tuple_asli = (5,)
print(type(tuple_asli))     # Output: <class 'tuple'>
```

### Kenapa pakai Tuple kalau ada List?

Karena sifatnya immutable, tuple cocok dipakai untuk data yang **tidak boleh berubah** selama program berjalan, misalnya koordinat tetap, konfigurasi, atau data yang dikembalikan dari fungsi (multiple return values). Tuple juga sedikit lebih cepat diproses dibanding list karena Python tahu isinya tidak akan berubah.

```python
def bagi(a, b):
    return a // b, a % b   # return sebagai tuple

hasil, sisa = bagi(17, 5)
print(hasil, sisa)   # Output: 3 2
```