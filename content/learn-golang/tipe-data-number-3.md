---
title: 'Tipe Data Number'
date: '2023-01-18'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Ada dua jenis tipe data number, yaitu:
1. Integer, tipe angka biasa.
2. Floating point, tipe angka desimal.

## Tipe Data Integer

Berikut adalah tipe data integer yang tersedia di golang:
1. `int8`. Nilai minimum: -128, nilai maksimum: 127
2. `int16`. Nilai minimum: -32768, niial maksimum: 32767
3. `int32`. Nilai minimum: -21474836648, nilai maksimum: 21474836647
4. `int64`. Nilai minimum: -9223372036854775808, nilai maksimum: 9223372036854775807
5. `uint8`. Nilai minimum: 0, nilai maksimum: 255
6. `uint16`. Nilai minimum: 0, nilai maksimum: 65535
7. `uint32`. Nilai minimum: 0, nilai maksimum: 4294967295
7. `uint64`. Nilai minimum: 0, nilai maksimum: 118446744073709551615

## Tipe Data Floating

Berikut adalah tipe data floating point yang tersedia di golang:
1. `float32`
2. `float64`
3. `complex64`
4. `complex128`

## Alias

Alias adalah nama lain untuk tipe data yang sudah ada. Berikut adalah contoh alias di golang:
1. `byte` adalah alias untuk `uint8`
2. `rune` adalah alias untuk `int32`
3. `int` adalah alias untuk minimal `int32`
4. `uint` adalah alias untuk minimal `uint32`

## Kode Program Number

Program di bawah ini akan mencetak angka.

```go
package main

import "fmt"

func main() {
	fmt.Println("Satu = ", 1)
	fmt.Println("Dua = ", 2)
	fmt.Println("Tiga koma lima = ", 3.5)
}
```