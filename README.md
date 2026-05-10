# 🧠 Penjelasan CSS Unit
<p align="justify">
CSS Unit adalah satuan ukuran dalam CSS yang dipakai untuk mengatur panjang, lebar, margin, padding, font-size, dan elemen lain. Ada dua jenis utama: absolute (tetap) dan relative (menyesuaikan konteks).</p> 

---

## 📌 Kategori CSS Unit

Ada 4 kategori CSS unit yaitu: 
   - **Integer**: bilangan bulat yang nilainya bisa positif/negatif.
     
     Contoh: `1` sampai `999`  |  `-999` sampai `-1`  
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

     a ) **Length 📏**  
     Absolute: `px`, `pt`, `pc`, `cm`, `mm`, `in`  |  Relative: `%`, `em`, `rem`, `ch`, `vh`, `vw`, `vmin`, `vmax`  
     ```css
        font-size: 16px;
        width: 50%;
        padding: 2rem;
     ```

     b ) **Angle**  
     Satuan: `deg`, `rad`, `grad`, `turn`  
     ```css
        transform: rotate(45deg);
     ```

     c ) **Time**  
     Satuan: `s` (second), `ms` (millisecond)  
     ```css
        transition: all 0.5s ease;
     ```

     d ) **Resolution 📸**  
     Satuan: `dpi` (dots per inch), `dpcm` (dots per centimeter), `dppx` (dots per pixel)  
     ```css
        @media (min-resolution: 300dpi) {
           body { font-size: 18px; }
        }
     ```

---

### 🌐 EM dan REM

- **EM**
  <p align="justify">  
  Adalah satuan relatif yang ukurannya bergantung pada ' font-size ' elemen induk. Nilai ' 1em ' sama dengan ukuran font elemen induk, sehingga sangat berguna untuk desain yang fleksibel dan responsif. Cocok untuk elemen yang skalanya ingin menyesuaikan font-size parent, misalnya padding tombol yang mengikuti ukuran teks di dalamnya. </p>
   
  Contoh:
    ```css
       button {
          font-size: 1em;      /* mengikuti parent */
          padding: 0.5em 1em;  /* padding ikut skala font */
       }
    ```

- **REM**
  <p align="justify">
  Adalah unit ukuran relatif di CSS yang ukurannya selalu berdasarkan ukuran font elemen root (biasanya), bukan elemen induknya seperti em. Menjadikannya pilihan ideal untuk desain web yang konsisten, dapat diakses, dan responsif karena seluruh skala ukuran dapat diubah dengan satu pengaturan di elemen. Cocok untuk tipografi utama (heading, paragraf) agar tidak berubah-ubah meski nested. </P>
  
  Contoh:
    ```css
       h1 {
          font-size: 2rem; /* 32px */
       }
    ```
    
---

### 🪟 ViewPort Unit

- **VW**  
  Definisi relatif terhadap lebar viewport (jendela browser). `1vw` = 1% dari lebar layar.

  Kapan digunakan:
  - Layout penuh layar (fluid layout) → Saat elemen harus menyesuaikan lebar layar otomatis.   
  - Tipografi responsif → Untuk teks besar (judul, banner) yang skalanya mengikuti lebar layar. Cocok agar font tidak terlalu kecil di layar besar.  
  - Elemen dekoratif proporsional → Misalnya lingkaran, kotak, atau ilustrasi yang harus selalu proporsional dengan lebar layar.  
  - Desain responsif tanpa media query → `vw` bisa dipakai untuk membuat elemen otomatis menyesuaikan layar tanpa harus menulis banyak breakpoint.

  Contoh:
    ```css
       .hero {
          width: 100vw;
       }
    ```
  
- **VH**  
  Definisi relatif terhadap tinggi viewport (jendela browser). `1vh` = 1% dari tinggi layar.

  Kapan digunakan:
  - Layout penuh layar (fullscreen section) → Membuat elemen memenuhi tinggi layar.   
  - Elemen proporsional terhadap tinggi layar → Cocok untuk desain yang menekankan tinggi daripada lebar, misalnya banner setengah layar.  
  - Tipografi responsif berbasis tinggi layar → Kadang ukuran font ingin menyesuaikan tinggi layar, bukan lebar.  
  - Kontainer vertikal fleksibel → Berguna untuk layout yang harus menyesuaikan tinggi layar tanpa bergantung pada parent.

  Contoh:
    ```css
       .hero {
          height: 50vh;
       }
    ```
  
- **VMIN**  
  Definisi relatif terhadap sisi terkecil dari viewport (lebar atau tinggi jendela browser). `1vmin` = 1% dari sisi terkecil layar.

  Kapan digunakan
  - Elemen proporsional di berbagai orientasi → Elemen tetap seimbang baik di portrait maupun landscape.   
  - Tipografi responsif yang aman → Teks menyesuaikan layar tapi tidak terlalu besar di layar lebar, karena mengikuti sisi terkecil.  
  - Elemen dekoratif atau grafis → Misalnya lingkaran, ikon, atau ilustrasi yang harus selalu proporsional dengan layar.  
     `vmin` memastikan bentuk tidak meluber di layar lebar.  
  - Desain cross-device → Berguna untuk memastikan elemen tetap proporsional di desktop (landscape) maupun mobile (portrait).

  Contoh:
    ```css
       h1 {
          font-size: 2rem; /* 32px */
       }
    ```

- **VMAX**  
  Definisi relatif terhadap sisi terbesar dari viewport (lebar atau tinggi jendela browser). `1vmax` = 1% dari sisi terbesar layar.

  Kapan digunakan
  - Elemen besar proporsional terhadap layar → Cocok untuk elemen dekoratif, background, atau tipografi yang ingin tetap menonjol di layar besar.  
  - Desain mengikuti orientasi layar → Saat portrait, sisi terbesar biasanya tinggi; saat landscape, sisi terbesar biasanya lebar. `vmax` memastikan elemen tetap proporsional terhadap dimensi terbesar.  
  - Full-screen layout → Digunakan untuk section atau container yang harus memenuhi layar dengan mempertimbangkan sisi terbesar.  
  - Elemen dekoratif responsif → Misalnya lingkaran, ilustrasi, atau animasi yang harus tetap besar meski layar berubah orientasi. 

  Contoh:
    ```css
       h1 {
          font-size: 2rem; /* 32px */
       }
    ```

- **CALC**  
  Definisi `calc()` adalah fungsi pada CSS yang memungkinkan kita melakukan operasi matematika atau kalkulasi pada nilai sebuah property.

  Nilai yang bisa dikelola dengan calc
  - Length  
  - Angle  
  - Time  
  - Percentage  
  - Number  

  Contoh:
    ```css
       h1 {
          font-size: 2rem; /* 32px */
       }
    ```
