# 📘 DAY 5: Fungsi & Modularisasi

```
╔════════════════════════════════════════════════════════════════╗
║           🐍 BELAJAR PYTHON DARI NOL - HARI KE-5              ║
║              FUNGSI & MODULARISASI PROGRAM                     ║
╚════════════════════════════════════════════════════════════════╝
```

Halo! Ini adalah dokumentasi hari kelima saya belajar Python. Hari ini saya belajar tentang **fungsi (function)** yang membantu kita membuat kode lebih rapi, terorganisir, dan bisa digunakan berulang kali. 🎯

---

## 📑 Daftar Isi

- [Apa itu Fungsi?](#-apa-itu-fungsi)
- [Fungsi Tanpa Parameter](#-1-fungsi-tanpa-parameter)
- [Fungsi dengan Parameter](#-2-fungsi-dengan-parameter)
- [Fungsi dengan Return Value](#-3-fungsi-dengan-return-value)
- [Default Parameter](#-4-default-parameter)
- [Multiple Return Values](#-5-multiple-return-values)
- [Modularisasi](#-modularisasi-kode)
- [Best Practices](#-best-practices)
- [Praktik Program](#-praktik-sistem-nilai-siswa)
- [Latihan Mandiri](#-latihan-mandiri)
- [Ringkasan](#-ringkasan)

---

## 🎯 Apa itu Fungsi?

Fungsi adalah blok kode yang dapat digunakan berulang kali tanpa harus menulis ulang kode yang sama.

### 🌟 Manfaat Fungsi:

| Manfaat | Penjelasan |
|---------|------------|
| **Reusability** | Gunakan kode yang sama berkali-kali |
| **Organization** | Kode lebih rapi dan terstruktur |
| **Debugging** | Lebih mudah mencari dan memperbaiki bug |
| **Collaboration** | Tim bisa kerja di fungsi berbeda |
| **Maintainability** | Mudah diupdate dan dipelihara |

---

### 💡 Struktur Dasar Fungsi

```python
def nama_fungsi(parameter):
    """Docstring: penjelasan fungsi"""
    # kode yang akan dijalankan
    return nilai  # opsional
```

**Penjelasan:**
- `def` → keyword untuk membuat fungsi
- `nama_fungsi` → nama fungsi (gunakan snake_case)
- `parameter` → input fungsi (opsional)
- `return` → output fungsi (opsional)

---

## 📘 1. Fungsi Tanpa Parameter

Fungsi paling sederhana tanpa parameter dan return value.

### 🔎 Contoh 1: Fungsi Sederhana

```python
def sapa():
    print("Halo! Selamat datang!")
    print("Semoga harimu menyenangkan!")

# Memanggil fungsi
sapa()
```

**💻 Output:**
```
Halo! Selamat datang!
Semoga harimu menyenangkan!
```

> **📝 Catatan:** Fungsi harus **dipanggil** dengan `()` agar dijalankan

---

### 🔎 Contoh 2: Fungsi untuk Menampilkan Menu

```python
def tampilkan_menu():
    print("=" * 30)
    print("      MENU UTAMA")
    print("=" * 30)
    print("1. Input Data")
    print("2. Lihat Data")
    print("3. Keluar")
    print("=" * 30)

# Memanggil fungsi
tampilkan_menu()
```

**💻 Output:**
```
==============================
      MENU UTAMA
==============================
1. Input Data
2. Lihat Data
3. Keluar
==============================
```

---

## 📘 2. Fungsi dengan Parameter

Fungsi yang menerima input (parameter) untuk diproses.

### 🔎 Contoh 3: Fungsi dengan Satu Parameter

```python
def sapa_nama(nama):
    print(f"Halo {nama}!")
    print("Senang bertemu denganmu!")

# Memanggil fungsi dengan argumen berbeda
sapa_nama("Agung")
sapa_nama("Budi")
sapa_nama("Sari")
```

**💻 Output:**
```
Halo Agung!
Senang bertemu denganmu!
Halo Budi!
Senang bertemu denganmu!
Halo Sari!
Senang bertemu denganmu!
```

---

### 🔎 Contoh 4: Fungsi dengan Multiple Parameters

```python
def perkenalan(nama, umur, kota):
    print(f"┌{'─' * 40}┐")
    print(f"│ Nama  : {nama:<30} │")
    print(f"│ Umur  : {umur:<30} │")
    print(f"│ Kota  : {kota:<30} │")
    print(f"└{'─' * 40}┘")

# Memanggil fungsi
perkenalan("Agung", 22, "Jakarta")
perkenalan("Sari", 20, "Bandung")
```

**💻 Output:**
```
┌────────────────────────────────────────┐
│ Nama  : Agung                          │
│ Umur  : 22                             │
│ Kota  : Jakarta                        │
└────────────────────────────────────────┘
┌────────────────────────────────────────┐
│ Nama  : Sari                           │
│ Umur  : 20                             │
│ Kota  : Bandung                        │
└────────────────────────────────────────┘
```

---

## 📘 3. Fungsi dengan Return Value

Fungsi yang mengembalikan nilai hasil pemrosesan.

### 🔎 Contoh 5: Fungsi Matematika

```python
def tambah(a, b):
    hasil = a + b
    return hasil

def kali(a, b):
    return a * b

def bagi(a, b):
    if b != 0:
        return a / b
    else:
        return "Error: Tidak bisa dibagi dengan nol!"

# Menggunakan fungsi
angka1 = 10
angka2 = 5

hasil_tambah = tambah(angka1, angka2)
hasil_kali = kali(angka1, angka2)
hasil_bagi = bagi(angka1, angka2)

print(f"{angka1} + {angka2} = {hasil_tambah}")
print(f"{angka1} × {angka2} = {hasil_kali}")
print(f"{angka1} ÷ {angka2} = {hasil_bagi}")
```

**💻 Output:**
```
10 + 5 = 15
10 × 5 = 50
10 ÷ 5 = 2.0
```

---

### 🔎 Contoh 6: Fungsi untuk Cek Bilangan Prima

```python
def cek_prima(angka):
    """Mengecek apakah angka adalah bilangan prima"""
    if angka < 2:
        return False
    
    for i in range(2, int(angka ** 0.5) + 1):
        if angka % i == 0:
            return False
    
    return True

# Testing fungsi
print("╔════════════════════════════════╗")
print("║   CEK BILANGAN PRIMA 1-20     ║")
print("╚════════════════════════════════╝")

for angka in range(1, 21):
    if cek_prima(angka):
        print(f"✅ {angka:2d} adalah bilangan prima")
    else:
        print(f"❌ {angka:2d} bukan bilangan prima")
```

**💻 Output:**
```
╔════════════════════════════════╗
║   CEK BILANGAN PRIMA 1-20     ║
╚════════════════════════════════╝
❌  1 bukan bilangan prima
✅  2 adalah bilangan prima
✅  3 adalah bilangan prima
❌  4 bukan bilangan prima
✅  5 adalah bilangan prima
...
```

---

## 📘 4. Default Parameter

Parameter dengan nilai default jika tidak diberikan argumen.

### 🔎 Contoh 7: Fungsi dengan Default Parameter

```python
def buat_profil(nama, umur, hobi="membaca", kota="Jakarta"):
    print(f"┌{'─' * 45}┐")
    print(f"│ {'PROFIL PENGGUNA':^43} │")
    print(f"├{'─' * 45}┤")
    print(f"│ Nama  : {nama:<35} │")
    print(f"│ Umur  : {umur:<35} │")
    print(f"│ Hobi  : {hobi:<35} │")
    print(f"│ Kota  : {kota:<35} │")
    print(f"└{'─' * 45}┘\n")

# Memanggil dengan semua parameter
buat_profil("Agung", 22, "coding", "Bandung")

# Memanggil dengan default parameter
buat_profil("Sari", 20)

# Memanggil dengan sebagian parameter
buat_profil("Budi", 23, hobi="gaming")
```

**💻 Output:**
```
┌─────────────────────────────────────────────┐
│              PROFIL PENGGUNA                │
├─────────────────────────────────────────────┤
│ Nama  : Agung                               │
│ Umur  : 22                                  │
│ Hobi  : coding                              │
│ Kota  : Bandung                             │
└─────────────────────────────────────────────┘

┌─────────────────────────────────────────────┐
│              PROFIL PENGGUNA                │
├─────────────────────────────────────────────┤
│ Nama  : Sari                                │
│ Umur  : 20                                  │
│ Hobi  : membaca                             │
│ Kota  : Jakarta                             │
└─────────────────────────────────────────────┘
```

---

## 📘 5. Multiple Return Values

Fungsi yang mengembalikan lebih dari satu nilai.

### 🔎 Contoh 8: Fungsi Statistik

```python
def hitung_statistik(angka_list):
    """Menghitung statistik dasar dari list angka"""
    total = sum(angka_list)
    rata_rata = total / len(angka_list)
    terbesar = max(angka_list)
    terkecil = min(angka_list)
    
    return total, rata_rata, terbesar, terkecil

# Menggunakan fungsi
nilai = [85, 90, 78, 92, 88, 76, 95]

total, rata, max_val, min_val = hitung_statistik(nilai)

print("╔════════════════════════════════╗")
print("║     STATISTIK NILAI SISWA     ║")
print("╚════════════════════════════════╝")
print(f"Data nilai    : {nilai}")
print(f"Total         : {total}")
print(f"Rata-rata     : {rata:.2f}")
print(f"Nilai tertinggi: {max_val}")
print(f"Nilai terendah : {min_val}")
```

**💻 Output:**
```
╔════════════════════════════════╗
║     STATISTIK NILAI SISWA     ║
╚════════════════════════════════╝
Data nilai    : [85, 90, 78, 92, 88, 76, 95]
Total         : 604
Rata-rata     : 86.29
Nilai tertinggi: 95
Nilai terendah : 76
```

---

### 🔎 Contoh 9: Fungsi Geometri

```python
def hitung_geometri(panjang, lebar):
    """Menghitung luas dan keliling persegi panjang"""
    luas = panjang * lebar
    keliling = 2 * (panjang + lebar)
    return luas, keliling

# Menggunakan fungsi
p, l = 8, 5
luas_persegi, keliling_persegi = hitung_geometri(p, l)

print(f"Persegi panjang {p} × {l} cm")
print(f"├─ Luas     : {luas_persegi} cm²")
print(f"└─ Keliling : {keliling_persegi} cm")
```

**💻 Output:**
```
Persegi panjang 8 × 5 cm
├─ Luas     : 40 cm²
└─ Keliling : 26 cm
```

---

## 📦 Modularisasi Kode

Memisahkan kode ke dalam file terpisah untuk organisasi yang lebih baik.

### 📄 File: `my_functions.py`

```python
"""
Module berisi fungsi-fungsi matematika dasar
"""

def tambah(a, b):
    """Menjumlahkan dua angka"""
    return a + b

def kurang(a, b):
    """Mengurangi dua angka"""
    return a - b

def kali(a, b):
    """Mengalikan dua angka"""
    return a * b

def bagi(a, b):
    """Membagi dua angka"""
    if b != 0:
        return a / b
    else:
        return "Error: Tidak bisa dibagi nol!"

def pangkat(a, b):
    """Memangkatkan angka a dengan b"""
    return a ** b
```

---

### 📄 File: `main.py`

```python
# Cara 1: Import seluruh module
import my_functions

hasil = my_functions.tambah(5, 3)
print(f"5 + 3 = {hasil}")

# Cara 2: Import fungsi spesifik
from my_functions import kali, bagi

hasil_kali = kali(4, 5)
hasil_bagi = bagi(10, 2)
print(f"4 × 5 = {hasil_kali}")
print(f"10 ÷ 2 = {hasil_bagi}")

# Cara 3: Import dengan alias
from my_functions import pangkat as power

hasil_pangkat = power(2, 3)
print(f"2³ = {hasil_pangkat}")

# Cara 4: Import semua (tidak disarankan)
# from my_functions import *
```

**💻 Output:**
```
5 + 3 = 8
4 × 5 = 20
10 ÷ 2 = 5.0
2³ = 8
```

---

## 🎯 Best Practices

### ✅ Menulis Fungsi yang Baik

```python
# ✅ BAIK: Nama deskriptif, single responsibility
def hitung_luas_lingkaran(jari_jari):
    """
    Menghitung luas lingkaran
    
    Args:
        jari_jari (float): Jari-jari lingkaran
        
    Returns:
        float: Luas lingkaran
    """
    pi = 3.14159
    return pi * jari_jari ** 2

# ❌ BURUK: Nama tidak jelas, multiple responsibility
def func(r):
    pi = 3.14
    luas = pi * r * r
    keliling = 2 * pi * r
    print(luas)
    print(keliling)
```

---

### 📋 Panduan Penamaan Fungsi

| ❌ Buruk | ✅ Baik | Alasan |
|----------|---------|--------|
| `f()` | `hitung_total()` | Lebih deskriptif |
| `getData()` | `get_data()` | Python style (snake_case) |
| `processInput()` | `validasi_input()` | Bahasa konsisten |
| `doStuff()` | `simpan_data()` | Jelaskan apa yang dilakukan |

---

### 📝 Docstring Best Practice

```python
def konversi_suhu(celsius, target="fahrenheit"):
    """
    Konversi suhu dari Celsius ke skala lain
    
    Parameters:
    -----------
    celsius : float
        Suhu dalam Celsius
    target : str, optional
        Skala target ('fahrenheit' atau 'kelvin')
        Default adalah 'fahrenheit'
    
    Returns:
    --------
    float
        Suhu dalam skala target
        
    Examples:
    ---------
    >>> konversi_suhu(0)
    32.0
    >>> konversi_suhu(100, 'kelvin')
    373.15
    
    Raises:
    -------
    ValueError
        Jika target bukan 'fahrenheit' atau 'kelvin'
    """
    if target == "fahrenheit":
        return (celsius * 9/5) + 32
    elif target == "kelvin":
        return celsius + 273.15
    else:
        raise ValueError("Target harus 'fahrenheit' atau 'kelvin'")
```

---

## 🧪 Praktik: Sistem Nilai Siswa

```python
def input_nilai():
    """Meminta input nilai dari user"""
    nama = input("Masukkan nama siswa: ")
    nilai = float(input("Masukkan nilai (0-100): "))
    return nama, nilai

def hitung_grade(nilai):
    """Menentukan grade berdasarkan nilai"""
    if nilai >= 90:
        return "A", "Excellent"
    elif nilai >= 80:
        return "B", "Very Good"
    elif nilai >= 70:
        return "C", "Good"
    elif nilai >= 60:
        return "D", "Fair"
    else:
        return "E", "Poor"

def tampilkan_laporan(data_siswa):
    """Menampilkan laporan nilai siswa"""
    print("\n" + "═" * 65)
    print(f"{'LAPORAN NILAI SISWA':^65}")
    print("═" * 65)
    print(f"{'No':<4} {'Nama':<20} {'Nilai':<10} {'Grade':<10} {'Predikat':<20}")
    print("─" * 65)
    
    for i, (nama, nilai) in enumerate(data_siswa, 1):
        grade, predikat = hitung_grade(nilai)
        print(f"{i:<4} {nama:<20} {nilai:<10.1f} {grade:<10} {predikat:<20}")
    
    print("═" * 65)
    
    # Hitung statistik
    if data_siswa:
        nilai_list = [nilai for _, nilai in data_siswa]
        rata = sum(nilai_list) / len(nilai_list)
        print(f"\nTotal siswa: {len(data_siswa)}")
        print(f"Rata-rata  : {rata:.2f}")
        print(f"Tertinggi  : {max(nilai_list):.1f}")
        print(f"Terendah   : {min(nilai_list):.1f}")

def main():
    """Fungsi utama program"""
    data_siswa = []
    
    while True:
        print("\n╔════════════════════════════════╗")
        print("║  SISTEM MANAJEMEN NILAI SISWA  ║")
        print("╚════════════════════════════════╝")
        print("1. Input nilai siswa")
        print("2. Tampilkan laporan")
        print("3. Keluar")
        
        pilihan = input("\nPilih menu (1-3): ")
        
        if pilihan == "1":
            try:
                nama, nilai = input_nilai()
                if 0 <= nilai <= 100:
                    data_siswa.append((nama, nilai))
                    print(f"✅ Data {nama} berhasil disimpan!")
                else:
                    print("❌ Nilai harus antara 0-100!")
            except ValueError:
                print("❌ Input tidak valid!")
                
        elif pilihan == "2":
            if data_siswa:
                tampilkan_laporan(data_siswa)
            else:
                print("❌ Belum ada data siswa!")
                
        elif pilihan == "3":
            print("\n✨ Terima kasih telah menggunakan program ini!")
            break
            
        else:
            print("❌ Pilihan tidak valid!")

# Jalankan program
if __name__ == "__main__":
    main()
```

---

## 🔍 Jenis-jenis Fungsi

### 1️⃣ Built-in Functions (Fungsi Bawaan Python)

```python
# Contoh fungsi bawaan Python
print("Fungsi Built-in:")
print(f"len([1,2,3]) = {len([1,2,3])}")
print(f"max([5,2,8]) = {max([5,2,8])}")
print(f"min([5,2,8]) = {min([5,2,8])}")
print(f"sum([1,2,3]) = {sum([1,2,3])}")
print(f"abs(-5) = {abs(-5)}")
print(f"round(3.14159, 2) = {round(3.14159, 2)}")
```

---

### 2️⃣ User-Defined Functions (Fungsi Buatan Sendiri)

```python
def kuadrat(x):
    """Menghitung kuadrat dari x"""
    return x ** 2

def faktorial(n):
    """Menghitung faktorial dari n"""
    if n == 0 or n == 1:
        return 1
    else:
        hasil = 1
        for i in range(2, n + 1):
            hasil *= i
        return hasil

print(f"kuadrat(5) = {kuadrat(5)}")
print(f"faktorial(5) = {faktorial(5)}")
```

---

### 3️⃣ Lambda Functions (Anonymous Functions)

```python
# Fungsi lambda: fungsi tanpa nama untuk operasi sederhana
kuadrat_lambda = lambda x: x ** 2
tambah_lambda = lambda a, b: a + b

print(f"kuadrat_lambda(5) = {kuadrat_lambda(5)}")
print(f"tambah_lambda(3, 7) = {tambah_lambda(3, 7)}")

# Sering digunakan dengan map, filter, sorted
angka = [1, 2, 3, 4, 5]
kuadrat_list = list(map(lambda x: x**2, angka))
print(f"Kuadrat dari {angka} = {kuadrat_list}")
```

---

## 🧪 Latihan Mandiri

Coba buat fungsi-fungsi berikut untuk latihan:

### 📝 Latihan 1: Kalkulator BMI
```
Buat fungsi untuk menghitung BMI (Body Mass Index)
- Input: berat (kg), tinggi (m)
- Return: BMI dan kategori (Kurus, Normal, Gemuk, Obesitas)
```

### 📝 Latihan 2: Validasi Email
```
Buat fungsi untuk validasi email
- Harus ada @ dan .
- Return True/False
```

### 📝 Latihan 3: Generator Password
```
Buat fungsi untuk generate password random
- Input: panjang password
- Return: password acak
```

### 📝 Latihan 4: Konverter Mata Uang
```
Buat fungsi konversi mata uang
- IDR ke USD, EUR, JPY, dst
- Input: jumlah dan mata uang tujuan
- Return: hasil konversi
```

### 📝 Latihan 5: Pembalik Kata
```
Buat fungsi untuk membalik kata/kalimat
- Input: "Python"
- Return: "nohtyP"
```

---

## ✅ Ringkasan

```
╔═══════════════════════════════════════════════════════════╗
║                📚 APA YANG SUDAH DIPELAJARI               ║
╚═══════════════════════════════════════════════════════════╝
```

Hari ini aku belajar:

- ✅ Membuat fungsi dengan keyword `def`
- ✅ Fungsi tanpa parameter dan dengan parameter
- ✅ Fungsi dengan return value
- ✅ Default parameter untuk nilai opsional
- ✅ Multiple return values (return tuple)
- ✅ Modularisasi dengan `import`
- ✅ Best practices menulis fungsi
- ✅ Docstring untuk dokumentasi
- ✅ Lambda functions untuk operasi sederhana
- ✅ Membuat program terstruktur dengan fungsi

---

## 🔗 Navigasi

- [⬅️ Day 4: Perulangan for-while](DAY4_Perulangan_ForWhile.md)
- [➡️ Day 6: Struktur Data - List, Tuple, Set](DAY6_Struktur_Data.md)
- [🏠 Kembali ke README](README.md)

---

## 💡 Tips Pro

```python
# 🌟 TIP 1: Gunakan *args untuk jumlah argumen tidak tentu
def jumlahkan(*angka):
    return sum(angka)

print(jumlahkan(1, 2, 3, 4, 5))  # 15

# 🌟 TIP 2: Gunakan **kwargs untuk keyword arguments
def info_user(**data):
    for key, value in data.items():
        print(f"{key}: {value}")

info_user(nama="Agung", umur=22, kota="Jakarta")

# 🌟 TIP 3: Function sebagai parameter (Higher-Order Function)
def operasi(func, a, b):
    return func(a, b)

print(operasi(lambda x, y: x + y, 5, 3))  # 8
```

---

## 📚 Referensi

- [Python Docs - Defining Functions](https://docs.python.org/3/tutorial/controlflow.html#defining-functions)
- [Python Docs - Default Argument Values](https://docs.python.org/3/tutorial/controlflow.html#default-argument-values)
- [PEP 257 - Docstring Conventions](https://peps.python.org/pep-0257/)

---

<div align="center">

```
┌─────────────────────────────────────────────────────────┐
│  🎯 "Fungsi membuat kode kita lebih rapi, mudah dibaca, │
│      dan bisa digunakan ulang!"                         │
└─────────────────────────────────────────────────────────┘
```

**🗓️ Day 5 Completed! ✨**

⭐ Jangan lupa beri bintang jika bermanfaat!

[⬆️ Kembali ke Atas](#-day-5-fungsi--modularisasi)

</div>

---

**Made with ❤️ by Agung**  
*Keep learning and keep coding!* 🚀
