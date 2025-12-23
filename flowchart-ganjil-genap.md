```mermaid
flowchart TD
    mulai@{ shape: circ, label: "Mulai"}
    input@{ shape: lean-r, label: "Input x"}
    proses@{ shape: rect, label: "hitung modulus"}
    ifG@{ shape: diamond, label: "x%2==0"}
    ganjil@{ shape: lean-r, label: "x bilangan ganjil"}
    genap@{ shape: lean-r, label: "x bilangan genap"}
    selesai@{ shape: dbl-circ, label: "Selesai"}

mulai-->input-->proses-->ifG
ifG-->|True| genap-->selesai
ifG-->|False| ganjil-->selesai
```
