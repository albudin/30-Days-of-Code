## Laporan 30 Days of Code
---
### Day 13 : Abstract Classes
#### Tujuan
mengambil apa yang kami pelajari kemarin tentang Warisan dan memperluasnya ke Kelas Abstrak.
#### Tugas
Diberi kelas Buku dan kelas Solusi, tulis kelas MyBook yang melakukan hal berikut:
Given a Book class and a Solution class, write a MyBook class that does the following:
* Inherits from Book
* Has a parameterized constructor taking these parameters:
  * String title
  * String author
  * int price
* Implements the Book class' abstract display() method so it prints these lines:
  * Title:,a space, and then the current instance's title.
  * Author:,a space, and then the current instance's author.
  * Price:,a space, and then the current instance's price.

Catatan: Karena kelas-kelas ini ditulis dalam file yang sama, Anda tidak boleh menggunakan pengubah akses (mis .: publik) ketika mendeklarasikan MyBook atau kode Anda tidak akan dieksekusi.
#### Format masuk
Anda tidak bertanggung jawab untuk membaca input apa pun dari stdin. Kelas Solusi membuat objek Buku dan memanggil konstruktor kelas MyBook (memberikannya argumen yang diperlukan). Kemudian memanggil metode tampilan pada objek Buku.
#### Format keluar
```
Title: $title
Author: $author
Price: $price
```
#### Contoh input
```
The Alchemist
Paulo Coelho
248
```
#### Contoh keluar
```
Title: The Alchemist
Author: Paulo Coelho
Price: 248
```
#### source code
```
//Baca MyBook Class
class MyBook extends Book{
    private int p;

    MyBook(String t,String a,int p){
        super(t,a);
        this.p=p;
    }

    void display(){
        System.out.println("Title: "+title);
        System.out.println("Author: "+author);
        System.out.println("Price: "+this.p);
    }
}
```
