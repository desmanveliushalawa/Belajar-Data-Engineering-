
---

## 📌 Deskripsi Singkat Project
Project ini adalah program Python sederhana untuk **membaca file CSV**, melakukan **filter data sesuai kriteria tertentu**, lalu menyimpan hasil filter ke file CSV baru.  
Tujuannya agar data yang besar bisa dipilah sesuai kebutuhan, misalnya hanya menampilkan orang dengan usia tertentu atau data dari kota tertentu.

---

## 📥 Input & 📤 Output
- **Input:**  
  - File CSV (misalnya `sales.csv`) berisi data tabel dengan kolom seperti 'Order_ID','Order_Date','Product','Category','Region','Sales','Quantity'.  
- **Output:**  
  - File CSV baru (misalnya `hasil_filter.csv`) yang hanya berisi baris sesuai kriteria filter.  
  - Contoh: jika filter `sales > 1000000`, maka hanya baris dengan sales lebih dari 1000000 yang tersimpan.

---

## ▶️ Cara Menjalankan Script
1. Pastikan Python sudah terinstall di komputer Anda.  
2. Install library **pandas** (jika belum ada):  
   ```bash
   pip install pandas
   ```
3. Simpan script Python (misalnya `filter_csv.py`) dengan isi seperti berikut:
   ```python
   import pandas as pd

   # Baca file CSV
   df = pd.read_csv("data.csv")

   # Filter data (contoh: Sales > 1000000)
   filtered_df = df[df["Sales"] > 1000000]

   # Simpan hasil ke CSV baru
   filtered_df.to_csv("hasil_filter.csv", index=False)

   print("Data berhasil difilter dan disimpan ke 'hasil_filter.csv'")
   ```
4. Jalankan script di terminal/command prompt:
   ```bash
   python filter_csv.py
   ```
5. Hasil filter akan tersimpan di file `hasil_filter.csv`.


