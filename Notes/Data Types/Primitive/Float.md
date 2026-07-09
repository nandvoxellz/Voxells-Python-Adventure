## Float
Float (kependekan dari floating-point) digunakan untuk menyimpan angka yang memiliki nilai desimal atau pecahan.

### 1. Aturan penulisan
Di bahasa Indonesia kita terbiasa menggunakan koma (`,`) untuk desimal, tetapi dalam standar pemrograman global (termasuk Python), wajib menggunakan titik (`.`).

**Catatan penting:** Kalau menulis desimal pakai koma, Python malah akan membacanya sebagai tipe data Tuple, bukan Float.
```python
# Penulisan yang BENAR
berat_badan = 65.5
suhu = -2.5

# Penulisan yang SALAH (ini malah dianggap Tuple, bukan Float!)
# berat_badan = 65,5
```

### 2. Notasi ilmiah
Jika berurusan dengan angka desimal yang sangat besar atau sangat kecil (biasanya di perhitungan sains/data), Python mendukung penulisan menggunakan huruf `e` atau `E` yang merepresentasikan "dikali 10 pangkat...".
```python
# Jarak bumi ke matahari (1.5 dikali 10 pangkat 8)
jarak_bumi_matahari = 1.5e8
print(jarak_bumi_matahari)   # Output: 150000000.0

# Ukuran bakteri yang sangat kecil (2.5 dikali 10 pangkat minus 4)
ukuran_bakteri = 2.5e-4
print(ukuran_bakteri)        # Output: 0.00025
```

### 3. Masalah presisi pada float
Coba perhatikan operasi matematika sederhana ini: `0.1 + 0.2`. Secara logika manusia, hasilnya pasti `0.3`. Tapi begini hasilnya di Python:
```python
hasil = 0.1 + 0.2
print(hasil)
# Output: 0.30000000000000004  <-- Lho, dari mana datangnya angka di belakang?!
```

**Catatan penting:** Ini bukan bug atau error di Python. Komputer memproses semua data dalam bentuk biner (0 dan 1), dan beberapa angka desimal (seperti 0.1 atau 0.2) tidak bisa diterjemahkan secara sempurna ke biner murni, sehingga muncul sisa presisi yang sangat kecil. Ini terjadi di hampir semua bahasa pemrograman, bukan cuma Python.

**Cara mengatasinya:** gunakan fungsi bawaan `round()` untuk membulatkan angka sesuai jumlah desimal yang diinginkan.
```python
hasil = 0.1 + 0.2

# Membulatkan hasil ke 1 angka di belakang koma
hasil_akurat = round(hasil, 1)
print(hasil_akurat)   # Output: 0.3 (sekarang sudah benar!)
```

### 4. Infinity & NaN
Terkadang kamu butuh angka untuk merepresentasikan nilai yang tidak terbatas atau bukan sebuah angka sama sekali. Python menyediakannya lewat float.
```python
# Infinity (Tak Terhingga) - berguna untuk logika pencarian nilai terkecil/terbesar
batas_atas = float('inf')
batas_bawah = float('-inf')

print(1000000 < batas_atas)   # Output: True (karena tak terhingga selalu lebih besar)

# NaN (Not a Number) - biasanya muncul kalau ada data yang hilang/rusak saat analisis data
data_rusak = float('nan')
```