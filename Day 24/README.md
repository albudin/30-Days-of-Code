## Laporan 30 Days of Code
---
### Day 24 : More Linked Lists
#### Tugas
class simpul disediakan untuk Anda di editor. Objek simpul memiliki bidang data integer, data, dan pointer instance simpul, next, menunjuk ke simpul lain (mis .: simpul berikutnya dalam daftar).
Fungsi removeDuplicate dideklarasikan di editor Anda, yang membawa pointer ke
kepala simpul daftar tertaut sebagai parameter. Selesaikan removeDuplicates sehingga menghapus semua duplikat dari daftar dan mengembalikan kepala dari daftar yang diperbarui.
Catatan: The kepala pointer mungkin nol, menunjukkan bahwa daftar itu kosong. Pastikan untuk mengatur ulang pointer Anda selanjutnya saat melakukan penghapusan untuk menghindari kerusakan daftar.
#### Format masuk
Anda tidak perlu membaca input apa pun dari stdin. Input berikut ditangani oleh kode rintisan yang dikunci dan diteruskan ke fungsi removeDuplicates:
Baris pertama berisi bilangan bulat, N, jumlah node yang akan dimasukkan.
N Baris berikutnya masing-masing berisi bilangan bulat yang menggambarkan nilai dari sebuah simpul yang dimasukkan pada ekor daftar.
#### Kendala
Elemen data dari argumen daftar tertaut akan selalu berada dalam urutan yang tidak menurun.
#### Format keluar
Fungsi removeDuplicates Anda harus mengembalikan kepala dari daftar tertaut yang diperbarui. Kode rintisan yang terkunci di editor Anda akan mencetak daftar yang dikembalikan ke stdout.
#### Contoh input
```
6
1
2
2
3
3
4
```
#### Contoh keluar
`1 2 3 4`
#### Penjelasan
N = 6, dan daftar kami yang tidak berkurang adalah{1,2,2,3,3,4}. Nilai 2 dan 3 keduanya muncul dua kali dalam daftar, jadi kami menghapus dua duplikat node. Kami kemudian mengembalikan daftar (naik) yang diperbarui, yaitu{1,2,3,4}.
#### source code
```
import java.io.*;
import java.util.*;
class Node{
	int data;
	Node next;
	Node(int d){
        data=d;
        next=null;
    }

}
class Solution
{

    public static Node removeDuplicates(Node head) {
      //Write your code here
      Node t=head;
      while(t.next!=null){
          if(t.data==t.next.data){
              t.next=t.next.next;
          }else{
              t=t.next;
          }
      }
      return head;

    }

    public static  Node insert(Node head,int data)

```
