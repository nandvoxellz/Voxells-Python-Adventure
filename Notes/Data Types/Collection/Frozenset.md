## Frozenset (`frozenset`)

`Frozenset` adalah versi **immutable** dari `set`. Semua sifat dan aturan set berlaku sama di sini (unordered, no duplicate, harus hashable), bedanya cuma satu: **tidak bisa diedit setelah dibuat**.

```python
warna = frozenset(["merah", "hijau", "biru"])
print(warna)   # Output: frozenset({'biru', 'hijau', 'merah'})
```

### Perbedaan dengan Set

| Sifat     | Set      | Frozenset |
|-----------|----------|-----------|
| Mutable   | ✅ True  | ❌ False  |
| Dibuat pakai | `set()` / `{}` | `frozenset()` |

```python
angka = frozenset([1, 2, 3])
angka.add(4)   # Error!
# Output: AttributeError: 'frozenset' object has no attribute 'add'
```

### Kenapa pakai Frozenset?

Karena immutable, frozenset bisa dipakai sebagai **key di dictionary** atau **elemen di dalam set lain** — hal yang tidak bisa dilakukan set biasa (karena set biasa gak hashable).

```python
data = {frozenset([1, 2]): "grup A"}
print(data)   # Output: {frozenset({1, 2}): 'grup A'}
```

Operasi himpunan (union, intersection, dll) tetap jalan normal seperti set biasa.

```python
a = frozenset([1, 2, 3])
b = frozenset([2, 3, 4])
print(a & b)   # Output: frozenset({2, 3})
```