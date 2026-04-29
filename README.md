# UTS Pengolahan Citra Digital

Repository ini berisi pengerjaan UTS mata kuliah Pengolahan Citra Digital. Pembahasan mencakup transformasi citra grayscale, visualisasi histogram, serta filtering citra menggunakan kernel konvolusi.

## Identitas

Nama: Muhammad Rafi Nur Setiawan  
NIM: 23424026  
Program Studi: Informatika  
Mata Kuliah: Pengolahan Citra Digital  
Dosen Pengampu: Anggay Luri Pramana, S.Kom., M.Kom  

## Isi Repository

Repository ini terdiri dari beberapa file utama:

1. `UTS_PCD.ipynb`  
   File Google Colab berisi kode program untuk pengerjaan soal nomor 1 dan nomor 2.

2. `analisis.txt`  
   File berisi analisis hasil pengolahan citra untuk soal nomor 1 dan nomor 2.

3. `gambar_input.png`  
   Citra grayscale yang digunakan sebagai input dalam proses pengolahan citra.

4. `hasil_soal_1.png`  
   Hasil visualisasi citra original, citra negatif, citra logaritmik, dan histogram masing-masing.

5. `hasil_soal_2.png`  
   Hasil visualisasi citra original, LPF, HPF, dan BPF.

## Soal Nomor 1

Pada soal nomor 1 dilakukan transformasi citra grayscale menggunakan dua metode, yaitu transformasi negatif dan transformasi logaritmik.

### Rumus Transformasi Negatif

```text
G = 255 - F
```

### Rumus Transformasi Logaritmik

```text
G = c × log(1 + F)
c = 255 / log(1 + max(F))
```

### Output

Output dari soal nomor 1 meliputi:

- Citra original
- Citra negatif
- Citra logaritmik
- Histogram citra original
- Histogram citra negatif
- Histogram citra logaritmik

## Soal Nomor 2

Pada soal nomor 2 dilakukan proses filtering menggunakan tiga jenis kernel konvolusi, yaitu Low Pass Filter, High Pass Filter, dan Band Pass Filter.

### Low Pass Filter

```text
(1/9) × [[1, 1, 1],
         [1, 1, 1],
         [1, 1, 1]]
```

### High Pass Filter

```text
[[-1, -1, -1],
 [-1,  8, -1],
 [-1, -1, -1]]
```

### Band Pass Filter

```text
[[ 0, -1,  0],
 [-1,  5, -1],
 [ 0, -1,  0]]
```

### Output

Output dari soal nomor 2 meliputi:

- Citra original
- Hasil Low Pass Filter
- Hasil High Pass Filter
- Hasil Band Pass Filter
- Nilai piksel rata-rata dari setiap hasil

## Tools yang Digunakan

- Python
- Google Colab
- OpenCV
- NumPy
- Matplotlib
- PIL

## Cara Menjalankan Program

1. Buka file `UTS_PCD.ipynb` di Google Colab.
2. Upload citra grayscale yang akan digunakan.
3. Jalankan setiap cell program secara berurutan.
4. Amati hasil transformasi citra, histogram, dan filtering.
5. Baca hasil analisis pada file `analisis.txt`.

## Hasil Analisis Singkat

Transformasi negatif membalik nilai intensitas citra, sehingga area terang menjadi gelap dan area gelap menjadi terang. Transformasi logaritmik meningkatkan intensitas piksel rendah sehingga detail pada area gelap lebih mudah terlihat.

Low Pass Filter menghasilkan citra yang lebih halus atau blur. High Pass Filter menonjolkan tepi dan perubahan intensitas tajam. Band Pass Filter pada kernel yang digunakan menghasilkan efek penajaman citra.

## Tujuan Repository

Repository ini dibuat untuk memenuhi tugas UTS mata kuliah Pengolahan Citra Digital pada materi transformasi intensitas citra dan filtering berbasis konvolusi.
