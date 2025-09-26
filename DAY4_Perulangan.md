📄 DAY4_Perulangan.md
# 📘 Day 4: Perulangan `for` dan `while`

Hari ini saya belajar tentang **perulangan (loop)** di Python. Dengan perulangan, kita bisa menjalankan kode **berulang kali** tanpa harus menulisnya berulang-ulang.

---

## 🔁 Perulangan `for`
Digunakan untuk mengulang sesuatu dengan jumlah yang sudah jelas.

```python
for i in range(5):
    print("Perulangan ke-", i)


💻 Output:

Perulangan ke- 0
Perulangan ke- 1
Perulangan ke- 2
Perulangan ke- 3
Perulangan ke- 4

🔁 Perulangan while

Digunakan ketika kita ingin mengulang selama kondisi tertentu bernilai True.

i = 1
while i <= 5:
    print("Hitungan ke-", i)
    i += 1


💻 Output:

Hitungan ke- 1
Hitungan ke- 2
Hitungan ke- 3
Hitungan ke- 4
Hitungan ke- 5

🚨 Break & Continue

break → menghentikan loop

continue → lompat ke iterasi berikutnya

for i in range(1, 6):
    if i == 3:
        continue
    if i == 5:
        break
    print("Angka:", i)


💻 Output:

Angka: 1
Angka: 2
Angka: 4
