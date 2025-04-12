
# 📘 Day 3: Kondisional `if`, `elif`, `else`

Hari ini aku belajar tentang **percabangan logika** dalam Python, yaitu bagaimana sebuah program bisa membuat keputusan berdasarkan kondisi tertentu.

---

## 🧠 Konsep Dasar

### Struktur Dasar `if`
```python
if kondisi:
    # kode yang dijalankan jika kondisi True
```
---

### Dengan else
```python
if kondisi:
    # kode jika True
else:
    # kode jika False
```
---

### Dengan elif
```python
if kondisi1:
    # kode jika kondisi1 True
elif kondisi2:
    # kode jika kondisi2 True
else:
    # kode jika semua kondisi False
```
---

## 🔎 Contoh 1: Mengecek Bilangan Positif / Negatif
```python
angka = int(input("Masukkan angka: "))

if angka > 0:
    print("Angka positif")
elif angka < 0:
    print("Angka negatif")
else:
    print("Angka nol")
```
---

## 🔎 Contoh 2: Menentukan Kategori Umur
```python
umur = int(input("Masukkan umur kamu: "))

if umur < 13:
    print("Anak-anak")
elif umur < 18:
    print("Remaja")
elif umur < 60:
    print("Dewasa")
else:
    print("Lansia")
```
---

## 🔎 Contoh 3: Nilai Ujian
```python
nilai = int(input("Masukkan nilai kamu: "))

if nilai >= 90:
    print("A")
elif nilai >= 80:
    print("B")
elif nilai >= 70:
    print("C")
elif nilai >= 60:
    print("D")
else:
    print("E")
```
---

## 📝 Catatan Tambahan
- Gunakan indentasi (spasi/tab) yang konsisten di dalam blok `if`.
- Gunakan tanda titik dua `:` setelah kondisi untuk memulai blok kode.
- Kondisi juga bisa menggunakan operator logika seperti: `and`, `or`, `not` untuk memeriksa lebih dari satu kondisi dalam percabangan.

---

## ✅ Ringkasan
Hari ini aku belajar:
- Struktur percabangan `if`, `elif`, dan `else`.
- Menulis logika bercabang untuk menangani berbagai kondisi.
- Menangani input dari pengguna dengan `input()` dan membuat keputusan berdasarkan nilai yang dimasukkan.

---

> _“Python membuat logika menjadi mudah dan menyenangkan.”_
