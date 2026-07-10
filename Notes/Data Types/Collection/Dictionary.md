## Dictionary (`dict`)

`Dictionary` di Python adalah tipe data koleksi yang menyimpan data dalam pasangan **key-value** (kunci-nilai), bukan berdasarkan posisi seperti list/tuple. Dictionary ditulis menggunakan tanda kurung kurawal `{}`, dengan format `key: value`.

```python
mahasiswa = {"nama": "Dika", "umur": 20, "aktif": True}
print(mahasiswa)   # Output: {'nama': 'Dika', 'umur': 20, 'aktif': True}
```

### Sifat Dictionary

| Sifat       | Nilai     | Keterangan                                                        |
|-------------|-----------|----------------------------------------------------------------------|
| Ordered     | ✅ True   | Sejak Python 3.7+, urutan key sesuai urutan input dipertahankan       |
| Mutable     | ✅ True   | Isi (value) dapat diedit, ditambah, atau dihapus setelah dibuat       |
| Heterogen   | ✅ True   | Value bisa berbagai tipe data; key harus *hashable* (int, str, tuple) |
| Duplicate   | ❌ False (key) | Key tidak boleh duplikat — kalau ditulis dua kali, value terakhir yang dipakai |
| Size        | Dinamis   | Jumlah pasangan key-value otomatis menyesuaikan isi                   |

### Akses data pakai Key, bukan indeks

```python
mahasiswa = {"nama": "Dika", "umur": 20}
print(mahasiswa["nama"])   # Output: Dika
print(mahasiswa[0])        # Error! KeyError: 0 (bukan indeks)
```

### Contoh: Mutable

```python
mahasiswa = {"nama": "Dika", "umur": 20}
mahasiswa["umur"] = 21          # Edit value
mahasiswa["jurusan"] = "TRKJ"   # Tambah pasangan baru
del mahasiswa["nama"]           # Hapus pasangan
print(mahasiswa)   # Output: {'umur': 21, 'jurusan': 'TRKJ'}
```

### Contoh: Key tidak boleh duplikat

```python
data = {"nama": "Dika", "nama": "Budi"}
print(data)   # Output: {'nama': 'Budi'}  (value terakhir yang menang)
```

### Key harus Hashable

Sama seperti elemen set, key dictionary harus tipe data immutable (`str`, `int`, `float`, `tuple`). List tidak bisa dipakai sebagai key.

```python
data = {["a", "b"]: "grup"}   # Error!
# Output: TypeError: unhashable type: 'list'
```

### Akses aman pakai `.get()`

Kalau key tidak ada, `[]` akan error, sedangkan `.get()` mengembalikan `None` (atau nilai default) tanpa crash.

```python
mahasiswa = {"nama": "Dika"}
print(mahasiswa.get("umur"))          # Output: None
print(mahasiswa.get("umur", 0))       # Output: 0  (default kalau gak ada)
```

### Kenapa pakai Dictionary?

Cocok dipakai kalau data punya struktur "label: nilai" yang jelas, alih-alih cuma urutan angka. Cari data lewat key juga jauh lebih cepat dibanding cari lewat isi di list.

```python
kamus = {"apel": "apple", "jeruk": "orange", "mangga": "mango"}
print(kamus["jeruk"])   # Output: orange
```