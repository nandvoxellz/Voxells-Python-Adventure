## Apa Itu Syntax?
Syntax adalah aturan tata bahasa dalam pemrograman. Sama seperti bahasa manusia (Indonesia atau Inggris) yang punya aturan penyusunan kalimat agar bisa dipahami orang lain, bahasa pemrograman juga punya aturan penulisan agar instruksinya bisa dipahami oleh komputer.

### Catatan penting
Jika kamu salah mengetik atau melanggar aturan syntax, komputer akan kebingungan dan menolak menjalankan program. Kejadian ini disebut **Syntax Error**. Ini adalah hal yang sangat normal dan hampir semua programmer (termasuk yang sudah profesional) masih sering mengalaminya — bukan tanda kamu bodoh atau tidak berbakat.
```python
print("Hello, World")   # Ini akan berjalan lancar
```

### 1. String harus diapit tanda kutip
Setiap teks (string) wajib diapit tanda kutip (`'` atau `"`). Kalau tidak, Python akan mengira teks tersebut adalah nama variabel, bukan teks biasa.
```python
# BENAR - "Hello, World" diapit tanda kutip, dikenali sebagai teks
print("Hello, World")

# SALAH - Python mengira Hello dan World adalah nama variabel yang belum pernah dibuat
print(Hello, World)
# Output: NameError: name 'Hello' is not defined
```

### 2. Python peka huruf besar/kecil (case-sensitive)
Python menganggap huruf besar dan huruf kecil sebagai karakter yang berbeda. `Nama`, `nama`, dan `NAMA` dianggap sebagai tiga variabel yang berbeda.
```python
nama = "Dika"

print(Nama)   # SALAH - akan error, karena yang dibuat sebelumnya adalah 'nama' huruf kecil
print(nama)   # BENAR
```

### 3. Indentasi (spasi di awal baris) itu wajib, bukan sekadar rapi-rapi
Di banyak bahasa lain, spasi/indentasi hanya soal kerapian visual. Di Python, indentasi adalah bagian dari aturan syntax itu sendiri — dipakai untuk menandai kode mana yang "masuk" ke dalam suatu blok (misalnya di dalam `if`, `for`, atau fungsi).
```python
umur = 20

# BENAR - baris di dalam if diberi indentasi (biasanya 4 spasi)
if umur >= 18:
    print("Sudah dewasa")

# SALAH - tidak ada indentasi, akan menghasilkan IndentationError
if umur >= 18:
print("Sudah dewasa")
```

### 4. Tanda titik dua (`:`) menandai awal sebuah blok
Setiap kali membuka blok kode baru (`if`, `for`, `while`, fungsi, dan sejenisnya), baris tersebut harus diakhiri dengan tanda titik dua.
```python
# BENAR
if umur >= 18:
    print("Sudah dewasa")

# SALAH - lupa tanda titik dua, akan menghasilkan SyntaxError
if umur >= 18
    print("Sudah dewasa")
```

### 5. Tanda kurung harus berpasangan
Setiap tanda kurung buka `(`, `[`, atau `{` harus punya pasangan penutup yang sesuai. Ini kesalahan yang paling sering terjadi karena lupa menutup kurung, terutama pada kode yang panjang.
```python
# BENAR
print("Hello, World")

# SALAH - kurung penutup tertinggal
print("Hello, World"
```

### 6. Cara membaca pesan error
Ketika terjadi Syntax Error, Python biasanya sudah cukup membantu dengan menunjukkan lokasi kesalahan dan jenis errornya. Jangan takut membaca pesan error — biasanya jawabannya sudah ada di situ.
```python
print(Hello, World)
```