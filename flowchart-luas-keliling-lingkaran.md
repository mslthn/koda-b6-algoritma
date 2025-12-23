```mermaid
flowchart TD
    mulai@{ shape: circ, label: "Mulai"}
    dec@{ shape: rect, label: "L= phi x r x r
    K = 2 x phi x r
    "}
    input@{ shape: lean-r, label: "Input: r"}
    if@{shape: diamond, label: "r%7 == 0"}
    inP7@{ shape: lean-r, label: "phi = 22/7"}
    inP3@{ shape: lean-r, label: "phi = 3.14"}
    pros@{ shape: rect, label: "hitungLuas = phi * r * r
    hitungKeliling = 2 * phi * r"}
    out@{ shape: lean-r, label: "Output: hitungLuas, hitungKeliling"}
    selesai@{ shape: dbl-circ, label: "Selesai"}
    
mulai-->input-->if
if-->|True| inP7-->pros
if-->|False| inP3-->pros
pros-->out-->selesai
```