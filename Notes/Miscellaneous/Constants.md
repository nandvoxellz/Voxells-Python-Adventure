## Apa Itu Constants?
Konstanta adalah "variabel" yang nilainya dirancang agar tetap dan tidak boleh diubah sepanjang program berjalan. Biasanya dipakai untuk nilai yang sudah pasti dan tidak seharusnya berubah, seperti nilai matematika, batas maksimal, atau pengaturan tetap dalam program.

### 1. Python tidak punya constant sungguhan
Berbeda dengan beberapa bahasa lain yang punya syntax khusus untuk mengunci nilai (misalnya `const` atau `final`), Python **tidak memiliki mekanisme bawaan** untuk benar-benar mencegah sebuah nilai diubah.

**Catatan penting:** Karena tidak ada penguncian sungguhan, secara teknis Python tetap mengizinkan nilai "konstanta" untuk diubah tanpa error. Aman secara syntax, tapi salah secara konsep.
```python
PI = 3.14159

# Ini tidak akan menghasilkan error sama sekali...
PI = 3
# ...tapi ini melanggar tujuan awal dibuatnya PI sebagai nilai tetap.
```

### 2. Konvensi penamaan: UPPERCASE
Karena tidak ada aturan teknis, komunitas Python sepakat menggunakan sebuah **konvensi**: tulis nama variabel dengan huruf kapital semua (UPPERCASE) untuk menandakan bahwa nilai tersebut dimaksudkan sebagai konstanta dan tidak boleh diubah.
```python
PI = 3.14159
MAKSIMAL_PENGGUNA = 100
GRAVITASI = 9.8
```

**Catatan penting:** Ini murni penanda visual untuk sesama programmer, bukan perintah untuk Python. Nama variabel biasa yang ditulis kapital pun tetap bisa diubah nilainya kapan saja — Python tidak memberi perlakuan khusus apa pun terhadap penulisan UPPERCASE.

### 3. Kenapa konvensi ini tetap penting
Meskipun tidak dipaksakan secara teknis, mengikuti konvensi ini tetap penting karena:
- Programmer lain (atau dirimu sendiri di masa depan) akan langsung tahu nilai tersebut tidak boleh diubah, tanpa perlu membaca ulang seluruh kode.
- Mengurangi risiko bug akibat nilai penting yang tidak sengaja tertimpa di tengah program.
```python
# Salah — mengubah nilai yang seharusnya tetap tanpa sadar
MAKSIMAL_PENGGUNA = 100
# ...ratusan baris kode kemudian...
MAKSIMAL_PENGGUNA = 50   # Oops, ini bisa merusak logika program lain yang bergantung pada nilai 100
```