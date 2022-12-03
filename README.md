# praktikum_6

### Nama : Sinta Hardianti Wijaya

### NIM : 312210342

### Kelas : TI.22.A3

## Latihan 

Soal latihan

![latihan 1 prak7](https://user-images.githubusercontent.com/115516473/205430348-c3591f43-c750-4df6-ba0e-a3e3e3c497b7.png)

## - Kode program menggunakan fungsi lambda

```
import math

a = lambda x: x ** 2
print(a(46))

b = lambda x,y: x**2 + y**2
print(b(4,6))

c = lambda *args : sum(args)/len(args)
print(c(5,7,9,11,10))

d = lambda s: "".join(set(s))
print(d("Tertimpa"))
```

