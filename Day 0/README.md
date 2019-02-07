## Laporan 30 Days of Code
---
### Day 0 : Hello, World
#### Tujuan
Dalam tantangan meninjau beberapa konsep dasar yang akan membantu memulai seri ini. gunakan sintaks yang sama (atau serupa) untuk membaca input dan menulis output dalam tantangan di seluruh HackerRank.
#### Tugas
Untuk menyelesaikan tantangan ini, harus menyimpan jalur input dari stdin ke variabel, cetak Hello, World. pada satu baris, dan akhirnya cetak nilai variabel Anda pada baris kedua.

`Catatan:` Instruksi ini berbasis Java, tetapi mendukung pengiriman dalam banyak bahasa populer. Anda dapat beralih bahasa menggunakan menu tarik-turun di atas editor, dan variabel dapat ditulis secara berbeda tergantung pada praktik terbaik dari bahasa kiriman Anda.
#### Format masuk
satu baris teks yang menunjukkan `inputString` (variabel yang isinya harus dicetak).
#### Format keluar
cetak Hello, World. pada baris pertama dan isi dari `inputString` pada baris kedua
#### Contoh input
`Welcome to 30 Days of Code!`
#### Contoh keluar
```
Hello, World.
Welcome to 30 Days of Code!
```
#### Souce Code
```
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;
public class Day0 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Scanner scan = new Scanner (System.in);
        String inputString = scan.nextLine();
        System.out.println("Hello, World.");
        System.out.println(inputString);

    }

}
```
