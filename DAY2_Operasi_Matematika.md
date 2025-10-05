# 📘 DAY 2: Operasi Matematika di Python

```
╔════════════════════════════════════════════════════════════════╗
║           🐍 BELAJAR PYTHON DARI NOL - HARI KE-2              ║
║                 OPERASI MATEMATIKA DASAR                       ║
╚════════════════════════════════════════════════════════════════╝
```

Halo! Ini adalah dokumentasi hari kedua saya belajar Python. Hari ini saya belajar mengenai **operasi matematika dasar** di Python. Operasi ini sangat penting karena sering digunakan dalam berbagai perhitungan di program. 🧮

---

## 📑 Daftar Isi

- [Operator Matematika Dasar](#-operator-matematika-dasar)
- [Contoh Penggunaan](#-contoh-penggunaan-operator)
- [Urutan Operasi](#-urutan-operasi-prioritas)
- [Operasi dengan Variabel](#-operasi-dengan-variabel)
- [Operasi Assignment](#-operasi-assignment-shorthand)
- [Fungsi Matematika Built-in](#-fungsi-matematika-built-in)
- [Praktik Program](#-praktik-program-kalkulator)
- [Latihan Mandiri](#-latihan-mandiri)
- [Ringkasan](#-ringkasan)

---

## ✨ Operator Matematika Dasar

Python memiliki 7 operator matematika dasar yang perlu kita kuasai:

| Operator | Simbol | Contoh | Hasil | Keterangan |
|----------|--------|--------|-------|------------|
| **Penjumlahan** | `+` | `5 + 3` | `8` | Menjumlahkan dua nilai |
| **Pengurangan** | `-` | `10 - 2` | `8` | Mengurangi dua nilai |
| **Perkalian** | `*` | `4 * 2` | `8` | Mengalikan dua nilai |
| **Pembagian** | `/` | `8 / 2` | `4.0` | Membagi (hasil float) |
| **Pembagian Bulat** | `//` | `7 // 2` | `3` | Pembagian (hasil integer) |
| **Modulus** | `%` | `10 % 3` | `1` | Sisa hasil pembagian |
| **Pangkat** | `**` | `2 ** 3` | `8` | Perpangkatan |

> **📝 Catatan:** Pembagian `/` selalu menghasilkan float (desimal), sedangkan `//` menghasilkan integer (bulat)

---

## 🧪 Contoh Penggunaan Operator

### 🔎 Contoh 1: Semua Operator Dasar

```python
# Mendefinisikan variabel
a = 10
b = 3

print("=" * 40)
print("  OPERASI MATEMATIKA DENGAN a=10, b=3")
print("=" * 40)

# Penjumlahan
print(f"Penjumlahan      : {a} + {b} = {a + b}")

# Pengurangan
print(f"Pengurangan      : {a} - {b} = {a - b}")

# Perkalian
print(f"Perkalian        : {a} * {b} = {a * b}")

# Pembagian
print(f"Pembagian        : {a} / {b} = {a / b:.2f}")

# Pembagian Bulat
print(f"Pembagian Bulat  : {a} // {b} = {a // b}")

# Modulus
print(f"Modulus          : {a} % {b} = {a % b}")

# Pangkat
print(f"Pangkat          : {a} ** {b} = {a ** b}")

print("=" * 40)
```

**💻 Output:**
```
========================================
  OPERASI MATEMATIKA DENGAN a=10, b=3
========================================
Penjumlahan      : 10 + 3 = 13
Pengurangan      : 10 - 3 = 7
Perkalian        : 10 * 3 = 30
Pembagian        : 10 / 3 = 3.33
Pembagian Bulat  : 10 // 3 = 3
Modulus          : 10 % 3 = 1
Pangkat          : 10 ** 3 = 1000
========================================
```

---

### 🔎 Contoh 2: Penjumlahan - Addition (`+`)

```python
# Penjumlahan angka
angka1 = 5
angka2 = 3
hasil = angka1 + angka2

print(f"{angka1} + {angka2} = {hasil}")

# Penjumlahan langsung
print(f"10 + 5 = {10 + 5}")

# Penjumlahan banyak angka
total = 1 + 2 + 3 + 4 + 5
print(f"1 + 2 + 3 + 4 + 5 = {total}")

# Penjumlahan dengan float
harga1 = 10.5
harga2 = 5.75
total_harga = harga1 + harga2
print(f"Rp {harga1} + Rp {harga2} = Rp {total_harga}")
```

**💻 Output:**
```
5 + 3 = 8
10 + 5 = 15
1 + 2 + 3 + 4 + 5 = 15
Rp 10.5 + Rp 5.75 = Rp 16.25
```

---

### 🔎 Contoh 3: Pengurangan - Subtraction (`-`)

```python
# Pengurangan sederhana
saldo = 100000
belanja = 35000
sisa = saldo - belanja

print(f"Saldo awal   : Rp {saldo:,}")
print(f"Belanja      : Rp {belanja:,}")
print(f"Sisa saldo   : Rp {sisa:,}")

# Angka negatif
suhu_pagi = 25
penurunan = 10
suhu_malam = suhu_pagi - penurunan
print(f"\nSuhu pagi: {suhu_pagi}°C")
print(f"Suhu malam: {suhu_malam}°C")
```

**💻 Output:**
```
Saldo awal   : Rp 100,000
Belanja      : Rp 35,000
Sisa saldo   : Rp 65,000

Suhu pagi: 25°C
Suhu malam: 15°C
```

---

### 🔎 Contoh 4: Perkalian - Multiplication (`*`)

```python
# Hitung total harga
harga_satuan = 15000
jumlah_beli = 4
total = harga_satuan * jumlah_beli

print(f"Harga satuan : Rp {harga_satuan:,}")
print(f"Jumlah beli  : {jumlah_beli} item")
print(f"Total bayar  : Rp {total:,}")

# Perkalian untuk luas
panjang = 8
lebar = 5
luas = panjang * lebar
print(f"\nLuas persegi panjang {panjang}m × {lebar}m = {luas}m²")

# String multiplication (bonus!)
print("\n" + "=" * 30)
print("*" * 10)
```

**💻 Output:**
```
Harga satuan : Rp 15,000
Jumlah beli  : 4 item
Total bayar  : Rp 60,000

Luas persegi panjang 8m × 5m = 40m²

==============================
**********
```

---

### 🔎 Contoh 5: Pembagian - Division (`/` dan `//`)

```python
# Pembagian biasa (/)
kue = 10
orang = 3

bagian_per_orang = kue / orang
print(f"{kue} kue dibagi {orang} orang = {bagian_per_orang:.2f} kue/orang")

# Pembagian bulat (//)
bagian_bulat = kue // orang
print(f"Bagian bulat = {bagian_bulat} kue/orang")

sisa_kue = kue % orang
print(f"Sisa kue = {sisa_kue} kue")

print("\n" + "─" * 40)

# Contoh lain
jarak = 100  # km
waktu = 3    # jam
kecepatan = jarak / waktu
print(f"Kecepatan: {jarak}km ÷ {waktu}jam = {kecepatan:.2f} km/jam")
```

**💻 Output:**
```
10 kue dibagi 3 orang = 3.33 kue/orang
Bagian bulat = 3 kue/orang
Sisa kue = 1 kue

────────────────────────────────────────
Kecepatan: 100km ÷ 3jam = 33.33 km/jam
```

---

### 🔎 Contoh 6: Modulus - Remainder (`%`)

```python
# Cek bilangan genap atau ganjil
angka = 7

if angka % 2 == 0:
    print(f"{angka} adalah bilangan GENAP")
else:
    print(f"{angka} adalah bilangan GANJIL")

# Konversi detik ke jam, menit, detik
total_detik = 3665

jam = total_detik // 3600
sisa = total_detik % 3600
menit = sisa // 60
detik = sisa % 60

print(f"\n{total_detik} detik = {jam} jam, {menit} menit, {detik} detik")

# Cek kelipatan
angka = 15
if angka % 5 == 0:
    print(f"\n{angka} adalah kelipatan 5")
```

**💻 Output:**
```
7 adalah bilangan GANJIL

3665 detik = 1 jam, 1 menit, 5 detik

15 adalah kelipatan 5
```

---

### 🔎 Contoh 7: Pangkat - Exponentiation (`**`)

```python
# Perpangkatan sederhana
print("TABEL PERPANGKATAN 2")
print("=" * 30)
for i in range(1, 11):
    hasil = 2 ** i
    print(f"2^{i:2d} = {hasil:5d}")

print("\n" + "=" * 30)

# Hitung luas lingkaran
jari_jari = 7
pi = 3.14159
luas = pi * jari_jari ** 2
print(f"Luas lingkaran r={jari_jari}cm: {luas:.2f} cm²")

# Akar kuadrat (pangkat 0.5)
angka = 16
akar = angka ** 0.5
print(f"\n√{angka} = {akar}")
```

**💻 Output:**
```
TABEL PERPANGKATAN 2
==============================
2^ 1 =     2
2^ 2 =     4
2^ 3 =     8
2^ 4 =    16
2^ 5 =    32
2^ 6 =    64
2^ 7 =   128
2^ 8 =   256
2^ 9 =   512
2^10 =  1024

==============================
Luas lingkaran r=7cm: 153.94 cm²

√16 = 4.0
```

---

## 🔢 Urutan Operasi (Prioritas)

Python mengikuti aturan matematika **PEMDAS**:

| Prioritas | Operator | Nama | Contoh |
|-----------|----------|------|--------|
| 1 | `()` | Kurung | `(2 + 3)` |
| 2 | `**` | Pangkat | `2 ** 3` |
| 3 | `*`, `/`, `//`, `%` | Kali, Bagi | `2 * 3` |
| 4 | `+`, `-` | Tambah, Kurang | `2 + 3` |

### 🔎 Contoh 8: Urutan Operasi

```python
# Tanpa kurung
hasil1 = 2 + 3 * 4
print(f"2 + 3 * 4 = {hasil1}")  # 14, bukan 20!

# Dengan kurung
hasil2 = (2 + 3) * 4
print(f"(2 + 3) * 4 = {hasil2}")  # 20

# Kompleks
hasil3 = 10 + 5 * 2 ** 3 / 4 - 1
print(f"10 + 5 * 2 ** 3 / 4 - 1 = {hasil3}")

# Step by step
print("\nStep by step:")
print(f"1. 2 ** 3 = {2 ** 3}")
print(f"2. 5 * 8 = {5 * 8}")
print(f"3. 40 / 4 = {40 / 4}")
print(f"4. 10 + 10 = {10 + 10}")
print(f"5. 20 - 1 = {20 - 1}")
```

**💻 Output:**
```
2 + 3 * 4 = 14
(2 + 3) * 4 = 20
10 + 5 * 2 ** 3 / 4 - 1 = 19.0

Step by step:
1. 2 ** 3 = 8
2. 5 * 8 = 40
3. 40 / 4 = 10.0
4. 10 + 10 = 20.0
5. 20 - 1 = 19.0
```

---

## 💾 Operasi dengan Variabel

### 🔎 Contoh 9: Kalkulasi dengan Variabel

```python
# Data belanja
nama_barang = "Buku Python"
harga = 50000
jumlah = 3
pajak_persen = 10

# Hitung
subtotal = harga * jumlah
pajak = subtotal * pajak_persen / 100
total = subtotal + pajak

# Tampilkan
print("╔" + "═" * 48 + "╗")
print("║" + f"{'STRUK PEMBELIAN':^48}" + "║")
print("╠" + "═" * 48 + "╣")
print(f"║ Barang: {nama_barang:<38} ║")
print(f"║ Harga : Rp {harga:>7,} × {jumlah} item{' ' * 17}║")
print("╠" + "─" * 48 + "╣")
print(f"║ Subtotal : Rp {subtotal:>28,} ║")
print(f"║ Pajak {pajak_persen}%: Rp {pajak:>28,.0f} ║")
print("╠" + "═" * 48 + "╣")
print(f"║ TOTAL    : Rp {total:>28,.0f} ║")
print("╚" + "═" * 48 + "╝")
```

**💻 Output:**
```
╔════════════════════════════════════════════════╗
║              STRUK PEMBELIAN                   ║
╠════════════════════════════════════════════════╣
║ Barang: Buku Python                            ║
║ Harga : Rp  50,000 × 3 item                    ║
╠────────────────────────────────────────────────╣
║ Subtotal : Rp                          150,000 ║
║ Pajak 10%: Rp                           15,000 ║
╠════════════════════════════════════════════════╣
║ TOTAL    : Rp                          165,000 ║
╚════════════════════════════════════════════════╝
```

---

## ⚡ Operasi Assignment (Shorthand)

Cara singkat untuk operasi matematika dengan variabel itu sendiri:

| Operator | Contoh | Setara dengan | Hasil |
|----------|--------|---------------|-------|
| `+=` | `x += 5` | `x = x + 5` | Tambah lalu assign |
| `-=` | `x -= 3` | `x = x - 3` | Kurang lalu assign |
| `*=` | `x *= 2` | `x = x * 2` | Kali lalu assign |
| `/=` | `x /= 4` | `x = x / 4` | Bagi lalu assign |
| `//=` | `x //= 3` | `x = x // 3` | Bagi bulat lalu assign |
| `%=` | `x %= 2` | `x = x % 2` | Modulus lalu assign |
| `**=` | `x **= 2` | `x = x ** 2` | Pangkat lalu assign |

### 🔎 Contoh 10: Assignment Operators

```python
# Contoh dengan saldo
saldo = 100000
print(f"Saldo awal: Rp {saldo:,}")

# Tambah saldo (deposit)
saldo += 50000
print(f"Setelah deposit Rp 50,000: Rp {saldo:,}")

# Kurangi saldo (penarikan)
saldo -= 30000
print(f"Setelah tarik Rp 30,000: Rp {saldo:,}")

# Bonus 10%
saldo *= 1.1
print(f"Setelah bonus 10%: Rp {saldo:,.0f}")

print("\n" + "=" * 40)

# Counter sederhana
counter = 0
print(f"Counter: {counter}")

counter += 1
print(f"Setelah counter += 1: {counter}")

counter += 1
print(f"Setelah counter += 1: {counter}")

counter *= 2
print(f"Setelah counter *= 2: {counter}")
```

**💻 Output:**
```
Saldo awal: Rp 100,000
Setelah deposit Rp 50,000: Rp 150,000
Setelah tarik Rp 30,000: Rp 120,000
Setelah bonus 10%: Rp 132,000

========================================
Counter: 0
Setelah counter += 1: 1
Setelah counter += 1: 2
Setelah counter *= 2: 4
```

---

## 📐 Fungsi Matematika Built-in

Python memiliki fungsi bawaan untuk operasi matematika:

| Fungsi | Kegunaan | Contoh | Hasil |
|--------|----------|--------|-------|
| `abs()` | Nilai absolut | `abs(-5)` | `5` |
| `round()` | Pembulatan | `round(3.7)` | `4` |
| `pow()` | Perpangkatan | `pow(2, 3)` | `8` |
| `max()` | Nilai terbesar | `max(1,5,3)` | `5` |
| `min()` | Nilai terkecil | `min(1,5,3)` | `1` |
| `sum()` | Jumlah list | `sum([1,2,3])` | `6` |

### 🔎 Contoh 11: Fungsi Matematika

```python
# Nilai absolut
suhu = -5
print(f"Suhu: {suhu}°C")
print(f"Suhu absolut: {abs(suhu)}°C")

print("\n" + "─" * 40)

# Pembulatan
harga = 15750.75
print(f"Harga asli: Rp {harga}")
print(f"Dibulatkan: Rp {round(harga)}")
print(f"1 desimal: Rp {round(harga, 1)}")
print(f"2 desimal: Rp {round(harga, 2)}")

print("\n" + "─" * 40)

# Max dan Min
nilai_siswa = [85, 92, 78, 95, 88]
print(f"Nilai siswa: {nilai_siswa}")
print(f"Nilai tertinggi: {max(nilai_siswa)}")
print(f"Nilai terendah: {min(nilai_siswa)}")
print(f"Total nilai: {sum(nilai_siswa)}")
print(f"Rata-rata: {sum(nilai_siswa) / len(nilai_siswa):.2f}")
```

**💻 Output:**
```
Suhu: -5°C
Suhu absolut: 5°C

────────────────────────────────────────
Harga asli: Rp 15750.75
Dibulatkan: Rp 15751
1 desimal: Rp 15750.8
2 desimal: Rp 15750.75

────────────────────────────────────────
Nilai siswa: [85, 92, 78, 95, 88]
Nilai tertinggi: 95
Nilai terendah: 78
Total nilai: 438
Rata-rata: 87.60
```

---

## 🧪 Praktik: Program Kalkulator

```python
print("╔" + "═" * 50 + "╗")
print("║" + " " * 15 + "🔢 KALKULATOR PYTHON" + " " * 15 + "║")
print("╚" + "═" * 50 + "╝\n")

# Input angka
angka1 = float(input("Masukkan angka pertama: "))
operator = input("Masukkan operator (+, -, *, /, //, %, **): ")
angka2 = float(input("Masukkan angka kedua: "))

# Proses kalkulasi
if operator == "+":
    hasil = angka1 + angka2
    operasi = "Penjumlahan"
elif operator == "-":
    hasil = angka1 - angka2
    operasi = "Pengurangan"
elif operator == "*":
    hasil = angka1 * angka2
    operasi = "Perkalian"
elif operator == "/":
    if angka2 != 0:
        hasil = angka1 / angka2
        operasi = "Pembagian"
    else:
        hasil = "Error"
        operasi = "Pembagian (tidak bisa dibagi nol!)"
elif operator == "//":
    if angka2 != 0:
        hasil = angka1 // angka2
        operasi = "Pembagian Bulat"
    else:
        hasil = "Error"
        operasi = "Pembagian Bulat (tidak bisa dibagi nol!)"
elif operator == "%":
    hasil = angka1 % angka2
    operasi = "Modulus"
elif operator == "**":
    hasil = angka1 ** angka2
    operasi = "Pangkat"
else:
    hasil = "Error"
    operasi = "Operator tidak valid"

# Tampilkan hasil
print("\n" + "═" * 52)
print(f"{operasi:^52}")
print("═" * 52)
print(f"{angka1} {operator} {angka2} = {hasil}")
print("═" * 52)
```

**💻 Output:**
```
╔══════════════════════════════════════════════════╗
║               🔢 KALKULATOR PYTHON               ║
╚══════════════════════════════════════════════════╝

Masukkan angka pertama: 15
Masukkan operator (+, -, *, /, //, %, **): *
Masukkan angka kedua: 4

====================================================
                    Perkalian
====================================================
15.0 * 4.0 = 60.0
====================================================
```

---

## 🧪 Latihan Mandiri

Coba buat program berikut untuk latihan:

### 📝 Latihan 1: Konversi Suhu
```
Buat program konversi suhu
- Celsius ke Fahrenheit: (C × 9/5) + 32
- Celsius ke Kelvin: C + 273.15
```

### 📝 Latihan 2: Hitung Luas & Keliling
```
Input: panjang dan lebar
Hitung dan tampilkan:
- Luas persegi panjang
- Keliling persegi panjang
```

### 📝 Latihan 3: Kalkulator BMI
```
Input: berat (kg), tinggi (m)
Hitung: BMI = berat / (tinggi ** 2)
Tampilkan hasil BMI
```

### 📝 Latihan 4: Hitung Diskon
```
Input: harga barang, persen diskon
Hitung:
- Jumlah diskon
- Harga setelah diskon
```

### 📝 Latihan 5: Konversi Waktu
```
Input: jumlah detik
Konversi ke: jam, menit, detik
Contoh: 3665 detik = 1 jam 1 menit 5 detik
```

---

## ✅ Ringkasan

```
╔═══════════════════════════════════════════════════════════╗
║                📚 APA YANG SUDAH DIPELAJARI               ║
╚═══════════════════════════════════════════════════════════╝
```

Hari ini aku belajar:

- ✅ 7 operator matematika dasar (+, -, *, /, //, %, **)
- ✅ Perbedaan `/` (pembagian float) dan `//` (pembagian bulat)
- ✅ Modulus `%` untuk sisa pembagian
- ✅ Pangkat `**` untuk perpangkatan
- ✅ Urutan operasi (PEMDAS)
- ✅ Assignment operators (+=, -=, *=, dll)
- ✅ Fungsi matematika built-in (abs, round, max, min, sum)
- ✅ Membuat program kalkulator sederhana

---

## 🔗 Navigasi

- [⬅️ Day 1: Instalasi & Tipe Data](DAY1_Python.md)
- [➡️ Day 3: Kondisional if-elif-else](DAY3_Kondisional_IfElse.md)
- [🏠 Kembali ke README](README.md)

---

## 💡 Tips Pro

```python
# 🌟 TIP 1: Gunakan underscore untuk angka besar agar mudah dibaca
jumlah = 1_000_000  # Sama dengan 1000000
print(jumlah)

# 🌟 TIP 2: Pembagian dengan pembulatan ke atas
import math
hasil = math.ceil(10 / 3)  # 4 (dibulatkan ke atas)

# 🌟 TIP 3: Format angka dengan koma
harga = 1500000
print(f"Rp {harga:,}")  # Rp 1,500,000
```

---

## 📚 Referensi

- [Python Docs - Numeric Types](https://docs.python.org/3/library/stdtypes.html#numeric-types-int-float-complex)
- [Python Docs - Built-in Functions](https://docs.python.org/3/library/functions.html)
- [Python Docs - Math Module](https://docs.python.org/3/library/math.html)

---

<div align="center">

```
┌─────────────────────────────────────────────────────────┐
│  🎯 "Matematika adalah fondasi dari programming.        │
│      Kuasai operasi dasar, kuasai Python!"             │
└─────────────────────────────────────────────────────────┘
```

**🗓️ Day 2 Completed! ✨**

⭐ Jangan lupa beri bintang jika bermanfaat!

[⬆️ Kembali ke Atas](#-day-2-operasi-matematika-di-python)

</div>

---

**Made with ❤️ by Agung**  
*Keep learning and keep coding!* 🚀
