---
title: '14 - Tipe Data Map'
date: '2023-01-15'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Map adalah tipe data lain yang berisikan kumpulan data yang sama, namun kita bisa menentukan jenis tipe data index yang akan digunakan. Sederhananya, map adalah tipe data kumpulan key-value. Berbeda dengan array dan slice, jumlah data yang dimasukkan ke dalam map boleh sebanyak-banyaknya, asalkan kata kuncinya berbeda.

## Kode Program Map

Berikut adalah contoh kode program map.

```go
person  := map[string]string{
    "name":     "Rizal Asrul",
    "address":  "Sidoarjo",

    fmt.Println(person)
    fmt.Println(person["name"])
    fmt.Println(person["address"])
}
```

## Function Map

Berikut adalah beberapa function umum pada map.

* `len(map)` digunakan untuk mendapatkan jumlah data di map.
* `make(map[TypeKey]TypeValue)` digunakan untuk membuat map baru.
* `delete(map, key)` digunakan untuk menghapus data di map dengan key.

## Kode Program Make

Berikut adalah contoh penggunaan function `make(map[TypeKey]TypeValue)`.

```go
func main() {
    book    := make(map[string]string)
    book["title"]   = "Buku Tulis"
    book["author"]  = "Rizal Asrul"
    book["wrong"]   = "Ups"

    delete(book, "wrong")

    fmt.Println(book)
}
```