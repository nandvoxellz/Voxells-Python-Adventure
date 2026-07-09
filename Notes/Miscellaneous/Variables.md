## Apa Itu Variabel?
Variabel berfungsi seperti wadah untuk menyimpan data. Syntax pembuatan variabel di Python sangat sederhana: cukup tuliskan nama variabel, tanda sama dengan (`=`), lalu nilai datanya.

### 1. Membuat variabel
```python
# Menyimpan teks
nama_murid = "Andi"

# Menyimpan angka
umur = 20

# Menyimpan nilai benar/salah (boolean)
suka_koding = True

# Menampilkan isi variabel
print(nama_murid)
```

### 2. Aturan penamaan variabel
Python punya beberapa aturan wajib soal penamaan variabel. Kalau dilanggar, akan menghasilkan `SyntaxError`.

- Hanya boleh terdiri dari huruf, angka, dan underscore (`_`).
- Tidak boleh diawali dengan angka.
- Tidak boleh mengandung spasi (gunakan underscore sebagai pengganti spasi).
- Tidak boleh menggunakan kata kunci bawaan Python (seperti `print`, `if`, `for`, `True`).
- Bersifat case-sensitive — `nama`, `Nama`, dan `NAMA` dianggap tiga variabel berbeda.

```python
# BENAR
nama_murid = "Andi"
umur2 = 20
_status = True

# SALAH - diawali angka
2umur = 20   # SyntaxError

# SALAH - mengandung spasi
nama murid = "Andi"   # SyntaxError
```

**Catatan penting:** Meskipun secara teknis diizinkan, sebaiknya hindari juga menamai variabel sama dengan nama fungsi bawaan Python (seperti `list`, `str`, atau `type`), karena akan "menimpa" fungsi aslinya selama program berjalan.
```python
list = [1, 2, 3]   # Menimpa fungsi bawaan list()
# print(list("halo"))  # Sekarang akan error, karena 'list' bukan lagi fungsi
```

### 3. Mengisi ulang nilai variabel (reassignment)
Nilai sebuah variabel bisa diganti kapan saja, bahkan dengan tipe data yang berbeda dari sebelumnya — karena Python bersifat Dynamically Typed.
```python
umur = 20
print(umur)   # Output: 20

umur = 21
print(umur)   # Output: 21

umur = "Dua puluh satu"   # Boleh, tipe datanya berubah jadi string
print(umur)   # Output: Dua puluh satu
```

### 4. Mengisi banyak variabel sekaligus
Python memungkinkan pengisian beberapa variabel dalam satu baris, baik dengan nilai yang sama maupun berbeda.
```python
# Nilai yang sama untuk beberapa variabel
a = b = c = 0

# Nilai berbeda dalam satu baris
nama, umur, aktif = "Dika", 20, True

print(nama)   # Output: Dika
print(umur)   # Output: 20
print(aktif)  # Output: True
```