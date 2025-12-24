# Algoritma Checkout Tokopedia
## Algoritma Checkout Tokopedia berbentuk deskripsi
1. Mulai
2. Cari barang yang akan dibeli
3. Lakukan checkout dengan cara tekan tombol checkout, atau tekan tombol beli langsung
4. Jika menekan tombol checkout masuk ke keranjang 
5. Pilih Barang yang mau di checkout
6. Tentukan metode pengiriman
7. Jika pembayaran COD tunggu barang sampai 
8. Jika barang sudah sampai maka bayar barang tersebut kepada kurir
9. Jika pembayaran tidak ingin COD maka pilih metode pembayaran lain selain cod dan
10. Konfirmasi Pembayaran
11. Stop
    

## Algoritma Checkout Tokopedia berbentuk Flowchart
```mermaid
flowchart TB
 Start@{ shape: circ, label: "start"} 
 FindProduct@{ shape: lean-r, label: "input: product"}
 CheckOutProcess@{ shape: diamond, label: "product == checkout"}
 CartProcess@{ shape: rect, label: "Tekan tombol keranjang"}
 CheckOut@{ shape: rect, label: "Pilih barang"}
 PriceMethod@{ shape: diamond, label: "product == cod"}
 PriceNotCod@{ shape: rect, label: "Pilih metode pembayaran"}
 Confirm@{ shape: rect, label: "Konfirmasi Pembayaran"}
 PriceIsCod@{ shape: rect, label: "Tunggu Barang Sampai"}
 PriceProductCod@{ shape: rect, label: "Bayar barang"}


 Stop@{ shape: dbl-circ, label: "stop"}

 Start-->FindProduct-->CheckOutProcess-->|true|CartProcess
 CartProcess-->CheckOut
 CheckOut-->PriceMethod-->|false|PriceNotCod-->Confirm-->Stop
 PriceMethod-->|true|PriceIsCod-->PriceProductCod-->Stop
 CheckOutProcess-->|false|PriceMethod
```