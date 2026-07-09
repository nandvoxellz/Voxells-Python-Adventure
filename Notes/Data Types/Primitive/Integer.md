## Integer (int)
Tipe data integer digunakan untuk menyimpan bilangan bulat (tanpa desimal).

### 1. Arbitrary-Precision
Di bahasa pemrograman lain, integer punya batas maksimal (biasanya mentok di angka 2 miliar). Jika dipaksa menghitung lebih dari itu, program akan crash atau angkanya jadi minus — kejadian ini disebut **Integer Overflow**.

**Catatan penting:** Di Python, tidak ada batasan ukuran untuk integer. Batasannya hanya seberapa besar kapasitas RAM komputer yang digunakan.
```python
# Menghitung angka raksasa tidak akan membuat Python error
angka_raksasa = 9999999999999999999 ** 5
print("Aman!")   # Python bisa memproses ini dengan santai
```

### 2. Pemisah ribuan
Sejak Python 3.6, kita bisa menggunakan garis bawah atau underscore (`_`) sebagai pemisah ribuan agar kode jauh lebih mudah dibaca manusia. Komputer akan mengabaikan tanda `_` ini.
```python
# Sulit dibaca
gaji_karyawan = 15000000

# Cara modern (Pythonic)
gaji_karyawan = 15_000_000
anggaran_negara = 1_500_000_000_000

print(gaji_karyawan)   # Output yang keluar tetap: 15000000
```

### 3. Format sistem bilangan lain
Python memudahkan penulisan angka dalam sistem bilangan selain desimal (basis 10) dengan menggunakan awalan `0` (nol) diikuti huruf tertentu.
```python
# Biner / Binary (Basis 2) - menggunakan awalan '0b'
angka_biner = 0b1010
print(angka_biner)   # Output desimal: 10

# Oktal / Octal (Basis 8) - menggunakan awalan '0o'
angka_oktal = 0o12
print(angka_oktal)   # Output desimal: 10

# Hexadesimal / Hexadecimal (Basis 16) - menggunakan awalan '0x'
# (sering dipakai untuk kode warna atau memori)
angka_hex = 0xFF
print(angka_hex)     # Output desimal: 255
```