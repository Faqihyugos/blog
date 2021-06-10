---
title: "Apa yang baru di Python 3.10?"
date: 2021-06-10T19:44:27+07:00
draft: false
cover: "img/python.jpg"
coverCaption: "Image Credit to [David Clode](https://unsplash.com/@davidclode?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) Unsplash"
tags: [
  "New python",
  "Pemrograman",
  "Python",
  "pyhton-3.10"
]
---

# Apa yang baru di Python 3.10

pengembangan python 3.10 telah stabil dan kami akhirnya dapat menguji semua fitur baru yang akan disertakan dalam rilis final.

Kami akan membahas beberapa tambahan paling menarik untuk Python seperti Structural Pattern Matching, Parenthesized context managers, pesan kesalahan yang baru dan lebih baik, dan New Type Union Operator.

## Structural Pattern Matching

Structural Pattern Matching adalah fitur luar biasa untuk ditambahkan ke Python yang benar-benar luar biasa.

Pattern Matching akan disajikan dalam bentuk umum: pernyataan kecocokan dan pernyataan kasus pola dengan tindakan terkait.

Pola/pattern dapat berupa: sequences, mappings, tipe data primitif, serta instance kelas. Dengan menggunakan _Pattern Matching_ kita bisa, misalnya untuk mengekstrak informasi dari tipe data yang kompleks, memasukkan ke dalam struktur data, dan menerapkan tindakan spesifik berdasarkan bentuk data yang berbeda.

Ini bukan hanya sintaks switch/case yang kita semua tahu dari bahasa pemrograman lain, tetapi juga menambahkan fungsionalitas kuat yang harus kita jelajahi.

### Example 1: Simple pattern: match to a literal

```python
def func(x):
    match x:
        case "x1":
            return "x1 .."
        case "x2":
            return "x2"
        case "x3" | "x4":  # Multiple literals can be combined with `|`
            return "Yay, "
        case _:
            return "Just another x..."
```

### Example 2: Patterns with a literal and variable

```python
def func(X):  # X = (x, y, z)
    # point is an (x, y) tuple
    match point:
        case (0, 0):
            print("Origin")
        case (0, y):
            print(f"Y={y}")
        case (x, 0):
            print(f"X={x}")
        case (x, y):
            print(f"X={x}, Y={y}")
        case _:
            raise ValueError("Not a point")
```

### Example 3: Patterns and classes

```python
class Point:
    x: int
    y: int

    def location(point):
        match point:
            case Point(x=0, y=0):
                print("Origin is the point's location.")
            case Point(x=0, y=y):
                print(f"Y={y} and the point is on the y-axis.")
            case Point(x=x, y=0):
                print(f"X={x} and the point is on the x-axis.")
            case Point():
                print("The point is located somewhere else on the plane.")
            case _:
                print("Not a point")
```

### Example 4: Guard

Kita dapat menambahkan klausa if ke sebuah pola, yang disebut guard. Jika penjaga salah, pertandingan dilanjutkan untuk mencoba blok kasus berikutnya. Perhatikan bahwa penangkapan nilai terjadi sebelum penjaga dievaluasi:

```python
match point:
    case Point(x, y) if x == y:
        print(f"The point is located on the diagonal Y=X at {x}.")
    case Point(x, y):
        print(f"Point is not on the diagonal.")
```

## Parenthesized context managers

Menggunakan tanda kurung terlampir untuk kelanjutan di beberapa baris dalam manajer konteks sekarang didukung. Hal ini memungkinkan pemformatan kumpulan panjang manajer konteks dalam beberapa baris dengan cara yang sama seperti sebelumnya dengan pernyataan impor. Misalnya, semua contoh ini sekarang valid:

```python
    ...

with (
    CtxManager1(),
    CtxManager2()
):
    ...

with (CtxManager1() as example,
      CtxManager2()):
    ...

with (CtxManager1(),
      CtxManager2() as example):
    ...

with (
    CtxManager1() as example1,
    CtxManager2() as example2
):
    ...
```

Anda juga dapat menggunakan tanda koma di akhir grup terlampir:

```python
with (
    CtxManager1() as example1,
    CtxManager2() as example2,
    CtxManager3() as example3,
):
    ...
```
Sintaks baru ini menggunakan kapasitas non LL(1) dari parser baru. Periksa [PEP 617](https://www.python.org/dev/peps/pep-0617/) untuk lebih jelasnya.

## Better Error Messages

Katakan bahwa Anda tidak langsung melompat ke Google saat pertama kali melihat:

` SyntaxError: unexpected EOF while parsing `

Hasil nomor satu di Google saat memasukkan SyntaxError menunjukkan bahwa banyak dari kita pasti melakukannya untuk mencari solusi dari error.

Ini bukan pesan kesalahan yang jelas, dan Python penuh dengan pesan kesalahan yang kurang ideal. Untungnya, seseorang memperhatikan dan banyak dari pesan ini telah ditingkatkan secara signifikan.

### Versi lama :

```python
a_dict = {x: 1, y: 2, z: 3

File "<python-input>", line 1
    a_dict = {x: 1, y: 2, z: 3
                              ^
SyntaxError: unexpected EOF while parsing
```

### Versi baru :

```python
a_dict = {x: 1, y: 2, z: 3

File "<python-input>", line 1
    a_dict = {x: 1, y: 2, z: 3
             ^
SyntaxError: '{' was never closed
```

## New Type Union Operator

Alih-alih menggunakan mengetik.union untuk mengekspresikan sintaks "baik tipe X atau tipe Y", versi baru python memperkenalkan operator serikat baru tipe X | Y. Operator baru ini memungkinkan kita untuk membuat kode dengan lebih rapi dan efisien.

### Versi lama :

```python
from typing import Union
def square(number: Union[int, float]) -> Union[int, float]:
    return number ** 2
isinstance('3', int | str)
```

### Versi baru :

```python
def square(number: int | float) -> int | float:
    return number ** 2
isinstance('3', int | str)
```

Fitur ini disumbangkan oleh Ken Jin. Kunjungi tautan ini ([PEP 612](https://www.python.org/dev/peps/pep-0612/)) untuk lebih jelasnya.



