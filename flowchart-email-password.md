```mermaid
flowchart TD
    mulai@{ shape: circ, label: "Mulai"}
    input@{ shape: lean-r, label: "Input: email, password"}
    if@{shape: diamond, label: "email || password == null"}
    epNull@{shape: lean-r, label: "Output: #quot;Email dan Password harus diisi!#quot;"}
    emPass@{shape: rect, label: "em = #quot;admin@mail.com#quot;
    pw = #quot;1234#quot;" }
    ifepBenar@{ shape: diamond, label: "email == em 
    && 
    password == pw"}
    loginBerhasil@{ shape: lean-r, label: "Output: #quot;Login berhasil!#quot;"}
    loginGagal@{ shape: lean-r, label: "Output: #quot;Email atau password salah!#quot;"}
    selesai@{ shape: dbl-circ, label: "Selesai"}
    
mulai-->input-->emPass-->if
if-->|True| epNull-->selesai
if-->|False| ifepBenar
ifepBenar-->|True| loginBerhasil-->selesai
ifepBenar-->|False| loginGagal-->selesai
```