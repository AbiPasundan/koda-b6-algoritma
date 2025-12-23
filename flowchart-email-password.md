flowchart-email-password.md

1. Masukan Email dan pw
2. jika email & pw kosong
3. Munculkan "Email & pw hrs d isi"
4. jika tidak
5. jika email adalah admin@mail.com & pw adalah 1234
6. Munculkan Login berhasil
7. Jika tidak munculkan email atau password salah

```mermaid
flowchart TB
 A@{ shape: circ, label: "start"} 
 B@{ shape: lean-r, label: "email: 'Email'"}
 C@{ shape: lean-r, label: "password: 'Password'"}
 D@{ shape: diamond, label: "email == ' ' || password == ' ' "}
 X@{ shape: lean-r, label: "output: 'Email dan Password harus di isi'"}
 E@{ shape: diamond , label: "email == 'admin@mail.com' && password == '1234 ' "}
 F@{ shape: lean-r, label: "Output: 'Login berhasil'"}
 G@{ shape: lean-r, label: "Output: 'Email atau Password Salah'"}
 Z@{ shape: dbl-circ, label: "stop"}


A-->B-->C-->D
D-->|true|X-->Z
D-->|false|E
E-->|true|G-->Z
E-->|false|F-->Z
```