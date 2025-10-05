# 📘 DAY 3: Kondisional `if`, `elif`, `else`

```
╔════════════════════════════════════════════════════════════════╗
║           🐍 BELAJAR PYTHON DARI NOL - HARI KE-3              ║
║              PERCABANGAN & LOGIKA KONDISIONAL                  ║
╚════════════════════════════════════════════════════════════════╝
```

Halo! Ini adalah dokumentasi hari ketiga saya belajar Python. Hari ini saya belajar tentang **percabangan logika** dalam Python, yaitu bagaimana sebuah program bisa membuat keputusan berdasarkan kondisi tertentu. 🧠

---

## 📑 Daftar Isi

- [Apa itu Kondisional?](#-apa-itu-kondisional)
- [Struktur IF](#-1-struktur-if)
- [Struktur IF-ELSE](#-2-struktur-if-else)
- [Struktur IF-ELIF-ELSE](#-3-struktur-if-elif-else)
- [Operator Perbandingan](#-operator-perbandingan)
- [Operator Logika](#-operator-logika)
- [Nested IF](#-nested-if-bersarang)
- [Praktik Program](#-praktik-program-lengkap)
- [Latihan Mandiri](#-latihan-mandiri)
- [Ringkasan](#-ringkasan)

---

## 🎯 Apa itu Kondisional?

Kondisional adalah cara program membuat keputusan berdasarkan kondisi tertentu. Seperti dalam kehidupan sehari-hari:
- **Jika** hujan, **maka** bawa payung
- **Jika** lapar, **maka** makan
- **Jika** nilai >= 80, **maka** lulus

### 🌟 Kenapa Kondisional Penting?

| Manfaat | Penjelasan |
|---------|------------|
| **Decision Making** | Program bisa membuat keputusan |
| **Dynamic Behavior** | Program bereaksi sesuai situasi |
| **User Interaction** | Respon berbeda untuk input berbeda |
| **Error Handling** | Tangani kondisi yang tidak diinginkan |

---

## 📘 1. Struktur `if`

### 💡 Konsep Dasar

Struktur `if` digunakan untuk menjalankan kode **hanya jika** kondisi bernilai `True`.

**Struktur:**
```python
if kondisi:
    # kode yang dijalankan jika kondisi True
```

---

### 🔎 Contoh 1: IF Sederhana

```python
umur = 18

if umur >= 18:
    print("Anda sudah dewasa")
    print("Anda boleh memiliki SIM")
```

**💻 Output:**
```
Anda sudah dewasa
Anda boleh memiliki SIM
```

> **📝 Catatan:** Kode di dalam `if` **harus diindentasi** (4 spasi atau 1 tab)

---

### 🔎 Contoh 2: IF dengan Input User

```python
nilai = int(input("Masukkan nilai ujian: "))

if nilai >= 75:
    print("🎉 Selamat! Anda LULUS!")
    print("Nilai Anda:", nilai)
```

**💻 Output (jika input 80):**
```
Masukkan nilai ujian: 80
🎉 Selamat! Anda LULUS!
Nilai Anda: 80
```

---

## 📘 2. Struktur `if-else`

### 💡 Konsep Dasar

Struktur `if-else` memberikan pilihan: jika kondisi `True` jalankan blok pertama, jika `False` jalankan blok kedua.

**Struktur:**
```python
if kondisi:
    # kode jika True
else:
    # kode jika False
```

---

### 🔎 Contoh 3: Cek Bilangan Genap/Ganjil

```python
angka = int(input("Masukkan angka: "))

if angka % 2 == 0:
    print(f"{angka} adalah bilangan GENAP")
else:
    print(f"{angka} adalah bilangan GANJIL")
```

**💻 Output:**
```
Masukkan angka: 7
7 adalah bilangan GANJIL
```

---

### 🔎 Contoh 4: Login Sederhana

```python
password_benar = "python123"
password_input = input("Masukkan password: ")

if password_input == password_benar:
    print("✅ Login berhasil!")
    print("Selamat datang di sistem!")
else:
    print("❌ Password salah!")
    print("Akses ditolak.")
```

**💻 Output (password salah):**
```
Masukkan password: abc
❌ Password salah!
Akses ditolak.
```

---

## 📘 3. Struktur `if-elif-else`

### 💡 Konsep Dasar

Struktur `if-elif-else` digunakan untuk **multiple kondisi**. Python akan mengecek satu per satu dari atas ke bawah.

**Struktur:**
```python
if kondisi1:
    # kode jika kondisi1 True
elif kondisi2:
    # kode jika kondisi2 True
elif kondisi3:
    # kode jika kondisi3 True
else:
    # kode jika semua kondisi False
```

---

### 🔎 Contoh 5: Mengecek Bilangan Positif/Negatif/Nol

```python
angka = int(input("Masukkan angka: "))

if angka > 0:
    print(f"{angka} adalah bilangan POSITIF ➕")
elif angka < 0:
    print(f"{angka} adalah bilangan NEGATIF ➖")
else:
    print("Angka adalah NOL 0️⃣")
```

**💻 Output:**
```
Masukkan angka: -5
-5 adalah bilangan NEGATIF ➖
```

---

### 🔎 Contoh 6: Menentukan Kategori Umur

```python
umur = int(input("Masukkan umur kamu: "))

print("\n" + "═" * 40)
if umur < 0:
    print("❌ Umur tidak valid!")
elif umur < 13:
    print("👶 Kategori: ANAK-ANAK")
    print("   Rentang: 0-12 tahun")
elif umur < 18:
    print("🧒 Kategori: REMAJA")
    print("   Rentang: 13-17 tahun")
elif umur < 60:
    print("👨 Kategori: DEWASA")
    print("   Rentang: 18-59 tahun")
else:
    print("👴 Kategori: LANSIA")
    print("   Rentang: 60+ tahun")
print("═" * 40)
```

**💻 Output:**
```
Masukkan umur kamu: 25

========================================
👨 Kategori: DEWASA
   Rentang: 18-59 tahun
========================================
```

---

### 🔎 Contoh 7: Sistem Grading Nilai

```python
nilai = int(input("Masukkan nilai kamu (0-100): "))

print("\n" + "╔" + "═" * 38 + "╗")
print("║     📊 HASIL PENILAIAN UJIAN        ║")
print("╚" + "═" * 38 + "╝")

if nilai > 100 or nilai < 0:
    print("❌ Nilai tidak valid! (Harus 0-100)")
elif nilai >= 90:
    print(f"Nilai: {nilai} → Grade: A 🌟")
    print("Predikat: EXCELLENT")
elif nilai >= 80:
    print(f"Nilai: {nilai} → Grade: B ⭐")
    print("Predikat: VERY GOOD")
elif nilai >= 70:
    print(f"Nilai: {nilai} → Grade: C ✨")
    print("Predikat: GOOD")
elif nilai >= 60:
    print(f"Nilai: {nilai} → Grade: D 💫")
    print("Predikat: FAIR")
else:
    print(f"Nilai: {nilai} → Grade: E ❌")
    print("Predikat: NEED IMPROVEMENT")
```

**💻 Output:**
```
Masukkan nilai kamu (0-100): 85

╔══════════════════════════════════════╗
║     📊 HASIL PENILAIAN UJIAN        ║
╚══════════════════════════════════════╝
Nilai: 85 → Grade: B ⭐
Predikat: VERY GOOD
```

---

## 🔍 Operator Perbandingan

Operator yang digunakan untuk membandingkan dua nilai:

| Operator | Arti | Contoh | Hasil |
|----------|------|--------|-------|
| `==` | Sama dengan | `5 == 5` | `True` |
| `!=` | Tidak sama dengan | `5 != 3` | `True` |
| `>` | Lebih besar | `7 > 5` | `True` |
| `<` | Lebih kecil | `3 < 5` | `True` |
| `>=` | Lebih besar atau sama | `5 >= 5` | `True` |
| `<=` | Lebih kecil atau sama | `4 <= 5` | `True` |

### 📝 Contoh Penggunaan:

```python
a = 10
b = 5

print(f"{a} == {b} → {a == b}")  # False
print(f"{a} != {b} → {a != b}")  # True
print(f"{a} > {b} → {a > b}")    # True
print(f"{a} < {b} → {a < b}")    # False
print(f"{a} >= {b} → {a >= b}")  # True
print(f"{a} <= {b} → {a <= b}")  # False
```

---

## 🔗 Operator Logika

Operator untuk menggabungkan beberapa kondisi:

| Operator | Arti | Contoh | Hasil |
|----------|------|--------|-------|
| `and` | Dan (semua harus True) | `True and True` | `True` |
| `or` | Atau (salah satu True) | `True or False` | `True` |
| `not` | Negasi (kebalikan) | `not True` | `False` |

---

### 🔎 Contoh 8: Operator AND

```python
umur = int(input("Masukkan umur: "))
punya_sim = input("Punya SIM? (ya/tidak): ").lower()

if umur >= 17 and punya_sim == "ya":
    print("✅ Anda boleh menyetir mobil!")
else:
    print("❌ Anda belum boleh menyetir mobil!")
    if umur < 17:
        print("   Alasan: Umur belum cukup")
    if punya_sim != "ya":
        print("   Alasan: Belum punya SIM")
```

**💻 Output:**
```
Masukkan umur: 18
Punya SIM? (ya/tidak): tidak
❌ Anda belum boleh menyetir mobil!
   Alasan: Belum punya SIM
```

---

### 🔎 Contoh 9: Operator OR

```python
hari = input("Masukkan hari: ").lower()

if hari == "sabtu" or hari == "minggu":
    print("🎉 Hari ini WEEKEND!")
    print("Waktunya istirahat dan have fun!")
else:
    print("💼 Hari ini hari kerja/sekolah")
    print("Semangat beraktivitas!")
```

**💻 Output:**
```
Masukkan hari: sabtu
🎉 Hari ini WEEKEND!
Waktunya istirahat dan have fun!
```

---

### 🔎 Contoh 10: Operator NOT

```python
sedang_hujan = False

if not sedang_hujan:
    print("☀️ Cuaca cerah!")
    print("Aman untuk pergi keluar")
else:
    print("🌧️ Sedang hujan!")
    print("Jangan lupa bawa payung")
```

**💻 Output:**
```
☀️ Cuaca cerah!
Aman untuk pergi keluar
```

---

## 🏗️ Nested IF (Bersarang)

IF di dalam IF untuk kondisi yang lebih kompleks.

### 🔎 Contoh 11: Cek Kelulusan Lengkap

```python
nama = input("Masukkan nama: ")
nilai_teori = int(input("Nilai teori (0-100): "))
nilai_praktik = int(input("Nilai praktik (0-100): "))
kehadiran = int(input("Persentase kehadiran (%): "))

print("\n" + "╔" + "═" * 48 + "╗")
print(f"║  📋 HASIL EVALUASI - {nama.upper():^28} ║")
print("╚" + "═" * 48 + "╝\n")

if kehadiran >= 75:
    print(f"✅ Kehadiran: {kehadiran}% (Memenuhi syarat)")
    
    if nilai_teori >= 70 and nilai_praktik >= 70:
        rata_rata = (nilai_teori + nilai_praktik) / 2
        print(f"✅ Nilai Teori: {nilai_teori}")
        print(f"✅ Nilai Praktik: {nilai_praktik}")
        print(f"📊 Rata-rata: {rata_rata:.1f}")
        
        if rata_rata >= 85:
            print("\n🌟 STATUS: LULUS DENGAN PUJIAN")
        else:
            print("\n🎉 STATUS: LULUS")
    else:
        print(f"❌ Nilai Teori: {nilai_teori}")
        print(f"❌ Nilai Praktik: {nilai_praktik}")
        print("\n❌ STATUS: TIDAK LULUS (Nilai kurang)")
else:
    print(f"❌ Kehadiran: {kehadiran}% (Tidak memenuhi)")
    print("\n❌ STATUS: TIDAK LULUS (Kehadiran kurang)")
```

**💻 Output:**
```
Masukkan nama: Agung
Nilai teori (0-100): 88
Nilai praktik (0-100): 90
Persentase kehadiran (%): 95

╔════════════════════════════════════════════════╗
║  📋 HASIL EVALUASI -          AGUNG           ║
╚════════════════════════════════════════════════╝

✅ Kehadiran: 95% (Memenuhi syarat)
✅ Nilai Teori: 88
✅ Nilai Praktik: 90
📊 Rata-rata: 89.0

🌟 STATUS: LULUS DENGAN PUJIAN
```

---

## 🧪 Praktik: Program Lengkap

### 🎮 Program Kalkulator Diskon

```python
print("╔" + "═" * 50 + "╗")
print("║" + " " * 15 + "🛒 KALKULATOR DISKON" + " " * 15 + "║")
print("╚" + "═" * 50 + "╝\n")

# Input data
nama_produk = input("Nama produk: ")
harga = float(input("Harga produk (Rp): "))
member = input("Apakah Anda member? (ya/tidak): ").lower()
jumlah = int(input("Jumlah beli: "))

# Hitung total awal
total_awal = harga * jumlah
diskon_persen = 0
diskon_rupiah = 0

# Tentukan diskon
if member == "ya":
    diskon_persen = 10
    print("\n✨ Anda mendapat diskon member 10%")
    
    if jumlah >= 5:
        diskon_persen = 20
        print("🎉 BONUS! Diskon naik jadi 20% karena beli >= 5 item")
else:
    if jumlah >= 10:
        diskon_persen = 15
        print("\n🎁 Anda mendapat diskon 15% karena beli >= 10 item")
    elif jumlah >= 5:
        diskon_persen = 10
        print("\n🎁 Anda mendapat diskon 10% karena beli >= 5 item")

# Hitung diskon dan total akhir
diskon_rupiah = total_awal * (diskon_persen / 100)
total_akhir = total_awal - diskon_rupiah

# Tampilkan struk
print("\n" + "═" * 52)
print(f"{'STRUK PEMBELIAN':^52}")
print("═" * 52)
print(f"Produk      : {nama_produk}")
print(f"Harga satuan: Rp {harga:,.0f}")
print(f"Jumlah      : {jumlah} item")
print(f"Status      : {'Member ⭐' if member == 'ya' else 'Non-Member'}")
print("-" * 52)
print(f"Subtotal    : Rp {total_awal:,.0f}")
print(f"Diskon ({diskon_persen}%): - Rp {diskon_rupiah:,.0f}")
print("-" * 52)
print(f"TOTAL BAYAR : Rp {total_akhir:,.0f}")
print("═" * 52)
print(f"Hemat       : Rp {diskon_rupiah:,.0f} 💰")
print("═" * 52)
```

**💻 Output:**
```
╔══════════════════════════════════════════════════╗
║               🛒 KALKULATOR DISKON               ║
╚══════════════════════════════════════════════════╝

Nama produk: Buku Python
Harga produk (Rp): 50000
Apakah Anda member? (ya/tidak): ya
Jumlah beli: 6

✨ Anda mendapat diskon member 10%
🎉 BONUS! Diskon naik jadi 20% karena beli >= 5 item

════════════════════════════════════════════════════
                 STRUK PEMBELIAN
════════════════════════════════════════════════════
Produk      : Buku Python
Harga satuan: Rp 50,000
Jumlah      : 6 item
Status      : Member ⭐
────────────────────────────────────────────────────
Subtotal    : Rp 300,000
Diskon (20%): - Rp 60,000
────────────────────────────────────────────────────
TOTAL BAYAR : Rp 240,000
════════════════════════════════════════════════════
Hemat       : Rp 60,000 💰
════════════════════════════════════════════════════
```

---

## 📝 Catatan Penting

### ✅ Yang Perlu Diingat:

| Aspek | Penjelasan |
|-------|------------|
| **Indentasi** | **WAJIB!** Gunakan 4 spasi atau 1 tab konsisten |
| **Titik dua `:`** | Selalu gunakan `:` setelah kondisi |
| **Operator** | `==` untuk perbandingan, `=` untuk assignment |
| **Boolean** | Kondisi menghasilkan `True` atau `False` |
| **Urutan** | Python cek kondisi dari atas ke bawah |

---

### 🚨 Kesalahan Umum:

```python
# ❌ SALAH - Lupa indentasi
if nilai >= 80:
print("Lulus")

# ✅ BENAR
if nilai >= 80:
    print("Lulus")

# ❌ SALAH - Lupa titik dua
if nilai >= 80
    print("Lulus")

# ✅ BENAR
if nilai >= 80:
    print("Lulus")

# ❌ SALAH - Gunakan = untuk perbandingan
if nilai = 80:
    print("Lulus")

# ✅ BENAR - Gunakan ==
if nilai == 80:
    print("Lulus")
```

---

## 🧪 Latihan Mandiri

Coba buat program berikut untuk latihan:

### 📝 Latihan 1: Cek Tahun Kabisat
```
Input: tahun
Output: "Tahun kabisat" atau "Bukan tahun kabisat"
Syarat kabisat: habis dibagi 4, kecuali kelipatan 100 (kecuali kelipatan 400)
```

### 📝 Latihan 2: Kalkulator BMI
```
Input: berat (kg), tinggi (m)
Hitung BMI dan kategori:
- < 18.5: Kurus
- 18.5-24.9: Normal
- 25-29.9: Gemuk
- >= 30: Obesitas
```

### 📝 Latihan 3: Validasi Username & Password
```
Buat sistem login sederhana
- Username minimal 5 karakter
- Password minimal 8 karakter
- Tampilkan pesan sesuai kesalahan
```

### 📝 Latihan 4: Konversi Nilai ke Huruf
```
Input: nilai angka
Output: 
- 85-100: Sangat Baik
- 70-84: Baik
- 55-69: Cukup
- 40-54: Kurang
- 0-39: Sangat Kurang
```

### 📝 Latihan 5: Sistem Parkir
```
Input: jenis kendaraan, lama parkir (jam)
Tarif:
- Motor: Rp 2000/jam
- Mobil: Rp 5000/jam
Diskon 50% jika parkir > 5 jam
```

---

## ✅ Ringkasan

```
╔═══════════════════════════════════════════════════════════╗
║                📚 APA YANG SUDAH DIPELAJARI               ║
╚═══════════════════════════════════════════════════════════╝
```

Hari ini aku belajar:

- ✅ Struktur percabangan `if`, `elif`, dan `else`
- ✅ Operator perbandingan (`==`, `!=`, `>`, `<`, `>=`, `<=`)
- ✅ Operator logika (`and`, `or`, `not`)
- ✅ Nested IF untuk kondisi kompleks
- ✅ Menangani input dari pengguna dengan `input()`
- ✅ Membuat keputusan berdasarkan kondisi
- ✅ Membuat program interaktif dengan kondisional

---

## 🔗 Navigasi

- [⬅️ Day 2: Operasi Matematika](DAY2_Operasi_Matematika.md)
- [➡️ Day 4: Perulangan for-while](DAY4_Perulangan_ForWhile.md)
- [🏠 Kembali ke README](README.md)

---

## 💡 Tips Pro

```python
# 🌟 TIP 1: Gunakan ternary operator untuk kondisi sederhana
umur = 20
status = "Dewasa" if umur >= 18 else "Anak-anak"
print(status)

# 🌟 TIP 2: Gunakan in untuk cek multiple nilai
hari = "sabtu"
if hari in ["sabtu", "minggu"]:
    print("Weekend!")

# 🌟 TIP 3: Cek tipe data dengan isinstance()
nilai = "80"
if isinstance(nilai, int):
    print("Nilai adalah integer")
else:
    print("Nilai bukan integer")
```

---

## 📚 Referensi

- [Python Docs - if Statements](https://docs.python.org/3/tutorial/controlflow.html#if-statements)
- [Python Docs - Boolean Operations](https://docs.python.org/3/library/stdtypes.html#boolean-operations-and-or-not)
- [Python Docs - Comparisons](https://docs.python.org/3/library/stdtypes.html#comparisons)

---

<div align="center">

```
┌─────────────────────────────────────────────────────────┐
│  🎯 "Python membuat logika menjadi mudah dan            │
│      menyenangkan!"                                     │
└─────────────────────────────────────────────────────────┘
```

**🗓️ Day 3 Completed! ✨**

⭐ Jangan lupa beri bintang jika bermanfaat!

[⬆️ Kembali ke Atas](#-day-3-kondisional-if-elif-else)

</div>

---

**Made with ❤️ by Agung**  
*Keep learning and keep coding!* 🚀
