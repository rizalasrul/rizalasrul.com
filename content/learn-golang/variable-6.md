---
title: '05 - Variable'
date: '2023-01-06'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Variable adalah tempat untuk menyimpan data. Variable digunakan agar kita dapat mengakses data yang sama dimanapun yang kita inginkan.

Di golang, variable hanya dapat menyimpan tipe data yang sama. Jika kita ingin menyimpan tipe data yang berbeda-beda, maka kita harus membuat variable lagi yang berbeda.

Untuk membuat variable, kita dapat menggunakan kata kunci `var` lalu diikuti dengan nama variable dan tipe datanya.

## Kode Program Variable

Program di bawah ini adalah contoh penggunaan dari variable.

```go
package main

import "fmt"

func main() {
    var name string

    name = "Rizal Asrul Pambudi"
    fmt.Println(name)

    name = "Asrul Rizal Pambudi"
    fmt.Println(name)
}
```

Jika kita membuat variable, maka kita wajib menyebutkan tipe data variable-nya. Namun jika kita langsung menginisialisasikan data pada variable-nya, maka kita tidak wajib menyebutkan tipe datanya.

Di bawah ini adalah contoh kode ketika menginisiasi variable menggunakan tipe data.

```go
package main

import "fmt"

func main() {
    var name string
}
```

Di bawah ini adalah contoh kode ketika menginisiasi variable tanpa tipe data.

```go
package main

import "fmt"

func main() {
    var name = "Rizal Asrul Pambudi"
}
```

Jika kita ingin secara spesifik menuliskan tipe datanya, seperti `int8` atau `float32`, maka kita perlu untuk mencantumkan tipe datanya.

```go
package main

import "fmt"

func main() {
    var age int8 = 29
}
```

Karena jika tidak, maka tipe data variable-nya akan bertipe integer biasa.

```go
package main

import "fmt"

func main() {
    var age = 29
}
```

## Kata Kunci var

Di golang, kata kunci `var` saat membuat variable sebenarnya tidak wajib dicantumkan, asalkan saat membuat variable kita langsung menginisialisasi datanya.

Agar tidak perlu menggunakan kata kunci `var`, kita perlu menggunakan kata kunci `:=` saat menginisialisasi data pada variable tersebut.

```go
package main

import "fmt"

func main() {
    name := "Rizal Asrul Pambudi"
    fmt.Println(name)

    name = "R. A. Pambudi"
    fmt.Println(name)
}
```

## Deklarasi Multiple Variable

Di golang, kita bisa membuat variable secara sekaligus banyak. Cara seperti ini dapat mempermudah untuk dibaca.

Kode di bawah ini adalah contoh ketika kita membuat variable satu per satu.

```go
package main

import "fmt"

func main() {
    var firstName   = "Rizal"
    var lastName    = "Asrul Pambudi"

    fmt.Println(firstName)
    fmt.Println(lastName)
}
```

Kode di bawah ini adalah contoh ketika kita membuat variable secara sekaligus banyak.

```go
package main

import "fmt"

func main() {
    var (
        firstName = "Rizal"
        lastName = "Asrul Pambudi"
    )

    fmt.Println(firstName)
    fmt.Println(lastName)
}
```