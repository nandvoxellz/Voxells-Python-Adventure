## Apa Itu Type Annotations?
Secara ringkas, Type Annotation adalah cara kita memberi tahu Python (dan sesama programmer) tentang jenis data apa yang seharusnya digunakan dalam suatu variabel, argumen fungsi, atau nilai kembalian fungsi.

### Catatan penting
Python bersifat **Dynamically Typed**, artinya secara bawaan Python akan menebak tipe data secara otomatis. Type Annotation tidak mengubah sifat ini — ia hanya memberikan "petunjuk resmi" secara tertulis, bukan aturan yang dipaksakan.
```python
nama: str = 12345   # Ini TIDAK akan error saat dijalankan!
# Python tetap menjalankannya, tapi IDE/text editor akan memberi peringatan
# karena isinya (int) tidak sesuai dengan anotasi (str)
```

**Catatan penting:** Sama seperti constant yang cuma konvensi penamaan, Type Annotation juga hanya "janji" ke sesama programmer — Python sendiri tidak benar-benar memaksakannya saat program dijalankan. Manfaat utamanya terasa lewat bantuan IDE (peringatan otomatis) dan kode yang lebih mudah dibaca orang lain.

### 1. Anotasi pada variabel dasar
Syntax-nya sangat mudah: cukup tambahkan titik dua (`:`) diikuti tipe datanya setelah nama variabel, sebelum tanda sama dengan (`=`).
```python
nama: str = "Dika"        # str = String (Teks)
umur: int = 20             # int = Integer (Angka bulat)
tinggi: float = 165.5      # float = Angka desimal
is_active: bool = True     # bool = Boolean (Benar/Salah)
```

### 2. Anotasi pada fungsi
Kita bisa menentukan tipe data untuk parameter yang masuk, dan tipe data untuk hasil akhir (return value) dari fungsi tersebut. Untuk menentukan tipe data kembalian, gunakan tanda panah kecil (`->`) sebelum titik dua di akhir definisi fungsi.
```python
# Fungsi menerima string dan mengembalikan string
def sapa_pengguna(nama: str) -> str:
    return f"Halo {nama}, selamat belajar koding!"

# Fungsi menerima dua angka bulat dan mengembalikan angka bulat
def tambah_angka(a: int, b: int) -> int:
    return a + b

pesan = sapa_pengguna("Miwa")
total = tambah_angka(5, 10)
```

### 3. Anotasi untuk tipe data kompleks
Untuk tipe data koleksi seperti List atau Dictionary, sejak Python 3.9 kita bisa langsung menuliskannya dengan huruf kecil dan menggunakan tanda kurung siku `[]` untuk menentukan tipe data di dalamnya.
```python
# List yang seluruh isinya HARUS berupa angka bulat (int)
daftar_nilai: list[int] = [80, 90, 75, 100]

# Dictionary dengan Key berupa string dan Value berupa angka bulat
stok_buah: dict[str, int] = {
    "Apel": 10,
    "Jeruk": 5
}
```