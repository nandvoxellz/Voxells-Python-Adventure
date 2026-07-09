## String
String di Python adalah tipe data untuk menyimpan teks (kumpulan karakter yang diapit tanda kutip). Bisa pakai kutip satu ('...') atau kutip dua ("..."), hasilnya sama saja, cuma beda gaya penulisan.

### Catatan penting
String di Python bersifat **immutable**, artinya sekali dibuat, isinya tidak bisa diubah langsung. Kalau kita ingin "mengubah" string, sebenarnya Python membuat string baru, bukan mengubah string yang lama.

## Contoh syntax string
Berikut adalah cara penulisan dan manipulasi string di Python:

### 1. Membuat string
Cukup apit teks dengan tanda kutip satu atau kutip dua, keduanya setara.
```python
nama: str = "Dika"
kota: str = 'Banjarmasin'
kalimat: str = "Aku punya 7 kucing"
```

### 2. Immutable
Sekali dibuat, isi string tidak bisa diubah langsung lewat index. Untuk "mengubah" string, kita harus membuat string baru.
```python
x = "halo"
# x[0] = "H"  # ini error!
x = "Halo"    # ini caranya, bikin ulang
```

### 3. String multi-baris
Gunakan kutip tiga (`"""..."""` atau `'''...'''`) untuk menulis teks yang terdiri dari beberapa baris.
```python
teks = """Ini baris satu
Ini baris dua"""
```

### 4. Kutip campur
Kalau teks mengandung tanda kutip di dalamnya, gunakan jenis kutip luar yang berbeda agar tidak bentrok.
```python
kalimat1 = "Dia bilang 'halo' tadi"
kalimat2 = 'Dia bilang "halo" tadi'
```

### 5. Concatenation dan repetition
String bisa digabung menggunakan operator `+`, dan diulang menggunakan operator `*`.
```python
a = "Hello" + " " + "World"   # "Hello World"
b = "ha" * 3                   # "hahaha"
```

### 6. Indexing dan slicing
String adalah urutan karakter, sehingga setiap karakternya bisa diakses menggunakan index, dan sebagian teksnya bisa diambil menggunakan slicing.
```python
s = "Python"
s[0]      # 'P'
s[-1]     # 'n'
s[0:3]    # 'Pyt'
```

### 7. f-string
Cara paling umum untuk menyisipkan nilai variabel ke dalam teks adalah dengan f-string, yaitu menambahkan huruf `f` sebelum tanda kutip.
```python
nama = "Nand"
print(f"Halo, {nama}!")   # Halo, Nand!
```

### 8. Method umum pada string
Python menyediakan banyak method bawaan untuk memanipulasi string, di antaranya:
```python
teks = "  Halo Dunia  "

teks.upper()      # "  HALO DUNIA  "
teks.lower()      # "  halo dunia  "
teks.strip()      # "Halo Dunia" (menghapus spasi di awal/akhir)
teks.split()      # ['Halo', 'Dunia']
teks.replace("Dunia", "Python")  # "  Halo Python  "
```