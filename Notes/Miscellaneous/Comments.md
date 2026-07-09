## Apa Itu Comments?
Comments adalah catatan di dalam kode yang diabaikan oleh komputer saat program dijalankan. Ini sangat berguna untuk meninggalkan jejak penjelasan bagi dirimu sendiri atau programmer lain di masa depan.

### 1. Komentar satu baris
Python menggunakan tanda pagar (`#`) untuk komentar satu baris. Semua teks setelah `#` di baris tersebut akan diabaikan oleh Python.
```python
# Ini adalah contoh komentar
print("Hello, World")   # <- kode ini akan tetap dieksekusi
```

### 2. Komentar banyak baris
Python sebenarnya tidak punya syntax khusus untuk komentar multi-baris seperti bahasa lain (`/* ... */`). Cara paling umum adalah menambahkan `#` di setiap baris, atau memanfaatkan triple-quote string (`"""..."""`) yang tidak diberi variabel penampung.

**Catatan penting:** Triple-quote yang dipakai sebagai "komentar" ini sebenarnya tetap dianggap string oleh Python, bukan komentar sungguhan — hanya kebetulan diabaikan kalau tidak disimpan ke variabel atau tidak berada di posisi docstring.
```python
# Ini baris komentar pertama
# Ini baris komentar kedua
# Ini baris komentar ketiga

"""
Ini juga sering dipakai sebagai
komentar banyak baris
"""
```

### 3. Shortcut komentar di VS Code
VS Code menyediakan shortcut untuk mengubah baris kode yang sedang diseleksi menjadi komentar (atau sebaliknya), tanpa perlu menambahkan `#` secara manual.

| Shortcut | OS |
|---|---|
| `Ctrl + /` | Windows / Linux |
| `Cmd + /` | macOS |

Shortcut ini bisa dipakai untuk satu baris maupun banyak baris sekaligus (blok kode yang diseleksi).

### 4. Kapan sebaiknya menulis komentar
Komentar paling berguna untuk menjelaskan **kenapa** sebuah kode ditulis seperti itu, bukan sekadar mengulang apa yang sudah jelas terlihat dari kodenya.
```python
# Kurang berguna, cuma mengulang yang sudah jelas
umur = 20   # mengisi variabel umur dengan angka 20

# Lebih berguna, menjelaskan alasan di baliknya
umur = 20   # syarat minimal usia untuk registrasi akun
```