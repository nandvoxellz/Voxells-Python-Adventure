## List (`list`)

`List` di Python adalah tipe data koleksi yang digunakan untuk menyimpan beberapa nilai (elemen) dalam satu variabel. List ditulis menggunakan tanda kurung siku `[]`, dengan tiap elemen dipisahkan koma.

```python
buah = ["apel", "jeruk", "mangga"]
print(buah)   # Output: ['apel', 'jeruk', 'mangga']
```

### Sifat List

| Sifat       | Nilai    | Keterangan                                              |
|-------------|----------|----------------------------------------------------------|
| Ordered     | ✅ True  | Elemen memiliki posisi/indeks tetap sesuai urutan input   |
| Mutable     | ✅ True  | Isi dapat diedit, ditambah, atau dihapus setelah dibuat   |
| Heterogen   | ✅ True  | Bisa menyimpan berbagai tipe data sekaligus dalam satu list |
| Duplicate   | ✅ True  | Boleh berisi elemen dengan nilai yang sama                |
| Size        | Dinamis  | Panjang list otomatis menyesuaikan jumlah elemen          |

### Contoh: Heterogen

```python
campuran = ["Dika", 20, True, 3.14]
print(campuran)   # Output: ['Dika', 20, True, 3.14]
```

### Contoh: Mutable

```python
angka = [1, 2, 3]
angka[0] = 99
print(angka)   # Output: [99, 2, 3]
```

### Contoh: Ordered & Duplicate

```python
angka = [5, 1, 5, 3]
print(angka[0])   # Output: 5   (elemen pertama, indeks 0)
print(angka[2])   # Output: 5   (nilai duplikat, tetap diizinkan)
```