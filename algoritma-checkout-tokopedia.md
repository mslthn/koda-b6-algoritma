# Algoritma Proses Checkout di Tokopedia

### Algoritma
1. mulai
2. buka tokopedia
3. apakah barang yang diinginkan sudah ada di keranjang?
3. jika tidak, cari barang yang diinginkan
4. pilih barnag mana yang ingin dicheckout
5. pilih varian dan tipe yang diinginkan
6. setelah memilih tipe, bisa memilih untuk "Beli langsung" atau tambah ke keranjang
9. jika memilih "+keranjang"
10. maka akan tampil "barang berhasil ditambahkan ke keranjang" pada tampilan
11. setelah menambahkan item ke keranjang, bisa melanjutkan untuk mencari barang lain atau keluar dari tokopedia
7. jika beli langsung
8. maka lanjut untuk proses checkout
8. pilih metode pembayaran
8. sesuaikan alamat pengiriman sesuai dengan yang dikehendaki
12. lanjut ke proses pembayaran
13. konfirmasikan pembayaran
14. selesai

### Flowchart
```mermaid
flowchart TD
    mulai@{ shape: circ, label: "Mulai"}
    lgsgKrjg@{shape: diamond, label: "keranjang == null"}
    cariBrg@{shape: lean-r, label: ""}
    pilBrg@{label: "pilih barang"}
    pilTipe@{shape: rect, label: ""}
    beliLgsg@{shape: diamond, label: "beli langsung?"}
    
    tamKrjg@{shape: diamond, label: "tambah item ke keranjang?"}
    tambahItemKeranjang@{shape: lean-r,label: "input: keranjang"}
    berhasilTambah@{shape: lean-r, label: "output: #quot;berhasil menambahkan barang ke keranjang!#quot;"}
    pilBrgKrjg@{label: "pilih barang"}
    co@{label: "checkout"}
    pilMetPem@{shape: lean-r, label: "input: metodePembayaran"}
    pilAlamat@{shape: lean-r, label: "input: alamat"}
    bayar@{}
    konfirmBayar@{}
    selesai@{ shape: dbl-circ, label: "Selesai"}

    lanjutBelanja@{shape: diamond, label: "Lanjut belanja?"}
    
mulai-->lgsgKrjg
lgsgKrjg-->|false| pilBrgKrjg-->co-->pilMetPem-->pilAlamat-->bayar-->konfirmBayar-->selesai
lgsgKrjg-->|true| cariBrg--> pilBrg-->pilTipe-->beliLgsg

beliLgsg-->tamKrjg
tamKrjg-->|ya| tambahItemKeranjang-->berhasilTambah-->lanjutBelanja
tamKrjg-->|tidak| selesai
beliLgsg-->|ya| co

lanjutBelanja-->|true| cariBrg
lanjutBelanja-->|false| selesai 
```

```mermaid
flowchart TD
    mulai@{ shape: circ, label: "Mulai"}
    cari@{shape: lean-r, label: "input: namaBarang"}
    dataItem@{shape: lean-r, label: "output: namaBarang1, 
    namaBarang2, 
    namaBarang3,
    ...
    namaBarangX"}
    
    pilihItem@{label: "namaBarangX"}
    pilihVarian@{shape: lean-r, label: "input: varian, tipe"}
    checkout@{}
    pilihMP@{shape: lean-r, label: "input: alamat, 
    metodePembayaran"}
    bayar@{}
    selesai@{shape: dbl-circ, label: "selesai"}

mulai-->cari
cari-->dataItem-->pilihItem
pilihItem-->pilihVarian
pilihVarian-->checkout
checkout-->pilihMP
pilihMP-->bayar
bayar-->selesai
```