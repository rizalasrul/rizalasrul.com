---
title: '01 - Hello World'
date: '2023-01-02'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Membuat program hello world di golang memang tidak sesederhana seperti kita membuat program hello world di PHP, python, atau javascript.

## Program Hello World

```go
package main

import "fmt"

func main() {
    fmt.PrintLn("Hello World")
}
```

## Compile

Anggaplah kita membuat program hello world di atas dengan nama file `helloworld.go`. Untuk melakukan kompilasi, kita dapat menggunakan command `go build helloworld.go`. Hasil dari kompilasi tersebut adalah binary file dengan nama `helloworld`.

Untuk menjalankan binary file tersebut, kita dapat menggunakan command `./helloworld`.

## Menjalankan tanpa compile

Ada cara cepat untuk menjalankan program golang tanpa harus melakukan compile. Cara tersebut adalah dengan menggunakan command `go run helloworld.go`.

Cara ini hanya dapat dilakukan untuk proses development di local. Kalau kita ingin rilis ke production, maka wajib untuk melakukan kompilasi.