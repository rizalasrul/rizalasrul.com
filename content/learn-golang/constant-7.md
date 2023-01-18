---
title: '06 - Constant'
date: '2023-01-07'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Constant adalah variable yang nilainya tidak bisa diubah lagi setelah pertama kali diberi nilai. Cara pembuatannya mirip dengan variable, yang membedakan hanya kata kunci yang digunakan, yaitu `const`.

## Kode Program Constant

Saat pembuatan constant, kita wajib langsung menuliskan nilainya.

```go
func main() {
    const firstName string  = "Rizal"
    const lastName          = "Asrul Pambudi"

    fmt.Println(firstName)
    fmt.Println(lastName)
}
```

Berbeda dengan variable, nilai dari constant tidak dapat diubah. Jika kita memaksa untuk mengubahnya, akan muncul pesan error.

```go
func main() {
    const firstName string  = "Rizal"
    const lastName          = "Asrul Pambudi"

	lastName    = "Widodo" // cannot assign to lastName (untyped string constant "Asrul Pambudi")

    fmt.Println(firstName)
    fmt.Println(lastName)
}
```

## Deklarasi Multiple Constant

Sama seperti variable, kita bisa membuat constant secara sekaligus banyak.

```go
func main() {
	const (
		firstName string    = "Rizal"
		lastName            = "Asrul Pambudi"
	)

    fmt.Println(firstName)
    fmt.Println(lastName)
}
```