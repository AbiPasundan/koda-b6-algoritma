```mermaid
flowchart TB
 A@{ shape: circ, label: "start"} 
 B@{ shape: lean-r, label: "Angka"}
 X@{ shape: diamond, label: "Angka == 0"}
 Y@{ shape: lean-l, label: "Tidak bisa dibagi"}
 C@{ shape: diamond, label: "Angka % 2"}
 D@{ shape: lean-l, label: "Genap"}
 E@{ shape: lean-l, label: "Ganjil"}
 Z@{ shape: dbl-circ, label: "stop"}
 A-->B-->
 C-->|Hasilnya 0|D[Genap]
 C-->|Hasilnya bukan 0|E[Ganjil]
 B-->X-->Y
 E-->Z
 D-->Z
```