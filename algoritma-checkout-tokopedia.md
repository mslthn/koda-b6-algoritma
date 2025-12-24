# Algoritma Proses Checkout di Tokopedia

### Algoritma
1. mulai
2. cari product yang ingin dicheckout
3. produk akan masuk ke keranjang
4. setelah menentukan barang yang ingin dicheckout, lanjut ke proses bayar
5. jika sukses akan tampil notif pembayaran berhasil
6. jika gagal, akan tampil notif pembayaran gagal

### Flowchart
```mermaid
flowchart TD
    mulai@{ shape: circ, label: "Mulai"}
    cari@{shape: lean-r, label: "input: product"}
    dataItem@{shape: rect, label: "cart += product"}
    
    isPaid@{shape: diamond, label: "isPaid"}
    bayarBerhasil@{shape: lean-r, label: "output: #quot; Pembayaran Berhasil"}
    bayarGagal@{shape: lean-r, label: "output: #quot; Pembayaran Gagal"}
    selesai@{shape: dbl-circ, label: "selesai"}

mulai-->cari
cari-->dataItem-->isPaid
isPaid-->|true| bayarBerhasil-->selesai
isPaid-->|false| bayarGagal-->selesai
```

    pilihMP@{shape: lean-r, label: "input: alamat, metodePembayaran"}