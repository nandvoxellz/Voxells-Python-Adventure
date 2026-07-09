## Apa Itu Data Types
Data types adalah klasifikasi yang menentukan jenis nilai yang disimpan di dalam sebuah variabel. Secara umum, tipe data di Python terbagi menjadi dua kategori utama: **Tipe Data Dasar (Primitif)** untuk menyimpan nilai tunggal, dan **Tipe Data Koleksi** untuk menyimpan banyak nilai sekaligus.

### Catatan penting
Python bersifat **Dynamically Typed**, artinya kamu tidak perlu menuliskan tipe data secara manual — Python akan menebaknya secara otomatis berdasarkan nilai yang diberikan.
```python
umur = 20        # otomatis dikenali sebagai int
nama = "Dika"     # otomatis dikenali sebagai str
```

## 1. Tipe Data Dasar (Primitif)
Ini adalah tipe data yang paling sering digunakan sehari-hari, masing-masing hanya menyimpan satu nilai tunggal.

### 1.1 Integer (int)
Digunakan untuk menyimpan bilangan bulat, baik positif maupun negatif, tanpa angka desimal.
```python
umur = 20
jumlah_barang = 255
ketinggian = 128
```

### 1.2 Float (float)
Digunakan untuk menyimpan bilangan desimal atau pecahan.

**Catatan penting:** Python (dan standar pemrograman internasional) menggunakan tanda titik (`.`) untuk desimal, bukan tanda koma (`,`).
```python
berat_badan = 56.69
tinggi_badan = 169.67
suhu = 27.5
```

### 1.3 String (str)
Digunakan untuk menyimpan teks atau kumpulan karakter. Nilai string selalu diapit tanda kutip tunggal (`'`) atau ganda (`"`).

**Catatan penting:** Tanda kutip pembuka dan penutup harus sejenis — kalau dibuka dengan `'`, harus ditutup dengan `'` juga, begitu pula dengan `"`. Kalau teksnya sendiri mengandung tanda kutip, gunakan jenis kutip lain untuk membungkusnya, atau tambahkan escape character (`\`) di depannya.
```python
nama = "Dika"
pesan = "Aku suka Markdown"

# Kutip berbeda untuk membungkus kutip di dalam teks
kata = "Miwa bilang 'aku juga mau'"

# Atau pakai escape character kalau terpaksa pakai kutip sejenis
kata = "Miwa bilang \"aku juga mau\""
```

### 1.4 Boolean (bool)
Digunakan untuk merepresentasikan nilai kebenaran logika. Hanya memiliki dua kemungkinan nilai: Benar atau Salah.

**Catatan penting:** Penulisan di Python bersifat case-sensitive, sehingga harus menggunakan huruf kapital di awal: `True` atau `False`.
```python
suka_python = True
punya_pasangan = False
```

## 2. Tipe Data Koleksi
Digunakan ketika kamu butuh menyimpan lebih dari satu nilai di dalam satu variabel tunggal.

| Tipe | Simbol | Berurutan? | Bisa diubah (mutable)? | Boleh duplikat? |
|---|---|---|---|---|
| List | `[]` | Ya | Ya | Ya |
| Tuple | `()` | Ya | Tidak | Ya |
| Dictionary | `{key: value}` | Ya (sejak Python 3.7+) | Ya | Key tidak boleh, value boleh |
| Set | `{}` | Tidak | Ya | Tidak |

### 2.1 List (list)
Kumpulan data yang berurutan dan bisa diubah (mutable) setelah dibuat. Ditandai dengan tanda kurung siku `[]`. Ini adalah tipe data koleksi yang paling sering dipakai.
```python
hobi = ["Membaca", "Koding", "Gaming"]

# Nilainya bisa diubah setelah dibuat
hobi[0] = "Jalan-jalan"
```

### 2.2 Tuple (tuple)
Mirip seperti List, tetapi tidak bisa diubah (immutable) setelah dibuat. Ditandai dengan tanda kurung biasa `()`. Sangat cocok untuk menyimpan data yang sifatnya permanen/tetap.
```python
koordinat_lokasi = (10.5, 20.1)
# koordinat_lokasi[0] = 11.0  <-- Ini akan menghasilkan TypeError!
```

### 2.3 Dictionary (dict)
Kumpulan data yang disimpan dalam format pasangan Kunci dan Nilai (Key-Value). Ditandai dengan tanda kurung kurawal `{}`.
```python
profil_user = {
    "nama": "Dika",
    "umur": 20,
    "role": "Admin"
}

# Cara memanggil nilainya menggunakan kuncinya
print(profil_user["nama"])   # Output: Dika
```

### 2.4 Set (set)
Kumpulan data yang unik (tidak boleh ada nilai duplikat) dan tidak berurutan. Ditandai dengan kurung kurawal `{}`, tapi tanpa pasangan kunci seperti Dictionary.
```python
angka_unik = {1, 2, 3, 3, 3, 4}
print(angka_unik)   # Output: {1, 2, 3, 4} (angka 3 yang ganda otomatis dihapus)
```

## 3. Cara Mengecek Tipe Data
Python menyediakan fungsi bawaan `type()` untuk mengecek tipe data suatu nilai — berguna terutama saat membaca kode orang lain atau mengolah data yang sumbernya tidak diketahui.
```python
data_misterius = "123"
data_lain = 123

print(type(data_misterius))   # Output: <class 'str'> (karena ada tanda kutip)
print(type(data_lain))        # Output: <class 'int'> (angka bulat asli)
```