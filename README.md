# 💡 Penjelasan CSS Units 💡
CSS Unit adalah satuan ukuran dalam CSS yang dipakai untuk mengatur panjang, lebar, margin, padding, font-size, dan elemen lain. Ada dua jenis utama: **absolute (tetap) dan relative (menyesuaikan konteks).**. 

---

## 📌 Kategori CSS Unit 📌  
Ada 4 kategori CSS unit yaitu:  
**Integer, Number, Percentage, Dimension** 🔢📊📐  
   - **Integer**: bilangan bulat yang nilainya bisa positif/negatif.  
     Contoh: `1` sampai `999` atau `-999` sampai `-1`  
     ```css
     z-index: 10;
     order: -2;
     ```

   - **Number**: bilangan pecahan yang nilainya di antara 0 dan satu.  
     Contoh: `0.5`  
     ```css
     opacity: 0.5;
     scale: 1.25;
     ```

   - **Percentage**: mempresentasikan sebagian dari nilai tertentu, dan selalu relatif terhadap nilai yang lain.  
     Contoh: `80%`  
     ```css
     width: 80%;
     margin-top: 10%;
     ```

   - **Dimension**: nomor yang memiliki satuan di belakangnya.  
     Turunan dimension ada 4 yaitu:  

     a) **Length 📏**  
     - Absolute: `px`, `pt`, `pc`, `cm`, `mm`, `in`  
     - Relative: `%`, `em`, `rem`, `ch`, `vh`, `vw`, `vmin`, `vmax`  
     ```css
     font-size: 16px;
     width: 50%;
     padding: 2rem;
     ```

     b) **Angle 🔄**  
     - Satuan: `deg`, `rad`, `grad`, `turn`  
     ```css
     transform: rotate(45deg);
     ```

     c) **Time ⏱️**  
     - Satuan: `s` (second), `ms` (millisecond)  
     ```css
     transition: all 0.5s ease;
     ```

     d) **Resolution 📸**  
     - Satuan: `dpi` (dots per inch), `dpcm` (dots per centimeter), `dppx` (dots per pixel)  
     ```css
     @media (min-resolution: 300dpi) {
       body { font-size: 18px; }
     }
     ```

## 📌 EM dan REM 📌 

- **EM**  
  Adalah satuan relatif yang ukurannya bergantung pada `font-size` elemen induk.  
  Nilai `1em` sama dengan ukuran font elemen induk, sehingga sangat berguna untuk desain yang fleksibel dan responsif.  
  Cocok untuk elemen yang skalanya ingin menyesuaikan font-size parent, misalnya padding tombol yang mengikuti ukuran teks di dalamnya.  
  - Contoh:
    ```css
    button {
      font-size: 1em;      /* mengikuti parent */
      padding: 0.5em 1em;  /* padding ikut skala font */
    }
    ```

- **REM**  
  Adalah unit ukuran relatif di CSS yang ukurannya selalu berdasarkan ukuran font elemen root (biasanya `<html>`), bukan elemen induknya seperti em.  
  Menjadikannya pilihan ideal untuk desain web yang konsisten, dapat diakses, dan responsif karena seluruh skala ukuran dapat diubah dengan satu pengaturan di elemen `<html>`.  
  Cocok untuk tipografi utama (heading, paragraf) agar tidak berubah-ubah meski nested.  
  - Contoh:
    ```css
    h1 {
         font-size: 2rem; /* 32px */
       }
    ```
