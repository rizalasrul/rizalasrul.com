---
title: '09 - Operasi Matematika'
date: '2023-01-10'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Di golang terdapat beberapa operator yang dapat kita gunakan dalam operasi matematika. Berikut adalah operatornya:

* \+ digunakan untuk penjumlahan
* \- digunakan untuk pengurangan
* \* digunakan untuk perkalian
* \/ digunakan untuk pembagian
* \% digunakan untuk sisa pembagian

## Augmented Assignments

Selain operator di atas, golang juga memiliki augmented assignments. Augmented assignments dapat digunakan untuk mempersingkat penulisan operasi kalkulasi terhadap variable dirinya sendiri.

* Operasi `a = a + 10` dapat disingkat menjadi `a += 10`.
* Operasi `a = a - 10` dapat disingkat menjadi `a -= 10`.
* Operasi `a = a * 10` dapat disingkat menjadi `a *= 10`.
* Operasi `a = a / 10` dapat disingkat menjadi `a /= 10`.
* Operasi `a = a % 10` dapat disingkat menjadi `a %= 10`.

Berikut adalah contoh program dari augmented assignments.

```go
func main() {
    var a   = 10
    a += 90

    fmt.Println(a) // 100
}
```

## Unary Operator

Sama seperti augmented assignments, unary operator dighnakan untuk mempersingkat penulisan operasi kalkulasi terhadap variable dirinya sendiri.

* Operasi `a = a + 1` dapat diganti menjadi `a++`.
* Operasi `a = a - 1` dapat diganti menjadi `a--`.
* Operator `-` diganti untuk menjadikan negatif.
* Operator `+` diganti untuk menjadikan positif.
* Operator `!` diganti untuk membalik nilai boolean.
