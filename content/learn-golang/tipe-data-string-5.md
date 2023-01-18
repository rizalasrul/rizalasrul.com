---
title: '04 - Tipe Data String'
date: '2023-01-05'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Kita sudah pernah menggunakan tipe data string ketika mencetak tulisan "Hello World" di tulisan sebelumnya. String adalah tipe data kumpulan karakter. Jumlah karakter di dalam string bisa nol sampai tidak terhingga.

## Kode Program String

Program di bawah ini akan mencetak string.

```go
package main

import "fmt"

func main() {
	fmt.Println("Selamat")
	fmt.Println("Selamat Malam")
	fmt.Println("Selamat Malam Dunia")
}
```

## Function Untuk String

Ada banyak function yang bisa digunakan untuk mengolah string. Beberapa contoh yang biasa digunakan adalah:

1. `len("string")`, digunakan untuk menghitung jumlah karakter di string.
2. `"string".[number]`, digunakan untuk mengambil nilai byte dari karakter pada posisi yang ditentukan.

```go
package main

import "fmt"

func main() {
	fmt.Println(len("Selamat")) // 7
	fmt.Println("Selamat Malam"[5]) // 97 --> byte dari karakter "a"
	fmt.Println("Selamat Malam Dunia"[10]) // 108 --> byte dari karakter "l"
}
```