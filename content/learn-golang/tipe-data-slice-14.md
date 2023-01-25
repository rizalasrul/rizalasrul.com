---
title: '13 - Tipe Data Slice'
date: '2023-01-14'
tags: ['golang', 'basic']
ShowToc: true
---

## Pendahuluan

Tipe data slice adalah potongan dari data array. Slice mirip dengan array, hanya saja ukuran dari slice bisa berubah. Slice dan array selalu terkoneksi karena slice mengakses sebagian atau seluruh data di array.

Tipe data slice memiliki tiga data: pointer, length, dan capacity.

* Pointer adalah penunjuk data pertama di array pada slice.
* Length adalah panjang dari slice.
* Capacity adalah kapasitas dari slice. Length tidak boleh lebih dari capacity.

## Membuat Slice dari Array

Untuk membuat slice dari array, kita dapat menggunakan function berikut ini:

1. `array[low:high]`, digunakan untuk membuat slice dari array dimulai index low sampai index sebelum high.
2. `array[low:]`, digunakan untuk membuat slice dari array dimulai index low sampai index akhir.
3. `array[:high]`, digunakan untuk membuat slice dari array dimulai index 0 sampai index sebelum high.
4. `array[:]`, digunakan untuk membuat slice dari array dimulai index 0 sampai index akhir.

## Kode Program Slice

Berikut adalah kode program slice.

```go
func main() {
    names   := [...]string{
        "Rizal",
        "Asrul",
        "Pambudi",
        "Joko",
        "Widodo",
        "Susilo",
        "Bambang",
        "Yudoyono",
    }
    slice   := names[4:6]

    fmt.Println(slice[0])
    fmt.Println(slice[1])
}
```

## Function Slice

Berikut adalah beberapa function umum pada slice.

* `len(slice)` digunakan untuk mendapatkan panjang.
* `cap(slice)` digunakan untuk mendapatkan kapasitas.
* `append(slice)` digunakan untuk membuat slice baru dengan menambah data ke posisi terakhir slice. Jika kapasitas slice sudah penuh, maka akan membuat array baru.
* `make([]TypeData, length, capacity)` digunakan untuk membuat slice baru.
* `copy(destination, source)` digunakan untuk menyalin slice dari source ke destination.

## Kode Program Append Slice

Berikut adalah contoh program append slice.

```go
func main() {
    days   := [...]string{
		"Senin",
		"Selasa",
		"Rabu",
		"Kamis",
		"Jumat",
		"Sabtu",
		"Minggu",
	}

	daySlice1	:= days[5:]
    fmt.Println(daySlice1)

	daySlice1[0]	= "Sabtu Baru"
	daySlice1[1]	= "Minggu Baru"
    fmt.Println(daySlice1)
    fmt.Println(days)

	daySlice2	:= append(daySlice1, "Libur Baru")
    fmt.Println(daySlice2)

	daySlice2[0]	= "Ups"
    fmt.Println(daySlice2)

    fmt.Println(daySlice2)
    fmt.Println(days)
}
```

## Kode Program Make Slice

Berikut adalah contoh program make slice.

```go
func main() {
    newSlice    := make([]string, 2, 5)
    newSlice[0] = "Rizal"
    newSlice[1] = "Rizal"

    fmt.Println(newSlice)
    fmt.Println(len(newSlice))
    fmt.Println(cap(newSlice))
}
```

## Kode Program Copy Slice

Berikut adalah contoh program copy slice.

```go
func main() {
    days   := [...]string{
		"Senin",
		"Selasa",
		"Rabu",
		"Kamis",
		"Jumat",
		"Sabtu",
		"Minggu",
	}
    fromSlice   := days[:]
    toSlice     := make([]string, len(fromSlice), cap(fromSlice))

    fmt.Println(toSlice)
    fmt.Println(fromSlice)

    copy(toSlice, fromSlice)

    fmt.Println(toSlice)
    fmt.Println(fromSlice)
}
```

## Perbedaan Array dengan Slice

Berikut adalah contoh perbedaan antara array dengan slice.

```go
func main() {
    iniArray    += [...]int{1, 2, 3, 4, 5}
    iniSlice    += [...]int{1, 2, 3, 4, 5}
}
```
