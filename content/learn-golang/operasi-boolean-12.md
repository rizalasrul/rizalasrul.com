---
title: '11 - Operasi Boolean'
date: '2023-01-12'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Operasi boolean cukup sederhana, yaitu operasi yang bisa digunakan oleh data bertipe `bool`.

Terdapat tiga buah operator, yaitu:

* Operator `&&` digunakan untuk "dan".
* Operator `||` digunakan untuk "atau".
* Operator `!` digunakan untuk "kebalikan".

## Operasi &&

Berikut adalah contoh hasil dari operator `&&`.

* Jika `true && true`, maka hasilnya adalah `true`.
* Jika `true && false`, maka hasilnya adalah `false`.
* Jika `false && true`, maka hasilnya adalah `false`.
* Jika `false && false`, maka hasilnya adalah `false`.

## Operasi &&

Berikut adalah contoh hasil dari operator `||`.

* Jika `true || true`, maka hasilnya adalah `true`.
* Jika `true || false`, maka hasilnya adalah `true`.
* Jika `false || true`, maka hasilnya adalah `true`.
* Jika `false || false`, maka hasilnya adalah `false`.

## Operasi !

Berikut adalah contoh hasil dari operator `!`.

* Jika `!true`, maka hasilnya adalah `false`.
* Jika `!false`, maka hasilnya adalah `true`.

## Kode Program Operasi Boolean

Operasi boolean akan banyak kita temukan ketika kita sudah belajar tentang pengkondisian. Untuk saat ini, berikut adalah contoh program operaso boolean.

```go
func main() {
    var nilaiAkhir  = 90
    var absensi     = 80

    var lulusNilaiAkhir bool    = nilaiAkhir > 80
    var lulusAbsensi bool       = absensi > 80

    var lulus bool  = lulusNilaiAkhir && lulusAbsensi
    fmt.Println(lulus) // false
}
```