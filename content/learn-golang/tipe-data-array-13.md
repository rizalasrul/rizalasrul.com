---
title: '12 - Tipe Data Array'
date: '2023-01-13'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Array adalah tipe data yang berisikan kumpulan data dengan tipe yang sama. Saat membuat array, kita perlu menentukan jumlah data yang bisa ditampung oleh array tersebut. Daya tampung array tidak bisa bertambah setelah array dibuat.

## Kode Program Array

Berikut adalah contoh kode program array.

```go
func main() {
    var names [3]string
    names[0]    = "Rizal"
    names[1]    = "Asrul"
    names[2]    = "Pambudi"

    fmt.Println(names[0])
    fmt.Println(names[1])
    fmt.Println(names[2])
}
```

## Membuat Array Langsung

Di golang, kita juga bisa membuat array secara langsung saat deklarasi variable. Berikut adalah contoh programmnya.

```go
func main() {
    var score = [3]int {
        100,
        90,
        80,
    }

    fmt.Println(score)
}
```

## Melihat Panjang dari Array

Untuk melihat panjang dari array, kita dapat menggunakan function `len(array)`. Berikut adalah contoh programnya.

```go
func main() {
    var score = [3]int {
        100,
        90,
        80,
    }

    fmt.Println(len(score))
}
```