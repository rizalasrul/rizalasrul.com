---
title: '08 - Type Declarations'
date: '2023-01-09'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Type declarations adalah kemampuan membuat ulang tipe data baru dari tipe data yang sudah ada. Type declarations biasanya digunakan untuk membuat alias terhadap tipe data yang sudah ada. Tujuannya adalah supaya lebih mudah dimengerti.

## Kode Program Type Declarations

Berikut adalah contoh program type declarations

```go
func main() {
    type NoKTP string

    var ktpSaya NoKTP   = "12211221"
    fmt.Println(ktpSaya)
    fmt.Println(NoKTP("333344444"))
}
```
