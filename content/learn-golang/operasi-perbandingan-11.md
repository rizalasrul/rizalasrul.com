---
title: '10 - Operasi Perbandingan'
date: '2023-01-11'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Operasi perbandingan adalah sebuah operasi untuk membandingkan dua buah data. Operasi perbandingan memiliki output berupa nilai boolean (`true` atau `false`).

## Operator Perbandingan

Berikut adalah beberapa operator perbandingan.

* Operator `>` digunakan untuk membandingan lebih dari.
* Operator `<` digunakan untuk membandingan kurang dari.
* Operator `>=` digunakan untuk membandingan kurang dari sama dengan.
* Operator `<=` digunakan untuk membandingan kurang dari sama dengan.
* Operator `==` digunakan untuk membandingan sama dengan.
* Operator `!=` digunakan untuk membandingan tidak sama dengan.

## Kode Program Operasi Perbandingan

Berikut adalah contoh kode program operasi perbandingan.

```go
func main() {
    var name1   = "Rizal"
    var name2   = "Rizal"

    var result1 bool    = name1 == name2
    fmt.Println(result1) // true

    var nilai1  = 100
    var nilai2  = 1000

    var result2 bool    = nilai1 > nilai2
    fmt.Println(result2) // false
}
```
