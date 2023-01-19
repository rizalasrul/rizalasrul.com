---
title: '07 - Konversi'
date: '2023-01-08'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Ada kalanya kita perlu untuk melakukan konversi antar tipe data. Contohnya tipe data angka yang awalnya `int32` dikonversi ke `int63`, yang awalnya integer dikonversi ke floating point.

## Kode Program Konversi Tipe Data Integer

Berikut adalah contoh program konversi tipe data integer

```go
func main() {
    var nilai32 int32   = 32768
    var nilai64 int64   = int64(nilai32)
    var nilai16 int16   = int16(nilai32)

    fmt.Println(nilai32) // 32768
    fmt.Println(nilai64) // 32768
    fmt.Println(nilai16) // -32768
}
```

Dari kode di atas, output yang menarik adalah output dari hasil konversi tipe data dari `int32` ke `int16`. Dilihat bahwa data `int16` akan bernilai -32768 jika dikonversi dari tipe data `int32`. Hal ini dikarenakan batas atas nilai `int16` adalah 32767. Karena melebihi batas atas, maka nilai tersebut akan kembali lagi ke batas bawah, yaitu -32768. Fenomena ini disebut dengan integer overflow.

## Kode Program Konversi Tipe Data String

Berikut adalah contoh program konversi tipe data integer

```go
func main() {
    var name    = "Rizal Asrul Pambudi" // string
    var e       = name[0] // byte
    var eString = string(e) // string

    fmt.Println(name) // Rizal Asrul Pambudi
    fmt.Println(eString) // R
}
```

Ketika kita mengambil salah satu karakter dari string, maka karakter yang kita ambil tersebut akan bertipe `byte`.
