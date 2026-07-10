## Set (`set`)

`Set` di Python adalah tipe data koleksi yang digunakan untuk menyimpan beberapa nilai unik (tidak ada duplikat) dalam satu variabel. Set ditulis menggunakan tanda kurung kurawal `{}`, dengan tiap elemen dipisahkan koma.

```python
warna = {"merah", "hijau", "biru"}
print(warna)   # Output: {'biru', 'hijau', 'merah'}  (urutan bisa beda tiap run)
```

### Sifat Set

| Sifat       | Nilai     | Keterangan                                                     |
|-------------|-----------|-------------------------------------------------------------------|
| Ordered     | ❌ False  | Elemen tidak memiliki posisi/indeks tetap, urutan bisa berubah-ubah |
| Mutable     | ✅ True   | Elemen dapat ditambah atau dihapus setelah dibuat                  |
| Heterogen   | ✅ True   | Bisa menyimpan berbagai tipe data sekaligus, selama elemennya *hashable* |
| Duplicate   | ❌ False  | Tidak boleh ada elemen dengan nilai yang sama (otomatis dihapus)    |
| Size        | Dinamis   | Panjang set otomatis menyesuaikan jumlah elemen unik               |

### Contoh: Tidak ada Duplicate

```python
angka = {1, 2, 2, 3, 3, 3}
print(angka)   # Output: {1, 2, 3}  (duplikat otomatis hilang)
```

### Contoh: Unordered (tidak bisa diakses pakai indeks)

```python
angka = {5, 1, 3}
print(angka[0])   # Error!
# Output: TypeError: 'set' object is not subscriptable
```

### Contoh: Mutable

```python
buah = {"apel", "jeruk"}
buah.add("mangga")
print(buah)   # Output: {'apel', 'jeruk', 'mangga'}

buah.remove("apel")
print(buah)   # Output: {'jeruk', 'mangga'}
```

### Elemen harus Hashable

Set hanya bisa berisi elemen yang *hashable* — artinya tipe data mutable seperti `list` atau `dict` tidak bisa dimasukkan ke dalam set.

```python
data = {1, 2, [3, 4]}   # Error!
# Output: TypeError: unhashable type: 'list'
```

### Set kosong — hati-hati!

```python
kosong = {}
print(type(kosong))   # Output: <class 'dict'>  (bukan set!)

set_kosong = set()
print(type(set_kosong))   # Output: <class 'set'>
```

`{}` kosong otomatis dianggap `dict`, bukan `set`. Untuk bikin set kosong, harus pakai `set()`.

### Kenapa pakai Set?

Set cocok dipakai kalau kamu butuh:
- Menghapus duplikat dari sebuah list dengan cepat
- Mengecek keanggotaan (`in`) dengan performa cepat (lebih cepat dari list untuk data besar)
- Melakukan operasi matematika himpunan (union, intersection, difference)

```python
angka_list = [1, 2, 2, 3, 3, 3, 4]
angka_unik = set(angka_list)
print(angka_unik)   # Output: {1, 2, 3, 4}

a = {1, 2, 3}
b = {2, 3, 4}
print(a | b)   # Union         → {1, 2, 3, 4}
print(a & b)   # Intersection  → {2, 3}
print(a - b)   # Difference    → {1}
```