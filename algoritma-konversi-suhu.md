# Algoritma Program Konversi Suhu
## Deskriptif
1. Mulai
2. tentukan nilai suhu dalam celcius (C) dan angka 1,2,atau 3 untuk memilih jenis konversi. 1 untuk celcius ke reamur, 2 untuk celciuc ke fahrenheit, dan 3 untuk celcius ke kelvin, jika angka yang dipilih tidak 1,2,atau 3 maka proses konversi tidak akan berjalan
3. hitung nilai konversi celsius (C) ke reamur (R) dengan cara mengalikan skala reamur yang bernilai 4 dengan nilai celcius (C) yang dibagi dengan skala celcius yang bernilai 5
4. hitung nilai konversi celcius (C) ke Fahrenheit (F) dengan cara mengalikan skala Fahrenheit yang bernilai 9 dengan nilai celcius (C) dibagi dengan skala celcius yang bernilai 5, kemudian ditambah 32
5. hitung nilai konversi celcius (C) ke Kelvin (K) dengan cara mengalikan skala Kelvin yang bernilai 5 dengan nilai celcius (C) dibagi dengan skala celcius yang bernilai 5, kemudian ditambah 273
6. tulis hasil konversi
7. selesai 

## Flowchart
```mermaid
flowchart TD
    mulai@{ shape: circ, label: "Mulai"}
    input@{ shape: lean-r, label: "Input: C, pil"}

    pil1@{shape: diamond, label: "if pil=1"}
    pil2@{shape: diamond, label: "elseif pil=2"}
    pil3@{shape: diamond, label: "elseif pil=3"}
    else@{shape: diamond, label: "else"}
    hR@{shape: rect, label: "R = C/5 * 4"}
    hF@{shape: rect, label: "F = ( C/5 * 9 ) + 32"}
    hK@{shape: rect, label: "K = C + 273"}
    hLain@{shape: lean-r, label: "output: #quot;input hanya bisa berupa angka 1, 2, atau 3!#quot;"}
    
    hasilR@{shape: lean-r, label: "output: #quot;hasil konversi ke Reamur sebesar#quot;, R"}
    hasilF@{shape: lean-r, label: "output: #quot;hasil konversi ke Fahreheit sebesar#quot;, F"}
    hasilK@{shape: lean-r, label: "output: #quot;hasil konversi ke Kelvin sebesar#quot;, K"}
    
    selesai@{ shape: dbl-circ, label: "Selesai"}
    
mulai-->input-->pil1
pil1-->|true| hR-->hasilR-->selesai
pil1-->|false| pil2
pil2-->|true| hF-->hasilF-->selesai
pil2-->|false| pil3
pil3-->|true| hK-->hasilK-->selesai
pil3-->|false| else
else--> hLain-->selesai
```

```mermaid
flowchart TD
    mulai@{ shape: circ, label: "Mulai"}
    input@{ shape: lean-r, label: "Input: C"}
    hitung@{ shape: rect, label: "R = C/5 * 4
    F = ( C/5 * 9 ) + 32
    K = C + 273"}
    hasil@{ shape: lean-r, label: "Output: R, F, K"}
    selesai@{ shape: dbl-circ, label: "Selesai"}
    
mulai-->input-->hitung-->hasil-->selesai
```