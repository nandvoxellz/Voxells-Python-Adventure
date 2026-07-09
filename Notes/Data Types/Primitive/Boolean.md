## Boolean
Boolean adalah tipe data di Python yang hanya memiliki dua kemungkinan nilai: `True` atau `False`. Boolean biasanya digunakan untuk merepresentasikan kondisi benar/salah, seperti hasil dari perbandingan atau logika.

### Catatan penting
Di Python, `True` dan `False` sebenarnya adalah bentuk khusus dari angka `1` dan `0`. Karena itu, boolean bisa dipakai dalam operasi matematika seperti angka biasa.
```python
True + True   # 2
False + 5     # 5
True == 1     # True
False == 0    # True
```

### 1. Membuat boolean
Boolean ditulis dengan huruf kapital di awal: `True` dan `False`.
```python
is_active: bool = True
is_logged_in: bool = False
```

### 2. Boolean dari hasil perbandingan
Operator perbandingan (`==`, `!=`, `>`, `<`, `>=`, `<=`) selalu menghasilkan nilai boolean.
```python
umur = 20
umur >= 18   # True
umur == 17   # False
```

### 3. Operator logika (and, or, not)
Digunakan untuk menggabungkan atau membalik nilai boolean.
```python
a = True
b = False

a and b   # False (keduanya harus True)
a or b    # True (salah satu True sudah cukup)
not a     # False (kebalikan dari a)
```

### 4. Truthy dan Falsy
Di Python, setiap nilai punya "nilai kebenaran" bawaan meskipun bukan boolean. Nilai yang dianggap **falsy** (setara `False`): `0`, `0.0`, `""`, `[]`, `{}`, `()`, dan `None`. Selain itu dianggap **truthy** (setara `True`).
```python
bool(0)        # False
bool("")       # False
bool([])       # False
bool("halo")   # True
bool(123)      # True
```

### 5. Fungsi bool()
Fungsi `bool()` digunakan untuk mengonversi nilai lain menjadi boolean, mengikuti aturan truthy/falsy di atas.
```python
bool(1)        # True
bool(0)        # False
bool("Dika")   # True
bool(None)     # False
```

### 6. Boolean dalam kondisi (if)
Boolean paling sering dipakai sebagai syarat dalam percabangan `if`.
```python
is_raining = True

if is_raining:
    print("Bawa payung")
else:
    print("Tidak perlu payung")
```