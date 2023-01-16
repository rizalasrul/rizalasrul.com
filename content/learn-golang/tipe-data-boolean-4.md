---
title: 'Tipe Data Boolean'
date: '2023-01-19'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Tipe data boolean adalah tipe data yang memiliki dua nilai, yaitu benar atau salah. Di golang, tipe data boolean direpresentasikan menggunakan keyword `bool`.

## Boolean

Berikut adalah tipe data boolean yang tersedia di golang:
1. `true`
2. `false`

## Kode Program Number

Program di bawah ini akan mencetak boolean.

```go
package main

import "fmt"

func main() {
	fmt.Println("Benar = ", true)
	fmt.Println("Salah = ", false)
}
```