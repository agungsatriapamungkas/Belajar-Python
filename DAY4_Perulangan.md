# 📘 DAY 4: Perulangan `for` dan `while`

```
╔════════════════════════════════════════════════════════════════╗
║           🐍 BELAJAR PYTHON DARI NOL - HARI KE-4              ║
║                   PERULANGAN (LOOPING)                         ║
╚════════════════════════════════════════════════════════════════╝
```

Halo! Ini adalah dokumentasi hari keempat saya belajar Python. Hari ini saya belajar tentang **perulangan (loop)** yang sangat penting untuk membuat program yang efisien. 🔄

---

## 📑 Daftar Isi

- [Apa itu Perulangan?](#-apa-itu-perulangan)
- [Perulangan FOR](#-1-perulangan-for)
- [Fungsi range()](#-fungsi-range)
- [Perulangan WHILE](#-2-perulangan-while)
- [Break dan Continue](#-perintah-kontrol-loop)
- [Praktik Program](#-praktik-program-tebak-angka)
- [Latihan Mandiri](#-latihan-mandiri)
- [Ringkasan](#-ringkasan)

---

## 🎯 Apa itu Perulangan?

Perulangan adalah cara untuk menjalankan kode yang sama berulang kali tanpa harus menulis kode yang sama berkali-kali. Python memiliki 2 jenis perulangan utama:

| Jenis | Digunakan Ketika | Contoh |
|-------|------------------|--------|
| **`for`** | Tahu berapa kali perulangan | Loop 1-10, loop list |
| **`while`** | Berdasarkan kondisi | Sampai user input benar |

---

## 📘 1. Perulangan `for`

### 💡 Konsep Dasar

Perulangan `for` digunakan ketika kita sudah tahu berapa kali perulangan akan dijalankan.

**Struktur:**
```python
for variabel in range(jumlah):
    # kode yang akan diulang
```

---

### 🔎 Contoh 1: For Loop Sederhana

```python
# Menampilkan angka 1 sampai 5
for i in range(1, 6):
    print("Angka:", i)
```

**💻 Output:**
```
Angka: 1
Angka: 2
Angka: 3
Angka: 4
Angka: 5
```

> **📝 Catatan:** `range(1, 6)` artinya dari 1 sampai 5 (6 tidak termasuk)

---

### 🔎 Contoh 2: For Loop dengan List

```python
# Menampilkan nama-nama buah
buah = ["apel", "jeruk", "mangga", "pisang"]

for nama_buah in buah:
    print("Buah favorit saya:", nama_buah)
```

**💻 Output:**
```
Buah favorit saya: apel
Buah favorit saya: jeruk
Buah favorit saya: mangga
Buah favorit saya: pisang
```

---

### 🔎 Contoh 3: Tabel Perkalian

```python
# Membuat tabel perkalian 2
angka = 2

print(f"Tabel perkalian {angka}:")
for i in range(1, 11):
    hasil = angka * i
    print(f"{angka} x {i} = {hasil}")
```

**💻 Output:**
```
Tabel perkalian 2:
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20
```

---

## 🎯 Fungsi `range()`

Fungsi `range()` sangat berguna untuk mengatur perulangan. Ada 3 cara menggunakannya:

### 📌 1. `range(stop)` - Dari 0 sampai stop-1

```python
for i in range(5):
    print(i)
```
**Output:** `0, 1, 2, 3, 4`

---

### 📌 2. `range(start, stop)` - Dari start sampai stop-1

```python
for i in range(2, 7):
    print(i)
```
**Output:** `2, 3, 4, 5, 6`

---

### 📌 3. `range(start, stop, step)` - Dengan langkah tertentu

```python
for i in range(0, 10, 2):
    print(i)
```
**Output:** `0, 2, 4, 6, 8`

---

### 🔄 Bonus: Range Mundur

```python
for i in range(10, 0, -1):
    print(i)
```
**Output:** `10, 9, 8, 7, 6, 5, 4, 3, 2, 1`

---

## 📘 2. Perulangan `while`

### 💡 Konsep Dasar

Perulangan `while` digunakan ketika perulangan bergantung pada kondisi tertentu.

**Struktur:**
```python
while kondisi:
    # kode yang akan diulang
    # jangan lupa ubah kondisi!
```

---

### 🔎 Contoh 4: While Loop Sederhana

```python
# Menghitung mundur dari 5 ke 1
angka = 5

while angka > 0:
    print("Hitung mundur:", angka)
    angka = angka - 1

print("Selesai!")
```

**💻 Output:**
```
Hitung mundur: 5
Hitung mundur: 4
Hitung mundur: 3
Hitung mundur: 2
Hitung mundur: 1
Selesai!
```

---

### 🔎 Contoh 5: Program Kalkulator dengan While

```python
# Program kalkulator sederhana
while True:
    print("\n=== Kalkulator Sederhana ===")
    print("1. Penjumlahan")
    print("2. Pengurangan")
    print("3. Keluar")
    
    pilihan = input("Pilih menu (1-3): ")
    
    if pilihan == "1":
        a = int(input("Masukkan angka pertama: "))
        b = int(input("Masukkan angka kedua: "))
        print("Hasil:", a + b)
    elif pilihan == "2":
        a = int(input("Masukkan angka pertama: "))
        b = int(input("Masukkan angka kedua: "))
        print("Hasil:", a - b)
    elif pilihan == "3":
        print("Terima kasih!")
        break
    else:
        print("Pilihan tidak valid!")
```

---

## ⚠️ Peringatan: Infinite Loop

> **BAHAYA!** Jangan buat loop tanpa akhir

```python
# ❌ JANGAN LAKUKAN INI!
# while True:
#     print("Loop tak berujung!")
```

**✅ Pastikan:**
- Ada kondisi yang bisa berubah menjadi `False`
- Atau gunakan `break` untuk keluar dari loop

---

## 🛑 Perintah Kontrol Loop

### 1️⃣ `break` - Keluar dari loop

```python
# Berhenti di angka 5
for i in range(10):
    if i == 5:
        break
    print(i)
```
**Output:** `0, 1, 2, 3, 4`

---

### 2️⃣ `continue` - Skip ke iterasi berikutnya

```python
# Lewati angka 2
for i in range(5):
    if i == 2:
        continue
    print(i)
```
**Output:** `0, 1, 3, 4`

---

### 📊 Perbandingan Break vs Continue

| Perintah | Fungsi | Contoh Penggunaan |
|----------|--------|-------------------|
| `break` | Keluar dari loop sepenuhnya | Ketika target sudah ditemukan |
| `continue` | Skip iterasi saat ini | Lewati data yang tidak valid |

---

## 🧪 Praktik: Program Tebak Angka

```python
import random

angka_rahasia = random.randint(1, 10)
percobaan = 0
max_percobaan = 3

print("╔════════════════════════════════╗")
print("║    🎮 GAME TEBAK ANGKA 🎮     ║")
print("╚════════════════════════════════╝")
print("Tebak angka antara 1-10!")
print(f"Kamu punya {max_percobaan} kesempatan!\n")

while percobaan < max_percobaan:
    try:
        tebakan = int(input(f"Percobaan {percobaan + 1}: "))
        
        if tebakan == angka_rahasia:
            print("🎉 Selamat! Tebakan kamu benar!")
            break
        elif tebakan < angka_rahasia:
            print("📈 Terlalu kecil!")
        else:
            print("📉 Terlalu besar!")
            
        percobaan += 1
        
    except ValueError:
        print("❌ Masukkan angka yang valid!")

if percobaan == max_percobaan:
    print(f"😞 Game Over! Angka rahasianya adalah {angka_rahasia}")
```

---

## 📝 Contoh Program Lainnya

### 📌 Menampilkan Bilangan Genap

```python
print("Bilangan genap 1-20:")
for i in range(1, 21):
    if i % 2 == 0:
        print(i, end=" ")
print()  # Newline
```
**Output:** `2 4 6 8 10 12 14 16 18 20`

---

### 📌 Hitung Jumlah dengan While

```python
jumlah = 0
angka = 1

while angka <= 10:
    jumlah += angka
    angka += 1

print(f"Jumlah 1-10 adalah: {jumlah}")
```
**Output:** `Jumlah 1-10 adalah: 55`

---

### 📌 Validasi Input

```python
while True:
    umur = input("Masukkan umur (harus angka): ")
    
    if umur.isdigit():
        print(f"✅ Umur kamu: {umur} tahun")
        break
    else:
        print("❌ Input tidak valid! Masukkan angka.")
```

---

### 📌 Menu Sederhana dengan Loop

```python
menu = ["Nasi Goreng", "Mie Goreng", "Ayam Bakar", "Sate"]

print("=== DAFTAR MENU ===")
for i, makanan in enumerate(menu, 1):
    print(f"{i}. {makanan}")
```
**Output:**
```
=== DAFTAR MENU ===
1. Nasi Goreng
2. Mie Goreng
3. Ayam Bakar
4. Sate
```

---

## 🔁 Catatan Penting

### ✅ Yang Perlu Diingat:

| Aspek | Penjelasan |
|-------|------------|
| **`for`** | Ketika tahu jumlah perulangan |
| **`while`** | Ketika perulangan tergantung kondisi |
| **`range()`** | Mengatur jumlah dan langkah perulangan |
| **`break`** | Keluar dari loop |
| **`continue`** | Skip iterasi saat ini |
| **Indentasi** | **WAJIB!** Gunakan 4 spasi atau tab |

---

### 🚨 Kesalahan Umum:

```python
# ❌ SALAH - Tidak ada indentasi
for i in range(5):
print(i)

# ✅ BENAR - Ada indentasi
for i in range(5):
    print(i)
```

```python
# ❌ SALAH - Lupa ubah kondisi while
x = 0
while x < 5:
    print(x)
    # Lupa x += 1 → infinite loop!

# ✅ BENAR
x = 0
while x < 5:
    print(x)
    x += 1
```

---

## 🧪 Latihan Mandiri

Coba buat program sederhana ini untuk latihan:

### 📝 Latihan 1: Program Daftar Nama
```
- Minta user input 5 nama
- Simpan dalam list
- Tampilkan semua nama dengan nomor urut
```

### 📝 Latihan 2: Hitung Total Belanja
```
- User input harga barang
- Loop sampai user ketik "selesai"
- Hitung total semua harga
```

### 📝 Latihan 3: Validasi Password
```
- User punya 3 kesempatan input password
- Password benar: "python123"
- Beri tahu jika benar atau salah
```

### 📝 Latihan 4: Piramida Bintang
```
Buat pola seperti ini:
*
**
***
****
*****
```

### 📝 Latihan 5: FizzBuzz
```
Print angka 1-20, tapi:
- Kelipatan 3 → print "Fizz"
- Kelipatan 5 → print "Buzz"  
- Kelipatan 3 dan 5 → print "FizzBuzz"
```

---

## ✅ Ringkasan

```
╔═══════════════════════════════════════════════════════════╗
║                    📚 APA YANG SUDAH DIPELAJARI           ║
╚═══════════════════════════════════════════════════════════╝
```

Hari ini aku belajar:

- ✅ Perulangan `for` untuk iterasi dengan jumlah yang sudah diketahui
- ✅ Perulangan `while` untuk iterasi berdasarkan kondisi
- ✅ Fungsi `range()` untuk mengatur rentang angka
- ✅ Perintah `break` dan `continue` untuk mengontrol alur perulangan
- ✅ Cara menghindari infinite loop
- ✅ Membuat program interaktif dengan perulangan
- ✅ Kombinasi loop dengan kondisional `if-elif-else`

---

## 🔗 Navigasi

- [⬅️ Day 3: Kondisional if-elif-else](DAY3_Kondisional_IfElse.md)
- [➡️ Day 5: Fungsi & Modularisasi](DAY5_Fungsi_Modularisasi.md)
- [🏠 Kembali ke README](README.md)

---

## 💡 Tips & Tricks

```python
# 🌟 TIP 1: Gunakan enumerate() untuk index dan value
buah = ["apel", "jeruk", "mangga"]
for index, nama in enumerate(buah):
    print(f"{index + 1}. {nama}")

# 🌟 TIP 2: Nested loop untuk pola
for i in range(5):
    for j in range(i + 1):
        print("*", end="")
    print()

# 🌟 TIP 3: List comprehension (akan dipelajari nanti)
kuadrat = [i**2 for i in range(1, 6)]
print(kuadrat)  # [1, 4, 9, 16, 25]
```

---

## 📚 Referensi

- [Python Docs - for statement](https://docs.python.org/3/tutorial/controlflow.html#for-statements)
- [Python Docs - while statement](https://docs.python.org/3/reference/compound_stmts.html#while)
- [Python Docs - range()](https://docs.python.org/3/library/stdtypes.html#range)

---

<div align="center">

```
┌─────────────────────────────────────────────────────────┐
│  🎯 "Dengan perulangan, kita bisa membuat program       │
│      yang lebih efisien dan powerful!"                  │
└─────────────────────────────────────────────────────────┘
```

**🗓️ Day 4 Completed! ✨**

⭐ Jangan lupa beri bintang jika bermanfaat!

[⬆️ Kembali ke Atas](#-day-4-perulangan-for-dan-while)

</div>

---

**Made with ❤️ by Agung**  
*Keep learning and keep coding!* 🚀
