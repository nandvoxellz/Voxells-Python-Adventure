## Apa Itu F-Strings?
F-string (Formatted String) adalah cara modern di Python (tersedia mulai Python 3.6 ke atas) untuk menggabungkan teks dan variabel. Fitur ini membuat kode jauh lebih rapi, singkat, dan mudah dibaca dibandingkan cara lama yang menggunakan banyak tanda plus (`+`) atau koma.

### Catatan penting
Syntax f-string sangat praktis: cukup tambahkan huruf `f` tepat sebelum tanda kutip teks, lalu letakkan variabel yang ingin dimasukkan ke dalam tanda kurung kurawal `{}`.

### 1. Penggunaan dasar
```python
nama = "Dika"
umur = 20

# Tanpa f-string
print("Halo, nama saya " + nama + " dan umur saya " + str(umur) + " tahun.")

# Dengan f-string
print(f"Halo, nama saya {nama} dan umur saya {umur} tahun.")
```

### 2. Ekspresi & operasi di dalam f-string
Di dalam `{}`, kamu tidak cuma bisa menaruh variabel, tapi juga ekspresi matematika, pemanggilan fungsi, bahkan method langsung.
```python
nama = "Dika"
umur = 20

# Operasi matematika langsung di dalam f-string
print(f"Tahun depan, umur {nama} adalah {umur + 1} tahun.")

# Memanggil method langsung
print(f"Nama kapital: {nama.upper()}")

# Memanggil fungsi
print(f"Panjang nama: {len(nama)} huruf")
```

### 3. Format angka (format specifier)
F-string mendukung format specifier setelah tanda titik dua (`:`) di dalam `{}`, berguna untuk mengatur jumlah angka desimal, pemisah ribuan, atau persentase.
```python
harga = 1500000
pi = 3.14159265

# Pembulatan ke 2 angka desimal
print(f"Nilai pi: {pi:.2f}")           # Output: Nilai pi: 3.14

# Pemisah ribuan
print(f"Harga: Rp{harga:,}")           # Output: Harga: Rp1,500,000

# Persentase
rasio = 0.756
print(f"Progress: {rasio:.1%}")        # Output: Progress: 75.6%
```

### 4. Perataan teks (alignment)
Format specifier juga bisa dipakai untuk mengatur lebar dan perataan teks, berguna untuk membuat tampilan tabel sederhana di terminal.
```python
nama = "Dika"

print(f"[{nama:<10}]")   # Rata kiri, lebar 10   -> [Dika      ]
print(f"[{nama:>10}]")   # Rata kanan, lebar 10  -> [      Dika]
print(f"[{nama:^10}]")   # Rata tengah, lebar 10 -> [   Dika   ]
```

### 5. Debug mode dengan `=`
Sejak Python 3.8, f-string punya trik praktis untuk debugging: tambahkan `=` setelah nama variabel di dalam `{}` untuk menampilkan nama variabel sekaligus nilainya sekaligus, tanpa perlu menulis manual.
```python
umur = 20

print(f"{umur}")     # Output: 20
print(f"{umur=}")    # Output: umur=20
```